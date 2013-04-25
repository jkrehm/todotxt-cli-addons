## Todo.txt Add-ons

For using todotxt-cli, please see: [https://github.com/ginatrapani/todo.txt-cli](https://github.com/ginatrapani/todo.txt-cli).

### Reminders
This add-on allows you to schedule reminders of your todo items. You do this by including a date or a date/time with the item, using the format:

	[YYYY-MM-DD]
	or
	[YYYY-MM-DD HH:MI]

where "hours" are in 24-hour time,
e.g.

	(A) Destroy the Death Star +Rebellion [2012-12-21]
	or
	(C) Take out the trash @Home [2012-12-21 18:45]

Note: If you do not include a time with the date, it will assume midnight (00:00).

Currently the notifications go out using [Pushover](https://pushover.net/). An API and user key are required in the todo.cfg file.

You call the add-on like so:

	todo.sh remind

I have mine set as a [cron job](http://www.adminschoice.com/crontab-quick-reference) that runs every minute and sends the notifications as needed.