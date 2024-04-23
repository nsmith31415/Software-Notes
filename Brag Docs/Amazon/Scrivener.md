#brag #amazon
### Technology used: 
* Various AWS Services:
	* CloudFormation
	* CloudWatch
	* SQS/SNS
	* APIGateway

### Problem: 
Network Engineers dislike having to find multiple different passwords to navigate the network, resulting in some engineers writing down passwords or saving them to their laptops.

### Solution: Scrivener
A FedRAMP-compliant certificate signing service and CLI tool to be deployed onto network devices allowing network engineers to acquire a certificate that will verify them end-to-end within the AWS network. 

### My biggest contribution: 
I had previous experience with the AWS network from my internship at AWS, so my job was to make sure that we were able to parse short device names and route engineers to the device that they are looking for. This was a complicated task because while some areas within the network had naming conventions, others didn't, or used older naming conventions that resulted in duplicate named devices from different regions or availability zones. 

I was in charge of setting up the logic to route our command line interface tool to the correct end device based on the engineer's input. What this ended up shaking down to was a lot of data analysis, many regular expressions, and a large amount of testing for edge cases.

I was able to manually audit the amount of devices we were able to successfully find, and before getting laid off by Amazon, I was preparing to automate this process into a weekly report. By the end of my employment with Amazon, I had confirmed that Scrivener CLI was able to successfully connect to 99.9% of the devices on the AWS network with a short name. The other devices could be successfully connected to by providing the short name and the region and network it was on (corp, prod, etc), or by providing the full network ID string.