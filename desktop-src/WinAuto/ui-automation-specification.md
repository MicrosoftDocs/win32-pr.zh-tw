---
title: 消費者介面自動化規格
description: 本主題提供 Microsoft 消費者介面自動化規格的總覽，以構成消費者介面自動化的 Windows 實作為基礎。
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3cbb7ed2caa49e855b25f749820de8cf24f1e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023719"
---
# <a name="ui-automation-specification"></a><span data-ttu-id="d42d6-103">消費者介面自動化規格</span><span class="sxs-lookup"><span data-stu-id="d42d6-103">UI Automation Specification</span></span>

<span data-ttu-id="d42d6-104">本主題提供 Microsoft 消費者介面自動化規格的總覽，以構成消費者介面自動化的 Windows 實作為基礎。</span><span class="sxs-lookup"><span data-stu-id="d42d6-104">This topic provides an overview of the Microsoft UI Automation Specification, which forms the basis of the Windows implementation of UI Automation.</span></span> <span data-ttu-id="d42d6-105">Microsoft Windows 以外的所有平臺都可支援消費者介面自動化規格。</span><span class="sxs-lookup"><span data-stu-id="d42d6-105">The UI Automation Specification can be supported across platforms other than Microsoft Windows.</span></span> <span data-ttu-id="d42d6-106">如需詳細資訊，請參閱 [消費者介面自動化規格](./uiauto-specandcommunitypromise.md)</span><span class="sxs-lookup"><span data-stu-id="d42d6-106">For more information, see [UI Automation Specification](./uiauto-specandcommunitypromise.md)</span></span>

<span data-ttu-id="d42d6-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="d42d6-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d42d6-108">Introducton</span><span class="sxs-lookup"><span data-stu-id="d42d6-108">Introducton</span></span>](#introducton)
-   [<span data-ttu-id="d42d6-109">消費者介面自動化元素</span><span class="sxs-lookup"><span data-stu-id="d42d6-109">UI Automation Elements</span></span>](#ui-automation-elements)
-   [<span data-ttu-id="d42d6-110">消費者介面自動化樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d42d6-110">UI Automation Tree</span></span>](#ui-automation-tree)
-   [<span data-ttu-id="d42d6-111">消費者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="d42d6-111">UI Automation Properties</span></span>](#ui-automation-properties)
-   [<span data-ttu-id="d42d6-112">UI 自動化控制項模式</span><span class="sxs-lookup"><span data-stu-id="d42d6-112">UI Automation Control Patterns</span></span>](#ui-automation-control-patterns)
-   [<span data-ttu-id="d42d6-113">UI 自動化控制項類型</span><span class="sxs-lookup"><span data-stu-id="d42d6-113">UI Automation Control Types</span></span>](#ui-automation-control-types)
-   [<span data-ttu-id="d42d6-114">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="d42d6-114">UI Automation Events</span></span>](#ui-automation-events)
-   [<span data-ttu-id="d42d6-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="d42d6-115">Related topics</span></span>](#related-topics)

## <a name="introducton"></a><span data-ttu-id="d42d6-116">Introducton</span><span class="sxs-lookup"><span data-stu-id="d42d6-116">Introducton</span></span>

<span data-ttu-id="d42d6-117">消費者介面自動化規格可讓您以程式設計方式存取 Windows 桌面上的 UI 元素，讓輔助技術產品（例如螢幕讀取器）提供使用者介面的相關資訊，以及透過標準輸入以外的方式操作 UI。</span><span class="sxs-lookup"><span data-stu-id="d42d6-117">The UI Automation Specification provides flexible programmatic access to UI elements on the Windows desktop, enabling assistive technology products such as screen readers to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span>

<span data-ttu-id="d42d6-118">消費者介面自動化在範圍內的範圍更廣，只限于介面定義。</span><span class="sxs-lookup"><span data-stu-id="d42d6-118">UI Automation is broader in scope than just an interface definition.</span></span> <span data-ttu-id="d42d6-119">它提供：</span><span class="sxs-lookup"><span data-stu-id="d42d6-119">It provides:</span></span>

-   <span data-ttu-id="d42d6-120">物件模型和函式，可讓用戶端應用程式輕鬆地接收事件、抓取屬性值，以及操作 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="d42d6-120">An object model and functions that make it easy for client applications to receive events, retrieve property values, and manipulate UI elements.</span></span>
-   <span data-ttu-id="d42d6-121">跨進程界限尋找和提取的核心基礎結構。</span><span class="sxs-lookup"><span data-stu-id="d42d6-121">A core infrastructure for finding and fetching across process boundaries.</span></span>
-   <span data-ttu-id="d42d6-122">提供者的一組介面，用來表示 UI 元素的樹狀結構、一般屬性和功能。</span><span class="sxs-lookup"><span data-stu-id="d42d6-122">A set of interfaces for providers to express the tree structure, general properties, and functionality of UI elements.</span></span>
-   <span data-ttu-id="d42d6-123">「控制項類型」屬性，可讓用戶端和提供者清楚地指出 UI 物件的通用屬性、功能和結構。</span><span class="sxs-lookup"><span data-stu-id="d42d6-123">A "control type" property that allows clients and providers to clearly indicate the common properties, functionality, and structure of a UI object.</span></span>

<span data-ttu-id="d42d6-124">消費者介面自動化可透過下列方式改善 Microsoft Active Accessibility：</span><span class="sxs-lookup"><span data-stu-id="d42d6-124">UI Automation improves on Microsoft Active Accessibility by:</span></span>

-   <span data-ttu-id="d42d6-125">啟用有效率的跨進程用戶端，同時繼續允許同進程存取。</span><span class="sxs-lookup"><span data-stu-id="d42d6-125">Enabling efficient out-of-process clients, while continuing to allow in-process access.</span></span>
-   <span data-ttu-id="d42d6-126">以允許用戶端跨進程的方式，公開 UI 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d42d6-126">Exposing more information about the UI in a way that allows clients to be out-of-process.</span></span>
-   <span data-ttu-id="d42d6-127">共存並利用 Microsoft Active Accessibility 而不會繼承其限制。</span><span class="sxs-lookup"><span data-stu-id="d42d6-127">Coexisting with and leveraging Microsoft Active Accessibility without inheriting its limitations.</span></span> <span data-ttu-id="d42d6-128">如需詳細資訊，請參閱 [Microsoft Active Accessibility 和消費者介面自動化比較](microsoft-active-accessibility-and-ui-automation-compared.md)。</span><span class="sxs-lookup"><span data-stu-id="d42d6-128">For more information, see [Microsoft Active Accessibility and UI Automation Compared](microsoft-active-accessibility-and-ui-automation-compared.md).</span></span>
-   <span data-ttu-id="d42d6-129">提供可輕鬆執行的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 替代方案。</span><span class="sxs-lookup"><span data-stu-id="d42d6-129">Providing an alternative to [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) that is simple to implement.</span></span>

<span data-ttu-id="d42d6-130">在 Windows 功能元件物件模型中， (COM) 型介面和 managed 介面的消費者介面自動化規格的實作為基礎。</span><span class="sxs-lookup"><span data-stu-id="d42d6-130">The implementation of the UI Automation Specification in Windows features Component Object Model (COM)-based interfaces and managed interfaces.</span></span>

## <a name="ui-automation-elements"></a><span data-ttu-id="d42d6-131">消費者介面自動化元素</span><span class="sxs-lookup"><span data-stu-id="d42d6-131">UI Automation Elements</span></span>

<span data-ttu-id="d42d6-132">消費者介面自動化會將 UI 的每個部分以 *Automation 元素* 公開至用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="d42d6-132">UI Automation exposes every piece of the UI to client applications as an *automation element*.</span></span> <span data-ttu-id="d42d6-133">提供者會提供每個元素的屬性值。</span><span class="sxs-lookup"><span data-stu-id="d42d6-133">Providers supply property values for each element.</span></span> <span data-ttu-id="d42d6-134">元素會以樹狀結構的形式公開，並以桌面作為根項目。</span><span class="sxs-lookup"><span data-stu-id="d42d6-134">Elements are exposed as a tree structure, with the desktop as the root element.</span></span>

<span data-ttu-id="d42d6-135">Automation 元素會公開其所代表之 UI 元素的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="d42d6-135">Automation elements expose common properties of the UI elements they represent.</span></span> <span data-ttu-id="d42d6-136">其中一個屬性是控制項類型，描述其基本外觀和功能 (例如按鈕或核取方塊) 。</span><span class="sxs-lookup"><span data-stu-id="d42d6-136">One of these properties is the control type, which describes its basic appearance and functionality (for example, a button or a check box).</span></span>

## <a name="ui-automation-tree"></a><span data-ttu-id="d42d6-137">消費者介面自動化樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d42d6-137">UI Automation Tree</span></span>

<span data-ttu-id="d42d6-138">消費者介面自動化樹狀結構代表整個 UI：根項目是目前的桌面，而子項目則是應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="d42d6-138">The UI Automation tree represents the entire UI: the root element is the current desktop, and child elements are application windows.</span></span> <span data-ttu-id="d42d6-139">每個子專案都可以包含代表功能表、按鈕、工具列等專案的元素。</span><span class="sxs-lookup"><span data-stu-id="d42d6-139">Each of these child elements can contain elements representing menus, buttons, toolbars, and so on.</span></span> <span data-ttu-id="d42d6-140">這些專案接著可以包含像清單專案的專案，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d42d6-140">These elements in turn can contain elements like list items, as the following illustration shows.</span></span>

![顯示使用者介面自動化樹狀結構的螢幕擷取畫面](images/uiatree.gif)

<span data-ttu-id="d42d6-142">請注意，消費者介面自動化樹狀結構中的同級順序相當重要。</span><span class="sxs-lookup"><span data-stu-id="d42d6-142">Be aware that the order of the siblings in the UI Automation tree is quite important.</span></span> <span data-ttu-id="d42d6-143">在視覺效果中彼此連續的物件也應該在消費者介面自動化樹狀結構中的彼此旁邊。</span><span class="sxs-lookup"><span data-stu-id="d42d6-143">Objects that are next to each other visually should also be next to each other in the UI Automation tree.</span></span>

<span data-ttu-id="d42d6-144">消費者介面自動化特定控制項的提供者，支援該控制項的子項目之間的導覽。</span><span class="sxs-lookup"><span data-stu-id="d42d6-144">UI Automation providers for a particular control support navigation among the child elements of that control.</span></span> <span data-ttu-id="d42d6-145">但是，提供者不在意這些控制項子樹之間的導覽。</span><span class="sxs-lookup"><span data-stu-id="d42d6-145">However, providers are not concerned with navigation between these control sub-trees.</span></span> <span data-ttu-id="d42d6-146">這是由消費者介面自動化 core 管理，並使用預設視窗提供者的資訊。</span><span class="sxs-lookup"><span data-stu-id="d42d6-146">This is managed by the UI Automation core, using information from the default window providers.</span></span>

<span data-ttu-id="d42d6-147">為了協助用戶端更有效率地處理 UI 資訊，架構支援自動化樹狀結構的替代視圖：原始視圖、控制項視圖和內容視圖。</span><span class="sxs-lookup"><span data-stu-id="d42d6-147">To help clients process UI information more effectively, the framework supports alternative views of the automation tree: raw view, control view, and content view.</span></span> <span data-ttu-id="d42d6-148">如下表所示，篩選的類型會決定視圖，而用戶端會定義視圖的範圍。</span><span class="sxs-lookup"><span data-stu-id="d42d6-148">As the following table shows, the type of filtering determines the views, and the client defines the scope of a view.</span></span>



| <span data-ttu-id="d42d6-149">自動化樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d42d6-149">Automation Tree</span></span> | <span data-ttu-id="d42d6-150">Description</span><span class="sxs-lookup"><span data-stu-id="d42d6-150">Description</span></span>                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d42d6-151">未經處理的檢視</span><span class="sxs-lookup"><span data-stu-id="d42d6-151">Raw view</span></span>        | <span data-ttu-id="d42d6-152">桌面為其根目錄之 automation 元素物件的完整樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="d42d6-152">The full tree of automation element objects for which the desktop is the root.</span></span>                                          |
| <span data-ttu-id="d42d6-153">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="d42d6-153">Control view</span></span>    | <span data-ttu-id="d42d6-154">當使用者感覺到 UI 結構時，會緊密對應至該原始視圖的子集。</span><span class="sxs-lookup"><span data-stu-id="d42d6-154">A subset of the raw view that closely maps to the UI structure as the user perceives it.</span></span>                                |
| <span data-ttu-id="d42d6-155">內容檢視</span><span class="sxs-lookup"><span data-stu-id="d42d6-155">Content view</span></span>    | <span data-ttu-id="d42d6-156">控制項視圖的子集，其中包含與使用者最相關的內容，例如下拉式方塊中的值。</span><span class="sxs-lookup"><span data-stu-id="d42d6-156">A subset of the control view that contains content most relevant to the user, like the values in a drop-down combo box.</span></span> |



 

<span data-ttu-id="d42d6-157">如需詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d42d6-157">For more information, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

## <a name="ui-automation-properties"></a><span data-ttu-id="d42d6-158">消費者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="d42d6-158">UI Automation Properties</span></span>

<span data-ttu-id="d42d6-159">消費者介面自動化規格會定義兩種屬性： Automation 元素屬性和控制項模式屬性。</span><span class="sxs-lookup"><span data-stu-id="d42d6-159">The UI Automation Specification defines two kinds of properties: automation element properties and control pattern properties.</span></span> <span data-ttu-id="d42d6-160">Automation 元素屬性會套用至大部分的控制項，並提供專案的相關基本資訊，例如其名稱。</span><span class="sxs-lookup"><span data-stu-id="d42d6-160">Automation element properties apply to most controls, providing fundamental information about the element, such as its name.</span></span> <span data-ttu-id="d42d6-161">控制項模式屬性適用于下一節所述的控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d42d6-161">Control pattern properties apply to control patterns, which are described next.</span></span>

<span data-ttu-id="d42d6-162">不同于 Microsoft Active Accessibility，每個消費者介面自動化屬性都是由 GUID 和程式設計名稱所識別，讓新的屬性更容易引進。</span><span class="sxs-lookup"><span data-stu-id="d42d6-162">Unlike with Microsoft Active Accessibility, every UI Automation property is identified by a GUID and a programmatic name, which makes new properties easier to introduce.</span></span>

<span data-ttu-id="d42d6-163">如需詳細資訊，請參閱 [UI Automation Properties Overview](uiauto-propertiesoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d42d6-163">For more information, see [UI Automation Properties Overview](uiauto-propertiesoverview.md).</span></span>

## <a name="ui-automation-control-patterns"></a><span data-ttu-id="d42d6-164">UI 自動化控制項模式</span><span class="sxs-lookup"><span data-stu-id="d42d6-164">UI Automation Control Patterns</span></span>

<span data-ttu-id="d42d6-165">控制項模式描述 automation 元素功能的特定層面。</span><span class="sxs-lookup"><span data-stu-id="d42d6-165">A control pattern describes a particular aspect of the functionality of an automation element.</span></span> <span data-ttu-id="d42d6-166">例如，簡單的「可點擊式」控制項（例如按鈕或超連結）應該支援叫用控制項模式，以代表「按一下」動作。</span><span class="sxs-lookup"><span data-stu-id="d42d6-166">For example, a simple "click-able" control like a button or hyperlink should support the Invoke control pattern to represent the "click" action.</span></span>

<span data-ttu-id="d42d6-167">每個控制項模式都是可能的 UI 功能和函數的標準標記法。</span><span class="sxs-lookup"><span data-stu-id="d42d6-167">Each control pattern is a canonical representation of possible UI features and functions.</span></span> <span data-ttu-id="d42d6-168">消費者介面自動化的目前執行會定義22個控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d42d6-168">The current implementation of UI Automation defines 22 control patterns.</span></span> <span data-ttu-id="d42d6-169">Windows 自動化 API 也可以支援自訂控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d42d6-169">The Windows Automation API can also support custom control patterns.</span></span> <span data-ttu-id="d42d6-170">不同于 Microsoft Active Accessibility 角色或狀態屬性，一個 automation 元素可以支援多個消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d42d6-170">Unlike Microsoft Active Accessibility role or state properties, one automation element can support multiple UI Automation control patterns.</span></span>

<span data-ttu-id="d42d6-171">如需詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d42d6-171">For more information, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

## <a name="ui-automation-control-types"></a><span data-ttu-id="d42d6-172">UI 自動化控制項類型</span><span class="sxs-lookup"><span data-stu-id="d42d6-172">UI Automation Control Types</span></span>

<span data-ttu-id="d42d6-173">控制項類型是 automation 元素屬性，可指定專案所代表的知名控制項。</span><span class="sxs-lookup"><span data-stu-id="d42d6-173">A control type is an automation element property that specifies a well-known control that the element represents.</span></span> <span data-ttu-id="d42d6-174">目前，消費者介面自動化定義38控制項類型，包括按鈕、核取方塊、下拉式方塊、DataGrid、檔、超連結、影像、工具提示、樹狀結構和視窗。</span><span class="sxs-lookup"><span data-stu-id="d42d6-174">Currently, UI Automation defines thirty-eight control types, including Button, CheckBox, ComboBox, DataGrid, Document, Hyperlink, Image, ToolTip, Tree, and Window.</span></span>

<span data-ttu-id="d42d6-175">在您可以將控制項類型指派給專案之前，專案必須符合特定條件，包括特定的自動化樹狀結構、屬性值、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="d42d6-175">Before you can assign a control type to an element, the element needs to meet certain conditions, including a particular automation tree structure, property values, control patterns, and events.</span></span> <span data-ttu-id="d42d6-176">不過，您不一定要這樣做。</span><span class="sxs-lookup"><span data-stu-id="d42d6-176">However, you are not limited to these.</span></span> <span data-ttu-id="d42d6-177">您可以使用自訂模式和屬性，以及預先定義的屬性來擴充控制項。</span><span class="sxs-lookup"><span data-stu-id="d42d6-177">You can extend a control with custom patterns and properties, as well as with the predefined ones.</span></span>

<span data-ttu-id="d42d6-178">預先定義的控制項類型總數明顯低於 Microsoft Active Accessibility [物件角色](object-roles.md)，因為消費者介面自動化控制項類型可以合併以表示一組較大的功能，而 Microsoft Active Accessibility 的角色則無法使用。</span><span class="sxs-lookup"><span data-stu-id="d42d6-178">The total number of predefined control types is significantly lower than Microsoft Active Accessibility [object roles](object-roles.md), because UI Automation control types can be combined to express a larger set of features while Microsoft Active Accessibility roles cannot.</span></span>

<span data-ttu-id="d42d6-179">如需詳細資訊，請參閱 [UI Automation Control Types Overview](uiauto-controltypesoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d42d6-179">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

## <a name="ui-automation-events"></a><span data-ttu-id="d42d6-180">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="d42d6-180">UI Automation Events</span></span>

<span data-ttu-id="d42d6-181">消費者介面自動化事件會通知應用程式變更和自動化元素所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="d42d6-181">UI Automation events notify applications of changes to, and actions taken with automation elements.</span></span> <span data-ttu-id="d42d6-182">有四種不同類型的消費者介面自動化事件，而且不一定表示 UI 的視覺狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="d42d6-182">There are four different types of UI Automation events, and they do not necessarily mean that the visual state of the UI has changed.</span></span> <span data-ttu-id="d42d6-183">消費者介面自動化事件模型與 Windows 中的 [new-winevent](winevents-infrastructure.md) framework 無關，不過 WINDOWS Automation API 使消費者介面自動化事件與 Microsoft Active Accessibility framework 互通。</span><span class="sxs-lookup"><span data-stu-id="d42d6-183">The UI Automation event model is independent of the [WinEvent](winevents-infrastructure.md) framework in Windows, although the Windows Automation API makes UI Automation events interoperable with the Microsoft Active Accessibility framework.</span></span>

<span data-ttu-id="d42d6-184">如需詳細資訊，請參閱 [UI Automation Events Overview](uiauto-eventsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d42d6-184">For more information, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d42d6-185">相關主題</span><span class="sxs-lookup"><span data-stu-id="d42d6-185">Related topics</span></span>

<span data-ttu-id="d42d6-186">[消費者介面自動化規格](./uiauto-specandcommunitypromise.md)， [Windows Automation API 總覽](windows-automation-api-overview.md)</span><span class="sxs-lookup"><span data-stu-id="d42d6-186">[UI Automation Specification](./uiauto-specandcommunitypromise.md), [Windows Automation API Overview](windows-automation-api-overview.md)</span></span>