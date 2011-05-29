Hosting Expiry Date
===================

Hosting Expiry Date is a Drupal module intended to extend Aegir to enable automated disabling and deleting of sites. The primary goal is to allow for sites to be disabled after a set time. For example, this could allow for 30-day try-before-you-buy periods, or disposable testing sites.

Basic Features (initial brainstorm)
==============

* Ability to specify, at the platform level, a default trial period.(?)
* This will then set an "expiry date" on sites installed on that platform
* On cron runs, these dates are checked and sites de-activated, if they are past their expiry date
* API to allow uc_hosting and/or uc_recurring to reset the expiry date.

The current plan
================
* We'll need to implement our own queue for this.
* A tab is needed on platforms (?) to allow default values to be set (should this be set per profile?)
* A field on the site is then set accordingly, and can be overridden manually
