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
