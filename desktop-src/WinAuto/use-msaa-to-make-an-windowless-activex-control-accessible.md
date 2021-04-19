---
title: 使用 MSAA 讓無視窗的 ActiveX 控制項可供存取
description: 說明如何使用 Microsoft Active Accessibility \ 32;API，以確保在) 用戶端應用程式上，輔助技術 (可以存取無視窗的 Microsoft ActiveX 控制項。
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX 控制項，協助工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968106"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="276f4-104">使用 MSAA 讓無視窗的 ActiveX 控制項可供存取</span><span class="sxs-lookup"><span data-stu-id="276f4-104">Use MSAA to make a windowless ActiveX control accessible</span></span>

<span data-ttu-id="276f4-105">說明如何使用 Microsoft Active Accessibility API，以確保可在) 用戶端應用程式 (輔助技術時，可存取無視窗的 Microsoft ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="276f4-105">Describes how to use the Microsoft Active Accessibility API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="276f4-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="276f4-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="276f4-107">技術</span><span class="sxs-lookup"><span data-stu-id="276f4-107">Technologies</span></span>

-   [<span data-ttu-id="276f4-108">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="276f4-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="276f4-109">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="276f4-109">Microsoft Active Accessibility</span></span>](microsoft-active-accessibility.md)

### <a name="prerequisites"></a><span data-ttu-id="276f4-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="276f4-110">Prerequisites</span></span>

-   <span data-ttu-id="276f4-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="276f4-111">C/C++</span></span>
-   <span data-ttu-id="276f4-112">Microsoft Win32 和元件物件模型 (COM) 程式設計</span><span class="sxs-lookup"><span data-stu-id="276f4-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="276f4-113">無視窗的 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="276f4-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="276f4-114">Microsoft Active Accessibility 伺服器</span><span class="sxs-lookup"><span data-stu-id="276f4-114">Microsoft Active Accessibility servers</span></span>

## <a name="instructions"></a><span data-ttu-id="276f4-115">指示</span><span class="sxs-lookup"><span data-stu-id="276f4-115">Instructions</span></span>

### <a name="step-1-implement-the-iaccessible-interface"></a><span data-ttu-id="276f4-116">步驟1：執行 IAccessible 介面。</span><span class="sxs-lookup"><span data-stu-id="276f4-116">Step 1: Implement the IAccessible interface.</span></span>

<span data-ttu-id="276f4-117">若要使無視窗的 ActiveX 控制項可供存取，您必須執行 Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，就像您對以視窗為基礎的控制項一樣，除了下列步驟中所述。</span><span class="sxs-lookup"><span data-stu-id="276f4-117">To make your windowless ActiveX control accessible, you must implement the Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="276f4-118">如需有關執行 **IAccessible** 的詳細資訊，請參閱 [Active Accessibility 伺服器的開發人員指南](developer-s-guide-for-active-accessibility-servers.md)。</span><span class="sxs-lookup"><span data-stu-id="276f4-118">For more information about implementing **IAccessible**, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="276f4-119">步驟2：執行 IServiceProvider 介面。</span><span class="sxs-lookup"><span data-stu-id="276f4-119">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="276f4-120">當用戶端要求有關無視窗控制項的協助工具資訊時，容器會呼叫您控制項的 [**IServiceProvider：： QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) 方法，以取得 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="276f4-120">When a client requests accessibility information about your windowless control, the container calls your control's [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method to retrieve the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="276f4-121">此範例顯示如何執行 [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) 方法。</span><span class="sxs-lookup"><span data-stu-id="276f4-121">This example shows how to implement the [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a><span data-ttu-id="276f4-122">步驟3：將 IAccessible：： get \_ accParent 方法呼叫委派給控制網站的 IAccessibleWindowlessSite：： GetParentAccessible 方法。</span><span class="sxs-lookup"><span data-stu-id="276f4-122">Step 3: Delegate IAccessible::get\_accParent method calls to the control site's IAccessibleWindowlessSite::GetParentAccessible method.</span></span>

<span data-ttu-id="276f4-123">當用戶端要求無視窗控制項的父物件時，容器會呼叫您控制項的 [**IAccessible：： get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 方法。</span><span class="sxs-lookup"><span data-stu-id="276f4-123">When a client requests the parent object of your windowless control, the container calls your control's [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span> <span data-ttu-id="276f4-124">您的 **get \_ accParent** 實應委派給容器的 [**IAccessibleWindowlessSite：： GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) 方法。</span><span class="sxs-lookup"><span data-stu-id="276f4-124">Your **get\_accParent** implementation should delegate to the [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method of the container.</span></span>

<span data-ttu-id="276f4-125">此範例顯示如何執行 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 方法。</span><span class="sxs-lookup"><span data-stu-id="276f4-125">This example shows how to implement the [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span>


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a><span data-ttu-id="276f4-126">步驟4：取得物件識別碼的範圍，以指派給無視窗控制項中的事件來源。</span><span class="sxs-lookup"><span data-stu-id="276f4-126">Step 4: Acquire a range of object IDs to assign to the event sources in your windowless control.</span></span>

<span data-ttu-id="276f4-127">就像以視窗為基礎的控制項一樣，無視窗的 ActiveX 控制項會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 函式來通知用戶端有重要的事件。</span><span class="sxs-lookup"><span data-stu-id="276f4-127">Like window-based controls, a windowless ActiveX control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function to notify clients of important events.</span></span> <span data-ttu-id="276f4-128">函數參數包含引發事件之專案的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="276f4-128">The function parameters include the object ID of the item that is raising the event.</span></span> <span data-ttu-id="276f4-129">無視窗控制項必須使用透過呼叫控制網站的 [**IAccessibleWindowlessSite：： AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) 方法取得的範圍中的值，來指派物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="276f4-129">Your windowless control must assign object IDs by using a value from a range acquired by calling the control site’s [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) method.</span></span>

<span data-ttu-id="276f4-130">此範例顯示如何從控制項容器取得物件識別碼值的範圍。</span><span class="sxs-lookup"><span data-stu-id="276f4-130">This example shows how to acquire a range of object ID values from the control container.</span></span>


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a><span data-ttu-id="276f4-131">步驟5：執行 IAccessibleHandler 介面。</span><span class="sxs-lookup"><span data-stu-id="276f4-131">Step 5: Implement the IAccessibleHandler interface.</span></span>

<span data-ttu-id="276f4-132">當無視窗控制項呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 函式時，控制項會指定引發事件之 UI 專案的物件識別碼，並將控制項容器指定為代表控制項回應 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息的視窗。</span><span class="sxs-lookup"><span data-stu-id="276f4-132">When a windowless control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function, the control specifies the object ID of the UI item that is raising the event, and specifies the control container as the window that will respond to [**WM\_GETOBJECT**](wm-getobject.md) messages on behalf of the control.</span></span>

<span data-ttu-id="276f4-133">如果用戶端應用程式回應事件，控制項容器會收到 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，其中包含引發事件之 UI 專案的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="276f4-133">If a client application responds to the event, the control container receives a [**WM\_GETOBJECT**](wm-getobject.md) message that includes the object ID of the UI item that raised the event.</span></span> <span data-ttu-id="276f4-134">控制項容器的回應方式是查詢「擁有」物件識別碼的無視窗控制項，然後呼叫該控制項的 [**IAccessibleHandler：： AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) 方法。</span><span class="sxs-lookup"><span data-stu-id="276f4-134">The control container responds by looking up the windowless control that "owns" the object ID, and then calling that control's [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) method.</span></span> <span data-ttu-id="276f4-135">**AccessibleObjectFromID** 方法會傳回 UI 專案的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標，而控制項容器會將指標轉送至用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="276f4-135">The **AccessibleObjectFromID** method returns the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the UI item, and the control container forwards the pointer to the client application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="276f4-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="276f4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="276f4-137">使用消費者介面自動化使無視窗的 ActiveX 控制項可供存取</span><span class="sxs-lookup"><span data-stu-id="276f4-137">Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="276f4-138">無視窗的 ActiveX 控制項協助工具</span><span class="sxs-lookup"><span data-stu-id="276f4-138">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 