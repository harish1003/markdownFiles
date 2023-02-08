### Product control manager / Product catalogue Management 
* product control manager is a centralised product and service catalog that will help service providers to construct, manage and deploy a layered product with full techinical and commericial definiation of product.

#### System  Architecture
*pcm client GUI - workshop domain - cm db - integerator - oracle sid - product export utility*

* CM database holds the master copy of product.
* Integerator transfers data from the Postgress to oracle sid which are all entities in released or approved state.

###     Integration 
* pcm provides mechanism to integrate this data with the external system.(BSS/OSS)
 > Inbound Integration Support :
* provides mechanism for supporting design-time activities such as like loading data into product control manager from external system  and using external task system to update the exisisting product control manager data. The data managed by the workshop API is in the only workshop format.

> Outbound Integration Suport
* This integration meachanism are based on SID data. pcm sid data is characterized as data which has been approved for use by external production systems.

# Modelling overview
* pcm is used to model the products that are offered to customers.
* Each building block is created separately in PCM and then assembled into a product offering. components are building blocks for all technical products.
* CSD [commercial service description] is building block for technical products. It can be linked to one more products offerings.
* Product offerings are commericial offere being made in the market place.
* Pricing consists of two main entities :
    * Pricing Plans : Are used to define pricing terms and rules.
                     Allows the modeler to define pricing ==independent== of a product offering.
    * Product Pricing Entities : this is used to associate a pricing plan with the product pricing entity or CSD or bundeled csd/product offering.
* Product offering defination are created by including one or more CSD in offerings definition, and then associating commericial rules with offering definition.
 
                * commercial rules
                * Availability rules
                * Promotion rules
                * cross sell rules
                * General rules
# Attributes 
* PCM supports the creation and management of an attribute library.
* 
    the basic attribute definition includes INTEGER,DECIMAL,BOOLEAN,TEXT,TIME,DATE,PROCESS OR HYPERLINK
    * We can set parameters by reference data, and specifying the enumerated restriction list.by either typing-in each allowable value or by loading in a pre-defined list of allowable values from a Reference Table. 
    * we can set min, max and allowable values to the attribute also default values.
    * attribute presence we can set to mandatory/optional
    *  Facets – Facets provides a mechanism for the modeler to characterize attributes so that the output from the Order Negotiator can be filtered based on specific needs (for example, return only those attributes that have the Billing Affecting facet). 
### fulfillment Prompts
    * fulfillment prompt describes that information that need to be collected from an end user to fullfill or provision the component.
### Components
* A componenet is typically defined as being a low-level service or resourse that is a part of a product that a subscriber consumes or uses. It is a smallest granular building block in a product model.
> component category : A Component Category is the entity that Product Control Manager uses to group together Components that typically share common attributes. Component Categories are also groupings of related attribute definitions that enable use of Product Specification Templates for Product Specification Modeling
### Product Specification
    * It is the collection of components, and also it is a technical representation of a product.
    * -- Product Specification Template -- this will enable modelers to define product specification without acquiring detailed knowledge of components that are all available in PCM.
    * product specification template can be used to create product specification from only those components which are created under component category 
### Commercial service descriptions
    * CSD is the basic building block for constructing product offerings. it     defines the commericial view of an underlying technical product            specification.
    * Association of CSD to product specification is called the ==Technical link==
    * CSD's can be combined to form the CSD bundles. A CSD bundle becomes the single entity within PCM.
### Product Offering
    * It represents what is externally presented to the market for the market use.
    * It consists of CSD, price plans, various rules.
### Product Catalog 
    * A product catalog is an entity which is used represent a logical grouping of product offerings from any product family.
### Commericial Entities in PCM 
    * There are six pre-defined commericial entities 
                - Market Segment
                - Market Campaign
                - Credit Rating
                - Serving Area
                - Customer Type 
                - Sales Channel
## Pricing 
    * PCM uses the following building blocks to define the pricing for a product offering:
            - Pricing plans 
            - Contracts
            - Rate Plan Description 
            - Product Pricing Entities 
### Pricing plans
    * Pricing plan is used to define pricing ==terms== and rules. A pricing Plan is a collection of one or more Terms.
    > ex: In terms would be -> Calling Plan Charge, Text Message Fee.Each term has the ability to group one or more related sub terms within the term.
    for eaxmple if modeler wants to charge different prices for weekends, and weekdays then those two are ==SUBTERMS==
    * Each subterm can have multiple times-spans, time-span can be defined in units of months,days,weeks,yeraly. we can also specify the price overrides.
### Product Pricing Entity
    * product pricing entity allow modeler to associate pricing plans with         modelling entities and contains the other pricing details
            - Effective dates for pricing(start,end)
            - Default Pricing
            - Alternate Pricing plans for csd's
            - Pricing rukles


