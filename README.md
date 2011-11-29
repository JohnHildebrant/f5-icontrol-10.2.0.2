# Certificate Reporting Tool


## Challenge:

SSL certificate management is a reactive process today and renewal is a manual process.  We’d like an abstracted view outside of the F5 management suite that shows current certificate configuration.  We also want to be alerted at user configurable intervals prior to expiration. 

## Desired Solution:

### Reporting Component

1.  User account secured web-based reporting interface that presents the following data:
	* Certificate Name
	* Certificate Expiration
	* Cipher strength
	* Active Directory tie-in preferred

2.  Admin account secured web-based management interface that allows configuration of:
	* Alert Intervals (multiple alerts desired – 3 weeks, 1 week, 1 day)
	* Service Account used to communicate with F5
	* IP Address of F5 
	* SMTP Alert destination addresses

3.  Interval-based querying of F5 device using iControl (SOAP/XML) to pull current Certificate data at least once every hour
  -	http://devcentral.f5.com/wiki/iControl.HomePage.ashx
  -	Target platform runs 10.2.1

### Alerting Component:

1.  Issue SMTP Alerts when a certificate reaches a configured alert interval.  (ie:  expiration date is X weeks away – send alert)

2.  Prevent spamming of alerts

### Using Git & Github

Your project must use `git` and `Github`. Create a new repository and push your work to Github constantly so that your source code is backed up and it is publicly available to receive feedback.

### Easy To Explore

Create a `README` for your project in the root.

* Easy to explore
** README
** lib and spec directory
* Easy to configure and run
** Rakefile
** Gemfile
* 5-Minute Presentation

### Presentation

Prepare a 5-minute presentation that employs a narrative, slides, code samples, diagrams, or hand gestures... anything you want to use. 

The importance of the presentation is to convey:

* What I hoped to learn?
* What I hoped to create?
* What I ended up creating?
* What I ended up learning?
* What else I could add?
* What else I could learn?

## Bonuses

### Work and Present with a Partner

I encourage you to find another person within the class to work with on the project.

### Write Tests

All through the exercises we have been using tests to help learn new concepts and verify code that we have written. Hopefully you see the value in tests and want to employ them in the code that you are writing.

### Practice your Presentation

At least once. Hopefully, for another person that will give you feedback and with enough time to make any adjustments.

### A Project that Works

The emphasis for the project is to challenge what you know about Ruby. The work does not have to be a finished, working product. Consider this an extended exercise or a starting point. It is not important that the project works but a bonus if it does.
