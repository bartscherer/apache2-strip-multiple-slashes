# apache2-strip-multiple-slashes

This is a macro to strip multiple slashes out of the URI using mod_rewrite and mod_macro. Tested on apache 2.4.48

## Requirements

- mod_proxy 
- mod_rewrite

## Usage

Place this file within the conf.d folder of apache2.

Then run a `a2enconf remove_multiple_slashes` to enable the configuration.

Finally execute `systemctl reload apache2` to enable the macro.

You can then use it like this:

```
<Directory /var/www/html/>
        Use RemoveMultipleSlashes
</Directory>
```

to remove the trailing slashes within URIs having /var/www/html/ as their document root. 
