# OptimaClientApi\AtrybutyTowaruApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pobierzAtrybut**](AtrybutyTowaruApi.md#pobierzatrybut) | **GET** /atrybuty-towaru/towary/{TwrId}/atrybut-towaru/{AttrKod} | Pobieranie atrybutów
[**ustawAtrybut**](AtrybutyTowaruApi.md#ustawatrybut) | **PUT** /atrybuty-towaru/towary/{TwrId}/atrybut/{AttrKod} | Ustawianie atrybutu towaru.
[**ustawAtrybuty**](AtrybutyTowaruApi.md#ustawatrybuty) | **POST** /atrybuty-towaru | Ustawianie atrybutów towaru masowo.
[**wyczyscAtrybutTowaru**](AtrybutyTowaruApi.md#wyczyscatrybuttowaru) | **DELETE** /atrybuty-towaru/{AttrKod} | Usuwanie atrybutów z towarów.
[**zmienWszystkimProduktomWartoscAtrybutu**](AtrybutyTowaruApi.md#zmienwszystkimproduktomwartoscatrybutu) | **PUT** /atrybuty-towaru/wartosc/{AttrKod} | Zmienia wartosc atrybutu we wszystkich produktach

# **pobierzAtrybut**
> \OptimaClientApi\Model\AtrybutTowaruItem pobierzAtrybut($twr_id, $attr_kod)

Pobieranie atrybutów

Pobiera atrybut

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OptimaClientApi\\AtrybutyTowaruApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$twr_id = 56; // int | Id Towaru dla którego pobieramy atrybut
$attr_kod = "attr_kod_example"; // string | Kod Atrybutu

try {
    $result = $apiInstance->pobierzAtrybut($twr_id, $attr_kod);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AtrybutyTowaruApi->pobierzAtrybut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **twr_id** | **int**| Id Towaru dla którego pobieramy atrybut |
 **attr_kod** | **string**| Kod Atrybutu |

### Return type

[**\OptimaClientApi\Model\AtrybutTowaruItem**](../Model/AtrybutTowaruItem.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **ustawAtrybut**
> ustawAtrybut($body, $twr_id, $attr_kod)

Ustawianie atrybutu towaru.

Ustawia atrybut

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OptimaClientApi\\AtrybutyTowaruApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \OptimaClientApi\Model\AtrybutTowaruWartoscItem(); // \OptimaClientApi\Model\AtrybutTowaruWartoscItem | Wartość którą ustawiamy atrybutowi
$twr_id = 56; // int | Id Towaru dla którego pobieramy atrybut
$attr_kod = "attr_kod_example"; // string | Kod Atrybutu

try {
    $apiInstance->ustawAtrybut($body, $twr_id, $attr_kod);
} catch (Exception $e) {
    echo 'Exception when calling AtrybutyTowaruApi->ustawAtrybut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\OptimaClientApi\Model\AtrybutTowaruWartoscItem**](../Model/AtrybutTowaruWartoscItem.md)| Wartość którą ustawiamy atrybutowi |
 **twr_id** | **int**| Id Towaru dla którego pobieramy atrybut |
 **attr_kod** | **string**| Kod Atrybutu |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **ustawAtrybuty**
> ustawAtrybuty($body)

Ustawianie atrybutów towaru masowo.

Ustawia atrybuty

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OptimaClientApi\\AtrybutyTowaruApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = array(new \OptimaClientApi\Model\AtrybutTowaruItem()); // \OptimaClientApi\Model\AtrybutTowaruItem[] | Wartość którą ustawiamy atrybutowi

try {
    $apiInstance->ustawAtrybuty($body);
} catch (Exception $e) {
    echo 'Exception when calling AtrybutyTowaruApi->ustawAtrybuty: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\OptimaClientApi\Model\AtrybutTowaruItem[]**](../Model/AtrybutTowaruItem.md)| Wartość którą ustawiamy atrybutowi |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **wyczyscAtrybutTowaru**
> wyczyscAtrybutTowaru($attr_kod)

Usuwanie atrybutów z towarów.

Usuwa atrybut o podanym kodzie ze wszystkich produktów

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OptimaClientApi\\AtrybutyTowaruApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$attr_kod = "attr_kod_example"; // string | Kod Atrybutu

try {
    $apiInstance->wyczyscAtrybutTowaru($attr_kod);
} catch (Exception $e) {
    echo 'Exception when calling AtrybutyTowaruApi->wyczyscAtrybutTowaru: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attr_kod** | **string**| Kod Atrybutu |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **zmienWszystkimProduktomWartoscAtrybutu**
> zmienWszystkimProduktomWartoscAtrybutu($body, $attr_kod)

Zmienia wartosc atrybutu we wszystkich produktach

Ustawia

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OptimaClientApi\\AtrybutyTowaruApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \OptimaClientApi\Model\AtrybutTowaruWartoscItem(); // \OptimaClientApi\Model\AtrybutTowaruWartoscItem | Wartość którą ustawiamy atrybutowi
$attr_kod = "attr_kod_example"; // string | Kod Atrybutu

try {
    $apiInstance->zmienWszystkimProduktomWartoscAtrybutu($body, $attr_kod);
} catch (Exception $e) {
    echo 'Exception when calling AtrybutyTowaruApi->zmienWszystkimProduktomWartoscAtrybutu: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\OptimaClientApi\Model\AtrybutTowaruWartoscItem**](../Model/AtrybutTowaruWartoscItem.md)| Wartość którą ustawiamy atrybutowi |
 **attr_kod** | **string**| Kod Atrybutu |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

