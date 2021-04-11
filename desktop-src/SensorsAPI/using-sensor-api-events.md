---
description: 感應器 API 會透過回呼介面提供事件通知。
ms.assetid: 0c396d54-cb2e-4b07-999f-3f4001db2a02
title: 使用感應器 API 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54fcb14138c1b20470a2b716e5cce86235c3102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944614"
---
# <a name="using-sensor-api-events"></a><span data-ttu-id="37ff1-103">使用感應器 API 事件</span><span class="sxs-lookup"><span data-stu-id="37ff1-103">Using Sensor API Events</span></span>

<span data-ttu-id="37ff1-104">感應器 API 會透過回呼介面提供事件通知。</span><span class="sxs-lookup"><span data-stu-id="37ff1-104">The Sensor API provides event notifications through callback interfaces.</span></span>

<span data-ttu-id="37ff1-105">若要接收事件通知，您的程式必須執行必要的 COM 回呼介面。</span><span class="sxs-lookup"><span data-stu-id="37ff1-105">To receive event notfications, your program must implement the required COM callback interfaces.</span></span> <span data-ttu-id="37ff1-106">若要從感應器接收事件，您必須執行 [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)。</span><span class="sxs-lookup"><span data-stu-id="37ff1-106">To receive events from sensors, you must implement [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="37ff1-107">若要接收來自感應器管理員的事件，您必須執行 [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents)。</span><span class="sxs-lookup"><span data-stu-id="37ff1-107">To receive events from the sensor manager, you must implement [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span>

<span data-ttu-id="37ff1-108">下列程式碼範例會建立可執行 [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)的類別。</span><span class="sxs-lookup"><span data-stu-id="37ff1-108">The following example code creates a class that implements [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span>


```C++
class CMyEvents : public ISensorEvents
{
public:

    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        if (ppv == NULL)
        {
            return E_POINTER;
        }
        if (iid == __uuidof(IUnknown))
        {
            *ppv = static_cast<IUnknown*>(this);
        }
        else if (iid == __uuidof(ISensorEvents))
        {
            *ppv = static_cast<ISensorEvents*>(this);
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
        AddRef();
        return S_OK;
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef); 
    }

    STDMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    //
    // ISensorEvents methods.
    //

    STDMETHODIMP OnEvent(
            ISensor *pSensor,
            REFGUID eventID,
            IPortableDeviceValues *pEventData)
    {
        HRESULT hr = S_OK;

        // Handle custom events here.

        return hr;
    }

    STDMETHODIMP OnDataUpdated(
            ISensor *pSensor,
            ISensorDataReport *pNewData)
    {
        HRESULT hr = S_OK;

        if(NULL == pNewData ||
           NULL == pSensor)
        {
            return E_INVALIDARG;
        }

        ULONG ulHour = 0;
        ULONG ulMinute = 0;
        ULONG ulSecond = 0;

        PROPVARIANT var = {};

        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

        if(SUCCEEDED(hr))
        {
            if(var.vt == VT_UI4)
            {
                // Get the hour value.
                ulHour = var.ulVal;                
            }
        }

        PropVariantClear(&var);

        if(SUCCEEDED(hr))
        {
            hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);
        }

        if(SUCCEEDED(hr))
        {
            if(var.vt == VT_UI4)
            {
                // Get the hour value.
                ulMinute = var.ulVal;
            }
        }

        PropVariantClear(&var);

        if(SUCCEEDED(hr))
        {
            hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);
        }

        if(SUCCEEDED(hr))
        {
            if(var.vt == VT_UI4)
            {
                // Get the hour value.
                ulSecond = var.ulVal;
            }
        }

        PropVariantClear(&var);

        if(SUCCEEDED(hr))
        {
            // Print
            wprintf_s(L"Current local time is: \n");
            wprintf_s(L"%02d:%02d:%02d (asynchronous)\n", ulHour, ulMinute, ulSecond);
        }

        return hr;
    }

    STDMETHODIMP OnLeave(
            REFSENSOR_ID sensorID)
    {
        HRESULT hr = S_OK;

        // Peform any housekeeping tasks for the sensor that is leaving.
        // For example, if you have maintained a reference to the sensor,
        // release it now and set the pointer to NULL.

        return hr;
    }

    STDMETHODIMP OnStateChanged(
            ISensor* pSensor,
            SensorState state)
    {
        HRESULT hr = S_OK;

        if(NULL == pSensor)
        {
            return E_INVALIDARG;
        }


        if(state == SENSOR_STATE_READY)
        {
            wprintf_s(L"\nTime sensor is now ready.");
        }
        else if(state == SENSOR_STATE_ACCESS_DENIED)
        {
            wprintf_s(L"\nNo permission for the time sensor.\n");
            wprintf_s(L"Enable the sensor in the control panel.\n");
        }
  

        return hr;
    }

    private:
        long m_cRef;

};

```



<span data-ttu-id="37ff1-109">在實回檔介面之後，您可以為特定感應器提供回呼類別實例的指標，以開始從感應器接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="37ff1-109">After implementing the callback interface, you can provide a particular sensor with a pointer to an instance of your callback class to start receiving event notifications from the sensor.</span></span>

<span data-ttu-id="37ff1-110">下列程式碼範例會建立回呼類別的實例，然後從感應器要求事件 notifcations。</span><span class="sxs-lookup"><span data-stu-id="37ff1-110">The following example code creates an instance of the callback class, and then requests event notifcations from a sensor.</span></span>


```C++
CMyEvents* pEventClass = NULL;
ISensorEvents* pMyEvents = NULL;

if(SUCCEEDED(hr))
{
    // Create an instance of the event class.
    pEventClass = new(std::nothrow) CMyEvents();        
}

if(SUCCEEDED(hr))
{
    // Retrieve the pointer to the callback interface.
    hr = pEventClass->QueryInterface(IID_PPV_ARGS(&pMyEvents));
}

if(SUCCEEDED(hr))
{
    // Start receiving events.
    hr = pSensor->SetEventSink(pMyEvents);
} 

```



<span data-ttu-id="37ff1-111">您可以撰寫類似的程式碼，以接收來自感應器管理員的事件。</span><span class="sxs-lookup"><span data-stu-id="37ff1-111">You can write similar code to receive events from the sensor manager.</span></span>

<span data-ttu-id="37ff1-112">下列範例程式碼顯示如何停止接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="37ff1-112">The following example code shows how to stop receiving event notifications.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = pSensor->SetEventSink(NULL);
}
```



## <a name="requesting-a-report-interval"></a><span data-ttu-id="37ff1-113">要求報表間隔</span><span class="sxs-lookup"><span data-stu-id="37ff1-113">Requesting a Report Interval</span></span>

<span data-ttu-id="37ff1-114">您可以建議應用程式收到資料更新事件的頻率值。</span><span class="sxs-lookup"><span data-stu-id="37ff1-114">You can suggest a value for how frequently your applicaton receives data-updated events.</span></span> <span data-ttu-id="37ff1-115">不過，感應器不需要在任何特定間隔提供事件。</span><span class="sxs-lookup"><span data-stu-id="37ff1-115">However, sensors are not required to provide events at any particular interval.</span></span> <span data-ttu-id="37ff1-116">您應該注意，您的建議值可能不符合感應器用來引發事件的實際報告間隔。</span><span class="sxs-lookup"><span data-stu-id="37ff1-116">You should be aware that your suggested value might not match the actual report interval the sensor uses to raise events.</span></span> <span data-ttu-id="37ff1-117">若要知道實際的報告間隔，請取出 [感應器 \_ 屬性 \_ 目前報告間隔] 屬性的值，如 [抓取 \_ \_ [和設定感應器屬性](setting-and-retrieving-sensor-properties.md)] 中所述。</span><span class="sxs-lookup"><span data-stu-id="37ff1-117">To know the actual report interval, retrieve the value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property, as described in [Retrieving and Setting Sensor Properties](setting-and-retrieving-sensor-properties.md).</span></span>

<span data-ttu-id="37ff1-118">下列範例程式碼會建立協助程式函式，要求感應器 \_ 屬性 \_ 目前 \_ 報表 \_ 間隔屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="37ff1-118">The following example code creates a helper function that requests a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="37ff1-119">此函式會採用要設定屬性之感應器的指標，以及表示要設定之新報表間隔的 **ULONG** 值。</span><span class="sxs-lookup"><span data-stu-id="37ff1-119">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="37ff1-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="37ff1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37ff1-121">關於感應器 API 事件</span><span class="sxs-lookup"><span data-stu-id="37ff1-121">About Sensor API Events</span></span>](about-sensor-events.md)
</dt> </dl>

 

 



