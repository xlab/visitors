## THIS IS A FORK (0.7.1)

Changeset:
* Support for Yandex search engine;
* Tweaked limits on keywords (20 to 100).
* Improved OS and browser detection

-----------------------

## WELCOME TO VISITORS 0.7

Hello, this is Visitors,
a fast and easy to use web log analyzer.

For more usage information, documentation and examples
please visit:

http://www.hping.org/visitors

or check the docs.html file in this directory
for the reference documentation.

## HOW TO COMPILE

Under UNIX systems just type:

	% make

Under WIN32 you need MINGW and MSYS, then follow the above
istructions.

For compliation problems please write an email to <antirez@invece.org>
with the exact problem, version of Visitors, environment, GCC used, and so
on.

## HOW TO USE WITH IIS LOGS

Use the `iis2apache.pl` perl script to do the conversion, like:

	cat yourIISLogFile.txt | perl iis2apache.pl > yourConvertedFile.txt

Then run visitors against `yourConvertedFile.txt`.

There is an alternative way to convert logs using a program
that does not require Perl, with Windows and Linux binaries.
This program is called RConvLog and it's possible to
download it at http://www.rebex.net/RConvLog/

## HOW TO GET SCREEN RESOLUTION INFORMATION

Log files don't contain information about the screen resolution
so in order to generate the screen resolution report Visitors needs
that you add the following code in your home page, after the <body>
tag:

```javascript
<script>
document.write("<div style=\"visiblity:hidden;display:none;\"><img src=\"visitors-screen-res-check.jpg?"+screen.width+"x"+screen.height+"x"+screen.colorDepth+"\" /></div>");
</script>
```

Without this code the screen resolution report will not work.

## HOW TO HELP

Please send patches, I'll merge it, but be aware the project is now licensed under the BSD license, it's no longer GPLed.

## THANKS TO ...

Please see the ChangeLog file for credits.

Enjoy,
Salvatore Sanfilippo
