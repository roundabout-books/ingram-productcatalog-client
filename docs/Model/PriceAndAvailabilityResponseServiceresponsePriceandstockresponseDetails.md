# PriceAndAvailabilityResponseServiceresponsePriceandstockresponseDetails

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**itemstatus** | **string** | SUCCESS or FAILED | [optional] 
**statusmessage** | **string** | Description of itemstatus | [optional] 
**ingrampartnumber** | **string** | Ingram Micro part number | [optional] 
**vendorpartnumber** | **string** | Manufacturer/Vendor part number | [optional] 
**globalskuid** | **string** |  | [optional] 
**customerprice** | **float** | Customer specific price for the product, excluding taxes | [optional] 
**partdescription1** | **string** | Product description part 1 | [optional] 
**partdescription2** | **string** | Product description part 2 | [optional] 
**vendornumber** | **string** |  | [optional] 
**vendorname** | **string** | Name of the vendor | [optional] 
**cpucode** | **string** |  | [optional] 
**class** | **string** | Ingram Micro assigned product classification -  A-Stocked product in all IM warehouses, B-Limited stock in IM warehouses, C-Stocked in fewer wareshouses, D-Ingram discontinued, E-Planned to be phased out as per the vendor, F-Carried for specific customer as per the contract, N-New SKU, O-Discontinued to be liquidated, S-Order for specialized demand, V-Discontinued by vendor, X-Direct Ship products from vendor | [optional] 
**skustatus** | **string** | Identifies if the SKU has been discontinued. | [optional] 
**mediacpu** | **string** |  | [optional] 
**categorysubcategory** | **string** |  | [optional] 
**retailprice** | **float** |  | [optional] 
**newmedia** | **string** |  | [optional] 
**enduserrequired** | **string** | Y - End user required N - Not required End user | [optional] 
**backorderflag** | **string** | Y- Allow Backorder Flag N- Not allowed | [optional] 
**skuauthorized** | **string** |  | [optional] 
**extendedvendorpartnumber** | **string** |  | [optional] 
**warehousedetails** | [**\Swagger\Client\Model\WarehouseListType[]**](WarehouseListType.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

