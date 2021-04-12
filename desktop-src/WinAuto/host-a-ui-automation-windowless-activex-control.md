---
title: 裝載消費者介面自動化無視窗的 ActiveX 控制項
description: 瞭解如何建立控制項容器，以裝載可執行 Microsoft 消費者介面自動化的無視窗 Microsoft ActiveX 控制項。
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- 消費者介面自動化，無視窗的 ActiveX 控制項
- 無視窗的 ActiveX 控制項，消費者介面自動化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315289"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a><span data-ttu-id="4c6f8-105">裝載消費者介面自動化無視窗的 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="4c6f8-105">Host a UI Automation Windowless ActiveX Control</span></span>

<span data-ttu-id="4c6f8-106">瞭解如何建立控制項容器，以裝載可執行 Microsoft 消費者介面自動化的無視窗 Microsoft ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-106">Learn how to create a control container that can host windowless Microsoft ActiveX controls that implement Microsoft UI Automation.</span></span> <span data-ttu-id="4c6f8-107">您可以使用此處所述的步驟，確保在) 用戶端應用程式 (的輔助技術可以存取您控制項容器中裝載的任何消費者介面自動化無視窗控制項。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-107">By using the steps described here, you can ensure that any UI Automation windowless controls that are hosted in your control container are accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4c6f8-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="4c6f8-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4c6f8-109">技術</span><span class="sxs-lookup"><span data-stu-id="4c6f8-109">Technologies</span></span>

-   [<span data-ttu-id="4c6f8-110">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="4c6f8-110">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="4c6f8-111">使用者介面自動化</span><span class="sxs-lookup"><span data-stu-id="4c6f8-111">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="4c6f8-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="4c6f8-112">Prerequisites</span></span>

-   <span data-ttu-id="4c6f8-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="4c6f8-113">C/C++</span></span>
-   <span data-ttu-id="4c6f8-114">Microsoft Win32 和元件物件模型 (COM) 程式設計</span><span class="sxs-lookup"><span data-stu-id="4c6f8-114">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="4c6f8-115">無視窗的 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="4c6f8-115">Windowless ActiveX controls</span></span>
-   <span data-ttu-id="4c6f8-116">消費者介面自動化提供者</span><span class="sxs-lookup"><span data-stu-id="4c6f8-116">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="4c6f8-117">指示</span><span class="sxs-lookup"><span data-stu-id="4c6f8-117">Instructions</span></span>

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a><span data-ttu-id="4c6f8-118">步驟1：代表無視窗控制項提供 IRawElementProviderSimple 介面。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-118">Step 1: Provide the IRawElementProviderSimple interface on behalf of the windowless control.</span></span>

<span data-ttu-id="4c6f8-119">只要系統需要無視窗控制項根目錄的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 指標，系統就會查詢控制項容器。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-119">Whenever the system needs the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer for the root of a windowless control, the system queries the control container.</span></span> <span data-ttu-id="4c6f8-120">為了取得指標，容器會呼叫無視窗控制項的 [**IServiceProvider：： QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) 方法的實作為。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-120">To retrieve the pointer, the container calls the windowless control's implementation of the [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>

<span data-ttu-id="4c6f8-121">如果控制項容器有消費者介面自動化的執行，則可以將無視窗控制項的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 指標傳回系統。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-121">If the control container has a UI Automation implementation, it can return the windowless control's [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer to the system.</span></span>

<span data-ttu-id="4c6f8-122">如果控制項容器有 Microsoft Active Accessibility 的執行，請呼叫 [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) 函式來取得代表控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，然後將 **IAccessible** 介面指標傳回系統。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-122">If the control container has a Microsoft Active Accessibility implementation, call the [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) function to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer that represents the control, and then return the **IAccessible** interface pointer to the system.</span></span>

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a><span data-ttu-id="4c6f8-123">步驟2：執行 IRawElementProviderWindowlessSite 介面。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-123">Step 2: Implement the IRawElementProviderWindowlessSite interface.</span></span>

<span data-ttu-id="4c6f8-124">控制項容器會執行 [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) 介面，以啟用以消費者介面自動化為基礎的無視窗控制項，以傳達其協助工具資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-124">A control container implements the [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) interface enable a windowless control that is based on UI Automation to communicate its accessibility information.</span></span>

1.  <span data-ttu-id="4c6f8-125">執行 [**IRawElementProviderWindowlessSite：： GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix)。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-125">Implement [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span></span>

    <span data-ttu-id="4c6f8-126">無視窗的控制項片段必須為自己建立唯一的執行時間識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-126">A windowless control fragment must create a unique runtime ID for itself.</span></span> <span data-ttu-id="4c6f8-127">若要建立其執行時間識別碼，無視窗的控制項片段會藉由呼叫控制網站的 [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) 方法來抓取前置詞值，然後將相對於無視窗控制項中所有其他片段的唯一整數值附加至前置詞。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-127">To create its runtime ID, a windowless control fragment retrieves a prefix value by calling the control site's [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method, and then appends to the prefix an integer value that is unique relative to all other fragments in the windowless control.</span></span>

    <span data-ttu-id="4c6f8-128">無視窗控制項的控制網站應藉由形成包含常數 **UiaAppendRuntimeId** 的 **SAFEARRAY** ，後面接著網站唯一的整數值，來執行 [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix)方法。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-128">The control site for a windowless control should implement the [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method by forming a **SAFEARRAY** that contains the constant **UiaAppendRuntimeId**, followed by an integer value that is unique to the site.</span></span>

    <span data-ttu-id="4c6f8-129">這個範例會示範如何傳回無視窗控制項的執行時間識別碼前置詞。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-129">This example shows how to return a runtime ID prefix for a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  <span data-ttu-id="4c6f8-130">執行 [**IRawElementProviderWindowlessSite：： GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-130">Implement the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method.</span></span>

    <span data-ttu-id="4c6f8-131">實消費者介面自動化的控制項必須將指標傳回給控制項的父片段提供者。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-131">A control that implements UI Automation must return a pointer to the control's parent fragment provider.</span></span>

    <span data-ttu-id="4c6f8-132">若要傳回片段的父系，執行 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) 介面的物件必須能夠執行 [**流覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-132">To return the parent of the fragment, an object that implements the [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) interface must be able to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span> <span data-ttu-id="4c6f8-133">由於控制項可能無法在父物件的可存取樹狀結構中判斷其位置，因此對無視窗控制項而言，執行 **導覽** 很困難。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-133">Implementing **Navigate** is difficult for a windowless control because the control might be unable to determine its location in the accessible tree of the parent object.</span></span> <span data-ttu-id="4c6f8-134">[**IRawElementProviderWindowlessSite：： GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment)方法可讓無視窗控制項查詢其網站中的相鄰片段，然後將該片段傳回給呼叫 **導覽** 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-134">The [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method enables the windowless control to query its site for the adjacent fragment, and then return that fragment to the client that called **Navigate**.</span></span>

    <span data-ttu-id="4c6f8-135">此範例顯示控制項容器如何抓取無視窗控制項的父片段。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-135">This example shows how a control container retrieves the parent fragment of a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a><span data-ttu-id="4c6f8-136">步驟3：選擇性：執行 IRawElementProviderHostingAccessibles 介面。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-136">Step 3: Optional: Implement the IRawElementProviderHostingAccessibles interface.</span></span>

<span data-ttu-id="4c6f8-137">如果您的控制項容器有消費者介面自動化提供者實作為協助工具樹狀結構的根，其中包含支援 Microsoft Active Accessibility 的無視窗 ActiveX 控制項，則請執行 [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) 介面。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-137">Implement the [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) interface if your control container has a UI Automation provider implementation that is the root of an accessibility tree that includes windowless ActiveX controls that support Microsoft Active Accessibility.</span></span> <span data-ttu-id="4c6f8-138">**IRawElementProviderHostingAccessibles** 介面具有單一方法 [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles)，可抓取您的控制項容器所裝載的所有 Microsoft Active Accessibility 型無視窗 ActiveX 控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標。</span><span class="sxs-lookup"><span data-stu-id="4c6f8-138">The **IRawElementProviderHostingAccessibles** interface has a single method, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), which retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers of all Microsoft Active Accessibility-based windowless ActiveX controls that are hosted by your control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c6f8-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c6f8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c6f8-140">如何裝載 MSAA 無視窗 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="4c6f8-140">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[<span data-ttu-id="4c6f8-141">無視窗的 ActiveX 控制項協助工具</span><span class="sxs-lookup"><span data-stu-id="4c6f8-141">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 