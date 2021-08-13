---
description: 本主題說明如何確認感應器可以提供一組特定的資料欄位。
ms.assetid: 918ba4a3-d2ac-47ee-ba29-f7ddf67ffbc5
title: 檢查支援的感應器資料欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa75c474dc4cd38d34074872765abc77a7dae00d18e8cc37d74cde70b6f22a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890263"
---
# <a name="checking-for-supported-sensor-data-fields"></a>檢查支援的感應器資料欄位

本主題說明如何確認感應器可以提供一組特定的資料欄位。

在您取出感應器物件之後，您可以呼叫 [**ISensor：： GetSupportedDataFields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) 來判斷感應器是否可以提供您所需的資料。

下列程式碼範例會建立協助程式函式，以測試感應器是否可以提供這三個範例資料欄位。 函式會採用感應器的指標作為其輸入，並傳回布林值，其中 **TRUE** 表示感應器可以提供所需的所有資料欄位。


```C++
BOOL CheckForSupportedDataFields(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;
    DWORD cKeys = 0; // Key count.
    BOOL bRet = FALSE;

    IPortableDeviceKeyCollection* pKeys = NULL; // Output

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        hr = pSensor->GetSupportedDataFields(&pKeys);
    }

    if(SUCCEEDED(hr))
    {
        hr = pKeys->GetCount(&cKeys);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk;
        BOOL bHour, bMinute, bSecond = FALSE;

        for (DWORD i = 0; i < cKeys; i++)
        {
            hr = pKeys->GetAt(i, &pk);

            if(SUCCEEDED(hr))
            {
                // Test for the data fields.
                if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_HOUR))
                {
                    bHour = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_MINUTE))
                {
                    bMinute = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_SECOND))
                {
                    bSecond = TRUE;
                }
            }
        }

        // Compute the return value.
        // If all three properties were found,
        // bRet will resolve to TRUE.
        bRet = bHour && bMinute && bSecond;
    }

    SafeRelease(&pKeys);

    return bRet;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport)
</dt> </dl>

 

 
