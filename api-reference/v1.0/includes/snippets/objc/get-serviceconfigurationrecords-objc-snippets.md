---
description: "Automatically generated file. DO NOT MODIFY"
---

```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/domains/{domain-name}/serviceConfigurationRecords"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
	completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

		NSError *jsonError = nil;
		NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
		NSMutableArray *domainDnsRecordList = [[NSMutableArray alloc] init];
		domainDnsRecordList = [jsonFinal valueForKey:@"value"];
		MSGraphDomainDnsRecord *domainDnsRecord = [[MSGraphDomainDnsRecord alloc] initWithDictionary:[domainDnsRecordList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```