SilentJack
==========
Nicholas J. Humfrey <njh@aelius.com>

For the latest version of SilentJack, please see:
http://www.aelius.com/njh/silentjack/

It is released under the GPL licence, see COPYING for details.


What is SilentJack ?
--------------------

SilentJack is a silence/dead air detector for the Jack Audio Connection Kit.

    Usage: silentjack [options] [COMMAND [ARG]...]
    Options:  -c <port>   Connect to this port
              -n <name>   Name of this client (default 'silentjack')
              -l <db>     Trigger level (default -40 decibels)
              -p <secs>   Period of silence required (default 1 second)
              -g <secs>   Grace period (default 0 seconds)
              -v          Enable verbose mode
              -r          Enable reverse behaviour (detect noise)
              -q          Enable quiet mode

SilentJack runs COMMAND after silence has been detected for the given 
number of seconds. SilentJack then waits for the command the finish, 
and then wait for the grace period before detecting silence again.

SilentJack's input port must be connected to an output port before 
it will start reporting silence.
