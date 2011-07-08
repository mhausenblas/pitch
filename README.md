# pitch - put it in the cloud for me, Helena

A cloud computing IaaS-level command line tool to get data 'in the cloud'.

## Usage

The general syntax and options of pitch are:

	pitch [OPTIONS] SOURCE TARGET 

where

	OPTIONS ... auth tokens such as username/password, access keys, WebID, OpenID, etc.
	SOURCE ... a local file/path pattern representing the source of the pitching
	TARGET ... the URI of the target representing the sink of the pitching

Note that the TARGET URI [scheme](http://tools.ietf.org/html/rfc3986#section-3.1) determines the access mode. For example, if you specify a `ftp://` URI you set pitch into the FTP transfer mode or if you use a `gs://` URI then, not very surprisingly you signal that you want to transfer your data to Google Storage. 

Now to a concrete usage example: imagine you want to put all CSV files in the current directory into a certain bucket in Google Storage. With pitch you'd do the following:

	$ pitch *. gs://lodcloud
	
If you don't specify the access credentials (as above), pitch will ask you for it.

	
## Targets

* S3
* Google Storage
* FTP
* _what else do we need?_

## Team

* [Michael](https://github.com/mhausenblas)
* [Helena](https://github.com/helenadeus) 

## License

This software is Public Domain.