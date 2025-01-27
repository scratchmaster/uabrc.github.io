# How to Request Support

Before reaching out to us, try searching this documentation for keywords related to your issue. If you aren't able to find anything, please try checking our FAQ located on [ask.cyberinfrastructure](https://ask.cyberinfrastructure.org/c/locales-data-centers-and-campus-rc/uab/52). If you still need help, please read on for how to send in a ticket and how to work with our ticketing system.

## How Do I Create a Support Ticket?

To Create a support ticket, send a descriptive email to <support@listserv.uab.edu> to create a ticket. Bonus points for including the following details.

For general issues:

1. What is your goal?
2. What steps were taken?
3. What was expected?
4. What actually happened?
5. How was the cluster accessed? Web Portal, SSH, VNC, etc.?
6. What software were you using? Please be as specific as possible. The command `module list` can be helpful here.

For outages:

1. What part of the cluster is affected? Please list any relevant affected nodes or other hardware that is not accessible. If you are unable to access the cluster please state that instead.
2. What were you working on when you noticed the outage?
3. How were you accessing the cluster? Web Portal, SSH, VNC, etc.?

### How Do I Work With Tickets I've Created?

UAB IT and Research Computing use ServiceNow for ticket management. When any email is sent to <support@listserv.uab.edu>, AskIT is notified and a ticket is created in ServiceNow and the ticket details are forwarded by email to every member of Research Computing staff.

When any email is sent to <support@listserv.uab.edu> the following happens:

1. An RITM ticket is created in ServiceNow and assigned to Research Computing.
2. The email is routed to Research Computing staff and the ticket creator from the `support@listserv.uab.edu` email list. Please **do not reply**. Replies create additional tickets and cause service delays.
3. A ticket creation email is sent from `askit@uab.edu` to Research Computing staff and the ticket creator. Please **do not reply**. Replies create additional tickets and cause service delays.
4. A monitoring email is sent from `support-watch@listserv.uab.edu` to Research Computing staff and the ticket creator. Replies will update the ticket with new information and send further emails to Research Computing staff and the ticket creator. Please _do_ reply to this and future emails from `support-watch@listserv.uab.edu` as needed to update the ticket. Before replying, please delete all previous quoted replies to avoid the accumulation of noise in the ticket. The images below show how to, and how not to, reply to `support-watch@listserv.uab.edu` emails.

    - Please reply like this:
        ![!Image showing reply without extraneous quoted text. Please do this.](images/support-watch-do-reply-like-this.png)

    - Not like this:
        ![!Image showing reply with extraneous quoted text. Please do not do this.](images/support-watch-do-not-reply-like-this.png)

If you prefer to use email to manage your ticket, please use the method of replying to emails from `support-watch@listserv.uab.edu`. Note that you will not be able to see any attachments this way. They are stripped off and added to the ticket in the ServiceNow web interface, available through the `RITM0000000` link in the `support-watch@listserv.uab.edu` emails.

If you prefer to use the ServiceNow web interface, please click the `RITM0000000` link in the email from `support-watch@listserv.uab.edu`.

<!-- markdownlint-disable MD046 -->
!!! important

    The UAB email server strips all potentially executable files from emails. This includes attachments with `.sh`, `.py` and `.exe` suffixes. Zip files containing those files will also be stripped. If you need to send script examples to us please rename the files to have a `.txt` suffix and inform us of their original nature.
<!-- markdownlint-enable MD046 -->

## How Do I Request Or Change A Project Space?

Projects are collaborative data and code storage spaces with controlled access. Any UAB investigator with a legitimate research need can request a project storage space. Please send an email with the following information, depending on what you need.

For more details on project storage, please see our [Storage](../data_management/storage.md) page.

### New Projects

1. What is the purpose of the project space?
2. What should we name the project? Short, descriptive, memorable names work best. The name will be used as the project folder name in our file system, so alphanumeric, underscore and dash characters only please.
3. Who should have access? Please provide a list of blazerids. The intended project owner will always have access.

### Access Management

1. What is the name of the project?
2. Who should be given access?
3. Who should no longer have access?

### Storage

1. What is the name of the project?
2. How much additional or total space will be needed?

### How do I request new software installed?

Before making a request for new software on Cheaha, please try searching our [modules](../cheaha/software/modules.md) or searching for packages on [Anaconda](../workflow_solutions/using_anaconda.md).

If you are not able to find a suitable module or package and would like a new piece of software installed on Cheaha, please [create a ticket](#how-do-i-create-a-support-ticket) with the name of the software, the version number, and a link to the installation instructions.

## Office Hours

For our office hours links please see [Contact Us](../index.md#contact-us).

## Status Updates

For status updates affecting our systems or services please visit <https://uabstatus.statuscast.com/#!/incidentlist?componentId=34990>.

At this page you can subscribe to notifications using the bell icon next to the name "Research Computing" near the top-left of the page.

![!subscribe button on status update page](images/support_status_update_subscribe.png)
