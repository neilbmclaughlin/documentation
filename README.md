# NeXt Warning System

## Vision

> We will deliver a warning service that will save lives and protect livelihoods; by providing accurate and relevant information to users who need it, when they need it, in ways they want it – so they can take the right action.

## Delivery strategy

* XWS will be designed to be hazard agnostic
* XWS will be designed to be organisation agnostic
* XWS will be designed so that it can be deployed independently by other parties
* XWS will be designed to allow for real-time deployment without downtime
* XWS will be designed to allow for configuration via a Admin UI for some key elements
* XWS will be designed to scale automatically to adapt to increased usage
* Any code created will be shared openly on GitHub
* XWS will use and contribute to open standards, common components and patterns
* Code will be documented to provide clear guidance on how to use it

## Alpha development areas <a name="alpha"></a>

| Name            | Priority              | Status  |   Description  |
| -------------   | -------------         | ---     | ---            |
| [xws-core-engine](https://github.com/NeXt-Warning-System/documentation/tree/master/xws-core-engine) | 1        | Planning    | Creating the link between the Message to the TargetArea(s) to the Location to the Contact to calculate who should receive the message |
| [xws-contact-web](https://github.com/NeXt-Warning-System/documentation/tree/master/xws-contact-web) | 2        | In dev      | The webpage used by Users to register, maintain and cancel their Contact from the service |
| [xws-message-web](https://github.com/NeXt-Warning-System/documentation/tree/master/xws-message-web) | 3        | In dev      | The internal interface for selecting the Message, TargetArea, InfoAdvice and InfoDetail |
| [xws-edw-service](https://github.com/NeXt-Warning-System/documentation/tree/master/xws-edw-service) | TBC      | Planning    | Providing a link between the core XWS application and the contacts provided by the telephony providers under our opt-in warning service Extended Direct Warnings (EDW) | 


### Other development areas

| Name            | Priority              | Status  |   Description  |
| -------------   | -------------         | ---     | ---            |
| [xws-contact-api](https://github.com/NeXt-Warning-System/documentation/tree/master/xws-contact-api) | TBC      | Not started | The API that is used in the xws-contact-web page. It allows Contact(s) to be linked with Location(s) an controls what optional messages are associated with each location |
| [xws-message-api](https://github.com/NeXt-Warning-System/documentation/tree/master/xws-message-api) | TBC      | Not started | The API that triggers the sending of a message. This can include information collated during the xws-message-web input |


## Data

There are certain data standards and sources that we should be using in XWS. These are listed below.

### Standards

| Name                                                                                                                                       | Source          | Notes  | 
| -------------                                                                                                                              |------------     |---------- |
| [Language](https://www.gov.uk/government/publications/open-standards-for-government/language-tags)                                         | GDS             |  |
| [Date-times and time-stamps](https://www.gov.uk/government/publications/open-standards-for-government/date-times-and-time-stamps-standard) | GDS             |  |
| Exchange of location point                                                                                                                 | GDS             | https://www.gov.uk/government/publications/open-standards-for-government/exchange-of-location-point |
| Encoding characters                         | GDS             | https://www.gov.uk/government/publications/open-standards-for-government/cross-platform-character-encoding-profile |
| Country codes                               | GDS             | https://www.gov.uk/government/publications/open-standards-for-government/country-codes |
| Local authorities in England                | GDS             | https://www.registers.service.gov.uk/registers/local-authority-eng |
| Local authorities in Scotland               | GDS             | https://www.registers.service.gov.uk/registers/local-authority-sct |
| Principal local authorities in Wales        | GDS             | https://www.registers.service.gov.uk/registers/principal-local-authority |
| Local authority type                        | GDS             | https://www.registers.service.gov.uk/registers/local-authority-type |
| Government org names                        | GDS             | https://www.registers.service.gov.uk/registers/government-organisation |
| Environment Agency Addressing Standard      | EA              | https://defra.sharepoint.com/sites/def-contentcloud/ |
| Environment Agency Public Facing Area Names | EA              | https://defra.sharepoint.com/sites/def-contentcloud/ |
| Environment Agency Flood Cause              | EA              | https://defra.sharepoint.com/sites/def-contentcloud/ |
| Environment Agency Flood Source             | EA              | https://defra.sharepoint.com/sites/def-contentcloud/ |


### Sources

| Name           | Source                 | Notes  |
| -------------  | ------------           | ------   |
| Location       | [OS Open Names](https://www.ordnancesurvey.co.uk/business-government/products/open-map-names) | Remove Scotland and Wales, filter to populatedPlace |
| Addresses      | [OS AddressBase Premium](https://www.ordnancesurvey.co.uk/business-government/products/addressbase-premium) | Remove Scotland and Wales |
