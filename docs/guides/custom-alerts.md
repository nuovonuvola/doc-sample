# Custom Alerts
Custom alerts allow you to monitor key productivity metrics in your cloud. This article explains which metrics you can monitor and how to configure them.

## Available metrics
The following metrics can be monitored:
* CPU usage (ID: 01)
* Memory (ID: 02)
* Network thresholds (ID: 03) 

## Basic setup 
Basic settings are based on percentages assigned to the metrics. If a value exceeds the specified percentage, an email is automatically sent to the administrator address stored in Data Center Designer.

### Basic arguments
* metric: provides the ID of the metric
* percentage: sets the threshold in %

**Example**

    SET https://example.com?metric=02&percentage=80
	
This command will set the threshhold for the memory metric (ID: 02) to 80%. This means the administrator will get an email as soon as the memory usage is equal or higher than 80% of the available capacity.

**Notes**
* If a setting is not set or set to zero, all emails will be omitted 
* Maximum number of emails sent per hour is restricted to 25

## Advanced setup
Arguments allow you to extend the conditions that must be met for an alarm to be triggered. Multiple arguments can be linked with an ampersand (&) character.

### Advanced arguments
* delay: Omits all emails for the given number in seconds
* altmail: Sends the warning to an additional email delivered with this argument. Note, that the administratir will always recieve an email when an alarma is triggered.
* trash: Removes all settings for the chosen metric.
* hilo: Uses 2 values to trigger an alarm when the first value is undershot or the second value is exceeded. Note, that the second value must equal or higher to the first value.

**Example**

    SET https://example.com?metric=01&percentage=50&delay=3000
	
This command will set the threshhold for the CPU usage to 50%. This will only trigger when the overusage will last for more than 5 Minutes (3.000 Seconds). 
	