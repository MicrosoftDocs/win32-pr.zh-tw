---
title: 如何裝載 MSAA 無視窗 ActiveX 控制項
description: 瞭解如何建立可裝載可執行 Microsoft Active Accessibility 之無視窗 Microsoft ActiveX 控制項的控制項容器。
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA，無視窗的 ActiveX 控制項
- 無視窗的 ActiveX 控制項、MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de45313b19490af3c3fffb633f3822ad93d25a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682413"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a><span data-ttu-id="6e7e3-105">如何裝載 MSAA 無視窗 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="6e7e3-105">How to Host an MSAA Windowless ActiveX Control</span></span>

<span data-ttu-id="6e7e3-106">瞭解如何建立可裝載可執行 Microsoft Active Accessibility 之無視窗 Microsoft ActiveX 控制項的控制項容器。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-106">Learn how to create a control container that can host windowless Microsoft ActiveX controls that implement Microsoft Active Accessibility.</span></span> <span data-ttu-id="6e7e3-107">依照此處所述的步驟，您可以確保在) 用戶端應用程式 (輔助技術可存取控制容器中裝載的任何 Microsoft Active Accessibility 型無視窗控制項。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-107">By following the steps described here, you can ensure that any Microsoft Active Accessibility-based windowless controls that are hosted in your control container are accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6e7e3-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="6e7e3-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6e7e3-109">技術</span><span class="sxs-lookup"><span data-stu-id="6e7e3-109">Technologies</span></span>

-   [<span data-ttu-id="6e7e3-110">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="6e7e3-110">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="6e7e3-111">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="6e7e3-111">Microsoft Active Accessibility</span></span>](microsoft-active-accessibility.md)

### <a name="prerequisites"></a><span data-ttu-id="6e7e3-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="6e7e3-112">Prerequisites</span></span>

-   <span data-ttu-id="6e7e3-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="6e7e3-113">C/C++</span></span>
-   <span data-ttu-id="6e7e3-114">Microsoft Win32 和元件物件模型 (COM) 程式設計</span><span class="sxs-lookup"><span data-stu-id="6e7e3-114">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="6e7e3-115">無視窗的 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="6e7e3-115">Windowless ActiveX controls</span></span>
-   <span data-ttu-id="6e7e3-116">Microsoft Active Accessibility 伺服器</span><span class="sxs-lookup"><span data-stu-id="6e7e3-116">Microsoft Active Accessibility servers</span></span>

## <a name="instructions"></a><span data-ttu-id="6e7e3-117">指示</span><span class="sxs-lookup"><span data-stu-id="6e7e3-117">Instructions</span></span>

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a><span data-ttu-id="6e7e3-118">步驟1：代表無視窗控制項提供根 IAccessible 介面。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-118">Step 1: Provide the root IAccessible interface on behalf of the windowless control.</span></span>

<span data-ttu-id="6e7e3-119">只要系統需要無視窗控制項根目錄的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 指標，系統就會查詢控制項容器。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-119">Whenever the system needs the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pointer for the root of a windowless control, the system queries the control container.</span></span> <span data-ttu-id="6e7e3-120">為了取得指標，容器會呼叫無視窗控制項的 [**IServiceProvider：： QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) 方法的實作為。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-120">To retrieve the pointer, the container calls the windowless control's implementation of the [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>

<span data-ttu-id="6e7e3-121">如果控制項容器有 Microsoft Active Accessibility 的執行，則可以將無視窗控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 指標傳回系統。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-121">If the control container has a Microsoft Active Accessibility implementation, it can return the windowless control's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pointer to the system.</span></span>

<span data-ttu-id="6e7e3-122">如果控制項容器具有 Microsoft 消費者介面自動化的執行，請呼叫 [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) 函式來取得代表控制項的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面指標，然後將 **IRawElementProviderSimple** 介面指標傳回系統。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-122">If the control container has a Microsoft UI Automation implementation, call the [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) function to obtain an [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface pointer that represents the control, and then return the **IRawElementProviderSimple** interface pointer to the system.</span></span>

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a><span data-ttu-id="6e7e3-123">步驟2： \_ 代表無視窗控制項回應 WM GETOBJECT message。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-123">Step 2: Respond to the WM\_GETOBJECT message on behalf of the windowless control.</span></span>

<span data-ttu-id="6e7e3-124">當用戶端應用程式回應無視窗控制項所引發的 New-winevent 時，控制項容器會代表控制項接收 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-124">When a client application responds to a WinEvent raised by a windowless control, the control container receives a [**WM\_GETOBJECT**](wm-getobject.md) message on behalf of the control.</span></span> <span data-ttu-id="6e7e3-125">訊息包含引發事件之無視窗控制項的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-125">The message includes the object ID of the windowless control that raised the event.</span></span>

<span data-ttu-id="6e7e3-126">控制項容器的回應方式是查詢「擁有」物件識別碼的無視窗控制項，然後呼叫該控制項的 [**IAccessibleHandler：： AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) 方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-126">The control container responds by looking up the windowless control that "owns" the object ID, and then calling that control's [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) method.</span></span> <span data-ttu-id="6e7e3-127">**AccessibleObjectFromID** 方法會傳回 UI 專案的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標，而控制項容器會傳回指向系統的指標，然後將指標轉送至用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-127">The **AccessibleObjectFromID** method returns the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the UI item, and the control container returns the pointer to the system, which forwards it to the client application.</span></span>

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a><span data-ttu-id="6e7e3-128">步驟3：執行 IAccessibleWindowlessSite 介面。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-128">Step 3: Implement the IAccessibleWindowlessSite interface.</span></span>

1.  <span data-ttu-id="6e7e3-129">執行 [**IAccessibleWindowlessSite：： GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) 方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-129">Implement the [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method.</span></span>

    <span data-ttu-id="6e7e3-130">當用戶端應用程式需要無視窗控制項根提供者父系的協助工具資訊時，系統會呼叫無視窗控制項的 [**IAccessible：： get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-130">When a client application needs accessibility information about the parent of the windowless control's root provider, the system calls the windowless control's [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span> <span data-ttu-id="6e7e3-131">控制項會藉由呼叫控制項容器的 [**IAccessibleWindowlessSite：： GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) 方法來回應，這個方法會提供無視窗控制項父系的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 指標。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-131">The control responds by calling the control container's [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method, which provides the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pointer of the windowless control's parent.</span></span>

2.  <span data-ttu-id="6e7e3-132">執行 [**IAccessibleWindowlessSite：： AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange)、 [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)和 [**ReleaseObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) 方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-132">Implement the [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges), and [**ReleaseObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) methods.</span></span>

    <span data-ttu-id="6e7e3-133">您的控制項容器必須維持物件識別碼範圍與無視窗控制項的對應。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-133">Your control container must maintain a mapping of object ID ranges to windowless controls.</span></span> <span data-ttu-id="6e7e3-134">對應可讓控制項容器識別應該回應物件識別碼之特定要求的控制項。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-134">The mapping enables the control container to identify the control that should respond to a particular request for an object ID.</span></span> <span data-ttu-id="6e7e3-135">下表顯示將物件識別碼範圍對應至無視窗控制項的範例。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-135">The following table shows an example of mapping object ID ranges to windowless controls.</span></span>

    

    | <span data-ttu-id="6e7e3-136">範圍基底</span><span class="sxs-lookup"><span data-stu-id="6e7e3-136">Range base</span></span> | <span data-ttu-id="6e7e3-137">範圍大小</span><span class="sxs-lookup"><span data-stu-id="6e7e3-137">Range size</span></span> | <span data-ttu-id="6e7e3-138">控制</span><span class="sxs-lookup"><span data-stu-id="6e7e3-138">Control</span></span>   |
    |------------|------------|-----------|
    | <span data-ttu-id="6e7e3-139">1000</span><span class="sxs-lookup"><span data-stu-id="6e7e3-139">1000</span></span>       | <span data-ttu-id="6e7e3-140">500</span><span class="sxs-lookup"><span data-stu-id="6e7e3-140">500</span></span>        | <span data-ttu-id="6e7e3-141">控制項1</span><span class="sxs-lookup"><span data-stu-id="6e7e3-141">Control 1</span></span> |
    | <span data-ttu-id="6e7e3-142">1500</span><span class="sxs-lookup"><span data-stu-id="6e7e3-142">1500</span></span>       | <span data-ttu-id="6e7e3-143">1000</span><span class="sxs-lookup"><span data-stu-id="6e7e3-143">1000</span></span>       | <span data-ttu-id="6e7e3-144">控制項2</span><span class="sxs-lookup"><span data-stu-id="6e7e3-144">Control 2</span></span> |
    | <span data-ttu-id="6e7e3-145">2500</span><span class="sxs-lookup"><span data-stu-id="6e7e3-145">2500</span></span>       | <span data-ttu-id="6e7e3-146">2000</span><span class="sxs-lookup"><span data-stu-id="6e7e3-146">2000</span></span>       | <span data-ttu-id="6e7e3-147">控制項1</span><span class="sxs-lookup"><span data-stu-id="6e7e3-147">Control 1</span></span> |

    

     

    <span data-ttu-id="6e7e3-148">控制項容器必須維持物件識別碼範圍與本身和所有無視窗子系的無視窗控制項的對應。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-148">The control container must maintain the mapping of object ID ranges to windowless controls for itself and all windowless children.</span></span> <span data-ttu-id="6e7e3-149">物件識別碼範圍不需要彼此相鄰。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-149">The object ID ranges do not need to be adjacent to one another.</span></span> <span data-ttu-id="6e7e3-150">此外，為了避免拒絕服務的攻擊，控制容器可以限制授與特定控制項的範圍數目。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-150">Also, to avoid denial-of-service attacks, the control container can place limits on the number of ranges that are granted to a particular control.</span></span> <span data-ttu-id="6e7e3-151">不過，允許每個控制項有一個以上的範圍，以便讓控制項成長變得很有用。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-151">However, it is useful to allow more than one range per control, to enable a control to grow.</span></span>

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a><span data-ttu-id="6e7e3-152">步驟4：選擇性：執行 IAccessibleHostingElementProviders 介面。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-152">Step 4: Optional: Implement the IAccessibleHostingElementProviders interface.</span></span>

<span data-ttu-id="6e7e3-153">如果您的控制項容器具有 Microsoft Active Accessibility server 的執行，而伺服器是協助工具樹狀結構的根，其中包含支援消費者介面自動化的無視窗 ActiveX 控制項，則請執行 [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) 介面。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-153">Implement the [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) interface if your control container has a Microsoft Active Accessibility server implementation and the server is the root of an accessibility tree that includes windowless ActiveX controls that support UI Automation.</span></span> <span data-ttu-id="6e7e3-154">**IAccessibleHostingElementProviders** 介面具有單一方法 [**GetEmbeddedFragmentRoots**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots)，可抓取控制項容器所裝載的所有消費者介面自動化無視窗 ActiveX 控制項的 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)介面指標。</span><span class="sxs-lookup"><span data-stu-id="6e7e3-154">The **IAccessibleHostingElementProviders** interface has a single method, [**GetEmbeddedFragmentRoots**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots), which retrieves the [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) interface pointers of all UI Automation windowless ActiveX controls that are hosted by your control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e7e3-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e7e3-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e7e3-156">如何裝載消費者介面自動化無視窗的 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="6e7e3-156">How to Host a UI Automation Windowless ActiveX Control</span></span>](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[<span data-ttu-id="6e7e3-157">無視窗的 ActiveX 控制項協助工具</span><span class="sxs-lookup"><span data-stu-id="6e7e3-157">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 