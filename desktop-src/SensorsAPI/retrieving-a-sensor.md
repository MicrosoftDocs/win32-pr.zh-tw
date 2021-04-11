---
description: 若要取出感應器物件，請使用 ISensorManager 介面。 您可以將此介面視為感應器 API 的根介面。 若要使用 ISensorManager，您必須先呼叫 COM CoCreateInstance 方法。
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: 取出感應器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cda6ea04d1a0580c38aef5a0b9c4186b908300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943318"
---
# <a name="retrieving-a-sensor-object"></a><span data-ttu-id="b0fb7-105">取出感應器物件</span><span class="sxs-lookup"><span data-stu-id="b0fb7-105">Retrieving a Sensor Object</span></span>

<span data-ttu-id="b0fb7-106">若要取出感應器物件，請使用 [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-106">To retrieve a sensor object, you use the [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) interface.</span></span> <span data-ttu-id="b0fb7-107">您可以將此介面視為感應器 API 的根介面。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-107">You can think of this interface as the root interface for the Sensor API.</span></span> <span data-ttu-id="b0fb7-108">若要使用 **ISensorManager**，您必須先呼叫 COM **CoCreateInstance** 方法。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-108">To use **ISensorManager**, you must first call the COM **CoCreateInstance** method.</span></span>

<span data-ttu-id="b0fb7-109">下列程式碼範例會建立感應器管理員的實例。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-109">The following example code creates an instance of the sensor manager.</span></span>


```C++
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
```



<span data-ttu-id="b0fb7-110">成功抓取 [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)的指標之後，您就可以依類別、類型或識別碼取得感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-110">After successfully retrieving a pointer to [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), you can retrieve sensors by category, type, or ID.</span></span> <span data-ttu-id="b0fb7-111">如果您依類型或類別來取得感應器，則會收到 [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) 介面的指標，其中包含屬於所要求之類別或類型的所有可用感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-111">If you retrieve sensors by type or category, you receive a pointer to an [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) interface that contains all the available sensors that belong to the requested category or type.</span></span> <span data-ttu-id="b0fb7-112">如果您依識別碼取得感應器，則會收到 [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) 介面的指標，代表您所要求的唯一感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-112">If you retrieve a sensor by its ID, you receive a pointer to an [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface that represents the unique sensor you requested.</span></span>

<span data-ttu-id="b0fb7-113">下列範例程式碼會抓取屬於名為「範例 \_ 感應器 \_ 類別 \_ 日期時間」類別的感應器集合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-113">The following example code retrieves a collection of sensors that belong to the category named SAMPLE\_SENSOR\_CATEGORY\_DATE\_TIME.</span></span> <span data-ttu-id="b0fb7-114">然後，程式碼會依索引來抓取集合中的第一個感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-114">The code then retrieves the first sensor in the collection by its index.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByCategory(SAMPLE_SENSOR_CATEGORY_DATE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested category.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



<span data-ttu-id="b0fb7-115">請注意，您可以使用 [感應器類別] 來取出所有可用的感應器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-115">Note that you can retrieve all of the available sensors by using SENSOR\_CATEGORY\_ALL.</span></span>

<span data-ttu-id="b0fb7-116">以類似的方式，您可以取得特定類型的感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-116">In a similar way, you can retrieve sensors of a particular type.</span></span>

<span data-ttu-id="b0fb7-117">下列範例程式碼會抓取型別為範例 \_ 感應器類型時間的感應器 \_ 集合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-117">The following example code retrieves a collection of sensors of the type named SAMPLE\_SENSOR\_TYPE\_TIME.</span></span> <span data-ttu-id="b0fb7-118">然後，程式碼會依索引來抓取集合中的第一個感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-118">The code then retrieves the first sensor in the collection by its index.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested type.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



<span data-ttu-id="b0fb7-119">若要依識別碼取出感應器，您必須知道感應器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-119">To retrieve a sensor by its ID, you must know the unique ID for the sensor.</span></span> <span data-ttu-id="b0fb7-120">感應器通常會在第一次連線時產生此識別碼，讓您識別相同製作和模型的多個感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-120">Sensors usually generate this ID when first connected to enable you to identify multiple sensors of the same make and model.</span></span> <span data-ttu-id="b0fb7-121">這表示您可能不會事先知道感應器識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-121">This means that you probably will not know the sensor ID in advance.</span></span> <span data-ttu-id="b0fb7-122">但是，如果您已儲存先前取出的特定感應器識別碼複本，例如藉由呼叫 [**ISensor：： GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid)，您可能會想要再次取出相同的感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-122">However, if you have stored a copy of a particular sensor ID that you previously retrieved, for example by calling [**ISensor::GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), you may want to retrieve the same sensor again.</span></span>

<span data-ttu-id="b0fb7-123">下列範例程式碼示範如何使用其識別碼來取出感應器。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-123">The following example code shows how to retrieve a sensor by using its ID.</span></span>


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



<span data-ttu-id="b0fb7-124">您也可以透過接收感應器管理員的事件，在感應器變成可用時加以取出。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-124">You can also retrieve sensors when they become available by receiving an event from the sensor manager.</span></span> <span data-ttu-id="b0fb7-125">如需詳細資訊，請參閱 [**ISensorManager：： SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)。</span><span class="sxs-lookup"><span data-stu-id="b0fb7-125">For more information, see [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0fb7-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0fb7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0fb7-127">**ISensorManagerEvents::OnSensorEnter**</span><span class="sxs-lookup"><span data-stu-id="b0fb7-127">**ISensorManagerEvents::OnSensorEnter**</span></span>](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
