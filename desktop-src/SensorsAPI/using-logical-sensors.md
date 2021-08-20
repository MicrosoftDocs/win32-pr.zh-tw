---
description: 使用邏輯感應器
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: 使用邏輯感應器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0178c0116efd968e78dd4efec991816647ec2af0f0fa47fdc823ca865ca31b4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968357"
---
# <a name="using-logical-sensors"></a>使用邏輯感應器

若要具現化邏輯感應器的裝置節點，或重新連線到現有的邏輯感應器裝置節點，應用程式或服務必須呼叫 [**ILogicalSensorManager：：連線**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))。 此方法的 *pPropertyStore* 參數需要 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的指標，其中包含要連接之感應器驅動程式的識別碼。 這表示您必須先建立屬性存放區，並將此資料加入至存放區，然後再呼叫這個方法。

### <a name="connecting-to-the-logical-sensor"></a>連接到邏輯感應器

若要連接到邏輯感應器，您必須至少提供硬體識別碼（如感應器驅動程式的 .inf 檔案中所定義），以及識別感應器的邏輯 **GUID** 。 當您選擇中斷感應器裝置節點的連線或卸載時，此平臺會使用此 **GUID** 來識別感應器。

下列程式碼範例會建立連接到指定之邏輯感應器的 helper 方法。 方法參數會接收感應器硬體識別碼和唯一 **GUID** 以識別感應器。


```C++
HRESULT ConnectToLogicalSensor(PCWSTR* wszHardwareID, GUID guidLogicalID)
{
    HRESULT hr = S_OK;
    
    ILogicalSensorManager* pLSM = NULL;
    IPropertyStore* pStore = NULL;
    PROPVARIANT pv = {};

    // Create the property store.
    hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pStore));

    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    // Fill in the values.
    if(SUCCEEDED(hr))
    {
        hr = InitPropVariantFromStringVector(wszHardwareID, 1, &pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_HardwareIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_CompatibleIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        // Connect to the logical sensor.
        hr = pLSM->Connect(guidLogicalID, pStore);
    }

    SafeRelease(&pStore);
    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="disconnecting-from-a-logical-sensor"></a>從邏輯感應器中斷連接

若要中斷與邏輯感應器的連線，您必須提供呼叫 [**連線**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))時所使用的相同邏輯識別碼。

下列範例程式碼會建立與邏輯感應器中斷連接的 helper 函數。


```C++
HRESULT DisconnectFromLogicalSensor(GUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM = NULL;
 
    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    if(SUCCEEDED(hr))
    {
        hr = pLSM->Disconnect(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="uninstalling-a-logical-sensor"></a>卸載邏輯感應器

若要卸載邏輯感應器，您必須提供呼叫 [**連線**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))時所使用的相同邏輯識別碼。

下列範例程式碼會建立可卸載邏輯感應器的 helper 函式。


```C++
HRESULT UninstallLogicalSensor(REFGUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM;
 
    // Create the logical sensor manager.
    hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_PPV_ARGS(&pLSM));
 
    if(SUCCEEDED(hr))
    {
        hr = pLSM->Uninstall(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於邏輯感應器](about-logical-sensors.md)
</dt> </dl>

 

 
