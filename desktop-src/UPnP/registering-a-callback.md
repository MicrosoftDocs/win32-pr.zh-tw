---
title: 註冊回呼
description: 如果應用程式在狀態變數的值變更時，或它所代表的服務實例變得無法使用時需要通知，應用程式必須註冊回呼函數。
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3dca603e6226d3171aed920311bafcf6844ec9fab5c7aa05deafee7a13fd8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768528"
---
# <a name="registering-a-callback"></a>註冊回呼

如果應用程式在狀態變數的值變更時，或它所代表的服務實例變得無法使用時需要通知，應用程式必須註冊回呼函數。 若要註冊要叫用之服務物件的回呼函式，請使用 [**IUPnPService：： AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) 方法。 這個方法可以用來註冊一個以上的回呼。

開發人員不應取消非同步回呼內的非同步作業。

> [!Note]  
> 在 Visual Basic 中加入回呼，與 VBScript 中使用的方法不同。 Visual Basic 中無法使用 VBScript 中使用的 **GetRef** 函式。 因此，開發人員必須建立以回呼函式作為預設方法的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 物件。 請參閱[註冊 Visual Basic 中的回呼](registering-a-callback-in-visual-basic.md)。

 

## <a name="vbscript-example"></a>VBScript 範例

下列 VBScript 程式碼定義回呼函式 **serviceChangeCallback**，當狀態變數的值變更或服務實例變成無法使用時，就會叫用此函數。 函數有四個引數。

函數的第一個引數會指定叫用回呼的原因。 因為狀態變數已變更，或服務實例已變成無法使用，所以會叫用它。

第二個引數是叫用回呼的服務物件。 如果叫用狀態變數變更的回呼，則函式會傳遞兩個額外的引數：已變更的變數名稱，以及其新值。

在此範例中，回呼只會顯示訊息方塊，以顯示已變更變數的名稱和其新值，以及是否已針對狀態變數變更叫用回呼。 否則，它會顯示一則訊息，表示服務實例已無法使用。

程式碼片段的最後一個部分會顯示如何使用 [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) 方法來註冊回呼函式。 服務物件變數、 *appService* 和 *xportService* 會假設為已初始化，如 [取得服務物件](obtaining-service-objects.md)所示。


```VB
'State Change Callback Function
 
'Note:  In the sub declaration statement below, VARIABLE_UPDATE
'is one of two possible values for the callbackType argument; 
'the other is SERVICE_INSTANCE_DIED

Sub serviceChangeCallback(callbacktype, svcObj, varName, value)
    If (callbacktype = "VARIABLE_UPDATE") then
        Dim outString
        outString = "State Variable Changed:" & vbCrLf
        outString = outString & varName & " == " & value
    
        MsgBox(outString, "Service Callback")
    Else if (callbacktype = "SERVICE_INSTANCE_DIED") then
        MsgBox("Service instance is no longer available", 
               "Service Callback")
    End If
End Sub

' ...
    
'Add our state change callback to each service
appService.AddCallback GetRef("serviceChangeCallback")
xportService.AddCallback GetRef("serviceChangeCallback")
```



## <a name="c-example"></a>C + + 範例


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

class CUPnPServiceCallback : public IUPnPServiceCallback
{
public:
    CUPnPServiceCallback()
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
            if(IsEqualIID(iid, IID_IUnknown) || IsEqualIID(iid, IID_IUPnPServiceCallback))
            {
                *ppvObject = static_cast<IUPnPServiceCallback*>(this);
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
    
    STDMETHODIMP StateVariableChanged(IUPnPService *pus, LPCWSTR pcwszStateVarName, VARIANT varValue)
    {
        HRESULT    hr = S_OK;
        BSTR ServiceId;
        hr = pus->get_Id(&ServiceId);
        if (SUCCEEDED(hr))
        {
            VARIANT AlphaVariant;
            VariantInit(&AlphaVariant);
            hr = VariantChangeType(&AlphaVariant, &varValue, VARIANT_ALPHABOOL, VT_BSTR);
            if(SUCCEEDED(hr))
            {
                printf("StateVariableChanged called for the %S service"
                       " for %S state variable with the value=%S.\n",
                        ServiceId, pcwszStateVarName, V_BSTR(&AlphaVariant));
                VariantClear(&AlphaVariant);
            }
            SysFreeString(ServiceId);
        }
        return hr;
    };

    STDMETHODIMP ServiceInstanceDied(IUPnPService *pus)
    {
        HRESULT hr = S_OK;
        BSTR ServiceType;
        hr = pus->get_ServiceTypeIdentifier(&ServiceType);
        if(SUCCEEDED(hr))
        {
            printf("ServiceInstanceDied called for the %S service!\n", ServiceType);
            SysFreeString(ServiceType);
        }
        return hr;
    };
    
private:
    LONG m_lRefCount;
    
};

HRESULT AddCallbackToService(IUPnPService* pUPnPService)
{
    HRESULT hr = S_OK;

    IUnknown* pUPnPServiceCallback = new CUPnPServiceCallback;
    if(NULL != pUPnPServiceCallback)
    {
        pUPnPServiceCallback->AddRef();
        hr = pUPnPService->AddCallback(pUPnPServiceCallback);
        pUPnPServiceCallback->Release();
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
    return hr;
}
```



 

 