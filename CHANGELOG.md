# Version 1.2.0 (2017-07-26)
- Supports Python 3.7 by renaming `async` to `is_async`. Thanks @Flimm!
- `UnpickleError` is now handled properly. Thanks @selwin!
- Redis Sentinel support. Thanks @SpeedyCoder!

# Version 1.1.0
- Fixed some admin related bugs. Thanks @seiryuz!
- More Django 2.0 compatibility fixes. Thanks @selwin and @koddr!
- Custom `Job` and `Worker` classes are now supported. Thanks @skirsdeda!
- `SENTRY_DSN` value in `settings.py` will now be used by default. Thanks @inetss!

# 1.0.1
- Django 2.0 compatibility fixes.
- Minor bug fixes

# 1.0.0

-   You can now view worker information
-   Detailed worker statistics such as failed/completed job count are
    now shown (requires RQ &gt;= 0.9.0). Thanks @seiryuz!
-   `rqstats` management command now allows you to monitor queue stats
    via CLI. Thanks @seiryuz!
-   Added `/stats.json` endpoint to fetch RQ stats in JSON format,
    useful for monitoring purposes. Thanks @seiryuz!
-   Fixed a crash when displaying deferring jobs. Thanks @Hovercross!
-   Added `sentry-dsn` cli option to `rqworker` management command.
    Thanks @efi-mk!
-   Improved performance when requeueing all jobs. Thanks
    @therefromhere!

# 0.9.6

-   More Django 1.10 compatibility fixes. Thanks @dmwyatt!
-   Improves performance when dealing with a large number of workers.
    Thanks @lucastamoios!

# 0.9.5

-   Fixed view paging for registry-based job lists. Thanks @smaccona!
-   Fixed an issue where multiple failed queues may appear for the same
    connection. Thanks @depaolim!
-   `rqworker` management command now closes all DB connections before
    executing jobs. Thanks @depaolim!
-   Fixed an argument parsing bug `rqworker` management command. Thanks
    @hendi!

# 0.9.3

-   Added a `--pid` option to `rqscheduler` management command. Thanks
    @vindemasi!
-   Added `--queues` option to `rqworker` management command. Thanks
    @gasket!
-   Job results are now shown on admin page. Thanks @mojeto!
-   Fixed a bug in interpreting `--burst` argument in `rqworker`
    management command. Thanks @claudep!
-   Added Requeue All feature in Failed Queue's admin page. Thanks
    @lucashowell!
-   Admin interface now shows time in local timezone. Thanks
    @randomguy91!
-   Other minor fixes by @jeromer and @sbussetti.

# 0.9.2

-   Support for Django 1.10. Thanks @jtburchfield!
-   Added `--queue-class` option to `rqworker` management command.
    Thanks @Krukov!

# 0.9.1

-   Added `-i` and `--queue` options to rqscheduler management command.
    Thanks @mbodock and @sbussetti!
-   Added `--pid` option to `rqworker` management command. Thanks
    @ydaniv!
-   Admin interface fixes for Django 1.9. Thanks @philippbosch!
-   Compatibility fix for `django-redis-cache`. Thanks @scream4ik!
-   *Backwards incompatible*: Exception handlers are now defined via
    `RQ_EXCEPTION_HANDLERS` in `settings.py`. Thanks @sbussetti!
-   Queues in django-admin are now sorted by name. Thanks @pnuckowski!

# 0.9.0

-   Support for Django 1.9. Thanks @aaugustin and @viaregio!
-   `rqworker` management command now accepts `--worker-ttl` argument.
    Thanks pnuckowski!
-   You can now easily specify custom `EXCEPTION_HANDLERS` in
    `settings.py`. Thanks @xuhcc!
-   `django-rq` now requires RQ &gt;= 0.5.5

# 0.8.0

-   You can now view deferred, finished and currently active jobs from
    admin interface.
-   Better support for Django 1.8. Thanks @epicserve and @seiryuz!
-   Requires RQ &gt;= 0.5.
-   You can now use StrictRedis with Django-RQ. Thanks @wastrachan!

# 0.7.0

-   Added `rqenqueue` management command for easy scheduling of tasks
    (e.g via cron
