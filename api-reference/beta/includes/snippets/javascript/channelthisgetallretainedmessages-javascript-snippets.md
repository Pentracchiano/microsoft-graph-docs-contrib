---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let channel = await client.api('/teams/8b081ef6-4792-4def-b2c9-c363a1bf41d5/channels/getAllRetainedMessages')
	.version('beta')
	.get();

```