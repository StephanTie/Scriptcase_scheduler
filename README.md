**Scriptcase Scheduler**

Scheduler for Scriptcase grid reports (in HTML or PDF format) where the results are stored or can be sent by mail automatically.

**Features:**

    - Schedule any grid report with minimal modifications.
    - Create a job, schedule it, and find the result in the Job Executed overview.
    - Tested on Scriptcase version 9.10.0002 and PHP version 8.1.6 (Not tested on older versions).
    - Jobs: Create an additional WHERE clause.
    - Schedule: Select a period during which the schedule is active, embed images, and send it to a mailing list.

Date: 27–12–2023

**Introduction**

I developed this project to address the need for scheduling, allowing me to send reports to users or schedule tasks while keeping all development within Scriptcase.

It's essential to note that this scheduler only functions when the security is turned off for the respective grid you intend to schedule. Therefore, it should not be published in the standard production environment. I utilize Docker to create a separate instance where only the system, via crontab, can access these unprotected applications while being connected to the same database. Another option is to set up an extra protected environment for enhanced security.

**Warning: Do not expose unprotected applications on the web!**

I use the crontab scheduler on Ubuntu Linux. For other environments, you will need to find alternatives to crontab (e.g., Task Scheduler on Windows).

I've provided a functional setup based on Scriptcase's security example application, scheduling reports based on categories, products, and customers. It is running with MySQL.

