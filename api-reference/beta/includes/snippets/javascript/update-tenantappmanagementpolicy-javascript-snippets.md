---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const tenantAppManagementPolicy = {
    isEnabled: true,
    applicationRestrictions: {
        passwordCredentials: [
            {
                restrictionType: 'passwordAddition',
                maxLifetime: null,
                restrictForAppsCreatedAfterDateTime: '2021-04-01T10:37:00Z'
            },
            {
                restrictionType: 'passwordLifetime',
                maxLifetime: 'P4DT12H30M5S',
                restrictForAppsCreatedAfterDateTime: '2019-01-01T10:37:00Z'
            }
        ]
    }
};

await client.api('/policies/defaultAppManagementPolicy')
	.version('beta')
	.update(tenantAppManagementPolicy);

```