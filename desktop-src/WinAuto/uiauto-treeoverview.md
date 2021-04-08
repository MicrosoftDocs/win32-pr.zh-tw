---
title: UI 自動化樹狀目錄概觀
description: 輔助技術產品和測試腳本會流覽 Microsoft 消費者介面自動化樹狀結構，以收集 UI 和其元素的相關資訊。
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- 消費者介面自動化，樹狀結構總覽
- 消費者介面自動化，樹狀結構的視圖
- 消費者介面自動化，樹狀結構的原始視圖
- 消費者介面自動化，樹狀結構的控制視圖
- 消費者介面自動化，樹狀結構的內容視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76bc9aa6568a3f4d63194d35ff0c7d8f59510c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839823"
---
# <a name="ui-automation-tree-overview"></a><span data-ttu-id="5e826-108">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="5e826-108">UI Automation Tree Overview</span></span>

<span data-ttu-id="5e826-109">輔助技術產品和測試腳本會流覽 Microsoft 消費者介面自動化樹狀結構，以收集 UI 和其元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e826-109">Assistive technology products and test scripts navigate the Microsoft UI Automation tree to gather information about the UI and its elements.</span></span>

<span data-ttu-id="5e826-110">在消費者介面自動化樹狀結構中的根項目，代表 Windows 桌面視窗 ( "desktop" ) 以及其子項目代表應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="5e826-110">In the UI Automation tree is a root element that represents the Windows desktop window ("the desktop") and whose child elements represent application windows.</span></span> <span data-ttu-id="5e826-111">每個子專案都可以包含代表 UI 片段的元素，例如功能表、按鈕、工具列和清單方塊。</span><span class="sxs-lookup"><span data-stu-id="5e826-111">Each of these child elements can contain elements that represent pieces of the UI, such as menus, buttons, toolbars, and list boxes.</span></span> <span data-ttu-id="5e826-112">這些元素可以包含專案，例如清單專案。</span><span class="sxs-lookup"><span data-stu-id="5e826-112">These elements can contain elements, such as list items.</span></span>

<span data-ttu-id="5e826-113">消費者介面自動化樹狀結構不是固定的結構。</span><span class="sxs-lookup"><span data-stu-id="5e826-113">The UI Automation tree is not a fixed structure.</span></span> <span data-ttu-id="5e826-114">因為它可能包含數千個專案，所以很少會在 totality 中看到它。</span><span class="sxs-lookup"><span data-stu-id="5e826-114">It is seldom seen in its totality because it might contain thousands of elements.</span></span> <span data-ttu-id="5e826-115">消費者介面自動化樹狀結構的元件是以用戶端的需求建立，而樹狀結構的結構會隨著專案的加入、移動或移除而變更。</span><span class="sxs-lookup"><span data-stu-id="5e826-115">Parts of the UI Automation tree are built as a client needs them, and the structure of the tree changes as elements are added, moved, or removed.</span></span>

<span data-ttu-id="5e826-116">消費者介面自動化提供者會在片段中的專案之間執行導覽，以支援消費者介面自動化樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="5e826-116">UI Automation providers support the UI Automation tree by implementing navigation among items in a fragment.</span></span> <span data-ttu-id="5e826-117">片段是特定架構中專案的完整子樹，並且具有根項目 (稱為通常裝載在視窗中的 *片段根*) 。</span><span class="sxs-lookup"><span data-stu-id="5e826-117">A fragment is a complete subtree of elements from a particular framework, and has a root element (called the *fragment root*) that is typically hosted in a window.</span></span>

<span data-ttu-id="5e826-118">提供者不在意從某個控制項流覽至另一個控制項。</span><span class="sxs-lookup"><span data-stu-id="5e826-118">Providers are not concerned with navigation from one control to another.</span></span> <span data-ttu-id="5e826-119">這是由消費者介面自動化 core 管理，其使用預設視窗提供者的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e826-119">This is managed by the UI Automation core, which uses information from the default window providers.</span></span>

<span data-ttu-id="5e826-120">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="5e826-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5e826-121">消費者介面自動化樹狀結構的視圖</span><span class="sxs-lookup"><span data-stu-id="5e826-121">Views of the UI Automation Tree</span></span>](#views-of-the-ui-automation-tree)
    -   [<span data-ttu-id="5e826-122">原始視圖</span><span class="sxs-lookup"><span data-stu-id="5e826-122">Raw View</span></span>](#raw-view)
    -   [<span data-ttu-id="5e826-123">控制項視圖</span><span class="sxs-lookup"><span data-stu-id="5e826-123">Control View</span></span>](#control-view)
    -   [<span data-ttu-id="5e826-124">內容視圖</span><span class="sxs-lookup"><span data-stu-id="5e826-124">Content View</span></span>](#content-view)
-   [<span data-ttu-id="5e826-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e826-125">Related topics</span></span>](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a><span data-ttu-id="5e826-126">消費者介面自動化樹狀結構的視圖</span><span class="sxs-lookup"><span data-stu-id="5e826-126">Views of the UI Automation Tree</span></span>

<span data-ttu-id="5e826-127">您可以篩選消費者介面自動化樹狀結構，以建立僅包含與特定用戶端相關之消費者介面自動化元素的視圖。</span><span class="sxs-lookup"><span data-stu-id="5e826-127">The UI Automation tree can be filtered to create views that contain only those UI Automation elements that are relevant for a particular client.</span></span> <span data-ttu-id="5e826-128">這種方法可讓用戶端自訂透過消費者介面自動化呈現的結構，以滿足其特定需求。</span><span class="sxs-lookup"><span data-stu-id="5e826-128">This approach allows clients to customize the structure that is presented through UI Automation to their particular needs.</span></span>

<span data-ttu-id="5e826-129">用戶端可以藉由設定範圍和篩選來自訂此視圖。</span><span class="sxs-lookup"><span data-stu-id="5e826-129">The client can customize the view by scoping and by filtering.</span></span> <span data-ttu-id="5e826-130">範圍是定義視圖的範圍，從基底元素開始。</span><span class="sxs-lookup"><span data-stu-id="5e826-130">Scoping is defining the extent of the view, starting from a base element.</span></span> <span data-ttu-id="5e826-131">例如，應用程式可能只想要尋找桌面的直接子系，或應用程式視窗的所有下階。</span><span class="sxs-lookup"><span data-stu-id="5e826-131">For example, the application might want to find only direct children of the desktop, or all descendants of an application window.</span></span> <span data-ttu-id="5e826-132">篩選會定義包含在此視圖中的專案類型。</span><span class="sxs-lookup"><span data-stu-id="5e826-132">Filtering is defining the types of elements that are included in the view.</span></span>

<span data-ttu-id="5e826-133">消費者介面自動化提供者藉由定義專案的屬性（包括 [**IUIAutomationElement：： IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 和 [**IUIAutomationElement：： IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) 屬性）來支援篩選。</span><span class="sxs-lookup"><span data-stu-id="5e826-133">UI Automation providers support filtering by defining properties on elements, including the [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) and [**IUIAutomationElement::IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) properties.</span></span>

<span data-ttu-id="5e826-134">消費者介面自動化提供三個預設視圖：原始視圖、控制項視圖和內容視圖。</span><span class="sxs-lookup"><span data-stu-id="5e826-134">UI Automation provides three default views: raw view, control view, and content view.</span></span> <span data-ttu-id="5e826-135">這些視圖是由執行的篩選類型所定義。</span><span class="sxs-lookup"><span data-stu-id="5e826-135">These views are defined by the type of filtering performed.</span></span> <span data-ttu-id="5e826-136">任何視圖的範圍是由應用程式所定義。</span><span class="sxs-lookup"><span data-stu-id="5e826-136">The scope of any view is defined by the application.</span></span> <span data-ttu-id="5e826-137">應用程式可以對屬性套用其他篩選;例如，只在控制項視圖中包含已啟用的控制項。</span><span class="sxs-lookup"><span data-stu-id="5e826-137">The application can apply other filters on properties; for example, to include only enabled controls in a control view.</span></span>

### <a name="raw-view"></a><span data-ttu-id="5e826-138">未經處理的檢視</span><span class="sxs-lookup"><span data-stu-id="5e826-138">Raw View</span></span>

<span data-ttu-id="5e826-139">消費者介面自動化樹狀結構的原始視圖是桌面為其根目錄之 Automation 元素的完整樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="5e826-139">The raw view of the UI Automation tree is the full tree of automation elements for which the desktop is the root.</span></span> <span data-ttu-id="5e826-140">原始視圖會緊密遵循應用程式的原生程式設計結構，而且是最詳細的可用視圖。</span><span class="sxs-lookup"><span data-stu-id="5e826-140">The raw view closely follows the native programmatic structure of an application, and is the most detailed view available.</span></span> <span data-ttu-id="5e826-141">它也是樹狀結構其他檢視的建置基底。</span><span class="sxs-lookup"><span data-stu-id="5e826-141">It is also the base on which the other views of the tree are built.</span></span> <span data-ttu-id="5e826-142">因為這個視圖相依于基礎 UI 架構，所以 Windows Presentation Foundation 的原始視圖 (WPF) 按鈕與 Microsoft Win32 按鈕的原始觀點不同。</span><span class="sxs-lookup"><span data-stu-id="5e826-142">Because this view depends on the underlying UI framework, the raw view of a Windows Presentation Foundation (WPF) button has a different raw view than a Microsoft Win32 button.</span></span>

<span data-ttu-id="5e826-143">原始視圖的取得方式是藉由搜尋元素而不指定屬性，或使用 [**IUIAutomation：： RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) 來取得 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 介面來導覽樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="5e826-143">The raw view is obtained by searching for elements without specifying properties or by using the [**IUIAutomation::RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) to get an [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) interface for navigating the tree.</span></span>

### <a name="control-view"></a><span data-ttu-id="5e826-144">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="5e826-144">Control View</span></span>

<span data-ttu-id="5e826-145">控制項檢視是未經處理檢視的子集。</span><span class="sxs-lookup"><span data-stu-id="5e826-145">The control view is a subset of the raw view.</span></span> <span data-ttu-id="5e826-146">它只包含將 [**IUIAutomationElement：： IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 屬性設定為 **TRUE** 的 UI 專案。</span><span class="sxs-lookup"><span data-stu-id="5e826-146">It includes only those UI items that have the [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) property set to **TRUE**.</span></span>

<span data-ttu-id="5e826-147">此控制視圖包含可提供資訊給使用者，或讓使用者執行動作的 UI 專案。</span><span class="sxs-lookup"><span data-stu-id="5e826-147">The control view includes the UI items that provide information to the user or enable the user to perform an action.</span></span> <span data-ttu-id="5e826-148">這些是自動化測試應用程式最感興趣的 UI 專案。</span><span class="sxs-lookup"><span data-stu-id="5e826-148">These are the UI items that are most interesting to automated testing applications.</span></span>

<span data-ttu-id="5e826-149">此控制視圖也包含對 UI 邏輯結構造成影響的非互動式 UI 專案。</span><span class="sxs-lookup"><span data-stu-id="5e826-149">The control view also includes noninteractive UI items that contribute to the logical structure of the UI.</span></span> <span data-ttu-id="5e826-150">這些包括專案容器，例如清單視圖標頭、工具列、功能表和狀態列。</span><span class="sxs-lookup"><span data-stu-id="5e826-150">These include item containers such as list view headers, toolbars, menus, and the status bar.</span></span> <span data-ttu-id="5e826-151">顯示在 [控制台] 中的其他非互動式專案是在對話方塊中具有資訊和靜態文字的圖形。</span><span class="sxs-lookup"><span data-stu-id="5e826-151">Other noninteractive items that appear in the control view are graphics with information and static text in a dialog box.</span></span>

<span data-ttu-id="5e826-152">非互動式專案只用于版面配置或裝飾用途，例如用來在對話方塊中配置控制項的面板，不會出現在控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="5e826-152">Noninteractive items used only for layout or decorative purposes, such as panels used to lay out controls in a dialog box, do not appear in the control view.</span></span>

<span data-ttu-id="5e826-153">消費者介面自動化樹狀結構的控制項視圖會緊密對應至使用者所察覺的 UI 結構。</span><span class="sxs-lookup"><span data-stu-id="5e826-153">The control view of the UI Automation tree closely maps to the UI structure perceived by an end user.</span></span> <span data-ttu-id="5e826-154">這可讓輔助技術產品更輕鬆地描述使用者的 UI，並協助使用者與應用程式互動。</span><span class="sxs-lookup"><span data-stu-id="5e826-154">This makes it easier for the assistive technology product to describe the UI to the end user and help that end user interact with the application.</span></span>

<span data-ttu-id="5e826-155">您可以藉由搜尋將 [**IUIAutomationElement：： IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 屬性設定為 true 的專案，或使用 [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) 來取得用於流覽樹狀結構的 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 介面，來取得控制項視圖。</span><span class="sxs-lookup"><span data-stu-id="5e826-155">The control view is obtained by searching for elements that have the [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) property set to true, or by using [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) to get an [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) interface for navigating the tree.</span></span>

### <a name="content-view"></a><span data-ttu-id="5e826-156">內容檢視</span><span class="sxs-lookup"><span data-stu-id="5e826-156">Content View</span></span>

<span data-ttu-id="5e826-157">消費者介面自動化樹狀結構的內容視圖是控制視圖的子集。</span><span class="sxs-lookup"><span data-stu-id="5e826-157">The content view of the UI Automation tree is a subset of the control view.</span></span> <span data-ttu-id="5e826-158">它僅包含同時具有 [**IUIAutomationElement：： IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 和 [**IUIAutomationElement：： IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) 屬性設定為 **TRUE** 的 UI 專案。</span><span class="sxs-lookup"><span data-stu-id="5e826-158">It includes only those UI items that have both the [**IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) and the [**IUIAutomationElement::IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) property set to **TRUE**.</span></span>

<span data-ttu-id="5e826-159">內容視圖包含可在使用者介面中傳達實際資訊的 UI 專案，包括可以接收鍵盤焦點的 UI 專案，以及在 UI 專案上不是標籤的一些文字。</span><span class="sxs-lookup"><span data-stu-id="5e826-159">The content view contains UI items that convey the actual information in a user interface, including UI items that can receive keyboard focus and some text that is not a label on a UI item.</span></span> <span data-ttu-id="5e826-160">這些是螢幕讀取器應用程式最感興趣的 UI 專案。</span><span class="sxs-lookup"><span data-stu-id="5e826-160">These are the UI items that are most interesting to a screen reader application.</span></span> <span data-ttu-id="5e826-161">例如，下拉式方塊中的值會出現在內容視圖中，因為這些值代表終端使用者所使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e826-161">For example, the values in a drop-down combo box appear in the content view because the values represent information being used by an end user.</span></span>

<span data-ttu-id="5e826-162">在內容視圖中，下拉式方塊和清單方塊都會表示為 UI 專案的集合，其中可以選取一個或多個專案。</span><span class="sxs-lookup"><span data-stu-id="5e826-162">In the content view, a combo box and a list box are both represented as a collection of UI items where one, or more than one, item can be selected.</span></span> <span data-ttu-id="5e826-163">其中一個專案一律會開啟，而且一個專案可以展開和折迭在內容視圖中是不相關的，因為它是設計用來顯示呈現給使用者的資料或內容。</span><span class="sxs-lookup"><span data-stu-id="5e826-163">The fact that one item is always open and one item can expand and collapse is irrelevant in the content view because it is designed to show the data, or content, that is being presented to the user.</span></span>

<span data-ttu-id="5e826-164">您可以藉由搜尋將 [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 和 [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) 屬性設定為 **TRUE** 的專案，或使用 [**IUIAutomation：： ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) 取得可流覽樹狀結構的 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 介面，來取得內容視圖。</span><span class="sxs-lookup"><span data-stu-id="5e826-164">The content view is obtained by searching for elements that have both the [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) and the [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) property set to **TRUE**, or by using [**IUIAutomation::ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) to get an [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) interface for navigating the tree.</span></span>

<span data-ttu-id="5e826-165">下列影像顯示控制項視圖和內容視圖之間的差異。</span><span class="sxs-lookup"><span data-stu-id="5e826-165">The following images show the differences between the control view and content view.</span></span> <span data-ttu-id="5e826-166">第一個影像顯示下拉式清單中有三個專案的簡單下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="5e826-166">The first image shows a simple combo box with three items in the dropdown list.</span></span> <span data-ttu-id="5e826-167">第二個影像顯示下拉式列示方塊 UI 專案如何出現在 UISpy.exe 應用程式的控制項和內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="5e826-167">The second image shows how the combo box UI items appear in the control and content views of the UISpy.exe application.</span></span>

![包含三個下拉式專案的簡單下拉式方塊的螢幕擷取畫面](images/combobox.png)

![uispy.exe 應用程式的螢幕擷取畫面，其中包含下拉式方塊專案的控制項和內容視圖](images/treeviews.jpg)

## <a name="related-topics"></a><span data-ttu-id="5e826-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e826-170">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5e826-171">**概念**</span><span class="sxs-lookup"><span data-stu-id="5e826-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5e826-172">建立 CUIAutomation 物件</span><span class="sxs-lookup"><span data-stu-id="5e826-172">Creating the CUIAutomation Object</span></span>](uiauto-creatingcuiautomation.md)
</dt> <dt>

[<span data-ttu-id="5e826-173">取得 UI 自動化項目</span><span class="sxs-lookup"><span data-stu-id="5e826-173">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="5e826-174">UI 自動化基礎</span><span class="sxs-lookup"><span data-stu-id="5e826-174">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 




