# ![LOGO](logo.png) Crossbrowsertesting.com Screenshot Comparisons **flow**ground Connector

## Description

A generated **flow**ground connector for the Crossbrowsertesting.com Screenshot Comparisons API (version 3.0.0).

Generated from: https://api.apis.guru/v2/specs/crossbrowsertesting.com/3.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:40:08+03:00

## API Description

What's in this version: 
 1. Compare two screenshots for layout differences 
 2. Compare a full screenshot test of browsers to a single baseline browser for layout differences. 
 3. Compare a screenshot test version to another test version - good for regression tests. 
 4. Get links to the Comparison UI for visual representation of layout differences

## Authorization

Supported authorization schemes:
- Basic Authentication

## Actions

### Compare Screenshot Test Versions

> Get comparison results for all browsers in target screenshot test against the same browser in the base screenshot test. This is a good method for regression testing. For example, you've run a screenshot test against a set of browsers that is "good". Then, after some changes, you run a new screenshot test against the same set of browsers. This method will compare each of the same browsers against each other. For example, IE9 will be compared to IE9 from an earlier test. This is a many-to-many comparison where the OS/Browser/Resolution must match between the two test versions in order for the comparison to return results. The two versions can be from the same screenshot_test_id or not.

#### Input Parameters
* `target_screenshot_test_id` - _required_ - test id of the target Screenshot Test
* `target_version_id` - _required_ - version id of the target Screenshot Test
* `base_version_id` - _required_ - version id of the base Screenshot Test
* `format` - _optional_ - The format of the returned data. Possible values are "json" or "jsonp".
* `callback` - _optional_ - Name of callback method for JSONP requests.
* `tolerance` - _optional_ - Used as the basis for detecting box model differences in element positioning and dimensions that should be flagged and reported back to the comparison results. The default is 30px which is a good basis for finding notable layout differences.

### Compare Full Screenshot Test

> Get comparison results for all browsers in target screenshot test against a base screenshot result. The base result can be from the same test or from another test run at an earlier time. This is a one-to-many comparison.

#### Input Parameters
* `target_screenshot_test_id` - _required_ - test id of the target Screenshot Test
* `target_version_id` - _required_ - version id of the target Screenshot Test
* `base_result_id` - _required_ - result id of the base Screenshot Test
* `format` - _optional_ - The format of the returned data. Possible values are "json" or "jsonp".
* `callback` - _optional_ - Name of callback method for JSONP requests.
* `tolerance` - _optional_ - Used as the basis for detecting box model differences in element positioning and dimensions that should be flagged and reported back to the comparison results. The default is 30px which is a good basis for finding notable layout differences.

### Compare Single Screenshot

> Get comparison results for a single target screenshot result against a base screenshot result. This is a one-to-one comparison.

#### Input Parameters
* `target_screenshot_test_id` - _required_ - test id of the target Screenshot Test
* `target_version_id` - _required_ - version id of the target Screenshot Test
* `target_result_id` - _required_ - result id of the target Screenshot Test
* `base_result_id` - _required_ - result id of the base Screenshot Test
* `format` - _optional_ - The format of the returned data. Possible values are "json" or "jsonp".
* `callback` - _optional_ - Name of callback method for JSONP requests.
* `tolerance` - _optional_ - Used as the basis for detecting box model differences in element positioning and dimensions that should be flagged and reported back to the comparison results. The default is 30px which is a good basis for finding notable layout differences.

## License

**flow**ground :- Telekom iPaaS / crossbrowsertesting-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
