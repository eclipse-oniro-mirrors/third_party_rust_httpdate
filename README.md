# Date and time utils for HTTP.

[![Build Status](https://travis-ci.org/pyfisch/httpdate.svg?branch=master)](https://travis-ci.org/pyfisch/httpdate)
[Documentation](https://pyfisch.github.io/httpdate/httpdate/index.html)

Multiple HTTP header fields store timestamps.
For example a response created on May 15, 2015 may contain the header
`Date: Fri, 15 May 2015 15:34:21 GMT`. Since the timestamp does not
contain any timezone or leap second information it is equvivalent to
writing 1431696861 Unix time. Rust’s `SystemTime` is used to store
these timestamps.

This crate provides two public functions:

* `parse_http_date` to parse a HTTP datetime string to a system time
* `fmt_http_date` to format a system time to a IMF-fixdate

Read the [blog post](https://pyfisch.org/blog/http-datetime-handling/) to learn
more.
