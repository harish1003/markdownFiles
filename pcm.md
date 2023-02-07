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
*
     

