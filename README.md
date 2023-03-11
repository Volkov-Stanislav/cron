[![GoDoc](http://godoc.org/github.com/robfig/cron?status.png)](http://godoc.org/github.com/robfig/cron)
[![Build Status](https://travis-ci.org/robfig/cron.svg?branch=master)](https://travis-ci.org/robfig/cron)


# cron

This library is forked from original project http://github.com/robfig/cron

After fork, added '#' in dow field, called nth, to indicate number of week in month, witch shedule must run.

Example: "* * * * 1#2" - will run on next Monday 2th week of month.

Refer to the origunal documentation here:
http://godoc.org/github.com/robfig/cron

### Background - Cron spec format

There are two cron spec formats in common usage:

- The "standard" cron format, described on [the Cron wikipedia page] and used by
  the cron Linux system utility.

- The cron format used by [the Quartz Scheduler], commonly used for scheduled
  jobs in Java software

[the Cron wikipedia page]: https://en.wikipedia.org/wiki/Cron
[the Quartz Scheduler]: http://www.quartz-scheduler.org/documentation/quartz-2.3.0/tutorials/tutorial-lesson-06.html

The original version of this package included an optional "seconds" field, which
made it incompatible with both of these formats. Now, the "standard" format is
the default format accepted, and the Quartz format is opt-in.
