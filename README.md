# max-uptime-keeper
Script to be run as a cron job that maintains max uptime records

============================
Can be run manually with no arguments.
============================

============================
Installation
============================
Can install it's self into /etc/cron.d/max-uptime-keeper when run as
    max-uptime-keeper -i [username]
        or
    max-uptime-keeper --install [username]

    username is the user for cron to run the script as.
    if username is omitted then the current user is used during install.

============================
Description
============================
    Using the default install the script is run once a minute to update $LogDir/uptime.current

    If the uptime indicates we have rebooted
    (ie: uptime right now is less than the last uptime stored in uptime.current)
    Then it updates
        $LogDir/uptime.log
    and
        $LogDir/uptime.max (as required)

    Logdir is /var/log/max-uptime-keeper

