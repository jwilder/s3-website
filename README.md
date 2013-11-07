s3-website
==========

Basic S3 static website deployment script.  

# Features

* Create a WS bucket w/ required ACL
* Minimize and gzip any JavaScript, CSS and HTML using [HTML Compressor](http://code.google.com/p/htmlcompressor/)
and [YUI Compressor](http://yui.github.io/yuicompressor/)
* Set correct content type and content-encoding headers
* Sets HTTP cache headers far into the future

It does not combine or rename assets for cache busting.  You'll need to use your 
static site generator for that. 

This has only been tested with [Jekyll](http://jekyllrb.com/) but should work with other staticaly generated sites. 

# Dependencies

* [AWS CLI](http://docs.aws.amazon.com/cli/latest/index.html)
* Java

# Setup

    1. git clone https://github.com/jwilder/s3-website.git
    2. export PATH=$PATH:/path/to/s3-website
    
# Usage
    
    s3-website _site www.yoursite.com

Defaults to us-east-1 region.

    AWS_REGION=us-west-1 s3-website _site www.yoursite.com
