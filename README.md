# ![LOGO](logo.png) LaunchDarkly **flow**ground Connector

## Description

A generated **flow**ground connector for the LaunchDarkly API (version 2.0.5).

Generated from: https://api.apis.guru/v2/specs/launchdarkly.com/2.0.5/swagger.json<br/>
Generated at: 2019-05-07T17:42:41+03:00

## API Description

Build custom integrations with the LaunchDarkly REST API

## Authorization

Supported authorization schemes:
- API Key
## Actions

### You can issue a GET request to the root resource to find all of the resource categories supported by the API.

*Tags:* `Root`

### Get a list of all audit log entries. The query parameters allow you to restrict the returned results by date ranges, resource specifiers, or a full-text search query.

*Tags:* `Audit log`

#### Input Parameters
* `before` - _optional_ - A timestamp filter, expressed as a Unix epoch time in milliseconds. All entries returned will have before this timestamp.
* `after` - _optional_ - A timestamp filter, expressed as a Unix epoch time in milliseconds. All entries returned will have occured after this timestamp.
* `q` - _optional_ - Text to search for. You can search for the full or partial name of the resource involved or fullpartial email address of the member who made the change.
* `limit` - _optional_ - A limit on the number of audit log entries to be returned, between 1 and 20.
* `spec` - _optional_ - A resource specifier, allowing you to filter audit log listings by resource.

### Use this endpoint to fetch a single audit log entry by its resouce ID.

*Tags:* `Audit log`

#### Input Parameters
* `resourceId` - _required_ - The resource ID.

### Get a list of statuses for all feature flags. The status includes the last time the feature flag was requested, as well as the state of the flag.

*Tags:* `Feature flags`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.

### Get the status for a particular feature flag.

*Tags:* `Feature flags`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `featureFlagKey` - _required_ - The feature flag's key. The key identifies the flag in your code.

### Get a list of all features in the given project.

*Tags:* `Feature flags`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `env` - _optional_ - By default, each feature will include configurations for each environment. You can filter environments with the env query parameter. For example, setting env=production will restrict the returned configurations to just your production environment.
* `tag` - _optional_ - Filter by tag. A tag can be used to group flags across projects.

### Creates a new feature flag.

*Tags:* `Feature flags`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.

### Delete a feature flag in all environments. Be careful-- only delete feature flags that are no longer being used by your application.

*Tags:* `Feature flags`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `featureFlagKey` - _required_ - The feature flag's key. The key identifies the flag in your code.

### Get a single feature flag by key.

*Tags:* `Feature flags`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `featureFlagKey` - _required_ - The feature flag's key. The key identifies the flag in your code.
* `env` - _optional_ - By default, each feature will include configurations for each environment. You can filter environments with the env query parameter. For example, setting env=production will restrict the returned configurations to just your production environment.

### Perform a partial update to a feature.

*Tags:* `Feature flags`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `featureFlagKey` - _required_ - The feature flag's key. The key identifies the flag in your code.

### Returns a list of all members in the account.

*Tags:* `Team members`

### Invite new members.

*Tags:* `Team members`

### Delete a team member by ID.

*Tags:* `Team members`

#### Input Parameters
* `memberId` - _required_ - The member ID.

### Get a single team member by ID.

*Tags:* `Team members`

#### Input Parameters
* `memberId` - _required_ - The member ID.

### Modify a team member by ID.

*Tags:* `Team members`

#### Input Parameters
* `memberId` - _required_ - The member ID.

### Returns a list of all projects in the account.

*Tags:* `Projects`

### Create a new project with the given key and name.

*Tags:* `Projects`

### Delete a project by key. Caution-- deleting a project will delete all associated environments and feature flags. You cannot delete the last project in an account.

*Tags:* `Projects`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.

### Fetch a single project by key.

*Tags:* `Projects`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.

### Modify a project by ID.

*Tags:* `Projects`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.

### Create a new environment in a specified project with a given name, key, and swatch color.

*Tags:* `Environments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.

### Delete an environment in a specific project.

*Tags:* `Environments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.

### Get an environment given a project and key.

*Tags:* `Environments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.

### Modify an environment by ID.

*Tags:* `Environments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.

### Return a complete list of custom roles.

*Tags:* `Custom roles`

### Create a new custom role.

*Tags:* `Custom roles`

### Delete a custom role by key.

*Tags:* `Custom roles`

#### Input Parameters
* `customRoleKey` - _required_ - The custom role key.

### Get one custom role by key.

*Tags:* `Custom roles`

#### Input Parameters
* `customRoleKey` - _required_ - The custom role key.

### Modify a custom role by key.

*Tags:* `Custom roles`

#### Input Parameters
* `customRoleKey` - _required_ - The custom role key.

### Get a list of all user segments in the given project.

*Tags:* `User segments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `tag` - _optional_ - Filter by tag. A tag can be used to group flags across projects.

### Creates a new user segment.

*Tags:* `User segments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.

### Delete a user segment.

*Tags:* `User segments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `userSegmentKey` - _required_ - The user segment's key. The key identifies the user segment in your code.

### Get a single user segment by key.

*Tags:* `User segments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `userSegmentKey` - _required_ - The user segment's key. The key identifies the user segment in your code.

### Perform a partial update to a user segment.

*Tags:* `User segments`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `userSegmentKey` - _required_ - The user segment's key. The key identifies the user segment in your code.

### Search users in LaunchDarkly based on their last active date, or a search query. It should not be used to enumerate all users in LaunchDarkly-- use the List users API resource.

*Tags:* `Users`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `q` - _optional_ - Search query.
* `limit` - _optional_ - Pagination limit.
* `offset` - _optional_ - Specifies the first item to return in the collection.
* `after` - _optional_ - A timestamp filter, expressed as a Unix epoch time in milliseconds. All entries returned will have occured after this timestamp.

### List all users in the environment. Includes the total count of users. In each page, there will be up to 'limit' users returned (default 20). This is useful for exporting all users in the system for further analysis. Paginated collections will include a next link containing a URL with the next set of elements in the collection.

*Tags:* `Users`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `limit` - _optional_ - Pagination limit.
* `h` - _optional_ - This parameter is required when following "next" links.
* `scrollId` - _optional_ - This parameter is required when following "next" links.

### Delete a user by ID.

*Tags:* `Users`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `userKey` - _required_ - The user's key.

### Get a user by key.

*Tags:* `Users`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `userKey` - _required_ - The user's key.

### Fetch a single flag setting for a user by key.

*Tags:* `User settings`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `userKey` - _required_ - The user's key.

### Fetch a single flag setting for a user by key.

*Tags:* `User settings`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `userKey` - _required_ - The user's key.
* `featureFlagKey` - _required_ - The feature flag's key. The key identifies the flag in your code.

### Specifically enable or disable a feature flag for a user based on their key.

*Tags:* `User settings`

#### Input Parameters
* `projectKey` - _required_ - The project key, used to tie the flags together under one project so they can be managed together.
* `environmentKey` - _required_ - The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
* `userKey` - _required_ - The user's key.
* `featureFlagKey` - _required_ - The feature flag's key. The key identifies the flag in your code.

### Fetch a list of all webhooks.

*Tags:* `Webhooks`

### Create a webhook.

*Tags:* `Webhooks`

### Delete a webhook by ID.

*Tags:* `Webhooks`

#### Input Parameters
* `resourceId` - _required_ - The resource ID.

### Get a webhook by ID.

*Tags:* `Webhooks`

#### Input Parameters
* `resourceId` - _required_ - The resource ID.

### Modify a webhook by ID.

*Tags:* `Webhooks`

#### Input Parameters
* `resourceId` - _required_ - The resource ID.

## License

**flow**ground :- Telekom iPaaS / launchdarkly-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
