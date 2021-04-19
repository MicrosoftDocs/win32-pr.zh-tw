---
description: 處理來自裝置的事件
ms.assetid: 529a8b7a-08b4-47de-8ed3-28e8fff0ede2
title: 處理來自裝置的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74692b73e39aa83286604408f3c556f5fbeb3f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986619"
---
# <a name="handling-events-from-the-device"></a>處理來自裝置的事件

WPD 應用程式所完成的另一項作業，就是處理裝置所引發的事件。

事件處理作業是使用下表所述的介面來完成。



| 介面                                                                      | 描述                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                           | 讓應用程式註冊接收非同步回呼。 |
| [**IPortableDeviceEventCallback 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback) | 包含應用程式的事件處理常式。                        |



 

範例應用程式 DeviceEvents .cpp 模組中的 CPortableDeviceEventsCallback 類別會示範應用程式如何執行 [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)。 在這個類別中， [**OnEvent**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) 方法的執行會將任何事件的參數寫入至應用程式的主控台視窗。 除了 OnEvent 方法之外，此類別還會實 AddRef 和 Release，用來維護物件的參考計數。


```C++
class CPortableDeviceEventsCallback : public IPortableDeviceEventCallback
{
public:
    CPortableDeviceEventsCallback() : m_cRef(1)
    {
    }

    ~CPortableDeviceEventsCallback()
    {
    }

    HRESULT __stdcall QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceEventCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    ULONG __stdcall AddRef()
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    ULONG __stdcall Release()
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

    HRESULT __stdcall OnEvent(
        IPortableDeviceValues* pEventParameters)
    {
        HRESULT hr = S_OK;

        if (pEventParameters != NULL)
        {
            printf("***************************\n** Device event received **\n***************************\n");
            DisplayStringProperty(pEventParameters, WPD_EVENT_PARAMETER_PNP_DEVICE_ID, L"WPD_EVENT_PARAMETER_PNP_DEVICE_ID");
            DisplayGuidProperty(pEventParameters, WPD_EVENT_PARAMETER_EVENT_ID, L"WPD_EVENT_PARAMETER_EVENT_ID");
        }

        return hr;
    }

    ULONG m_cRef;
};
```



範例應用程式會在其 RegisterForEventNotifications helper 函數中具現化 CPortableDeviceEventsCallback 類別。 此函數會使用 new 運算子來建立回呼物件的實例。 然後，它會呼叫 [**IPortableDevice：： Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) 方法來註冊回呼並開始接收事件。


```C++
void RegisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT                        hr = S_OK;
    LPWSTR                         wszEventCookie = NULL;
    CPortableDeviceEventsCallback* pCallback = NULL;

    if (pDevice == NULL)
    {
        return;
    }

    // Check to see if we already have an event registration cookie.  If so,
    // then avoid registering again.
    // NOTE: An application can register for events as many times as they want.
    //       This sample only keeps a single registration cookie around for
    //       simplicity.
    if (g_strEventRegistrationCookie.GetLength() > 0)
    {
        printf("This application has already registered to receive device events.\n");
        return;
    }

    // Create an instance of the callback object.  This will be called when events
    // are received.
    if (hr == S_OK)
    {
        pCallback = new CPortableDeviceEventsCallback();
        if (pCallback == NULL)
        {
            hr = E_OUTOFMEMORY;
            printf("Failed to allocate memory for IPortableDeviceEventsCallback object, hr = 0x%lx\n",hr);
        }
    }

    // Call Advise to register the callback and receive events.
    if (hr == S_OK)
    {
        hr = pDevice->Advise(0, pCallback, NULL, &wszEventCookie);
        if (FAILED(hr))
        {
            printf("! Failed to register for device events, hr = 0x%lx\n",hr);
        }
    }

    // Save the event registration cookie if event registration was successful.
    if (hr == S_OK)
    {
        g_strEventRegistrationCookie = wszEventCookie;
    }

    // Free the event registration cookie, if one was returned.
    if (wszEventCookie != NULL)
    {
        CoTaskMemFree(wszEventCookie);
        wszEventCookie = NULL;
    }

    if (hr == S_OK)
    {
        printf("This application has registered for device event notifications and was returned the registration cookie '%ws'", g_strEventRegistrationCookie.GetString());
    }

    // If a failure occurs, remember to delete the allocated callback object, if one exists.
    if (pCallback != NULL)
    {
        pCallback->Release();
    }
```



一旦範例應用程式透過接收事件，它就會呼叫 UnregisterForEventNotifications helper 函數。 接著，此函式會呼叫 [**IPortableDevice：： Unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) 方法，將回呼從接收事件中取消註冊。


```C++
void UnregisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT hr = S_OK;

    if (pDevice == NULL)
    {
        return;
    }

    hr = pDevice->Unadvise(g_strEventRegistrationCookie);
    if (FAILED(hr))
    {
        printf("! Failed to unregister for device events using registration cookie '%ws', hr = 0x%lx\n",g_strEventRegistrationCookie.GetString(), hr);
    }

    if (hr == S_OK)
    {
        printf("This application used the registration cookie '%ws' to unregister from receiving device event notifications", g_strEventRegistrationCookie.GetString());
    }

    g_strEventRegistrationCookie = L"";
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceEventCallback 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



