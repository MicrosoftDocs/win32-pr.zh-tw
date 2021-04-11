---
description: 以非同步方式叫用服務方法
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: 以非同步方式叫用服務方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d312cc76cf8cb737136629c1e2c8135d1b7bd1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193700"
---
# <a name="invoking-service-methods-asynchronously"></a>以非同步方式叫用服務方法

WpdServiceApiSample 應用程式包含的程式碼會示範應用程式如何以非同步方式叫用服務方法。 此範例會使用下列介面。



|                                                                                         |                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 介面                                                                               | 描述                                                                                                                                                             |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | 用來取出 **IPortableDeviceServiceMethods** 介面，以便在指定的服務上叫用方法。                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | 用來叫用服務方法。                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                                  | 用來保存外寄方法參數和傳入方法的結果。 如果方法不需要任何參數或傳回任何結果，這可以是 **Null** 。 |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | 當方法完成時，由應用程式所執行以接收方法的結果。                                                                               |



 

當使用者在命令列選擇選項 "10" 時，應用程式會叫用在 ServiceMethods .cpp 模組中找到的 **InvokeMethodsAsync** 方法。 請注意，在叫用方法之前，範例應用程式會在連線的裝置上開啟連絡人服務。

服務方法會封裝每個服務定義和實行的功能。 它們對每種服務類型都是唯一的，並以 GUID 表示。 例如，連絡人服務會定義 **BeginSync** 方法，讓應用程式呼叫以準備裝置來同步處理連絡人物件，並使用 **EndSync** 方法來通知裝置同步處理已完成。 應用程式會藉由呼叫 [**IPortableDeviceServiceMethods：： Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)來執行可攜式裝置服務方法。

服務方法不應與 WPD 命令混淆。 WPD 命令是標準 WPD 設備磁碟機介面 (DDI) 的一部分，而且是 WPD 應用程式與驅動程式之間的通訊機制。 命令是預先定義的，依類別目錄分組 (例如， **WPD \_ CATEGORY \_ COMMON**) ，並且以 **PROPERTYKEY** 結構表示。 應用程式會藉由呼叫 [**IPortableDeviceService：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)，將命令傳送至設備磁碟機。 如需詳細資訊，請參閱命令主題。

**InvokeMethodsAsync** 方法會叫用 [**IPortableDeviceService：：方法**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities)來取出 [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。 使用這個介面時，它會叫用 **InvokeMethodAsync** helper 函數兩次;針對 **BeginSync** 方法，一次用於 **EndSync** 方法。 在此範例中， **InvokeMethodAsync** 會在呼叫 [**IPortableDeviceServiceMethodCallback：： OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) 時無限期等候全域事件發出信號。

下列程式碼會使用 **InvokeMethodsAsync** 方法。


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



**InvokeMethodAsync** helper 函式會針對它所叫用的每個方法，執行下列動作：

-   建立監視的全域事件控制碼，以判斷方法是否完成。
-   建立 **CMethodCallback** 物件，該物件會提供做為 [**IPortableDeviceServiceMethods： InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync)的引數。
-   呼叫 **IPortableDeviceServiceMethods：： InvokeAsync** 方法以叫用指定的方法。
-   監視全域事件控制碼是否完成。
-   執行清除。

**CMethodCallback** 類別會示範應用程式如何執行 [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)。 此類別中的 **OnComplete** 執行會通知事件，告知應用程式服務方法已完成。 除了 **OnComplete** 方法之外，此類別還會執行 **AddRef**、 **QueryInterface** 和 **Release**，用來維護物件的參考計數和它所執行的介面。


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
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
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
