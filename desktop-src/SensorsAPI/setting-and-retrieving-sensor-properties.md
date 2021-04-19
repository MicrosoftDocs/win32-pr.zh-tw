---
description: 本主題說明如何取出和設定感應器屬性的值。 ISensor 介面提供了設定和取出感應器屬性值的方法。
ms.assetid: 7d10e5b4-bae7-4564-84eb-75c6a2eeef8f
title: 正在抓取和設定感應器屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f64bf0e253f47ae2d8cd1f4945f3b87aa3406b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979915"
---
# <a name="retrieving-and-setting-sensor-properties"></a>正在抓取和設定感應器屬性

本主題說明如何取出和設定感應器屬性的值。 [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor)介面提供了設定和取出感應器屬性值的方法。

## <a name="retrieving-sensor-properties"></a>正在抓取感應器屬性

您可以先從感應器取得某些屬性值，然後再讓使用者啟用。 製造商名稱或感應器型號等資訊可協助您決定程式是否可以使用感應器。

您可以選擇取出單一屬性值，或同時抓取屬性值的集合。 若要取出單一值，請呼叫 [**ISensor：： GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty)。 若要取出值的集合，請呼叫 [**ISensor：： GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties)。 您可以透過第一個參數將 **Null** 傳遞至 **ISensor：： GetProperties**，以抓取感應器的所有屬性。

下列範例程式碼會建立可列印單一屬性值的 helper 函式。 函式會接收要從中取出值的感應器指標，以及包含要列印之屬性的屬性索引鍵。 函數可以列印數位、字串和 **GUID** s 的值，但不能列印其他更複雜的類型。


```C++
HRESULT PrintSensorProperty(ISensor* pSensor, REFPROPERTYKEY pk)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    PROPVARIANT pv = {};

    hr = pSensor->GetProperty(pk, &pv);

    if(SUCCEEDED(hr))
    {
        if(pv.vt == VT_UI4)  // Number
        {
            wprintf_s(L"\nSensor integer value: %u\n", pv.ulVal);
        }
        else if(pv.vt == VT_LPWSTR)  // String
        {
            wprintf_s(L"\nSensor string value: %s\n", pv.pwszVal);
        }
        else if(pv.vt == VT_CLSID)  // GUID
        {
            int iRet = 0;

            // Convert the GUID to a string.
            OLECHAR wszGuid[39] = {}; // Buffer for string.
            iRet = ::StringFromGUID2(*(pv.puuid), wszGuid, 39);

            assert(39 == iRet); // Count of characters returned for GUID.

            wprintf_s(L"\nSensor GUID value: %s\n", wszGuid);
        }
        else  // Interface or vector
        {
            wprintf_s(L"\nSensor property is a compound type. Unable to print value.");
        }
    }

    PropVariantClear(&pv);

    return hr;    
}
```



下列程式碼範例會建立函式，以抓取和列印屬性的集合。 要列印的屬性集是由名為 SensorProperties 的陣列所定義。


```C++
HRESULT PrintSensorProperties(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    DWORD cVals = 0; // Count of returned properties.
    IPortableDeviceKeyCollection* pKeys = NULL; // Input
    IPortableDeviceValues* pValues = NULL;  // Output

    // Properties to print.
    const PROPERTYKEY SensorProperties[] =
    {
        SENSOR_PROPERTY_MANUFACTURER,
        SENSOR_PROPERTY_SERIAL_NUMBER,
        SENSOR_PROPERTY_DESCRIPTION,
        SENSOR_PROPERTY_FRIENDLY_NAME
    };

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER,                                 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        // Add the properties to the key collection.
        for (DWORD dwIndex = 0; dwIndex < ARRAYSIZE(SensorProperties); dwIndex++)
        {
            hr = pKeys->Add(SensorProperties[dwIndex]);

            if(FAILED(hr))
            {
                // Unexpected.
                // This example returns the failed HRESULT.
                // You may choose to ignore failures, here.
                break;
            }
        }
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the properties from the sensor.
        hr = pSensor->GetProperties(pKeys, &pValues);
    }

    if(SUCCEEDED(hr))
    {
        // Get the number of values returned.        
        hr = pValues->GetCount(&cVals);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk; // Keys
        PROPVARIANT pv = {}; // Values

        // Loop through the values;
        for (DWORD i = 0; i < cVals; i++)
        {
            // Get the value at the current index.
            hr = pValues->GetAt(i, &pk, &pv);

            if(SUCCEEDED(hr))
            { 
                // Find and print the property.
                if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_MANUFACTURER))
                {
                    wprintf_s(L"\nManufacturer: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_SERIAL_NUMBER))
                {
                    wprintf_s(L"Serial number: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_FRIENDLY_NAME))
                {
                    wprintf_s(L"Friendly name: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_DESCRIPTION))
                {
                    wprintf_s(L"Description: %s\n", pv.pwszVal);
                }
            }

            PropVariantClear(&pv);
        } // end i loop        
    }

    SafeRelease(&pKeys);
    SafeRelease(&pValues);

    return hr;
};
```



## <a name="setting-sensor-properties"></a>設定感應器屬性

在您可以設定感應器的屬性值之前，使用者必須先啟用感應器。 此外，並非所有的感應器屬性都可以設定。

若要設定屬性的一或多個值，請呼叫 [**ISensor：： SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties)。 您可以使用 [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) 指標來提供這個方法，其中包含要設定之屬性的集合及其相關聯的值。 方法會傳回對應的 [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) 介面，其中可能包含無法設定之屬性的錯誤碼。

下列程式碼範例會建立協助程式函式，以針對 [感應器 \_ 屬性 \_ 目前 \_ 報表間隔] 屬性 \_ 設定新值。 此函式會採用要設定屬性之感應器的指標，以及表示要設定之新報表間隔的 **ULONG** 值。  (請注意，設定這個特定屬性的值並不保證感應器會接受指定的值。 如需有關此屬性如何運作的詳細資訊，請參閱 [**感應器屬性**](sensor-properties.md) 。 ) 


```C++
HRESULT SetCurrentReportInterval(ISensor* pSensor, ULONG ulNewInterval)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    IPortableDeviceValues* pPropsToSet = NULL; // Input
    IPortableDeviceValues* pPropsReturn = NULL; // Output

    // Create the input object.
    hr = CoCreateInstance(__uuidof(PortableDeviceValues),
                            NULL,
                            CLSCTX_INPROC_SERVER,                           
                            IID_PPV_ARGS(&pPropsToSet));

    if(SUCCEEDED(hr))
    {
        // Add the current report interval property.
        hr = pPropsToSet->SetUnsignedIntegerValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, ulNewInterval);
    }

    if(SUCCEEDED(hr))
    {
        // Only setting a single property, here.
        hr = pSensor->SetProperties(pPropsToSet, &pPropsReturn);
    }

    // Test for failure.
    if(hr == S_FALSE)
    {
        HRESULT hrError = S_OK;
      
        // Check results for failure.
        hr = pPropsReturn->GetErrorValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, &hrError);

        if(SUCCEEDED(hr))
        {
            // Print an error message.
            wprintf_s(L"\nSetting current report interval failed with error 0x%X\n", hrError);

            // Return the error code.
            hr = hrError;
        }
    }
    else if(hr == E_ACCESSDENIED)
    {
        // No permission. Take appropriate action.
    }

    SafeRelease(&pPropsToSet);
    SafeRelease(&pPropsReturn);
   
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**感應器屬性**](sensor-properties.md)
</dt> </dl>

 

 
