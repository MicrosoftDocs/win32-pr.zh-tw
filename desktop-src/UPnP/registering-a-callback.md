---
title: 註冊回呼
description: 如果應用程式在狀態變數的值變更時，或它所代表的服務實例變得無法使用時需要通知，應用程式必須註冊回呼函數。
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9095ab4b5b2d43a12f7e806eabc24b174a0311
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682556"
---
# <a name="registering-a-callback"></a><span data-ttu-id="8196b-103">註冊回呼</span><span class="sxs-lookup"><span data-stu-id="8196b-103">Registering a Callback</span></span>

<span data-ttu-id="8196b-104">如果應用程式在狀態變數的值變更時，或它所代表的服務實例變得無法使用時需要通知，應用程式必須註冊回呼函數。</span><span class="sxs-lookup"><span data-stu-id="8196b-104">If the application requires notification when the value of a state variable changes or the service instance it represents becomes unavailable, the application must register a callback function.</span></span> <span data-ttu-id="8196b-105">若要註冊要叫用之服務物件的回呼函式，請使用 [**IUPnPService：： AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) 方法。</span><span class="sxs-lookup"><span data-stu-id="8196b-105">To register a callback function for the service object to invoke, use the [**IUPnPService::AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="8196b-106">這個方法可以用來註冊一個以上的回呼。</span><span class="sxs-lookup"><span data-stu-id="8196b-106">This method can be used to register more than one callback.</span></span>

<span data-ttu-id="8196b-107">開發人員不應取消非同步回呼內的非同步作業。</span><span class="sxs-lookup"><span data-stu-id="8196b-107">Developers should not cancel an asynchronous operation inside an asynchronous callback.</span></span>

> [!Note]  
> <span data-ttu-id="8196b-108">在 Visual Basic 中加入回呼，與 VBScript 中使用的方法不同。</span><span class="sxs-lookup"><span data-stu-id="8196b-108">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="8196b-109">Visual Basic 中無法使用 VBScript 中使用的 **GetRef** 函式。</span><span class="sxs-lookup"><span data-stu-id="8196b-109">The **GetRef** function used in the VBScript is not available in Visual Basic.</span></span> <span data-ttu-id="8196b-110">因此，開發人員必須建立以回呼函式作為預設方法的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 物件。</span><span class="sxs-lookup"><span data-stu-id="8196b-110">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="8196b-111">請參閱 [註冊 Visual Basic 中的回呼](registering-a-callback-in-visual-basic.md)。</span><span class="sxs-lookup"><span data-stu-id="8196b-111">See [Registering a Callback in Visual Basic](registering-a-callback-in-visual-basic.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="8196b-112">VBScript 範例</span><span class="sxs-lookup"><span data-stu-id="8196b-112">VBScript Example</span></span>

<span data-ttu-id="8196b-113">下列 VBScript 程式碼定義回呼函式 **serviceChangeCallback**，當狀態變數的值變更或服務實例變成無法使用時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="8196b-113">The following VBScript code defines the callback function **serviceChangeCallback**, to be invoked when the values of state variables change or when the service instance becomes unavailable.</span></span> <span data-ttu-id="8196b-114">函數有四個引數。</span><span class="sxs-lookup"><span data-stu-id="8196b-114">The function has four arguments.</span></span>

<span data-ttu-id="8196b-115">函數的第一個引數會指定叫用回呼的原因。</span><span class="sxs-lookup"><span data-stu-id="8196b-115">The first argument to the function specifies the reason the callback is invoked.</span></span> <span data-ttu-id="8196b-116">因為狀態變數已變更，或服務實例已變成無法使用，所以會叫用它。</span><span class="sxs-lookup"><span data-stu-id="8196b-116">It is invoked either because a state variable changed, or because the service instance has become unavailable.</span></span>

<span data-ttu-id="8196b-117">第二個引數是叫用回呼的服務物件。</span><span class="sxs-lookup"><span data-stu-id="8196b-117">The second argument is the Service object for which the callback is invoked.</span></span> <span data-ttu-id="8196b-118">如果叫用狀態變數變更的回呼，則函式會傳遞兩個額外的引數：已變更的變數名稱，以及其新值。</span><span class="sxs-lookup"><span data-stu-id="8196b-118">If the callback is invoked for a state variable change, then the function is passed two additional arguments: the name of the variable that changed, and its new value.</span></span>

<span data-ttu-id="8196b-119">在此範例中，回呼只會顯示訊息方塊，以顯示已變更變數的名稱和其新值，以及是否已針對狀態變數變更叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="8196b-119">In this example, the callback simply displays a message box that shows the name of the changed variable and its new value, and if the callback was invoked for a state variable change.</span></span> <span data-ttu-id="8196b-120">否則，它會顯示一則訊息，表示服務實例已無法使用。</span><span class="sxs-lookup"><span data-stu-id="8196b-120">Otherwise, it displays a message that indicates the service instance is no longer available.</span></span>

<span data-ttu-id="8196b-121">程式碼片段的最後一個部分會顯示如何使用 [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) 方法來註冊回呼函式。</span><span class="sxs-lookup"><span data-stu-id="8196b-121">The last part of the code fragment shows how to register the callback function using the [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="8196b-122">服務物件變數、 *appService* 和 *xportService* 會假設為已初始化，如 [取得服務物件](obtaining-service-objects.md)所示。</span><span class="sxs-lookup"><span data-stu-id="8196b-122">The service object variables, *appService* and *xportService* are assumed to have been initialized as shown in [Obtaining Service Objects](obtaining-service-objects.md).</span></span>


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



## <a name="c-example"></a><span data-ttu-id="8196b-123">C + + 範例</span><span class="sxs-lookup"><span data-stu-id="8196b-123">C++ Example</span></span>


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



 

 