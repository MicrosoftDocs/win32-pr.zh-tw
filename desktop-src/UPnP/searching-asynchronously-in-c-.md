---
title: 在 c + + 中以非同步方式搜尋
description: 您可以使用下列程式碼作為 c + + 應用程式的基礎，以非同步方式搜尋裝置。 程式碼會藉由建立繼承自它的類別，來實 IUPnPDeviceFinderCallback 介面。
ms.assetid: bb874e60-6a93-4d94-be67-ba03ba92eff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6751872cbddf402a74df4899cd6c99424c9d0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932429"
---
# <a name="searching-asynchronously-in-c"></a>在 c + + 中以非同步方式搜尋

您可以使用下列程式碼作為 c + + 應用程式的基礎，以非同步方式搜尋裝置。 程式碼會藉由建立繼承自它的類別，來實 [**IUPnPDeviceFinderCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback) 介面。

若要同時執行 [**IUPnPDeviceFinderCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback) 和 [**IUPnPDeviceFinderAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface)，類別必須繼承自兩個介面。 **IUPnPDeviceFinderAddCallbackWithInterface** 的執行是選擇性的，但如果您選擇執行，則您也必須執行 **IUPnPDeviceFinderCallback**。


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")
#pragma comment(lib, "user32.lib")

class CUPnPDeviceFinderCallback : public IUPnPDeviceFinderCallback
{
public:
    CUPnPDeviceFinderCallback()
    {
        m_lRefCount = 0;
    };
    
    STDMETHODIMP QueryInterface(REFIID iid, LPVOID* ppvObject)
    {
        HRESULT hr = S_OK;
        
        if(NULL == ppvObject)
        {
            hr = E_POINTER;
        }
        else
        {
            *ppvObject = NULL;
        }
        
        if(SUCCEEDED(hr))
        {
            if(IsEqualIID(iid, IID_IUnknown) || IsEqualIID(iid, IID_IUPnPDeviceFinderCallback))
            {
                *ppvObject = static_cast<IUPnPDeviceFinderCallback*>(this);
                AddRef();
            }
            else
            {
                hr = E_NOINTERFACE;
            }
        }
        
        return hr;
    };
    
    STDMETHODIMP_(ULONG) AddRef()
    {
        return ::InterlockedIncrement(&m_lRefCount);
    };
    
    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRefCount = ::InterlockedDecrement(&m_lRefCount);
        if(0 == lRefCount)
        {
            delete this;
        }
        
        return lRefCount;
    };
    
    STDMETHODIMP DeviceAdded(LONG lFindData, IUPnPDevice* pDevice)
    {
        HRESULT hr = S_OK;

        //You should save pDevice so that it is accessible outside the scope of this method.

        BSTR UniqueDeviceName;
        hr = pDevice->get_UniqueDeviceName(&UniqueDeviceName);
        if (SUCCEEDED(hr))
        {
            BSTR FriendlyName;
            hr = pDevice->get_FriendlyName(&FriendlyName);
            if (SUCCEEDED(hr))
            {
                printf("Device Added: udn: %S, name: %S\n", FriendlyName, UniqueDeviceName);
                ::SysFreeString(FriendlyName);
            }
            ::SysFreeString(UniqueDeviceName);
        }
        return hr;
        
    };
    
    STDMETHODIMP DeviceRemoved(LONG lFindData, BSTR bstrUDN)
    {
        printf("Device Removed: udn: %S", bstrUDN);
        return S_OK;
    };
    
    STDMETHODIMP SearchComplete(LONG lFindData)
    {
        return S_OK;
    };
    
    
    
private:
    LONG m_lRefCount;
    
};

HRESULT FindUPnPDevice(BSTR TypeURI)
{
    HRESULT hr = S_OK;
    
    IUPnPDeviceFinderCallback* pUPnPDeviceFinderCallback = new CUPnPDeviceFinderCallback();
    if(NULL != pUPnPDeviceFinderCallback)
    {
        pUPnPDeviceFinderCallback->AddRef();
        IUPnPDeviceFinder* pUPnPDeviceFinder;
        hr = CoCreateInstance(CLSID_UPnPDeviceFinder, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUPnPDeviceFinder, reinterpret_cast<void**>(&pUPnPDeviceFinder));
        if(SUCCEEDED(hr))
        {
            LONG lFindData;
            hr = pUPnPDeviceFinder->CreateAsyncFind(TypeURI, 0, pUPnPDeviceFinderCallback, &lFindData);
            if(SUCCEEDED(hr))
            {
                hr = pUPnPDeviceFinder->StartAsyncFind(lFindData);
                if(SUCCEEDED(hr))
                {
                    // STA threads must pump messages
                    MSG Message;
                    BOOL bGetMessage;
                    while(bGetMessage = GetMessage(&Message, NULL, 0, 0) && -1 != bGetMessage)
                    {
                        DispatchMessage(&Message);      
                    }
                }
                pUPnPDeviceFinder->CancelAsyncFind(lFindData);
            }
            pUPnPDeviceFinder->Release();
        }
        pUPnPDeviceFinderCallback->Release();
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
   
    return hr;
}
```



 

 




