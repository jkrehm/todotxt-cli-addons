## Todo.txt Add-ons

For using todotxt-cli, please see: [https://github.com/ginatrapani/todo.txt-cli](https://github.com/ginatrapani/todo.txt-cli).

### Reminders

*Requirements*

- Python 2.7+
- [Requests](http://docs.python-requests.org/en/latest/user/install/)

This add-on allows you to schedule reminders of your todo items. You do this by including a date or a date/time with the item, using the format:

	[YYYY-MM-DD]
	or
	[YYYY-MM-DD HH:MI]

where "hours" are in 24-hour time,
e.g.

	(A) Destroy the Death Star +Rebellion [2012-12-21]
	or
	(C) Take out the trash @Home [2012-12-21 18:45]

Note: If you do not include a time with the date, it will assume 8am (08:00).

Notifications go out via:

- [Push Bullet](https://www.pushbullet.com//) (requires API key)
- [Pushover](https://pushover.net/) (requires API and user keys)

The notification service configuration is set in the todo.cfg file, e.g.

    export API_TYPE="PUSHBULLET"
    export API_TOKEN="yourapikey"

You call the add-on like so:

	todo.sh remind

I have mine set as a [cron job](http://www.adminschoice.com/crontab-quick-reference) that runs every minute and sends the notifications as needed.