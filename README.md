# http-gzip-time

> Get remote server date and time for vulnerable servers

### Description

[This post](http://jcarlosnorte.com/security/2016/02/21/date-leak-gzip-tor.html) inspired me to write this bash script because I just wanted to spend time doing something fun. As it seems, some of the servers with gzip compression (most likely Windows servers) seem to send the timezone as part of [GZip header](http://www.forensicswiki.org/wiki/Gzip#File_header).

### Examples

```shell
$ ./gzip-time http://techgaun.com
The server does not seem to have gzip compression enabled.

$ ./gzip-time http://reddit.com
Note: This server might be sending time in UTC instead of local time.

The server date time is: 2016-02-23 04:50:49
The UTC time is: 2016-02-23 04:50:49

$ ./gzip-time http://bing.com
The server date time is: 2016-02-22 20:50:56
The UTC time is: 2016-02-23 04:50:56
```
