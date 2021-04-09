---
title: UI 自動化提供者概觀
description: 本主題概要說明控制項開發人員如何執行消費者介面自動化提供者。
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- 消費者介面自動化，提供者總覽
- 消費者介面自動化，提供者類型
- 消費者介面自動化，提供者概念
- 提供者，關於
- 提供者，類型
- 提供者，概念
- 提供者、元素
- 提供者，導覽
- 提供者、視圖
- 提供者、架構
- 提供者、片段
- 提供者、主機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932097"
---
# <a name="ui-automation-providers-overview"></a><span data-ttu-id="12867-115">UI 自動化提供者概觀</span><span class="sxs-lookup"><span data-stu-id="12867-115">UI Automation Providers Overview</span></span>

<span data-ttu-id="12867-116">Microsoft 消費者介面自動化提供者是一個軟體物件，它會公開應用程式 UI 的元素，讓協助工具用戶端應用程式可以取得專案的相關資訊，並叫用其功能。</span><span class="sxs-lookup"><span data-stu-id="12867-116">A Microsoft UI Automation provider is a software object that exposes an element of an application's UI so that accessibility client applications can retrieve information about the element and invoke its functionality.</span></span> <span data-ttu-id="12867-117">一般而言，UI 中的每個控制項或其他相異元素都有提供者。</span><span class="sxs-lookup"><span data-stu-id="12867-117">In general, each control or other distinct element in a UI has a provider.</span></span>

<span data-ttu-id="12867-118">Microsoft 針對 Microsoft Win32、Windows Forms 和 Windows Presentation Foundation (WPF) 所提供的每個標準控制項，各包含一個提供者。</span><span class="sxs-lookup"><span data-stu-id="12867-118">Microsoft includes a provider for each of the standard controls that are supplied with Microsoft Win32, Windows Forms, and Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="12867-119">這表示標準控制項會自動公開給消費者介面自動化用戶端;您不需要為標準控制項執行任何協助工具介面。</span><span class="sxs-lookup"><span data-stu-id="12867-119">This means that the standard controls are automatically exposed to UI Automation clients; you do not need to implement any accessibility interfaces for the standard controls.</span></span>

<span data-ttu-id="12867-120">如果您的應用程式包含任何自訂控制項，您必須為這些控制項執行消費者介面自動化提供者，使其可供協助工具用戶端應用程式存取。</span><span class="sxs-lookup"><span data-stu-id="12867-120">If your application includes any custom controls, you need to implement UI Automation providers for those controls to make them accessible to accessibility client applications.</span></span> <span data-ttu-id="12867-121">您也需要為不包含提供者的任何協力廠商控制項，執行提供者。</span><span class="sxs-lookup"><span data-stu-id="12867-121">You also need to implement providers for any third party controls that do not include a provider.</span></span> <span data-ttu-id="12867-122">您可以藉由執行消費者介面自動化提供者介面和控制項模式介面來執行提供者。</span><span class="sxs-lookup"><span data-stu-id="12867-122">You implement a provider by implementing UI Automation provider interfaces and control pattern interfaces.</span></span>

<span data-ttu-id="12867-123">本主題概要說明控制項開發人員如何執行消費者介面自動化提供者。</span><span class="sxs-lookup"><span data-stu-id="12867-123">This topic provides an overview of how control developers implement UI Automation providers.</span></span> <span data-ttu-id="12867-124">其中包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="12867-124">It includes the following sections.</span></span>

-   [<span data-ttu-id="12867-125">提供者類型</span><span class="sxs-lookup"><span data-stu-id="12867-125">Types of Providers</span></span>](#types-of-providers)
-   [<span data-ttu-id="12867-126">使用者介面自動化提供者概念</span><span class="sxs-lookup"><span data-stu-id="12867-126">UI Automation Provider Concepts</span></span>](#ui-automation-provider-concepts)
    -   [<span data-ttu-id="12867-127">元素</span><span class="sxs-lookup"><span data-stu-id="12867-127">Elements</span></span>](#elements)
    -   [<span data-ttu-id="12867-128">架構</span><span class="sxs-lookup"><span data-stu-id="12867-128">Frameworks</span></span>](#frameworks)
    -   [<span data-ttu-id="12867-129">片段</span><span class="sxs-lookup"><span data-stu-id="12867-129">Fragments</span></span>](#fragments)
    -   [<span data-ttu-id="12867-130">主控件</span><span class="sxs-lookup"><span data-stu-id="12867-130">Hosts</span></span>](#hosts)
-   [<span data-ttu-id="12867-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="12867-131">Related topics</span></span>](#related-topics)

## <a name="types-of-providers"></a><span data-ttu-id="12867-132">提供者類型</span><span class="sxs-lookup"><span data-stu-id="12867-132">Types of Providers</span></span>

<span data-ttu-id="12867-133">消費者介面自動化提供者分為兩類：伺服器端提供者，以及用戶端 (或 *proxy*) 提供者。</span><span class="sxs-lookup"><span data-stu-id="12867-133">UI Automation providers fall into two categories: server-side providers, and client-side (or *proxy*) providers.</span></span>

<span data-ttu-id="12867-134">伺服器端提供者是一個物件（例如自訂控制項），其中包含自己的相關消費者介面自動化提供者介面的原生執行。</span><span class="sxs-lookup"><span data-stu-id="12867-134">A server-side provider is an object, such as a custom control, that contains its own native implementation of the relevant UI Automation provider interfaces.</span></span> <span data-ttu-id="12867-135">伺服器端提供者會將它的提供者介面實作為消費者介面自動化核心（可服務來自用戶端的要求），藉此與用戶端應用程式跨進程界限進行通訊。</span><span class="sxs-lookup"><span data-stu-id="12867-135">A server-side provider communicates with client applications across the process boundary by exposing its implementation of the provider interfaces to the UI Automation core, which services requests from clients.</span></span> <span data-ttu-id="12867-136">如需伺服器端提供者的詳細資訊，請參閱 [Server-Side 消費者介面自動化提供者執行](uiauto-serversideprovider.md)。</span><span class="sxs-lookup"><span data-stu-id="12867-136">For more information about server-side providers, see [Implementing a Server-Side UI Automation Provider](uiauto-serversideprovider.md).</span></span>

<span data-ttu-id="12867-137">用戶端提供者（或 proxy）是代表控制項實消費者介面自動化提供者介面的物件，並不包含其本身的完整提供者執行。</span><span class="sxs-lookup"><span data-stu-id="12867-137">A client-side provider, or proxy, is an object that implements UI Automation provider interfaces on behalf of a control does not include a full provider implementation of its own.</span></span> <span data-ttu-id="12867-138">如果沒有 proxy，則這類控制項在消費者介面自動化中大多是不透明的，它只能提供視窗控制碼 (**HWND**) 所提供的基本資訊，例如控制項位置。</span><span class="sxs-lookup"><span data-stu-id="12867-138">Without a proxy, such a control is largely opaque to UI Automation, which can supply only basic information available from the window handle (**HWND**), such as the control location.</span></span> <span data-ttu-id="12867-139">一般而言，proxy 提供者會藉由傳送和接收 Windows 訊息，在整個進程界限上與應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="12867-139">Typically, proxy providers communicate with the application across the process boundary by sending and receiving Windows messages.</span></span> <span data-ttu-id="12867-140">如需詳細資訊，請參閱 [消費者介面自動化提供者執行 Client-Side (Proxy) ](uiauto-clientsideprovider.md)。</span><span class="sxs-lookup"><span data-stu-id="12867-140">For more information, see [Implementing a Client-Side (Proxy) UI Automation Provider](uiauto-clientsideprovider.md).</span></span>

## <a name="ui-automation-provider-concepts"></a><span data-ttu-id="12867-141">使用者介面自動化提供者概念</span><span class="sxs-lookup"><span data-stu-id="12867-141">UI Automation Provider Concepts</span></span>

<span data-ttu-id="12867-142">本節提供某些主要概念的簡短說明，讓您了解以便實作使用者介面自動化提供者。</span><span class="sxs-lookup"><span data-stu-id="12867-142">This section provides brief explanations of some of the key concepts you need to understand in order to implement UI Automation providers.</span></span>

### <a name="elements"></a><span data-ttu-id="12867-143">元素</span><span class="sxs-lookup"><span data-stu-id="12867-143">Elements</span></span>

<span data-ttu-id="12867-144">消費者介面自動化專案是消費者介面自動化用戶端可以看見的 UI 的部分（通常是 windows 或控制項）。</span><span class="sxs-lookup"><span data-stu-id="12867-144">UI Automation elements are pieces of the UI—typically windows or controls—that are visible to UI Automation clients.</span></span> <span data-ttu-id="12867-145">範例包含應用程式視窗、窗格、按鈕、工具提示、清單方塊和清單項目。</span><span class="sxs-lookup"><span data-stu-id="12867-145">Examples include application windows, panes, buttons, tooltips, list boxes, and list items.</span></span>

<span data-ttu-id="12867-146">消費者介面自動化元素會以樹狀結構的形式公開給用戶端。</span><span class="sxs-lookup"><span data-stu-id="12867-146">UI Automation elements are exposed to clients as a tree.</span></span> <span data-ttu-id="12867-147">消費者介面自動化藉由在某個專案之間導覽來建立樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="12867-147">UI Automation constructs the tree by navigating from one element to another.</span></span> <span data-ttu-id="12867-148">每個元素的提供者都會啟用導覽。</span><span class="sxs-lookup"><span data-stu-id="12867-148">Navigation is enabled by the provider for each element.</span></span> <span data-ttu-id="12867-149">每個元素都可以指向其本身的父項目、其同級元素，以及其第一個和最後一個子專案。</span><span class="sxs-lookup"><span data-stu-id="12867-149">Each element can point to its own parent element, its sibling elements, and its first and last child elements.</span></span>

<span data-ttu-id="12867-150">用戶端可以在三個主要視圖中看到消費者介面自動化樹狀結構，如下表所述：</span><span class="sxs-lookup"><span data-stu-id="12867-150">A client can see the UI Automation tree in three principal views, as described in the following table:</span></span>



| <span data-ttu-id="12867-151">檢視</span><span class="sxs-lookup"><span data-stu-id="12867-151">View</span></span>         | <span data-ttu-id="12867-152">描述</span><span class="sxs-lookup"><span data-stu-id="12867-152">Description</span></span>                                                    |
|--------------|----------------------------------------------------------------|
| <span data-ttu-id="12867-153">未經處理的檢視</span><span class="sxs-lookup"><span data-stu-id="12867-153">Raw view</span></span>     | <span data-ttu-id="12867-154">包含所有元素。</span><span class="sxs-lookup"><span data-stu-id="12867-154">Includes all elements.</span></span>                                         |
| <span data-ttu-id="12867-155">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="12867-155">Control view</span></span> | <span data-ttu-id="12867-156">包含控制項的元素。</span><span class="sxs-lookup"><span data-stu-id="12867-156">Includes elements that are controls.</span></span>                           |
| <span data-ttu-id="12867-157">內容檢視</span><span class="sxs-lookup"><span data-stu-id="12867-157">Content view</span></span> | <span data-ttu-id="12867-158">包含可將資訊傳達給使用者的控制項元素。</span><span class="sxs-lookup"><span data-stu-id="12867-158">Includes control elements that convey information to the user.</span></span> |



 

<span data-ttu-id="12867-159">提供者實作負責將項目定義為內容項目或控制項項目。</span><span class="sxs-lookup"><span data-stu-id="12867-159">It is the responsibility of the provider implementation to define an element as a content element or a control element.</span></span> <span data-ttu-id="12867-160">控制項不一定是內容項目，但所有的內容項目都會是控制項項目。</span><span class="sxs-lookup"><span data-stu-id="12867-160">Control elements may or may not also be content elements, but all content elements are control elements.</span></span>

<span data-ttu-id="12867-161">如需樹狀結構用戶端視圖的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="12867-161">For more information on the client view of the tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

### <a name="frameworks"></a><span data-ttu-id="12867-162">架構</span><span class="sxs-lookup"><span data-stu-id="12867-162">Frameworks</span></span>

<span data-ttu-id="12867-163">架構是一個元件，管理該畫面區域的子控制項、點擊測試和呈現。</span><span class="sxs-lookup"><span data-stu-id="12867-163">A framework is a component that manages child controls, hit-testing, and rendering in an area of the screen.</span></span> <span data-ttu-id="12867-164">例如，Win32 視窗（通常稱為 **HWND**）可以做為包含多個消費者介面自動化元素（例如功能表列、狀態列和按鈕）的架構。</span><span class="sxs-lookup"><span data-stu-id="12867-164">For example, a Win32 window, often referred to as an **HWND**, can serve as a framework that contains multiple UI Automation elements, such as a menu bar, a status bar, and buttons.</span></span>

<span data-ttu-id="12867-165">Win32 容器控制項（例如清單方塊和樹狀檢視控制項）被視為是架構，因為它們包含自己的程式碼來轉譯子專案，並對其執行點擊測試。</span><span class="sxs-lookup"><span data-stu-id="12867-165">Win32 container controls such as list boxes and tree-view controls are considered to be frameworks because they contain their own code for rendering child items and performing hit-testing on them.</span></span> <span data-ttu-id="12867-166">相較之下，WPF 清單方塊並不是架構，因為呈現和點擊測試都是由包含視窗處理。</span><span class="sxs-lookup"><span data-stu-id="12867-166">By contrast, a WPF list box is not a framework, because the rendering and hit-testing is being handled by the containing window.</span></span>

<span data-ttu-id="12867-167">應用程式中的 UI 可由不同的架構所組成。</span><span class="sxs-lookup"><span data-stu-id="12867-167">The UI in an application can be made up of different frameworks.</span></span> <span data-ttu-id="12867-168">例如，應用程式中的 **HWND** 可能包含動態 HTML (DHTML) 它可以在 **HWND** 中包含下拉式列示方塊，例如下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="12867-168">For example, an **HWND** in an application might contain Dynamic HTML (DHTML) which in turn can contain a component such as a combo box in an **HWND**.</span></span>

### <a name="fragments"></a><span data-ttu-id="12867-169">片段</span><span class="sxs-lookup"><span data-stu-id="12867-169">Fragments</span></span>

<span data-ttu-id="12867-170">來自特定架構之元素的完整子樹稱為片段。</span><span class="sxs-lookup"><span data-stu-id="12867-170">A complete subtree of elements from a particular framework is called a fragment.</span></span> <span data-ttu-id="12867-171">子樹狀結構之根目錄節點的項目稱為片段根目錄。</span><span class="sxs-lookup"><span data-stu-id="12867-171">The element at the root node of the subtree is called a fragment root.</span></span> <span data-ttu-id="12867-172">片段根目錄沒有父代，但裝載于其他架構中，通常是 Win32 視窗 (**HWND**) 。</span><span class="sxs-lookup"><span data-stu-id="12867-172">A fragment root does not have a parent, but is hosted within some other framework, usually a Win32 window (**HWND**).</span></span>

### <a name="hosts"></a><span data-ttu-id="12867-173">主機</span><span class="sxs-lookup"><span data-stu-id="12867-173">Hosts</span></span>

<span data-ttu-id="12867-174">每個片段的根節點都必須裝載于元素中，通常是 Win32 視窗 (**HWND**) 。</span><span class="sxs-lookup"><span data-stu-id="12867-174">The root node of every fragment must be hosted in an element, usually a Win32 window (**HWND**).</span></span> <span data-ttu-id="12867-175">例外狀況是桌面，桌面並沒有裝載於任何其他項目中。</span><span class="sxs-lookup"><span data-stu-id="12867-175">The exception is the desktop, which is not hosted in any other element.</span></span> <span data-ttu-id="12867-176">自訂控制項的主機是控制項本身的 **HWND** ，而不是應用程式視窗或可能包含最上層控制項群組的任何其他視窗。</span><span class="sxs-lookup"><span data-stu-id="12867-176">The host of a custom control is the **HWND** of the control itself, not the application window or any other window that might contain groups of top-level controls.</span></span>

<span data-ttu-id="12867-177">片段的主機在提供消費者介面自動化服務方面扮演著重要的角色。</span><span class="sxs-lookup"><span data-stu-id="12867-177">The host of a fragment plays an important role in providing UI Automation services.</span></span> <span data-ttu-id="12867-178">可在片段根目錄中進行巡覽並提供某些預設屬性，讓自訂提供者不需要進行實作。</span><span class="sxs-lookup"><span data-stu-id="12867-178">It enables navigation to the fragment root, and supplies some default properties so that the custom provider does not have to implement them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12867-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="12867-179">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="12867-180">**概念**</span><span class="sxs-lookup"><span data-stu-id="12867-180">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="12867-181">執行 Client-Side 消費者介面自動化提供者</span><span class="sxs-lookup"><span data-stu-id="12867-181">Implementing a Client-Side UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
</dt> <dt>

[<span data-ttu-id="12867-182">執行 Server-Side 消費者介面自動化提供者</span><span class="sxs-lookup"><span data-stu-id="12867-182">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="12867-183">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="12867-183">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




