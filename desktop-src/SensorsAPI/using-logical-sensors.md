---
description: 使用邏輯感應器
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: 使用邏輯感應器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0493cfe8ff3a489e926792f9a101eb5d9db6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112621"
---
# <a name="using-logical-sensors"></a><span data-ttu-id="1e181-103">使用邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="1e181-103">Using Logical Sensors</span></span>

<span data-ttu-id="1e181-104">若要具現化邏輯感應器的裝置節點，或重新連線到現有的邏輯感應器裝置節點，應用程式或服務必須呼叫 [**ILogicalSensorManager：： Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1e181-104">To instantiate a device node for a logical sensor, or to reconnect to an existing logical sensor device node, an application or service must call [**ILogicalSensorManager::Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span> <span data-ttu-id="1e181-105">此方法的 *pPropertyStore* 參數需要 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的指標，其中包含要連接之感應器驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e181-105">The *pPropertyStore* parameter for this method requires a pointer to an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface that contains the IDs for the sensor drivers to connect to.</span></span> <span data-ttu-id="1e181-106">這表示您必須先建立屬性存放區，並將此資料加入至存放區，然後再呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1e181-106">This means that you must create a property store and add this data to the store before calling this method.</span></span>

### <a name="connecting-to-the-logical-sensor"></a><span data-ttu-id="1e181-107">連接到邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="1e181-107">Connecting to the Logical Sensor</span></span>

<span data-ttu-id="1e181-108">若要連接到邏輯感應器，您必須至少提供硬體識別碼（如感應器驅動程式的 .inf 檔案中所定義），以及識別感應器的邏輯 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="1e181-108">To connect to a logical sensor, you must provide, at a minimum, a hardware ID, as defined in the sensor driver's .inf file, and a logical **GUID** that identifies the sensor.</span></span> <span data-ttu-id="1e181-109">當您選擇中斷感應器裝置節點的連線或卸載時，此平臺會使用此 **GUID** 來識別感應器。</span><span class="sxs-lookup"><span data-stu-id="1e181-109">The platform uses this **GUID** to identify the sensor when you choose to disconnect from, or uninstall, the sensor device node.</span></span>

<span data-ttu-id="1e181-110">下列程式碼範例會建立連接到指定之邏輯感應器的 helper 方法。</span><span class="sxs-lookup"><span data-stu-id="1e181-110">The following example code creates a helper method that connects to a specified logical sensor.</span></span> <span data-ttu-id="1e181-111">方法參數會接收感應器硬體識別碼和唯一 **GUID** 以識別感應器。</span><span class="sxs-lookup"><span data-stu-id="1e181-111">The method parameters receive the sensor hardware ID and a unique **GUID** to identify the sensor.</span></span>


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



### <a name="disconnecting-from-a-logical-sensor"></a><span data-ttu-id="1e181-112">從邏輯感應器中斷連接</span><span class="sxs-lookup"><span data-stu-id="1e181-112">Disconnecting from a Logical Sensor</span></span>

<span data-ttu-id="1e181-113">若要中斷與邏輯感應器的連線，您必須提供呼叫 [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))時所使用的相同邏輯識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e181-113">To disconnect from a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="1e181-114">下列範例程式碼會建立與邏輯感應器中斷連接的 helper 函數。</span><span class="sxs-lookup"><span data-stu-id="1e181-114">The following example code creates a helper function that disconnects from a logical sensor.</span></span>


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



### <a name="uninstalling-a-logical-sensor"></a><span data-ttu-id="1e181-115">卸載邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="1e181-115">Uninstalling a Logical Sensor</span></span>

<span data-ttu-id="1e181-116">若要卸載邏輯感應器，您必須提供呼叫 [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))時所使用的相同邏輯識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e181-116">To uninstall a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="1e181-117">下列範例程式碼會建立可卸載邏輯感應器的 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="1e181-117">The following example code creates a helper function that uninstalls a logical sensor.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1e181-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e181-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e181-119">關於邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="1e181-119">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> </dl>

 

 
