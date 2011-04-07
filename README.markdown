Hosting Trial
=============

Hosting trial is a Drupal module intended to extend Aegir to enable time-limited trials. The primary goal is to allow for sites to be disabled after a set time. For example, this will allowfor 30-day try-before-you-buy periods.

Basic Features (initial brainstorm)
==============

* Ability to specify, at the platform level, a default trial period.
* This will then set an "expiry date" on sites installed on that platform
* On cron runs, these dates are checked and sites de-activated, if they are past their expiry date
* Hooks to allow uc_hosting and/or uc_recurring to reset the expiry date.

The current plan
================
* Site cron runs seem to be a reasonable place to check this. hook_post_hosting_TASK_TYPE_task looks like a good hook candidate. So, define a hosting_trial_post_hosting_cron_task().
* A tab is needed on platforms to allow default values to be set (should this be set per profile?)
* A field on the site is then set accordingly, and can be overridden manually
