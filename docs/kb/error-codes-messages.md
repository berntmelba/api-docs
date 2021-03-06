# Error Codes & Messages


## [](#error-code-1)Error Code: 1

```
<rsp stat="fail" version="1.0">
    <err code="1">Invalid API key or user key</err>
</rsp>
```

**Problem**: Either the user and/or API keys are
incorrect, or the API key has expired.

**Solution**: Check the user and API keys in the
request. If the user key was entered accurately, then submit a
request for a new API key.

## [](#error-code-2)Error Code: 2

```
<rsp stat="fail" version="1.0">
    <err code="2">Invalid action</err>
</rsp>
```

**Problem**: The requested operation was not
recognized by the API.

**Solution**: Verify that the requested operation is
valid for the target object type. If that operation is allowed,
then check for misspellings and other typos.

## [](#error-code-3)Error Code: 3

```
<rsp stat="fail" version="1.0">
    <err code="3">Invalid prospect ID</err>
</rsp>
```

**Problem**: Pardot could not find a match for the
provided prospect ID.

**Solution**: Verify that the prospect ID is
accurate.

## [](#error-code-4)Error Code: 4

```
<rsp stat="fail" version="1.0">
    <err code="4">Invalid prospect email address</err>
</rsp>
```

**Problem**: Pardot could not find a prospect with the provided email address (for read/update/delete),
or the prospect email address is too long (> 255 characters) or has invalid syntax
(does not match `/^[^ @]{1,64}@[^ @]{1,255}\.[^ @]{2,13}$/`) (for create/upsert).

**Solution**: If running create/upsert, verify the email address is valid.
If running read/update/delete, verify the a prospect with this email address exists in your Pardot account.

## [](#error-code-5)Error Code: 5

```
<rsp stat="fail" version="1.0">
    <err code="5">Invalid query parameters</err>
</rsp>
```

**Problem**: Pardot did not recognize any of the
provided search parameters.

**Solution**: Check parameter spellings. Also, ensure
that the specified search parameter is supported by the API. See
[Supported
Search Criteria](prospects#supported-search-criteria) in [Querying
Prospects](prospects) for more details.

## [](#error-code-6)Error Code: 6

```
<rsp stat="fail" version="1.0">
    <err code="6">Invalid time frame</err>
</rsp>
```

**Problem**: The value of the
`timeframe` search parameter was not recognized.

**Solution**: Check for misspellings in the
`timeframe` value. Also, verify that the provided value
is supported by the API. See [Supported Search
Criteria](prospects#supported-search-criteria) in [Prospects](prospects)
for supported `timeframe` values.

## [](#error-code-7)Error Code: 7

```
<rsp stat="fail" version="1.0">
    <err code="7">Invalid timestamp</err>
</rsp>
```

**Problem**: Pardot could not decipher a specified
timestamp.

**Solution**: Verify that the timestamp adheres to GNU
standards for date and time input. See [
GNU Date Input Format &amp; Syntax](http://www.gnu.org/software/tar/manual/html_node/Date-input-formats.html) for more information. Also,
ensure all characters in the timestamp are URL safe. See [Supported Search
Criteria](prospects#supported-search-criteria) in [Prospects](prospects)
for supported values.

## [](#error-code-8)Error Code: 8

```
<rsp stat="fail" version="1.0">
    <err code="8">Invalid time range</err>
</rsp>
```

**Problem**: The provided start timestamp is later
than the end timestamp.

**Solution**: Swap the values of the timestamps.

## [](#error-code-9)Error Code: 9

```
<rsp stat="fail" version="1.0">
    <err code="9">A prospect with the specified email address already exists</err>
</rsp>
```

**Problem**: The provided email address is already
assigned to a prospect within Pardot. This can occur if a
`create` request with the same email address is
submitted more than once.

**Solution**: Check the existing prospect record to
see if data can be merged through an `update`
request.

## [](#error-code-10)Error Code: 10

```
<rsp stat="fail" version="1.0">
    <err code="10">Invalid user ID</err>
</rsp>
```

**Problem**: The provided user ID does not exist in
Pardot.

**Solution**: Verify that the user ID was typed
correctly and matches the intended user in Pardot.

## [](#error-code-11)Error Code: 11

```
<rsp stat="fail" version="1.0">
    <err code="11">Invalid user email address</err>
</rsp>
```

**Problem**: The provided user email address could
not be found in Pardot.

**Solution**: Verify that the provided email address
belongs to a registered Pardot user and that it was typed
correctly.

## [](#error-code-12)Error Code: 12

```
<rsp stat="fail" version="1.0">
    <err code="12">Invalid group ID</err>
</rsp>
```

**Problem**: The provided group ID does not exist
in Pardot.

**Solution**: Verify that the group ID was typed
correctly and matches the intended group in Pardot.

## [](#error-code-13)Error Code: 13

```
<rsp stat="fail" version="1.0">
    <err code="13">One or more required parameters are missing</err>
</rsp>
```

**Problem**: One or more of the required parameters
for this type of request are missing.

**Solution**: Verify that all of the required
parameters have been provided. Check that all parameter names were
spelled accurately and as specified in [Object Field References](object-field-references). Ensure the
proper URL punctuation was used, including `?` before
parameters and `&` between parameters.

## [](#error-code-14)Error Code: 14

```
<rsp stat="fail" version="1.0">
    <err code="14">Non-existent prospect ID; No email address provided</err>
</rsp>
```

**Problem**: The ID provided for the
`upsert` was not valid, and no email address was
provided for a new prospect to be created.

**Solution**: Verify the provided ID. If creating a
new prospect was intended, ensure that an email address was
provided.

## [](#error-code-15)Error Code: 15

```
<rsp stat="fail" version="1.0">
    <err code="15">Login failed</err>
</rsp>
```

**Problem**: The provided email address, password,
or user key is invalid.

**Solution**: Check the provided credentials for
typos. Also, ensure that the specified user account has at least
"Marketing" access privileges.

## [](#error-code-16)Error Code: 16

```
<rsp stat="fail" version="1.0">
    <err code="16">Invalid ID</err>
</rsp>
```

**Problem**: The provided ID is not valid.

**Solution**: Ensure that only valid integer values
were provided.

## [](#error-code-17)Error Code: 17

```
<rsp stat="fail" version="1.0">
    <err code="17">Invalid ID range</err>
</rsp>
```

**Problem**: The provided ID range is not
valid.

**Solution**: Swap the values of the specified
IDs.

## [](#error-code-18)Error Code: 18

```
<rsp stat="fail" version="1.0">
    <err code="18">Invalid value for profile criteria matching status</err>
</rsp>
```

**Problem**: The provided value for a profile
criteria's matching status was not recognized.

**Solution**: Ensure that only the values
`match`, `nomatch`, or `unknown`
are being used.

## [](#error-code-19)Error Code: 19

```
<rsp stat="fail" version="1.0">
    <err code="19">Invalid value specified for sort_by</err>
</rsp>
```

**Problem**: The provided value for the
`sort_by` is not a supported sorting order.

**Solution**: Check that the specified sorting values
are listed in Using (Object Type): Supported Sorting Options
section for the target object.

## [](#error-code-20)Error Code: 20

```
<rsp stat="fail" version="1.0">
    <err code="20">Invalid value specified for sort_order</err>
</rsp>
```

**Problem**: The provided value for the
`sort_order` is not a supported sorting order.

**Solution**: Ensure that only the values
`ascending` or `descending` are being
used.

## [](#error-code-21)Error Code: 21

```
<rsp stat="fail" version="1.0">
    <err code="21">Invalid value specified for offset</err>
</rsp>
```

**Problem**: The provided value for
`offset` could not be interpreted as an integer.

**Solution**: Check for typos that may prevent the
value from being interpreted.

## [](#error-code-22)Error Code: 22

```
<rsp stat="fail" version="1.0">
    <err code="22">Unsupported feature in this version of the API</err>
</rsp>
```

**Problem**: The feature requested by the API call
is not implemented in this version of the API.

**Solution**: Update the request to use the necessary
API version.

## [](#error-code-23)Error Code: 23

```
<rsp stat="fail" version="1.0">
    <err code="23">Invalid value specified for limit</err>
</rsp>
```

**Problem**: The provided value for
`limit` is invalid.

**Solution**: Ensure that the provided value is an
integer and is no larger than 200.

## [](#error-code-24)Error Code: 24

```
<rsp stat="fail" version="1.0">
    <err code="24">Invalid visitor ID</err>
</rsp>
```

**Problem**: The provided visitor ID does not exist
in Pardot.

**Solution**: Verify that the visitor ID was typed
correctly and matches the intended visitor in Pardot.

## [](#error-code-25)Error Code: 25

```
<rsp stat="fail" version="1.0">
    <err code="25">Parameter is_starred must be true or false</err>
</rsp>
```

**Problem**: The value specified for
`is_starred` could not be interpreted as a boolean.

**Solution**: Verify that only the values
`true` or `false` were specified.

## [](#error-code-26)Error Code: 26

```
<rsp stat="fail" version="1.0">
    <err code="26">Parameter assigned must be true or false</err>
</rsp>
```

**Problem**: The value specified for
`assigned` could not be interpreted as a boolean.

**Solution**: Verify that only the values
`true` or `false` were specified.

## [](#error-code-27)Error Code: 27

```
<rsp stat="fail" version="1.0">
    <err code="27">Parameter deleted must be true or false</err>
</rsp>
```

**Problem:** The value specified for
`deleted` could not be interpreted as a boolean.

**Solution:** Verify that only the values
`true` or `false` were specified.

## [](#error-code-28)Error Code: 28

```
<rsp stat="fail" version="1.0">
    <err code="28">Parameter new must be true or false</err>
</rsp>
```

**Problem:** The value specified for
`new` could not be interpreted as a boolean.

**Solution:** Verify that only the values
`true` or `false` were specified.

## [](#error-code-29)Error Code: 29

```
<rsp stat="fail" version="1.0">
    <err code="29">Invalid value specified for score</err>
</rsp>
```

**Problem**: The value specified for
`score` could not be interpreted as an integer.

**Solution**: Check for typos that may prevent the
value from being interpreted correctly.

## [](#error-code-30)Error Code: 30

```
<rsp stat="fail" version="1.0">
    <err code="30">Invalid score range specified</err>
</rsp>
```

**Problem**: The provided score range is not
valid.

**Solution**: Swap the values of the specified
scores.

## [](#error-code-31)Error Code: 31

```
<rsp stat="fail" version="1.0">
    <err code="31">Invalid combination of parameters for score</err>
</rsp>
```

**Problem**: A conflicting set of query criteria
for the prospect's score has been specified.

**Solution**: Make sure that
`score_equal_to` is not being used in combination with
`score_greater_than` or
`score_less_than`.

## [](#error-code-32)Error Code: 32

```
<rsp stat="fail" version="1.0">
    <err code="32">Invalid value specified for grade</err>
</rsp>
```

**Problem**: The value specified for
`grade` is not one of the allowed options.

**Solution**: Check for typos that may prevent
`grade` from being interpreted correctly. See [Supported Search
Criteria](prospects#supported-search-criteria) in [Prospects](prospects)
for supported values. Also, ensure that the specified grades are
URL-encoded.

## [](#error-code-33)Error Code: 33

```
<rsp stat="fail" version="1.0">
    <err code="33">Invalid grade range specified</err>
</rsp>
```

**Problem**: The provided grade range is not
valid.

**Solution**: Swap the values of the specified
grades.

## [](#error-code-34)Error Code: 34

```
<rsp stat="fail" version="1.0">
    <err code="34">Invalid combination of parameters for grade</err>
</rsp>
```

**Problem**: A conflicting set of query criteria
for the grade has been specified.

**Solution**: Make sure that
`grade_equal_to` is not being used in combination with
`grade_greater_than` or
`grade_less_than`.

## [](#error-code-35)Error Code: 35

```
<rsp stat="fail" version="1.0">
    <err code="35">Invalid opportunity ID</err>
</rsp>
```

**Problem**: Pardot could not find a match for the
provided opportunity ID.

**Solution**: Verify that the opportunity ID is
accurate.

## [](#error-code-36)Error Code: 36

```
<rsp stat="fail" version="1.0">
    <err code="36">One or more required parameter values are missing</err>
</rsp>
```

**Problem**: Some of the parameters necessary to
complete the specified API request were omitted from the
request.

**Solution**: Ensure that all required parameters have
been included. In addition, check from typos in the parameter
names. Also check that the request has been properly formatted.

## [](#error-code-37)Error Code: 37

```
<rsp stat="fail" version="1.0">
    <err code="37">A SalesForce connector was detected</err>
</rsp>
```

**Problem**: Your Pardot account has a SalesForce
connector. When a SalesForce connector is present, opportunities and prospect account
cannot be modified by Pardot.

**Solution**: **_(NOT
RECOMMENDED)_** Deleting the SalesForce connector will
allow for opportunity modification to be done through the API.
However, doing so will disable synchronization with SalesForce. If
a SalesForce connector is present, modifications to opportunities
must be done within SalesForce.

## [](#error-code-38)Error Code: 38

```
<rsp stat="fail" version="1.0">
    <err code="38">Invalid campaign ID</err>
</rsp>
```

**Problem**: Pardot could not find a match for the
provided campaign ID.

**Solution**: Verify that the campaign ID is
accurate.

## [](#error-code-39)Error Code: 39

```
<rsp stat="fail" version="1.0">
    <err code="39">Invalid profile ID</err>
</rsp>
```

**Problem**: Pardot could not find a match for the
provided profile ID.

**Solution**: Verify that the profile ID is
accurate.

## [](#error-code-40)Error Code: 40

```
<rsp stat="fail" version="1.0">
    <err code="40">Invalid opportunity probability</err>
</rsp>
```

**Problem**: The value specified for
`probability` is not valid.

**Solution**: Ensure that the specified value is a
number between 0 and 100 inclusive.

## [](#error-code-41)Error Code: 41

```
<rsp stat="fail" version="1.0">
    <err code="41">Invalid probability range specified</err>
</rsp>
```

**Problem**: The specified probability range is not
valid.

**Solution**: Ensure that the specified values are
numbers between 0 and 100 inclusive. It may also be necessary to
swap the values of the specified probabilities.

## [](#error-code-42)Error Code: 42

```
<rsp stat="fail" version="1.0">
    <err code="42">Invalid opportunity value</err>
</rsp>
```

**Problem**: The value specified for
`value` is not valid.

**Solution**: Ensure that the specified value is a
non-negative number.

## [](#error-code-43)Error Code: 43

```
<rsp stat="fail" version="1.0">
    <err code="43">Invalid opportunity value range specified</err>
</rsp>
```

**Problem**: The specified value range is not
valid.

**Solution**: Ensure that the specified values are
non-negative numbers. It may also be necessary to swap the
specified values.

## [](#error-code-44)Error Code: 44

```
<rsp stat="fail" version="1.0">
    <err code="44">The provided prospect_id and prospect_email parameters do not match</err>
</rsp>
```

**Problem**: The specified
`prospect_email` and `prospect_id` parameters
do not correspond to the same prospect.

**Solution**: Ensure that the specified email address
and the ID both correspond to the desired prospect. (Note:
Typically, only one of these parameters is required. Consider
omitting one of them.)

## [](#error-code-45)Error Code: 45

```
<rsp stat="fail" version="1.0">
    <err code="45">The provided user_id and user_email parameters do not match</err>
</rsp>
```

**Problem**: The specified `user_id` and
`user_email` parameters do not correspond to the same
user.

**Solution**: Ensure that the specified email address
and the ID both correspond to the desired user. (Note: Typically,
only one of these parameters is required. Consider omitting one of
them.)

## [](#error-code-46)Error Code: 46

```
<rsp stat="fail" version="1.0">
    <err code="46">This API user lacks sufficient permissions for the requested operation</err>
</rsp>
```

**Problem**: The currently authenticated API user
has does not have the necessary permissions to perform the
requested operation.

**Solution**: Some API operations are only available
to users with Administrative permissions. If the requested
operation has such a requirement, re-authenticate as an
administrative user and resubmit the request. See the [Authentication](authentication) section for more
information.

## [](#error-code-47)Error Code: 47

```
<rsp stat="fail" version="1.0">
    <err code="47">Multiple assignment targets were specified</err>
</rsp>
```

**Problem**: More than one object was specified as
a target for this `ASSIGN` request. For example, both a
group and user may have been specified as targets of a prospect
assignment.

**Solution**: Ensure that only one target is specified
when submitting an `ASSIGN` request.

## [](#error-code-48)Error Code: 48

```
<rsp stat="fail" version="1.0">
    <err code="48">Invalid visit ID</err>
</rsp>
```

**Problem**: The provided visit ID does not exist
in Pardot.

**Solution**: Verify that the visit ID was typed
correctly and matches the intended visit in Pardot.

## [](#error-code-49)Error Code: 49

```
<rsp stat="fail" version="1.0">
    <err code="49">Access Denied</err>
</rsp>
```

**Problem**: User is not authorized to perform the requested operation either due to access restrictions or forbidden method of passing credentials

**Solution**: Verify user has required access to perform the requested operation.  Ensure credentials are passed via a supported method as per the API documentation.  Contact customer support if problem persists.

## [](#error-code-50)Error Code: 50

```
<rsp stat="fail" version="1.0">
    <err code="50">Invalid boolean</err>
</rsp>
```

**Problem**: Need a valid boolean value, like
true.

**Solution**: Make sure to use lowercase.

## [](#error-code-51)Error Code: 51

```
<rsp stat="fail" version="1.0">
    <err code="51">Invalid parameter</err>
</rsp>
```

**Problem**: Object type is invalid.

**Solution**: Change the object type to one of the
allowed types.

## [](#error-code-53)Error Code: 53

```
<rsp stat="fail" version="1.0">
    <err code="53">Client IP address/location must be activated before accessing API</err>
</rsp>
```

**Problem**: IP is not whitelisted.

**Solution**: Whitelist IP address to access the
API.

## [](#error-code-54)Error Code: 54

```
<rsp stat="fail" version="1.0">
    <err code="54">Email address is already in use</err>
</rsp>
```

**Problem**: Email address is already being used by
other prospect.

**Solution**: Use different email address.

## [](#error-code-55)Error Code: 55

```
<rsp stat="fail" version="1.0">
    <err code="55">Invalid list ID</err>
</rsp>
```

**Problem**: You either did not specify the list
ID, or that List ID doesn't exist.

**Solution**: Specify an ID, or check to make sure
using the correct ID.

## [](#error-code-56)Error Code: 56

```
<rsp stat="fail" version="1.0">
    <err code="56">Invalid number entered for field</err>
</rsp>
```

**Problem**: The value entered doesn't match the
field's type of Number.

**Solution**: Verify that there are no characters in
the value.

## [](#error-code-57)Error Code: 57

```
<rsp stat="fail" version="1.0">
    <err code="57">Invalid date entered for field</err>
</rsp>
```

**Problem**: The value entered doesn't match the
field's type of Date, it is an invalid format.

**Solution**: Verify that the timestamp adheres to GNU
standards for date and time input. See [
GNU Date Input Format &amp; Syntax](http://www.gnu.org/software/tar/manual/html_node/Date-input-formats.html) for more information. Also,
ensure all characters in the timestamp are URL safe. See [Supported Search
Criteria](prospects#supported-search-criteria) in [Prospects](prospects)
for supported values.

## [](#error-code-58)Error Code: 58

```
<rsp stat="fail" version="1.0">
    <err code="58">That prospect is already a memeber of that list. Update the membership instead.</err>
</rsp>
```

**Problem**: The prospect is a member of the list
already.

**Solution**: Update the membership.

## [](#error-code-59)Error Code: 59

```
<rsp stat="fail" version="1.0">
    <err code="59">A CRM connector was detected/err>
</rsp>
```

**Problem**: Your Pardot account has a CRM
connector. When a CRM connector is present, opportunities and prospect account cannot be
modified by Pardot.

**Solution**: **_(NOT
RECOMMENDED)_** Deleting the CRM connector will allow
for opportunity modification to be done through the API. However,
doing so will disable synchronization with your CRM. If a CRM
connector is present, modifications to opportunities must be done
within your CRM.

## [](#error-code-60)Error Code: 60

```
<rsp stat="fail" version="1.0">
    <err code="60">Invalid HTTP request method</err>
</rsp>
```

**Problem**: Cannot delete with this method.

**Solution**: Use methods POST or DELETE.

## [](#error-code-61)Error Code: 61

```
<rsp stat="fail" version="1.0">
    <err code="61">Invalid prospect account id</err>
</rsp>
```

**Problem**: Prospect Account ID was incorrect or
doesn't exist.

**Solution**: Verify that the prospect account ID was
typed correctly and matches the intended Propsect Account in
Pardot.

## [](#error-code-62)Error Code: 62

```
<rsp stat="fail" version="1.0">
    <err code="62">Conflicting Update</err>
</rsp>
```

**Problem**: Another update is occurring at the
same time.

**Solution**: Wait before performing this action.

## [](#error-code-63)Error Code: 63

```
<rsp stat="fail" version="1.0">
    <err code="63">Too many IDs specified</err>
</rsp>
```

**Problem**: There is a limit on how many IDs you
can specify for this query.

**Solution**: Lower the amount of IDs you are querying
for.

## [](#error-code-64)Error Code: 64

```
<rsp stat="fail" version="1.0">
    <err code="64">Email content missing required variables</err>
</rsp>
```

**Problem**: The content of the email is missing
required variables.

**Solution**: Ensure that all required variables, such
as unsubscribe link, are present.

## [](#error-code-65)Error Code: 65

```
<rsp stat="fail" version="1.0">
    <err code="65">Invalide email format</err>
</rsp>
```

**Problem**: Doesn't have all required fields
present or are not in proper format, such as from address.

**Solution**: Ensure all fields are present,
populated, and in proper format.

## [](#error-code-66)Error Code: 66

```
<rsp stat="fail" version="1.0">
    <err code="66">You have exceeded your concurrent request limit.  Please wait, before trying again</err>
</rsp>
```

**Problem**: Have made too many requests in this
time period.

**Solution**: Wait a little before making more
requests.

## [](#error-code-67)Error Code: 67

```
<rsp stat="fail" version="1.0">
    <err code="67">You have reached or exceeded the limit of how many of this type of object you may have.</err>
</rsp>
```

**Problem**: You have too many of this object type to create more.

**Solution**: Delete some of the object if you need to make more.

## [](#error-code-68)Error Code: 68

```
<rsp stat="fail" version="1.0">
    <err code="68">Template with this id does not exist.</err>
</rsp>
```

**Problem**: The template you are trying to access does not exist.

**Solution**: Make sure you are using the correct template ID or create a new one to use.

## [](#error-code-70)Error Code: 70

```
<rsp stat="fail" version="1.0">
    <err code="70">Batch processing is limited to 50 prospects at once.</err>
</rsp>
```

**Problem**: You are requesting to batch more prospects in an operation than we allow.

**Solution**: Ensure that your batch request has 50 or fewer prospects.

## [](#error-code-71)Error Code: 71

```
<rsp stat="fail" version="1.0">
    <err code="71">Input needs to be valid JSON or XML</err>
</rsp>
```

**Problem**: You've inputted invalid JSON or XML.

**Solution**: Ensure that your request is properly formatted.

## [](#error-code-72)Error Code: 72

```
<rsp stat="fail" version="1.0">
    <err code="72">JSON has been corrupted, hash does not match</err>
</rsp>
```

**Problem**: The encoded JSON has been corrupted at some point.

**Solution**: Please ensure that you are sending the correct information.

## [](#error-code-73)Error Code: 73

```
<rsp stat="fail" version="1.0">
    <err code="73">Currently there is not an Email Plug-in Campaign associated to successfully track this email. Please contact your Pardot administrator to ensure there is a proper campaign associated with the Account Settings in Pardot.</err>
</rsp>
```

**Problem**: Currently there is not an Email Plug-in Campaign associated to successfully track this email.

**Solution**: Please contact your Pardot administrator to ensure there is a proper campaign associated with the Account Settings in Pardot.

## [](#error-code-74)Error Code: 74

```
<rsp stat="fail" version="1.0">
    <err code="74">The email client is not supported by the plugin API</err>
</rsp>
```

**Problem**: The email client used is not supported by this API.

**Solution**: Please use an appropriate email client.

## [](#error-code-75)Error Code: 75

```
<rsp stat="fail" version="1.0">
    <err code="75">There was an error processing the request for the account variable tags</err>
</rsp>
```

**Problem**: There was an error processing the request for the account variable tags.

**Solution**: Please review the variable tags, and resubmit the request.

## [](#error-code-76)Error Code: 76

```
<rsp stat="fail" version="1.0">
    <err code="76">API access was disabled</err>
</rsp>
```

**Problem**: API access for your account has been disabled.

**Solution**: Contact customer support.

## [](#error-code-77)Error Code: 77

```
<rsp stat="fail" version="1.0">
    <err code="77">Invalid prospect fid</err>
</rsp>
```

**Problem**: The provided Prospect FID was invalid.

**Solution**: Please provide a valid Prospect FID.

## [](#error-code-79)Error Code: 79

```
<rsp stat="fail" version="1.0">
    <err code="79">Invalid CRM_FID</err>
</rsp>
```

**Problem**: The CRM FID provided is invalid.

**Solution**: Please provide a valid CRM FID that can be accessed by your account, or is already attached to a prospect.

## [](#error-code-80)Error Code: 80

```
<rsp stat="fail" version="1.0">
    <err code="80">Invalid CRM_TYPE</err>
</rsp>
```

**Problem**: The CRM type provided or used is invalid.

**Solution**: Please specify a correct CRM type.

## [](#error-code-81)Error Code: 81

```
<rsp stat="fail" version="1.0">
    <err code="81">Prospect ID and FID do not match</err>
</rsp>
```

**Problem**: The provided Prospect ID and FID do not match a single prospect.

**Solution**: Please provide a prospect ID and FID that match a single prospect.

## [](#error-code-83)Error Code: 83

```
<rsp stat="fail" version="1.0">
    <err code="83">No valid CRM connectors available</err>
</rsp>
```

**Problem**: Your account does not have an available CRM connector.

**Solution**: Please add a CRM connector to your account.

## [](#error-code-85)Error Code: 85

```
<rsp stat="fail" version="1.0">
    <err code="85">Unable to save the prospect</err>
</rsp>
```

**Problem**: For some reason, the prospect was not saved.

**Solution**: Please resubmit the request or review the original request for errors.

## [](#error-code-86)Error Code: 86

```
<rsp stat="fail" version="1.0">
    <err code="86">Invalid Template id</err>
</rsp>
```

**Problem**: The template ID provided does not correspond to a template.

**Solution**: Please provide a template ID that is valid.

## [](#error-code-88)Error Code: 88

```
<rsp stat="fail" version="1.0">
    <err code="88">Your account must use version 4 of the API.</err>
</rsp>
```

**Problem**: You have requested version 3 of the API, but your account must use version 4.

**Solution**: Please make the request using `/version/4` in place of `/version/3`.

## [](#error-code-89)Error Code: 89

```
<rsp stat="fail" version="1.0">
    <err code="89">Your account is unable to use version 4 of the API.</err>
</rsp>
```

**Problem**: You have requested version 4 of the API, but your account must use version 3.

**Solution**: Please make the request using `/version/3` in place of `/version/4`.

## [](#error-code-90)Error Code: 90

```
<rsp stat="fail" version="1.0">
    <err code="90">Prospect array should be a flat array of attributes</err>
</rsp>
```

**Problem**: The prospect array given was not a flat array, and it should have been.

**Solution**: Resubmit the request with a flat array. [example](/kb/api-version-4/prospects#endpoints-for-batch-processing)

## [](#error-code-91)Error Code: 91

```
<rsp stat="fail" version="1.0">
    <err code="91">Prospect array must be keyed by email address</err>
</rsp>
```

**Problem**: The prospect array given was not keyed by email addresses, but should have been.

**Solution**: Resubmit the request with an array keyed by email addresses. [example](/kb/api-version-3/prospects#endpoints-for-batch-processing)

## [](#error-code-92)Error Code: 92

```
<rsp stat="fail" version="1.0">
    <err code="92">Prospect record could not be found</err>
</rsp>
```

**Problem**: The prospect record was not found with the provided information.

**Solution**: Resubmit the request with different parameters.

## [](#error-code-93)Error Code: 93

```
<rsp stat="fail" version="1.0">
    <err code="93">The selected template is missing send options</err>
</rsp>
```

**Problem**: Send options are required for the template.

**Solution**: Resubmit the request with send options.

## [](#error-code-94)Error Code: 94

```
<rsp stat="fail" version="1.0">
    <err code="94">The provided version is not a valid number</err>
</rsp>
```

**Problem**: The version number used is not valid.

**Solution**: Resubmit the request with a valid version number.

## [](#error-code-95)Error Code: 95

```
<rsp stat="fail" version="1.0">
    <err code="95">Folder name is invalid</err>
</rsp>
```

**Problem**: The name for the folder is not valid.

**Solution**: Resubmit the request with a valid folder name.

## [](#error-code-96)Error Code: 96

```
<rsp stat="fail" version="1.0">
    <err code="96">User does not have access to this folder</err>
</rsp>
```

**Problem**: The role assigned for this user does not have access to this folder.

**Solution**: Update the users permissions and resubmit the request.

## [](#error-code-97)Error Code: 97

```
<rsp stat="fail" version="1.0">
    <err code="97">The folder ID provided does not exist</err>
</rsp>
```

**Problem**: No folder was found for the ID provided.

**Solution**: Resubmit the request with a different folder ID.

## [](#error-code-98)Error Code: 98

```
<rsp stat="fail" version="1.0">
    <err code="98">Prospect not mailable</err>
</rsp>
```

**Problem**: One or more of the recipient prospects cannot receive the email requested (due to opting out, being flagged as "Do Not Email", or for other reasons)

**Solution**: Check that the recipient list is correct, and that the prospect's email preferences are up-to-date.

## [](#error-code-99)Error Code: 99

```
<rsp stat="fail" version="1.0">
    <err code="99">User with the provided email already exists</err>
</rsp>
```

**Problem**: A user with the email provided is already in the system.

**Solution**: Resubmit the request with a different email address.

## [](#error-code-100)Error Code: 100

```
<rsp stat="fail" version="1.0">
    <err code="100">The provided time zone is invalid</err>
</rsp>
```

**Problem**: The value provided does not match a valid time zone.

**Solution**: Resubmit the request with a different time zone.

## [](#error-code-101)Error Code: 101

```
<rsp stat="fail" version="1.0">
    <err code="101">The provided role is invalid</err>
</rsp>
```

**Problem**: The value provided for role is not valid.

**Solution**: Resubmit the request with a different role.

## [](#error-code-102)Error Code: 102

```
<rsp stat="fail" version="1.0">
    <err code="102">The CRM Username specified is currently applied to another user</err>
</rsp>
```

**Problem**: This CRM username is already in use and cannot be used for another user.

**Solution**: Resubmit the request with a different CRM username to apply for the user.

## [](#error-code-103)Error Code: 103

```
<rsp stat="fail" version="1.0">
    <err code="103">A CRM connector was not detected</err>
</rsp>
```

**Problem**: A CRM connector was not found.

**Solution**: Make sure to configure a valid CRM connector and try again.

## [](#error-code-104)Error Code: 104

```
<rsp stat="fail" version="1.0">
    <err code="104">The CRM Username specified was not detected</err>
</rsp>
```

**Problem**: The CRM username was not found.

**Solution**: Verify the CRM username provided is correct and try again.

## [](#error-code-105)Error Code: 105

```
<rsp stat="fail" version="1.0">
    <err code="105">There is no activation hash for the specified user</err>
</rsp>
```

**Problem**: The activation hash for the provided user was not found.

## [](#error-code-106)Error Code: 106

```
<rsp stat="fail" version="1.0">
    <err code="106">User is already active</err>
</rsp>
```

**Problem**: The user is already activate.

## [](#error-code-107)Error Code: 107

```
<rsp stat="fail" version="1.0">
    <err code="107">Password does not meet requirements</err>
</rsp>
```

**Problem**: The submitted password does not meet the password requirements.

**Solution**: Resubmit the request using a password that meets the [requirements](http://help.pardot.com/customer/portal/articles/2128470-password-faq).

## [](#error-code-108)Error Code: 108

```
<rsp stat="fail" version="1.0">
    <err code="108">This Asset cannot be deleted because it is being used in other places.</err>
</rsp>
```

**Problem**: Unable to delete an asset if it is used in other places.

**Solution**: Remove all dependencies of this asset and try again.

## [](#error-code-109)Error Code: 109

```
<rsp stat="fail" version="1.0">
    <err code="109">The requested record was not found.</err>
</rsp>
```

**Problem**: Unable to find the requested resource.

**Solution**: Verify the parameters are correct and resubmit the request.

## [](#error-code-110)Error Code: 110

```
<rsp stat="fail" version="1.0">
    <err code="110">Invalid Account Id</err>
</rsp>
```

**Problem**: Invalid account id submitted.

**Solution**: Verify the account id is correct and resubmit the request.

## [](#error-code-111)Error Code: 111

```
<rsp stat="fail" version="1.0">
    <err code="111">The Integration Username specified is currently applied to another Account</err>
</rsp>
```

**Problem**: Unable to use the submitted username as it is already used.

**Solution**: Resubmit the request using a different integration username.

## [](#error-code-112)Error Code: 112

```
<rsp stat="fail" version="1.0">
    <err code="112">Missing recipient to Track With Engage.</err>
</rsp>
```

**Problem**: The recipient parameter is missing.

**Solution**: Resubmit the request with a valid recipient.

## [](#error-code-113)Error Code: 113

```
<rsp stat="fail" version="1.0">
    <err code="113">Missing CRM ID or Email Address of recipient.</err>
</rsp>
```

**Problem**: The request is missing required information.

**Solution**: Resubmit the request with a valid CRM ID or email address.

## [](#error-code-114)Error Code: 114

```
<rsp stat="fail" version="1.0">
    <err code="114">Invalid CRM ID or Email Address of recipient.</err>
</rsp>
```

**Problem**: The CRM ID or email address is invalid.

**Solution**: Resubmit the request with a valid CRM ID or email address.

## [](#error-code-115)Error Code: 115

```
<rsp stat="fail" version="1.0">
    <err code="115">Number of recipients is more than threshold.</err>
</rsp>
```

**Problem**: The number of recipients provided is too large.

**Solution**: Resubmit the request with less recipients.

## [](#error-code-116)Error Code: 116

```
<rsp stat="fail" version="1.0">
    <err code="116">Request outdated.</err>
</rsp>
```

**Problem**: The request time has expired.

**Solution**: Resubmit the request.

## [](#error-code-117)Error Code: 117

```
<rsp stat="fail" version="1.0">
    <err code="117">There was an error deleting the micro campaign.</err>
</rsp>
```

**Problem**: There was an error deleting the micro campaign.

## [](#error-code-118)Error Code: 118

```
<rsp stat="fail" version="1.0">
    <err code="118">This API can only be called in a test environment.</err>
</rsp>
```

**Problem**: This endpoint can only be called in a test environment.

## [](#error-code-119)Error Code: 119

```
<rsp stat="fail" version="1.0">
    <err code="119">Unable to create refresh tokens for Salesforce connector</err>
</rsp>
```

**Problem**: Unable to create a refresh token for the Salesforce connector for authentication.

**Solution**: Resubmit the request to try again. If the problem persists, contact support.

## [](#error-code-120)Error Code: 120

```
<rsp stat="fail" version="1.0">
    <err code="120">Unable to verify Salesforce connector</err>
</rsp>
```

**Problem**: Unable to verify the Salesforce connector.

**Solution**: Resubmit the request to try again. If the problem persists, contact support.

## [](#error-code-121)Error Code: 121

```
<rsp stat="fail" version="1.0">
    <err code="121">Unable to sync Prospect with Salesforce</err>
</rsp>
```

**Problem**: Unable to sync prospects with Salesforce.

**Solution**: Resubmit the request to try again. If the problem persists, contact support.

## [](#error-code-122)Error Code: 122

```
<rsp stat="fail" version="1.0">
    <err code="122">Daily API rate limit met</err>
</rsp>
```

**Problem**: The daily allowed API requests have been met.

**Solution**: Wait until the next calendar day for the daily limit to reset and try again.

## [](#error-code-123)Error Code: 123

```
<rsp stat="fail" version="1.0">
    <err code="123">Unable to verify Salesforce username; User may already have a verified Salesforce username.</err>
</rsp>
```

**Problem**: Unable to verify Salesforce username.

**Solution**: Verify if the username has already been verified in the system.

## [](#error-code-124)Error Code: 124

```
<rsp stat="fail" version="1.0">
    <err code="124">Unable to set Salesforce username or id</err>
</rsp>
```

**Problem**: Unable to set the Salesforce username or id.

**Solution**: Verify the Salesforce username or ID is correct and resubmit the request.

## [](#error-code-125)Error Code: 125

```
<rsp stat="fail" version="1.0">
    <err code="125">Cannot accept both user_id and crm_owner_fid.</err>
</rsp>
```

**Problem**: This request only accepts a user_id or crm_owner_fid but not both.

**Solution**: Resubmit the request passing only a user_id or crm_owner_fid.

## [](#error-code-126)Error Code: 126

```
<rsp stat="fail" version="1.0">
    <err code="126">Invalid authentication mechanism</err>
</rsp>
```

**Problem**: This authentication method has been deprecated.

**Solution**: Resubmit the request using a valid [authentication](/#authentication) method.

## [](#error-code-131)Error Code: 131

```
<rsp stat="fail" version="1.0">
    <err code="131">Your account is locked due to too many failed login attempts. Reset your password at https://pi.pardot.com/user/passwordReset</err>
</rsp>
```

**Problem**: Too many invalid api requests have been made.

**Solution**: Reset your password at https://pi.pardot.com/user/passwordReset

## [](#error-code-10000)Error Code: 10000

```
<rsp stat="fail" version="1.0">
    ...
    <err code="10000" param="...">...</err>
    ...
</rsp>
```

**Problem**: An error occurred when processing the
parameter designated in the `param` attribute of the
`<err>` node. Several `<err>`
nodes may be contained within the ```
<rsp>` node if
multiple errors occurred.

**Solution**: The `msg` attribute of each
`<err>` node should contain advice as to how to
remedy the error(s).
