# Swagger\Client\CatalogApi

All URIs are relative to *https://api.ingrammicro.com:443/sandbox/resellers/v5*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getV5CatalogProductsearch**](CatalogApi.md#getv5catalogproductsearch) | **GET** /catalog | Search product catalog
[**multiSKUPriceAndStock**](CatalogApi.md#multiskupriceandstock) | **POST** /catalog/priceandavailability | Find availability of upto 50 SKUs

# **getV5CatalogProductsearch**
> \Swagger\Client\Model\ProductSearchResponse getV5CatalogProductsearch($customer_number, $iso_country_code, $part_number)

Search product catalog

Search product catalog using Ingram part numbers, vendor/manufacturer part numbers, customer part numbers or UPC. Use this endpoint to find the ingrampartnumber using vendorpartnumber or UPC.  - PartNumber field is capable of searching Ingram part numbers, vendor/manufacturer part numbers, customer part numbers or UPC.  *NOTE: isoCountryCode and customerNumber is mandatory.*

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: application
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CatalogApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_number = "20-222222"; // string | Your unique Ingram Micro customer number
$iso_country_code = "US"; // string | 2 chars country code
$part_number = "1AQ821"; // string | Part Number can be ingram part number or vendor part number or customer part number or UPC

try {
    $result = $apiInstance->getV5CatalogProductsearch($customer_number, $iso_country_code, $part_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CatalogApi->getV5CatalogProductsearch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_number** | **string**| Your unique Ingram Micro customer number | [default to 20-222222]
 **iso_country_code** | **string**| 2 chars country code | [default to US]
 **part_number** | **string**| Part Number can be ingram part number or vendor part number or customer part number or UPC | [default to 1AQ821]

### Return type

[**\Swagger\Client\Model\ProductSearchResponse**](../Model/ProductSearchResponse.md)

### Authorization

[application](../../README.md#application)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **multiSKUPriceAndStock**
> \Swagger\Client\Model\PriceAndAvailabilityResponse multiSKUPriceAndStock($body)

Find availability of upto 50 SKUs

Please use this end-point to find the price and availability of up to 50 SKUs while placing an order. This endpoint helps to confirm the details just prior to placing a real-time call.  This endpoint is not for refreshing the full catalog with availability and pricing information. We are applying rate-limits on this endpoint and continuous cyclical calls will start erroring out. Customers that perform this activity may lose access to the endpoint.  For the full catalog refresh, we can provide a Price and Inventory file in flat file format, which can be obtained through FTP download. Please contact your sales rep for details.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: application
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CatalogApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PriceAndAvailabilityRequest(); // \Swagger\Client\Model\PriceAndAvailabilityRequest | 

try {
    $result = $apiInstance->multiSKUPriceAndStock($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CatalogApi->multiSKUPriceAndStock: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PriceAndAvailabilityRequest**](../Model/PriceAndAvailabilityRequest.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\PriceAndAvailabilityResponse**](../Model/PriceAndAvailabilityResponse.md)

### Authorization

[application](../../README.md#application)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

