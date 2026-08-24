vichan-x - A more lightweight and full featured PHP imageboard.
========================================================

As of 24 August 2026 it supports PHP8.1.

About
------------
vichan-x is a free light-weight, fast, highly configurable and user-friendly
imageboard software package forked from vichan. It is written in PHP and has few dependencies.

Some documentation may be found on our [wiki](https://github.com/166d/vichan-x/wiki). (feel free to contribute)

History
------------
vichan-x is a fork of (now defunc'd) [vichan](http://github.com/vichan-devel/vichan),
a great imageboard package, actively adding a lot of features and removing the bloat vichan had.

### Maintainer timeline
1. [@166d](https://github.com/166d) - 2026 (vichan-x)
2. [@perdedora](https://github.com/perdedora) and [@RealAngeleno](https://github.com/RealAngeleno) - 2023-2025.
3. Development Commission lead by [@basedgentoo](https://github.com/basedgentoo), [@kuz-sysadmin](https://github.com/kuz-sysadmin), and [@RealAngeleno](https://github.com/RealAngeleno). (2023 - 2023)
4. [@h00j](https://github.com/h00j) (2021 - ???)
5. [@ctrlcctrlv](https://github.com/ctrlcctrlv) (2017 - 2021)
6. [@czaks](https://github.com/czaks) (2014 - 2017) (The author of vichan fork)
7. [@savetheinternet](https://github.com/savetheinternet) (2010 - 2014) (The creator of Tinyboard)

Requirements
------------
1.	PHP >= 8.2
2.	MySQL/MariaDB server
3.	[mbstring](http://www.php.net/manual/en/mbstring.installation.php)
4.	[PHP GD](http://www.php.net/manual/en/intro.image.php)
5.	[PHP PDO](http://www.php.net/manual/en/intro.pdo.php)
6.	A Unix-like OS, preferrably FreeBSD or GNU/Linux

We try to make sure vichan-x is compatible with all major web servers. vichan-x does not include an Apache `.htaccess` file nor does it need one.

### Recommended
1.	MySQL/MariaDB server >= 5.5.3
2.	ImageMagick (command-line ImageMagick or GraphicsMagick preferred).
3.	[APCu (Alternative PHP Cache)](http://php.net/manual/en/book.apcu.php),
	[Memcached](http://www.php.net/manual/en/intro.memcached.php) or
	[Redis](https://redis.io/docs/about/)

Contributing
------------
You can contribute to vichan-x by:
*	Developing patches/improvements/translations and using GitHub to submit pull requests
*	Providing feedback and suggestions
*	Writing/editing documentation

Installation
-------------
1.	Get the latest development version with:

        git clone git://github.com/166d/vichan-x.git

2.	run ```composer install``` inside the directory
3.	Navigate to ```install.php``` in your web browser and follow the
	prompts.
4.	vichan-x should now be installed. Log in to ```mod.php``` with the
	default username and password combination: **admin / password**.

Please remember to change the administrator account password.

See also: [Configuration Basics](https://github.com/166d/vichan-x/wiki/config).

Upgrade
-------
Note: In the near future, upgrading from old versions of vichan, and any version of Tinyboard, will be deprecated.

To upgrade from any version of Tinyboard, vichan or vichan-x:

Either run ```git pull``` to update your files, if you used git, or
backup your ```inc/instance-config.php```, replace all your files in place
(don't remove boards etc.), then put ```inc/instance-config.php``` back and
finally run ```install.php```.

To migrate from a Kusaba X board, use http://github.com/vichan-devel/Tinyboard-Migration

Support
--------
vichan-x is still beta software -- there are bound to be bugs. If you find a
bug, please report it.

CLI tools
-----------------
There are a few command line interface tools, based on Tinyboard-Tools. These need
to be launched from a Unix shell account (SSH, or something). They are located in a ```tools/```
directory.

You actually don't need these tools for your imageboard functioning, they are aimed
at the power users. You won't be able to run these from shared hosting accounts
(i.e. all free web servers).

Oekaki
------
vichan-x makes use of [wPaint](https://github.com/websanova/wPaint) for oekaki. After you pull the repository, however, you will need to download wPaint separately using git's `submodule` feature. Use the following commands:

```
git submodule init
git submodule update
```

To enable oekaki, add all the scripts listed in `js/wpaint.js` to your `instance-config.php`.

WebM support
------------
Read `inc/lib/webm/README.md` for information about enabling webm.

Docker
------------
Vichan-x comes with a Dockerfile and docker-compose configuration, the latter aimed primarily at development and testing.
See the `docker/doc.md` file for more information.

vichan-x API
----------
vichan provides by default a 4chan-compatible JSON API. For documentation on this, see:
https://github.com/vichan-devel/vichan-API/ .
