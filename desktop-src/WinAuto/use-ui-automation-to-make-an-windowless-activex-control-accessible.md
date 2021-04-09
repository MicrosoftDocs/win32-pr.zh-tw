---
title: 如何使用消費者介面自動化使無視窗的 ActiveX 控制項可供存取
description: 說明如何使用 Microsoft 消費者介面自動化 \ 32;API，以確保在) 用戶端應用程式上，輔助技術 (可以存取無視窗的 Microsoft ActiveX 控制項。
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- 無視窗的 ActiveX 控制項，協助工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ada1d26463b0654c1808f6e4fd43f571687d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682637"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="0af83-104">如何使用消費者介面自動化使無視窗的 ActiveX 控制項可供存取</span><span class="sxs-lookup"><span data-stu-id="0af83-104">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>

<span data-ttu-id="0af83-105">說明如何使用 Microsoft 消費者介面自動化 API，以確保可在) 用戶端應用程式 (輔助技術時，可存取無視窗的 Microsoft ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="0af83-105">Describes how to use the Microsoft UI Automation API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0af83-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="0af83-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0af83-107">技術</span><span class="sxs-lookup"><span data-stu-id="0af83-107">Technologies</span></span>

-   [<span data-ttu-id="0af83-108">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="0af83-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="0af83-109">使用者介面自動化</span><span class="sxs-lookup"><span data-stu-id="0af83-109">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="0af83-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="0af83-110">Prerequisites</span></span>

-   <span data-ttu-id="0af83-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="0af83-111">C/C++</span></span>
-   <span data-ttu-id="0af83-112">Microsoft Win32 和元件物件模型 (COM) 程式設計</span><span class="sxs-lookup"><span data-stu-id="0af83-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="0af83-113">無視窗的 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="0af83-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="0af83-114">消費者介面自動化提供者</span><span class="sxs-lookup"><span data-stu-id="0af83-114">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="0af83-115">指示</span><span class="sxs-lookup"><span data-stu-id="0af83-115">Instructions</span></span>

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a><span data-ttu-id="0af83-116">步驟1：執行消費者介面自動化提供者介面。</span><span class="sxs-lookup"><span data-stu-id="0af83-116">Step 1: Implement the UI Automation provider interfaces.</span></span>

<span data-ttu-id="0af83-117">若要讓您的應用程式可供存取，您必須為無視窗的 ActiveX 控制項（包括 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)、 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)、 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)和 [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents)）執行消費者介面自動化提供者介面。</span><span class="sxs-lookup"><span data-stu-id="0af83-117">To make your application accessible, you must implement the UI Automation provider interfaces for your windowless ActiveX control, including [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), and [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span></span> <span data-ttu-id="0af83-118">您應該執行這些介面，就像是針對以視窗為基礎的控制項一樣，除了下列步驟中所述。</span><span class="sxs-lookup"><span data-stu-id="0af83-118">You should implement these interfaces just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="0af83-119">如需有關執行 UIA 提供者介面的詳細資訊，請參閱 [消費者介面自動化提供者程式設計人員手冊](uiauto-providerportal.md)。</span><span class="sxs-lookup"><span data-stu-id="0af83-119">For more information about implementing UIA provider interfaces, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="0af83-120">步驟2：執行 IServiceProvider 介面。</span><span class="sxs-lookup"><span data-stu-id="0af83-120">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="0af83-121">當用戶端需要無視窗控制項的協助工具資訊時，控制項容器會呼叫您控制項的 **IServiceProvider：： QueryService** 方法，以抓取控制項的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0af83-121">When a client needs accessibility information about your windowless control, the control container calls your control's **IServiceProvider::QueryService** method to retrieve the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface pointer for your control.</span></span>

<span data-ttu-id="0af83-122">下列範例顯示如何執行 **QueryService** 方法。</span><span class="sxs-lookup"><span data-stu-id="0af83-122">The following example shows how to implement the **QueryService** method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a><span data-ttu-id="0af83-123">步驟3：執行 IRawElementProviderFragment：：流覽方法。</span><span class="sxs-lookup"><span data-stu-id="0af83-123">Step 3: Implement the IRawElementProviderFragment::Navigate method.</span></span>

<span data-ttu-id="0af83-124">當您的無視窗控制項的 [**IRawElementProviderFragment：：導覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) 方法被呼叫，以流覽至無視窗控制項根提供者的父系或同級時，您的 **流覽** 方法應該會委派給控制項容器的 [**IRawElementProviderWindowlessSite：： GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) 方法。</span><span class="sxs-lookup"><span data-stu-id="0af83-124">When your windowless control’s [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method is called to navigate to the parent or a sibling of the windowless control's root provider, your **Navigate** method should delegate to the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method of the control container.</span></span>

<span data-ttu-id="0af83-125">下列範例示範如何執行 [**流覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) 方法。</span><span class="sxs-lookup"><span data-stu-id="0af83-125">The following example shows how to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a><span data-ttu-id="0af83-126">步驟4：執行 IRawElementProviderFragment：： GetRuntimeId 方法。</span><span class="sxs-lookup"><span data-stu-id="0af83-126">Step 4: Implement the IRawElementProviderFragment::GetRuntimeId method.</span></span>

<span data-ttu-id="0af83-127">當您的無視窗控制項收到其 [**IRawElementProviderFragment：： GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) 方法的呼叫時，控制項必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="0af83-127">When your windowless control receives a call to its [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) method, the control must do the following:</span></span>

1.  <span data-ttu-id="0af83-128">藉由呼叫控制網站的 [**IRawElementProviderWindowlessSite：： GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) 方法，來取得執行時間識別碼首碼。</span><span class="sxs-lookup"><span data-stu-id="0af83-128">Retrieve a runtime ID prefix by calling the control site's [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>
2.  <span data-ttu-id="0af83-129">將整數附加到執行時間識別碼前置詞，以建立控制項的唯一執行時間識別碼。</span><span class="sxs-lookup"><span data-stu-id="0af83-129">Create a unique runtime ID for the control by appending an integer to the runtime ID prefix.</span></span>
3.  <span data-ttu-id="0af83-130">將執行時間識別碼傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="0af83-130">Return the runtime ID to the caller.</span></span>

<span data-ttu-id="0af83-131">下列範例顯示如何執行 [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) 方法。</span><span class="sxs-lookup"><span data-stu-id="0af83-131">The following example shows how to implement the [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a><span data-ttu-id="0af83-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="0af83-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0af83-133">使用 MSAA 讓無視窗的 ActiveX 控制項可供存取</span><span class="sxs-lookup"><span data-stu-id="0af83-133">Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="0af83-134">無視窗的 ActiveX 控制項協助工具</span><span class="sxs-lookup"><span data-stu-id="0af83-134">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 