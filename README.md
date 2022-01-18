Humidity Controller
===================
Keep those plants happy.

Schedule [run][1] to execute every few minutes as a `cron` job, e.g.
```cron
# m h  dom mon dow   command
#
# Every minute, check to see whether we need to turn on/off the humidifier.
* * * * *       cd /home/david/src/humidity-controller && ./run >last-run.log 2>&1
```

If the measured relative humidity is above a preset maximum while the
humidifier is on, `run` will turn it off.

If the measured relative humidity is below a preset minimum while the
humidifier is off, `run` will turn it on.

[1]: ./run

