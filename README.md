**Latest stable version is: https://github.com/sendinblue/APIv3-python-library/tree/v4.2.2**

# SendinBlue's API v3 Python Library

SendinBlue's API exposes the entire SendinBlue features via a standardized programmatic interface. Please refer to the full [documentation](https://developers.sendinblue.com) to learn more.

This is the wrapper for the API. It implements all the features of the API v3.

SendinBlue's API matches the [OpenAPI v2 definition](https://www.openapis.org/). The specification can be downloaded [here](https://api.sendinblue.com/v3/swagger_definition.yml).

This PYTHON package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project and is reviewed and maintained by SendinBlue:

- API version: 3.0.0
- Build package: io.swagger.codegen.v3.generators.python.PythonClientCodegen
For more information, please visit [https://account.sendinblue.com/support](https://account.sendinblue.com/support)

## Requirements.

Compatible from Python version 2.7 to 3.5

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import sib_api_v3_sdk 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import sib_api_v3_sdk
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
configuration = sib_api_v3_sdk.Configuration()
configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api-key'] = 'Bearer'
# Configure API key authorization: partner-key
configuration = sib_api_v3_sdk.Configuration()
configuration.api_key['partner-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['partner-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.AccountApi(sib_api_v3_sdk.ApiClient(configuration))

try:
    # Get your account informations, plans and credits details
    api_response = api_instance.get_account()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AccountApi->get_account: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to *https://api.sendinblue.com/v3*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountApi* | [**get_account**](docs/AccountApi.md#get_account) | **GET** /account | Get your account informations, plans and credits details
*AttributesApi* | [**create_attribute**](docs/AttributesApi.md#create_attribute) | **POST** /contacts/attributes/{attributeCategory}/{attributeName} | Creates contact attribute
*AttributesApi* | [**delete_attribute**](docs/AttributesApi.md#delete_attribute) | **DELETE** /contacts/attributes/{attributeCategory}/{attributeName} | Deletes an attribute
*AttributesApi* | [**get_attributes**](docs/AttributesApi.md#get_attributes) | **GET** /contacts/attributes | Lists all attributes
*AttributesApi* | [**update_attribute**](docs/AttributesApi.md#update_attribute) | **PUT** /contacts/attributes/{attributeCategory}/{attributeName} | Updates contact attribute
*ContactsApi* | [**add_contact_to_list**](docs/ContactsApi.md#add_contact_to_list) | **POST** /contacts/lists/{listId}/contacts/add | Add existing contacts to a list
*ContactsApi* | [**create_attribute**](docs/ContactsApi.md#create_attribute) | **POST** /contacts/attributes/{attributeCategory}/{attributeName} | Creates contact attribute
*ContactsApi* | [**create_contact**](docs/ContactsApi.md#create_contact) | **POST** /contacts | Create a contact
*ContactsApi* | [**create_folder**](docs/ContactsApi.md#create_folder) | **POST** /contacts/folders | Create a folder
*ContactsApi* | [**create_list**](docs/ContactsApi.md#create_list) | **POST** /contacts/lists | Create a list
*ContactsApi* | [**delete_attribute**](docs/ContactsApi.md#delete_attribute) | **DELETE** /contacts/attributes/{attributeCategory}/{attributeName} | Deletes an attribute
*ContactsApi* | [**delete_contact**](docs/ContactsApi.md#delete_contact) | **DELETE** /contacts/{email} | Deletes a contact
*ContactsApi* | [**delete_folder**](docs/ContactsApi.md#delete_folder) | **DELETE** /contacts/folders/{folderId} | Delete a folder (and all its lists)
*ContactsApi* | [**delete_list**](docs/ContactsApi.md#delete_list) | **DELETE** /contacts/lists/{listId} | Delete a list
*ContactsApi* | [**get_attributes**](docs/ContactsApi.md#get_attributes) | **GET** /contacts/attributes | Lists all attributes
*ContactsApi* | [**get_contact_info**](docs/ContactsApi.md#get_contact_info) | **GET** /contacts/{email} | Retrieves contact informations
*ContactsApi* | [**get_contact_stats**](docs/ContactsApi.md#get_contact_stats) | **GET** /contacts/{email}/campaignStats | Get the campaigns statistics for a contact
*ContactsApi* | [**get_contacts**](docs/ContactsApi.md#get_contacts) | **GET** /contacts | Get all the contacts
*ContactsApi* | [**get_contacts_from_list**](docs/ContactsApi.md#get_contacts_from_list) | **GET** /contacts/lists/{listId}/contacts | Get the contacts in a list
*ContactsApi* | [**get_folder**](docs/ContactsApi.md#get_folder) | **GET** /contacts/folders/{folderId} | Returns folder details
*ContactsApi* | [**get_folder_lists**](docs/ContactsApi.md#get_folder_lists) | **GET** /contacts/folders/{folderId}/lists | Get the lists in a folder
*ContactsApi* | [**get_folders**](docs/ContactsApi.md#get_folders) | **GET** /contacts/folders | Get all the folders
*ContactsApi* | [**get_list**](docs/ContactsApi.md#get_list) | **GET** /contacts/lists/{listId} | Get the details of a list
*ContactsApi* | [**get_lists**](docs/ContactsApi.md#get_lists) | **GET** /contacts/lists | Get all the lists
*ContactsApi* | [**import_contacts**](docs/ContactsApi.md#import_contacts) | **POST** /contacts/import | Import contacts
*ContactsApi* | [**remove_contact_from_list**](docs/ContactsApi.md#remove_contact_from_list) | **POST** /contacts/lists/{listId}/contacts/remove | Remove existing contacts from a list
*ContactsApi* | [**request_contact_export**](docs/ContactsApi.md#request_contact_export) | **POST** /contacts/export | Export contacts
*ContactsApi* | [**update_attribute**](docs/ContactsApi.md#update_attribute) | **PUT** /contacts/attributes/{attributeCategory}/{attributeName} | Updates contact attribute
*ContactsApi* | [**update_contact**](docs/ContactsApi.md#update_contact) | **PUT** /contacts/{email} | Updates a contact
*ContactsApi* | [**update_folder**](docs/ContactsApi.md#update_folder) | **PUT** /contacts/folders/{folderId} | Update a contact folder
*ContactsApi* | [**update_list**](docs/ContactsApi.md#update_list) | **PUT** /contacts/lists/{listId} | Update a list
*EmailCampaignsApi* | [**create_email_campaign**](docs/EmailCampaignsApi.md#create_email_campaign) | **POST** /emailCampaigns | Create an email campaign
*EmailCampaignsApi* | [**delete_email_campaign**](docs/EmailCampaignsApi.md#delete_email_campaign) | **DELETE** /emailCampaigns/{campaignId} | Delete an email campaign
*EmailCampaignsApi* | [**email_export_recipients**](docs/EmailCampaignsApi.md#email_export_recipients) | **POST** /emailCampaigns/{campaignId}/exportRecipients | Export the recipients of a campaign
*EmailCampaignsApi* | [**get_email_campaign**](docs/EmailCampaignsApi.md#get_email_campaign) | **GET** /emailCampaigns/{campaignId} | Get campaign informations
*EmailCampaignsApi* | [**get_email_campaigns**](docs/EmailCampaignsApi.md#get_email_campaigns) | **GET** /emailCampaigns | Return all your created campaigns
*EmailCampaignsApi* | [**send_email_campaign_now**](docs/EmailCampaignsApi.md#send_email_campaign_now) | **POST** /emailCampaigns/{campaignId}/sendNow | Send an email campaign id of the campaign immediately
*EmailCampaignsApi* | [**send_report**](docs/EmailCampaignsApi.md#send_report) | **POST** /emailCampaigns/{campaignId}/sendReport | Send the report of a campaigns
*EmailCampaignsApi* | [**send_test_email**](docs/EmailCampaignsApi.md#send_test_email) | **POST** /emailCampaigns/{campaignId}/sendTest | Send an email campaign to your test list
*EmailCampaignsApi* | [**update_campaign_status**](docs/EmailCampaignsApi.md#update_campaign_status) | **PUT** /emailCampaigns/{campaignId}/status | Update a campaign status
*EmailCampaignsApi* | [**update_email_campaign**](docs/EmailCampaignsApi.md#update_email_campaign) | **PUT** /emailCampaigns/{campaignId} | Update a campaign
*FoldersApi* | [**create_folder**](docs/FoldersApi.md#create_folder) | **POST** /contacts/folders | Create a folder
*FoldersApi* | [**delete_folder**](docs/FoldersApi.md#delete_folder) | **DELETE** /contacts/folders/{folderId} | Delete a folder (and all its lists)
*FoldersApi* | [**get_folder**](docs/FoldersApi.md#get_folder) | **GET** /contacts/folders/{folderId} | Returns folder details
*FoldersApi* | [**get_folder_lists**](docs/FoldersApi.md#get_folder_lists) | **GET** /contacts/folders/{folderId}/lists | Get the lists in a folder
*FoldersApi* | [**get_folders**](docs/FoldersApi.md#get_folders) | **GET** /contacts/folders | Get all the folders
*FoldersApi* | [**update_folder**](docs/FoldersApi.md#update_folder) | **PUT** /contacts/folders/{folderId} | Update a contact folder
*ListsApi* | [**add_contact_to_list**](docs/ListsApi.md#add_contact_to_list) | **POST** /contacts/lists/{listId}/contacts/add | Add existing contacts to a list
*ListsApi* | [**create_list**](docs/ListsApi.md#create_list) | **POST** /contacts/lists | Create a list
*ListsApi* | [**delete_list**](docs/ListsApi.md#delete_list) | **DELETE** /contacts/lists/{listId} | Delete a list
*ListsApi* | [**get_contacts_from_list**](docs/ListsApi.md#get_contacts_from_list) | **GET** /contacts/lists/{listId}/contacts | Get the contacts in a list
*ListsApi* | [**get_folder_lists**](docs/ListsApi.md#get_folder_lists) | **GET** /contacts/folders/{folderId}/lists | Get the lists in a folder
*ListsApi* | [**get_list**](docs/ListsApi.md#get_list) | **GET** /contacts/lists/{listId} | Get the details of a list
*ListsApi* | [**get_lists**](docs/ListsApi.md#get_lists) | **GET** /contacts/lists | Get all the lists
*ListsApi* | [**remove_contact_from_list**](docs/ListsApi.md#remove_contact_from_list) | **POST** /contacts/lists/{listId}/contacts/remove | Remove existing contacts from a list
*ListsApi* | [**update_list**](docs/ListsApi.md#update_list) | **PUT** /contacts/lists/{listId} | Update a list
*ProcessApi* | [**get_process**](docs/ProcessApi.md#get_process) | **GET** /processes/{processId} | Return the informations for a process
*ProcessApi* | [**get_processes**](docs/ProcessApi.md#get_processes) | **GET** /processes | Return all the processes for your account
*ResellerApi* | [**add_credits**](docs/ResellerApi.md#add_credits) | **POST** /reseller/children/{childAuthKey}/credits/add | Add Email and/or SMS credits to a specific child account
*ResellerApi* | [**associate_ip_to_child**](docs/ResellerApi.md#associate_ip_to_child) | **POST** /reseller/children/{childAuthKey}/ips/associate | Associate a dedicated IP to the child
*ResellerApi* | [**create_child_domain**](docs/ResellerApi.md#create_child_domain) | **POST** /reseller/children/{childAuthKey}/domains | Creates a domain for a child account
*ResellerApi* | [**create_reseller_child**](docs/ResellerApi.md#create_reseller_child) | **POST** /reseller/children | Creates a reseller child
*ResellerApi* | [**delete_child_domain**](docs/ResellerApi.md#delete_child_domain) | **DELETE** /reseller/children/{childAuthKey}/domains/{domainName} | Deletes the sender domain of the reseller child based on the childAuthKey and domainName passed
*ResellerApi* | [**delete_reseller_child**](docs/ResellerApi.md#delete_reseller_child) | **DELETE** /reseller/children/{childAuthKey} | Deletes a single reseller child based on the childAuthKey supplied
*ResellerApi* | [**dissociate_ip_from_child**](docs/ResellerApi.md#dissociate_ip_from_child) | **POST** /reseller/children/{childAuthKey}/ips/dissociate | Dissociate a dedicated IP to the child
*ResellerApi* | [**get_child_domains**](docs/ResellerApi.md#get_child_domains) | **GET** /reseller/children/{childAuthKey}/domains | Gets all the sender domains of a specific child account
*ResellerApi* | [**get_child_info**](docs/ResellerApi.md#get_child_info) | **GET** /reseller/children/{childAuthKey} | Gets the info about a specific child account
*ResellerApi* | [**get_reseller_childs**](docs/ResellerApi.md#get_reseller_childs) | **GET** /reseller/children | Gets the list of all reseller&#39;s children accounts
*ResellerApi* | [**get_sso_token**](docs/ResellerApi.md#get_sso_token) | **GET** /reseller/children/{childAuthKey}/auth | Get session token to access Sendinblue (SSO)
*ResellerApi* | [**remove_credits**](docs/ResellerApi.md#remove_credits) | **POST** /reseller/children/{childAuthKey}/credits/remove | Remove Email and/or SMS credits from a specific child account
*ResellerApi* | [**update_child_account_status**](docs/ResellerApi.md#update_child_account_status) | **PUT** /reseller/children/{childAuthKey}/accountStatus | Updates infos of reseller&#39;s child account status based on the childAuthKey supplied
*ResellerApi* | [**update_child_domain**](docs/ResellerApi.md#update_child_domain) | **PUT** /reseller/children/{childAuthKey}/domains/{domainName} | Updates the sender domain of reseller&#39;s child based on the childAuthKey and domainName passed
*ResellerApi* | [**update_reseller_child**](docs/ResellerApi.md#update_reseller_child) | **PUT** /reseller/children/{childAuthKey} | Updates infos of reseller&#39;s child based on the childAuthKey supplied
*SMSCampaignsApi* | [**create_sms_campaign**](docs/SMSCampaignsApi.md#create_sms_campaign) | **POST** /smsCampaigns | Creates an SMS campaign
*SMSCampaignsApi* | [**delete_sms_campaign**](docs/SMSCampaignsApi.md#delete_sms_campaign) | **DELETE** /smsCampaigns/{campaignId} | Delete the SMS campaign
*SMSCampaignsApi* | [**get_sms_campaign**](docs/SMSCampaignsApi.md#get_sms_campaign) | **GET** /smsCampaigns/{campaignId} | Get an SMS campaign
*SMSCampaignsApi* | [**get_sms_campaigns**](docs/SMSCampaignsApi.md#get_sms_campaigns) | **GET** /smsCampaigns | Returns the informations for all your created SMS campaigns
*SMSCampaignsApi* | [**request_sms_recipient_export**](docs/SMSCampaignsApi.md#request_sms_recipient_export) | **POST** /smsCampaigns/{campaignId}/exportRecipients | Exports the recipients of the specified campaign.
*SMSCampaignsApi* | [**send_sms_campaign_now**](docs/SMSCampaignsApi.md#send_sms_campaign_now) | **POST** /smsCampaigns/{campaignId}/sendNow | Send your SMS campaign immediately
*SMSCampaignsApi* | [**send_sms_report**](docs/SMSCampaignsApi.md#send_sms_report) | **POST** /smsCampaigns/{campaignId}/sendReport | Send report of SMS campaigns
*SMSCampaignsApi* | [**send_test_sms**](docs/SMSCampaignsApi.md#send_test_sms) | **POST** /smsCampaigns/{campaignId}/sendTest | Send an SMS
*SMSCampaignsApi* | [**update_sms_campaign**](docs/SMSCampaignsApi.md#update_sms_campaign) | **PUT** /smsCampaigns/{campaignId} | Updates an SMS campaign
*SMSCampaignsApi* | [**update_sms_campaign_status**](docs/SMSCampaignsApi.md#update_sms_campaign_status) | **PUT** /smsCampaigns/{campaignId}/status | Update the campaign status
*SMTPApi* | [**create_smtp_template**](docs/SMTPApi.md#create_smtp_template) | **POST** /smtp/templates | Create a transactional email template
*SMTPApi* | [**delete_hardbounces**](docs/SMTPApi.md#delete_hardbounces) | **POST** /smtp/deleteHardbounces | Delete hardbounces
*SMTPApi* | [**delete_smtp_template**](docs/SMTPApi.md#delete_smtp_template) | **DELETE** /smtp/templates/{templateId} | Delete an inactive transactional email template
*SMTPApi* | [**get_aggregated_smtp_report**](docs/SMTPApi.md#get_aggregated_smtp_report) | **GET** /smtp/statistics/aggregatedReport | Get your transactional email activity aggregated over a period of time
*SMTPApi* | [**get_email_event_report**](docs/SMTPApi.md#get_email_event_report) | **GET** /smtp/statistics/events | Get all your transactional email activity (unaggregated events)
*SMTPApi* | [**get_smtp_report**](docs/SMTPApi.md#get_smtp_report) | **GET** /smtp/statistics/reports | Get your transactional email activity aggregated per day
*SMTPApi* | [**get_smtp_template**](docs/SMTPApi.md#get_smtp_template) | **GET** /smtp/templates/{templateId} | Returns the template informations
*SMTPApi* | [**get_smtp_templates**](docs/SMTPApi.md#get_smtp_templates) | **GET** /smtp/templates | Get the list of transactional email templates
*SMTPApi* | [**get_transac_email_content**](docs/SMTPApi.md#get_transac_email_content) | **GET** /smtp/emails/{uuid} | Get the personalized content of a sent transactional email
*SMTPApi* | [**get_transac_emails_list**](docs/SMTPApi.md#get_transac_emails_list) | **GET** /smtp/emails | Get the list of transactional emails on the basis of allowed filters
*SMTPApi* | [**send_template**](docs/SMTPApi.md#send_template) | **POST** /smtp/templates/{templateId}/send | Send a template
*SMTPApi* | [**send_test_template**](docs/SMTPApi.md#send_test_template) | **POST** /smtp/templates/{templateId}/sendTest | Send a template to your test list
*SMTPApi* | [**send_transac_email**](docs/SMTPApi.md#send_transac_email) | **POST** /smtp/email | Send a transactional email
*SMTPApi* | [**update_smtp_template**](docs/SMTPApi.md#update_smtp_template) | **PUT** /smtp/templates/{templateId} | Updates a transactional email templates
*SendersApi* | [**create_sender**](docs/SendersApi.md#create_sender) | **POST** /senders | Create a new sender
*SendersApi* | [**delete_sender**](docs/SendersApi.md#delete_sender) | **DELETE** /senders/{senderId} | Delete a sender
*SendersApi* | [**get_ips**](docs/SendersApi.md#get_ips) | **GET** /senders/ips | Return all the dedicated IPs for your account
*SendersApi* | [**get_ips_from_sender**](docs/SendersApi.md#get_ips_from_sender) | **GET** /senders/{senderId}/ips | Return all the dedicated IPs for a sender
*SendersApi* | [**get_senders**](docs/SendersApi.md#get_senders) | **GET** /senders | Get the list of all your senders
*SendersApi* | [**update_sender**](docs/SendersApi.md#update_sender) | **PUT** /senders/{senderId} | Update a sender
*TransactionalSMSApi* | [**get_sms_events**](docs/TransactionalSMSApi.md#get_sms_events) | **GET** /transactionalSMS/statistics/events | Get all the SMS activity (unaggregated events)
*TransactionalSMSApi* | [**get_transac_aggregated_sms_report**](docs/TransactionalSMSApi.md#get_transac_aggregated_sms_report) | **GET** /transactionalSMS/statistics/aggregatedReport | Get your SMS activity aggregated over a period of time
*TransactionalSMSApi* | [**get_transac_sms_report**](docs/TransactionalSMSApi.md#get_transac_sms_report) | **GET** /transactionalSMS/statistics/reports | Get your SMS activity aggregated per day
*TransactionalSMSApi* | [**send_transac_sms**](docs/TransactionalSMSApi.md#send_transac_sms) | **POST** /transactionalSMS/sms | Send the SMS campaign to the specified mobile number
*WebhooksApi* | [**create_webhook**](docs/WebhooksApi.md#create_webhook) | **POST** /webhooks | Create a webhook
*WebhooksApi* | [**delete_webhook**](docs/WebhooksApi.md#delete_webhook) | **DELETE** /webhooks/{webhookId} | Delete a webhook
*WebhooksApi* | [**get_webhook**](docs/WebhooksApi.md#get_webhook) | **GET** /webhooks/{webhookId} | Get a webhook details
*WebhooksApi* | [**get_webhooks**](docs/WebhooksApi.md#get_webhooks) | **GET** /webhooks | Get all webhooks
*WebhooksApi* | [**update_webhook**](docs/WebhooksApi.md#update_webhook) | **PUT** /webhooks/{webhookId} | Update a webhook


## Documentation For Models

 - [AddChildDomain](docs/AddChildDomain.md)
 - [AddContactToList](docs/AddContactToList.md)
 - [AddCredits](docs/AddCredits.md)
 - [CreateAttribute](docs/CreateAttribute.md)
 - [CreateAttributeEnumeration](docs/CreateAttributeEnumeration.md)
 - [CreateChild](docs/CreateChild.md)
 - [CreateContact](docs/CreateContact.md)
 - [CreateEmailCampaign](docs/CreateEmailCampaign.md)
 - [CreateEmailCampaignRecipients](docs/CreateEmailCampaignRecipients.md)
 - [CreateEmailCampaignSender](docs/CreateEmailCampaignSender.md)
 - [CreateList](docs/CreateList.md)
 - [CreateModel](docs/CreateModel.md)
 - [CreateReseller](docs/CreateReseller.md)
 - [CreateSender](docs/CreateSender.md)
 - [CreateSenderIps](docs/CreateSenderIps.md)
 - [CreateSenderModel](docs/CreateSenderModel.md)
 - [CreateSmsCampaign](docs/CreateSmsCampaign.md)
 - [CreateSmsCampaignRecipients](docs/CreateSmsCampaignRecipients.md)
 - [CreateSmtpEmail](docs/CreateSmtpEmail.md)
 - [CreateSmtpTemplate](docs/CreateSmtpTemplate.md)
 - [CreateSmtpTemplateSender](docs/CreateSmtpTemplateSender.md)
 - [CreateUpdateContactModel](docs/CreateUpdateContactModel.md)
 - [CreateUpdateFolder](docs/CreateUpdateFolder.md)
 - [CreateWebhook](docs/CreateWebhook.md)
 - [CreatedProcessId](docs/CreatedProcessId.md)
 - [DeleteHardbounces](docs/DeleteHardbounces.md)
 - [EmailExportRecipients](docs/EmailExportRecipients.md)
 - [ErrorModel](docs/ErrorModel.md)
 - [GetAccountMarketingAutomation](docs/GetAccountMarketingAutomation.md)
 - [GetAccountPlan](docs/GetAccountPlan.md)
 - [GetAccountRelay](docs/GetAccountRelay.md)
 - [GetAccountRelayData](docs/GetAccountRelayData.md)
 - [GetAggregatedReport](docs/GetAggregatedReport.md)
 - [GetAttributes](docs/GetAttributes.md)
 - [GetAttributesAttributes](docs/GetAttributesAttributes.md)
 - [GetAttributesEnumeration](docs/GetAttributesEnumeration.md)
 - [GetCampaignOverview](docs/GetCampaignOverview.md)
 - [GetCampaignRecipients](docs/GetCampaignRecipients.md)
 - [GetCampaignStats](docs/GetCampaignStats.md)
 - [GetChildDomain](docs/GetChildDomain.md)
 - [GetChildDomains](docs/GetChildDomains.md)
 - [GetChildInfoApiKeys](docs/GetChildInfoApiKeys.md)
 - [GetChildInfoApiKeysV2](docs/GetChildInfoApiKeysV2.md)
 - [GetChildInfoApiKeysV3](docs/GetChildInfoApiKeysV3.md)
 - [GetChildInfoCredits](docs/GetChildInfoCredits.md)
 - [GetChildInfoStatistics](docs/GetChildInfoStatistics.md)
 - [GetChildrenList](docs/GetChildrenList.md)
 - [GetClient](docs/GetClient.md)
 - [GetContactCampaignStats](docs/GetContactCampaignStats.md)
 - [GetContactCampaignStatsClicked](docs/GetContactCampaignStatsClicked.md)
 - [GetContactCampaignStatsLinks](docs/GetContactCampaignStatsLinks.md)
 - [GetContactCampaignStatsOpened](docs/GetContactCampaignStatsOpened.md)
 - [GetContactCampaignStatsTransacAttributes](docs/GetContactCampaignStatsTransacAttributes.md)
 - [GetContactCampaignStatsUnsubscriptions](docs/GetContactCampaignStatsUnsubscriptions.md)
 - [GetContactCampaignStatsUnsubscriptionsAdminUnsubscription](docs/GetContactCampaignStatsUnsubscriptionsAdminUnsubscription.md)
 - [GetContactCampaignStatsUnsubscriptionsUserUnsubscription](docs/GetContactCampaignStatsUnsubscriptionsUserUnsubscription.md)
 - [GetContactDetails](docs/GetContactDetails.md)
 - [GetContacts](docs/GetContacts.md)
 - [GetEmailCampaigns](docs/GetEmailCampaigns.md)
 - [GetEmailEventReport](docs/GetEmailEventReport.md)
 - [GetEmailEventReportEvents](docs/GetEmailEventReportEvents.md)
 - [GetExtendedCampaignOverviewSender](docs/GetExtendedCampaignOverviewSender.md)
 - [GetExtendedCampaignStats](docs/GetExtendedCampaignStats.md)
 - [GetExtendedClientAddress](docs/GetExtendedClientAddress.md)
 - [GetExtendedContactDetailsStatistics](docs/GetExtendedContactDetailsStatistics.md)
 - [GetExtendedContactDetailsStatisticsClicked](docs/GetExtendedContactDetailsStatisticsClicked.md)
 - [GetExtendedContactDetailsStatisticsLinks](docs/GetExtendedContactDetailsStatisticsLinks.md)
 - [GetExtendedContactDetailsStatisticsMessagesSent](docs/GetExtendedContactDetailsStatisticsMessagesSent.md)
 - [GetExtendedContactDetailsStatisticsOpened](docs/GetExtendedContactDetailsStatisticsOpened.md)
 - [GetExtendedContactDetailsStatisticsUnsubscriptions](docs/GetExtendedContactDetailsStatisticsUnsubscriptions.md)
 - [GetExtendedContactDetailsStatisticsUnsubscriptionsAdminUnsubscription](docs/GetExtendedContactDetailsStatisticsUnsubscriptionsAdminUnsubscription.md)
 - [GetExtendedContactDetailsStatisticsUnsubscriptionsUserUnsubscription](docs/GetExtendedContactDetailsStatisticsUnsubscriptionsUserUnsubscription.md)
 - [GetExtendedListCampaignStats](docs/GetExtendedListCampaignStats.md)
 - [GetFolder](docs/GetFolder.md)
 - [GetFolderLists](docs/GetFolderLists.md)
 - [GetFolders](docs/GetFolders.md)
 - [GetIp](docs/GetIp.md)
 - [GetIpFromSender](docs/GetIpFromSender.md)
 - [GetIps](docs/GetIps.md)
 - [GetIpsFromSender](docs/GetIpsFromSender.md)
 - [GetList](docs/GetList.md)
 - [GetLists](docs/GetLists.md)
 - [GetProcess](docs/GetProcess.md)
 - [GetProcesses](docs/GetProcesses.md)
 - [GetReports](docs/GetReports.md)
 - [GetReportsReports](docs/GetReportsReports.md)
 - [GetSendersList](docs/GetSendersList.md)
 - [GetSendersListIps](docs/GetSendersListIps.md)
 - [GetSendersListSenders](docs/GetSendersListSenders.md)
 - [GetSmsCampaignOverview](docs/GetSmsCampaignOverview.md)
 - [GetSmsCampaignStats](docs/GetSmsCampaignStats.md)
 - [GetSmsCampaigns](docs/GetSmsCampaigns.md)
 - [GetSmsEventReport](docs/GetSmsEventReport.md)
 - [GetSmsEventReportEvents](docs/GetSmsEventReportEvents.md)
 - [GetSmtpTemplateOverview](docs/GetSmtpTemplateOverview.md)
 - [GetSmtpTemplateOverviewSender](docs/GetSmtpTemplateOverviewSender.md)
 - [GetSmtpTemplates](docs/GetSmtpTemplates.md)
 - [GetSsoToken](docs/GetSsoToken.md)
 - [GetStatsByDomain](docs/GetStatsByDomain.md)
 - [GetTransacAggregatedSmsReport](docs/GetTransacAggregatedSmsReport.md)
 - [GetTransacEmailContent](docs/GetTransacEmailContent.md)
 - [GetTransacEmailContentEvents](docs/GetTransacEmailContentEvents.md)
 - [GetTransacEmailsList](docs/GetTransacEmailsList.md)
 - [GetTransacEmailsListTransactionalEmails](docs/GetTransacEmailsListTransactionalEmails.md)
 - [GetTransacSmsReport](docs/GetTransacSmsReport.md)
 - [GetTransacSmsReportReports](docs/GetTransacSmsReportReports.md)
 - [GetWebhook](docs/GetWebhook.md)
 - [GetWebhooks](docs/GetWebhooks.md)
 - [ManageIp](docs/ManageIp.md)
 - [PostContactInfo](docs/PostContactInfo.md)
 - [PostContactInfoContacts](docs/PostContactInfoContacts.md)
 - [PostSendFailed](docs/PostSendFailed.md)
 - [PostSendSmsTestFailed](docs/PostSendSmsTestFailed.md)
 - [RemainingCreditModel](docs/RemainingCreditModel.md)
 - [RemainingCreditModelChild](docs/RemainingCreditModelChild.md)
 - [RemainingCreditModelReseller](docs/RemainingCreditModelReseller.md)
 - [RemoveContactFromList](docs/RemoveContactFromList.md)
 - [RemoveCredits](docs/RemoveCredits.md)
 - [RequestContactExport](docs/RequestContactExport.md)
 - [RequestContactImport](docs/RequestContactImport.md)
 - [RequestContactImportNewList](docs/RequestContactImportNewList.md)
 - [RequestSmsRecipientExport](docs/RequestSmsRecipientExport.md)
 - [SendEmail](docs/SendEmail.md)
 - [SendEmailAttachment](docs/SendEmailAttachment.md)
 - [SendReport](docs/SendReport.md)
 - [SendReportEmail](docs/SendReportEmail.md)
 - [SendSms](docs/SendSms.md)
 - [SendSmtpEmail](docs/SendSmtpEmail.md)
 - [SendSmtpEmailAttachment](docs/SendSmtpEmailAttachment.md)
 - [SendSmtpEmailBcc](docs/SendSmtpEmailBcc.md)
 - [SendSmtpEmailCc](docs/SendSmtpEmailCc.md)
 - [SendSmtpEmailReplyTo](docs/SendSmtpEmailReplyTo.md)
 - [SendSmtpEmailSender](docs/SendSmtpEmailSender.md)
 - [SendSmtpEmailTo](docs/SendSmtpEmailTo.md)
 - [SendTemplateEmail](docs/SendTemplateEmail.md)
 - [SendTestEmail](docs/SendTestEmail.md)
 - [SendTestSms](docs/SendTestSms.md)
 - [SendTransacSms](docs/SendTransacSms.md)
 - [UpdateAttribute](docs/UpdateAttribute.md)
 - [UpdateAttributeEnumeration](docs/UpdateAttributeEnumeration.md)
 - [UpdateCampaignStatus](docs/UpdateCampaignStatus.md)
 - [UpdateChild](docs/UpdateChild.md)
 - [UpdateChildAccountStatus](docs/UpdateChildAccountStatus.md)
 - [UpdateChildDomain](docs/UpdateChildDomain.md)
 - [UpdateContact](docs/UpdateContact.md)
 - [UpdateEmailCampaign](docs/UpdateEmailCampaign.md)
 - [UpdateEmailCampaignRecipients](docs/UpdateEmailCampaignRecipients.md)
 - [UpdateEmailCampaignSender](docs/UpdateEmailCampaignSender.md)
 - [UpdateList](docs/UpdateList.md)
 - [UpdateSender](docs/UpdateSender.md)
 - [UpdateSmsCampaign](docs/UpdateSmsCampaign.md)
 - [UpdateSmtpTemplate](docs/UpdateSmtpTemplate.md)
 - [UpdateSmtpTemplateSender](docs/UpdateSmtpTemplateSender.md)
 - [UpdateWebhook](docs/UpdateWebhook.md)
 - [GetChildInfo](docs/GetChildInfo.md)
 - [GetExtendedCampaignOverview](docs/GetExtendedCampaignOverview.md)
 - [GetExtendedClient](docs/GetExtendedClient.md)
 - [GetExtendedContactDetails](docs/GetExtendedContactDetails.md)
 - [GetExtendedList](docs/GetExtendedList.md)
 - [GetSmsCampaign](docs/GetSmsCampaign.md)
 - [GetAccount](docs/GetAccount.md)
 - [GetEmailCampaign](docs/GetEmailCampaign.md)


## Documentation For Authorization


## api-key

- **Type**: API key
- **API key parameter name**: api-key
- **Location**: HTTP header

## partner-key

- **Type**: API key
- **API key parameter name**: partner-key
- **Location**: HTTP header

## Support and Feedback

Be sure to visit the SendinBlue official [documentation website](https://sendinblue.readme.io/docs ) for additional information about our API.

If you find a bug, please post the issue on [Github](https://github.com/sendinblue/APIv3-python-library/issues).

As always, if you need additional assistance, drop us a note [here](https://account.sendinblue.com/support).

## Author

contact@sendinblue.com

