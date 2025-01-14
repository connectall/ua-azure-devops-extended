# ua-azure-devops-extended

The ConnectALL Azure DevOps Extended Universal Adapter is developed as an extension to the universal adapter capability of ConnectALL. This adapter will allow the user to extend ConnectALL to include special scenarios for Azure DevOps. Current capabilities and limitations will be defined below.

Please refer to the [ConnectALL Tech Docs](https://techdocs.broadcom.com/us/en/ca-enterprise-software/valueops/connectall/3-6/adapters/universal-adapter.html) for more information.

If you are an existing SaaS customer, please contact Broadcom Support to enable the adapter in your environment. If you are using ConnectALL On-Premise, you may download and install this adapter in your environment. If you are not yet a customer, [please reach out to learn more](https://enterprise-software.broadcom.com/contact-us).

# Setup

## Supported Entities

This Universal Adapter currently supports the following entities:
* PickLists

*Note: This Universal Adapter is provided as-is. It is tested and validated using the entities and configurations as defined. Any additional customizations are not supported and should be made at your own discretion.*

## Connection Details

* **Connection Name:** *Name of Application*
* **Application Type:** Azure DevOps Extended
* **URL:** https://dev.azure.com/{organization} (replace with your organization name)
* **User Name:** Leave Blank
* **Password:** Personal Access Token
* **Application Category:** *Pick from dropdown list*
* **Time Zone:** Not Required
* **Select Group:** *Set if neccessary*
* **Auth Option:** Header
* **Authentication Type:** Basic
* **API Key:** Leave Blank
* **API Value:** Leave Blank

## Flow Filters

Flow filters are not supported and are not necessary for the current update-only functionality

## Example Automation

Aggregate Clarity Projects into a Logic Flow Adapter, then update a pre-existing picklist in Azure DevOps with the aggregated list of Projects.

# Known Limitations

Azure DevOps cannot retroactively add a picklist to a custom field. For this reason, automatic creation of a list is not supported or advised. (You won't be able to add the list to a custom field after creating it from the API.)

Best practice is to create your Azure DevOps custom field and populate it with placeholder values prior to creating your automation in ConnectALL. You will be able to see and select your list on the Entity Mapping tab.

# Supporting Documentation

Third Party API Documentation: [Link to API Documentation](https://learn.microsoft.com/en-us/rest/api/azure/devops/processes/lists/list?view=azure-devops-rest-7.1)
