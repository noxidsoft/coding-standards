How to use:

copy 'Deprecated' directory including DeprecatedClassesSniff.php and DeprecatedFunctionsSniff.php) into ./Joomla/Sniffs

Deprecated sniffs are disabled by default and need to be enabled via a startup parameter (set to 1 to to report all, or to joomla version to only report relevant):

--runtime-set enable_deprecated_joomla_sniff 4.0

For the Geany editor you can use this PHP Code Sniffer line (customize to hold you phpcs location and --standard):

~/.composer/vendor/bin/phpcs --report-width=250 --standard=Joomla-Custom "%f" --runtime-set enable_deprecated_joomla_sniff 1 | sed -e 's/^/%f |/' | egrep 'WARNING|ERROR'

For the Geany editor you can use this PHP Code Fixer line (customize to hold you phpcbf location and --standard):

~/.composer/vendor/bin/phpcbf --standard=Joomla-Custom "%f" --runtime-set enable_deprecated_joomla_sniff 4.0
