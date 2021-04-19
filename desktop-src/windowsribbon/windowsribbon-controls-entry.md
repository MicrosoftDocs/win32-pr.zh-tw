---
title: Windows 功能區架構控制項程式庫
description: 本節所包含的主題描述 Windows 功能區架構所包含的一組控制項。 此處所列的控制項是功能區中公開命令功能的 UI 物件。
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968919"
---
# <a name="windows-ribbon-framework-control-library"></a><span data-ttu-id="c12b4-104">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="c12b4-104">Windows Ribbon Framework Control Library</span></span>

<span data-ttu-id="c12b4-105">本節所包含的主題描述 Windows 功能區架構所包含的一組控制項。</span><span class="sxs-lookup"><span data-stu-id="c12b4-105">The topics contained in this section describe the set of controls that are included with the Windows Ribbon framework.</span></span> <span data-ttu-id="c12b4-106">此處所列的控制項是功能區中公開命令功能的 UI 物件。</span><span class="sxs-lookup"><span data-stu-id="c12b4-106">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span>

-   [<span data-ttu-id="c12b4-107">簡介</span><span class="sxs-lookup"><span data-stu-id="c12b4-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="c12b4-108">控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-108">The Controls</span></span>](#windows-ribbon-framework-control-library)
    -   [<span data-ttu-id="c12b4-109">基本控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-109">Basic Controls</span></span>](#basic-controls)
    -   [<span data-ttu-id="c12b4-110">容器控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-110">Container Controls</span></span>](#container-controls)
    -   [<span data-ttu-id="c12b4-111">專用控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-111">Specialized Controls</span></span>](#specialized-controls)
-   [<span data-ttu-id="c12b4-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="c12b4-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="c12b4-113">簡介</span><span class="sxs-lookup"><span data-stu-id="c12b4-113">Introduction</span></span>

<span data-ttu-id="c12b4-114">功能區架構是由索引標籤和[快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)[等元件](windowsribbon-controls-tab.md)所組成，這些元件會一起運作來提供豐富的 UI 體驗。</span><span class="sxs-lookup"><span data-stu-id="c12b4-114">The Ribbon framework is composed of components such as [Tabs](windowsribbon-controls-tab.md) and the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), that work together to deliver a rich UI experience.</span></span> <span data-ttu-id="c12b4-115">這些元件會個別公開不同類型的命令，讓客戶在功能區應用程式之間有組織、可預測的體驗。</span><span class="sxs-lookup"><span data-stu-id="c12b4-115">Individually, these components expose different types of Commands to give customers an organized, predictable experience across Ribbon applications.</span></span> <span data-ttu-id="c12b4-116">例如，每個索引標籤都會公開與在應用程式工作區中的特定內容部分建立和操作相關的命令，而 [ [應用程式] 功能表](windowsribbon-controls-applicationmenu.md) 則會公開與完整專案相關的功能，例如整個檔、圖片或影片。</span><span class="sxs-lookup"><span data-stu-id="c12b4-116">For example, each Tab exposes Commands related to creating and acting on specific parts of the content within the application workspace, whereas the [Application Menu](windowsribbon-controls-applicationmenu.md) exposes functionality related to a complete project, such as an entire document, picture, or movie.</span></span>

<span data-ttu-id="c12b4-117">本主題提供功能區控制項的完整清單，其中包含每個控制項的簡短描述，並提供更詳細檔的連結（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="c12b4-117">This topic provides a comprehensive list of Ribbon controls and includes a brief description for each control, with links to more detailed documentation where available.</span></span>

## <a name="the-controls"></a><span data-ttu-id="c12b4-118">控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-118">The Controls</span></span>

<span data-ttu-id="c12b4-119">功能區架構由兩個 [視圖](windowsribbon-reference-elements-view.md)組成： [**功能區**](windowsribbon-element-ribbon.md) 視圖和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 視圖。</span><span class="sxs-lookup"><span data-stu-id="c12b4-119">The Ribbon framework is composed of two [Views](windowsribbon-reference-elements-view.md): the [**Ribbon**](windowsribbon-element-ribbon.md) View and the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span> <span data-ttu-id="c12b4-120">每個視圖都可以裝載數個元件，作為架構所轉譯和管理之所有控制項的呈現容器。</span><span class="sxs-lookup"><span data-stu-id="c12b4-120">Each View can host several components that act as presentation containers for all controls that are rendered and managed by the framework.</span></span>

<span data-ttu-id="c12b4-121">當 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 裝載 [**CoNtextMenu**](windowsribbon-element-contextmenu.md)元素、[**浮動工具列**](windowsribbon-element-minitoolbar.md)元素或兩者時，[**功能區**](windowsribbon-element-ribbon.md)視圖會裝載 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)元素、 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)元素和功能區命令列。</span><span class="sxs-lookup"><span data-stu-id="c12b4-121">The [**Ribbon**](windowsribbon-element-ribbon.md) View hosts the [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element, [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) element, and ribbon command bar while the [**ContextPopup**](windowsribbon-element-contextpopup.md) View hosts a [**ContextMenu**](windowsribbon-element-contextmenu.md) element, a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element, or both.</span></span>

<span data-ttu-id="c12b4-122">每個 framework 控制項都是由與其 [**命令類型**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)相關聯的功能所區分。</span><span class="sxs-lookup"><span data-stu-id="c12b4-122">Each framework control is distinguished by the functionality associated with its [**Command type**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span></span>

### <a name="basic-controls"></a><span data-ttu-id="c12b4-123">基本控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-123">Basic Controls</span></span>

<span data-ttu-id="c12b4-124">基本控制項包含一或多個按鈕，只要按一下滑鼠，就能執行簡單的動作。</span><span class="sxs-lookup"><span data-stu-id="c12b4-124">Basic controls consist of one or more buttons that can be invoked by a single mouse click to perform a simple action.</span></span>

> [!Note]  
> <span data-ttu-id="c12b4-125">[**微調**](windowsribbon-element-spinner.md)項是包含編輯控制項的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c12b4-125">The [**Spinner**](windowsribbon-element-spinner.md) is an exception as it contains an edit control.</span></span>

 

<span data-ttu-id="c12b4-126">下表列出功能區架構中的基本控制項。</span><span class="sxs-lookup"><span data-stu-id="c12b4-126">The following table lists the basic controls in the Ribbon framework.</span></span>



| <span data-ttu-id="c12b4-127">控制</span><span class="sxs-lookup"><span data-stu-id="c12b4-127">Control</span></span>                                                  | <span data-ttu-id="c12b4-128">標記元素</span><span class="sxs-lookup"><span data-stu-id="c12b4-128">Markup Element</span></span>                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="c12b4-129">按鈕</span><span class="sxs-lookup"><span data-stu-id="c12b4-129">Button</span></span>](windowsribbon-controls-button.md)              | [<span data-ttu-id="c12b4-130">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="c12b4-130">**Button**</span></span>](windowsribbon-element-button.md)             |
| [<span data-ttu-id="c12b4-131">核取方塊</span><span class="sxs-lookup"><span data-stu-id="c12b4-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)         | [<span data-ttu-id="c12b4-132">**相應**</span><span class="sxs-lookup"><span data-stu-id="c12b4-132">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)         |
| [<span data-ttu-id="c12b4-133">說明按鈕</span><span class="sxs-lookup"><span data-stu-id="c12b4-133">Help Button</span></span>](windowsribbon-controls-helpbutton.md)     | [<span data-ttu-id="c12b4-134">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="c12b4-134">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)     |
| [<span data-ttu-id="c12b4-135">Spinner</span><span class="sxs-lookup"><span data-stu-id="c12b4-135">Spinner</span></span>](windowsribbon-controls-spinner.md)            | [<span data-ttu-id="c12b4-136">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="c12b4-136">**Spinner**</span></span>](windowsribbon-element-spinner.md)           |
| [<span data-ttu-id="c12b4-137">切換按鈕</span><span class="sxs-lookup"><span data-stu-id="c12b4-137">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md) | [<span data-ttu-id="c12b4-138">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="c12b4-138">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a><span data-ttu-id="c12b4-139">容器控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-139">Container Controls</span></span>

<span data-ttu-id="c12b4-140">容器控制項是由控制項群組、功能表、清單或專案和命令集合所組成。</span><span class="sxs-lookup"><span data-stu-id="c12b4-140">Container controls are composed of groups of controls, menus, lists, or item and Command collections.</span></span>

<span data-ttu-id="c12b4-141">架構會區分兩種類型的容器，也就是靜態和動態。</span><span class="sxs-lookup"><span data-stu-id="c12b4-141">The framework distinguishes between two types of containers, static and dynamic.</span></span>

### <a name="static-containers"></a><span data-ttu-id="c12b4-142">靜態容器</span><span class="sxs-lookup"><span data-stu-id="c12b4-142">Static Containers</span></span>

<span data-ttu-id="c12b4-143">在功能區標記檔案中，會宣告和擴展靜態容器，以及所有相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="c12b4-143">Static containers are declared and populated, along with all associated resources, in the Ribbon markup file.</span></span> <span data-ttu-id="c12b4-144">這些控制項無法在執行時間修改。</span><span class="sxs-lookup"><span data-stu-id="c12b4-144">These controls cannot be modified at run time.</span></span>

<span data-ttu-id="c12b4-145">靜態控制項的優點包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="c12b4-145">The advantages of static controls include the following:</span></span>

-   <span data-ttu-id="c12b4-146">快速建立原型。</span><span class="sxs-lookup"><span data-stu-id="c12b4-146">Rapid prototyping.</span></span> <span data-ttu-id="c12b4-147">靜態控制項可讓您快速建立功能區模擬，類似于最終的功能區設計，而不需要複雜的程式碼。</span><span class="sxs-lookup"><span data-stu-id="c12b4-147">Static controls make it possible to quickly build a Ribbon mock-up resembling a final Ribbon design that requires no complicated code.</span></span>
-   <span data-ttu-id="c12b4-148">輕鬆修改。</span><span class="sxs-lookup"><span data-stu-id="c12b4-148">Easy modifications.</span></span> <span data-ttu-id="c12b4-149">靜態控制項的大部分元素、屬性、資源和配置都可以在標記中修改。</span><span class="sxs-lookup"><span data-stu-id="c12b4-149">Most elements, attributes, resources, and layouts of static controls can be modified in markup.</span></span>
-   <span data-ttu-id="c12b4-150">一致的 UI。</span><span class="sxs-lookup"><span data-stu-id="c12b4-150">Consistent UI.</span></span> <span data-ttu-id="c12b4-151">設計完善的應用程式提供一致且穩定的 UI，可避免在執行時間變更功能表和清單。</span><span class="sxs-lookup"><span data-stu-id="c12b4-151">Well-designed applications provide a consistent and stable UI that avoids changes to menus and lists at run time.</span></span>

<span data-ttu-id="c12b4-152">下表描述功能區架構中的靜態容器控制項。</span><span class="sxs-lookup"><span data-stu-id="c12b4-152">The following table describes the static container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="c12b4-153">控制</span><span class="sxs-lookup"><span data-stu-id="c12b4-153">Control</span></span>                                                        | <span data-ttu-id="c12b4-154">標記元素</span><span class="sxs-lookup"><span data-stu-id="c12b4-154">Markup Element</span></span>                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="c12b4-155">應用程式功能表</span><span class="sxs-lookup"><span data-stu-id="c12b4-155">Application Menu</span></span>](windowsribbon-controls-applicationmenu.md) | [<span data-ttu-id="c12b4-156">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="c12b4-156">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md) |
| [<span data-ttu-id="c12b4-157">內容快顯視窗</span><span class="sxs-lookup"><span data-stu-id="c12b4-157">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)       | [<span data-ttu-id="c12b4-158">**CoNtextPopup**</span><span class="sxs-lookup"><span data-stu-id="c12b4-158">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)       |
| [<span data-ttu-id="c12b4-159">下拉式按鈕</span><span class="sxs-lookup"><span data-stu-id="c12b4-159">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)  | [<span data-ttu-id="c12b4-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="c12b4-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)   |
| [<span data-ttu-id="c12b4-161">群組</span><span class="sxs-lookup"><span data-stu-id="c12b4-161">Group</span></span>](windowsribbon-controls-group.md)                      | [<span data-ttu-id="c12b4-162">**Group**</span><span class="sxs-lookup"><span data-stu-id="c12b4-162">**Group**</span></span>](windowsribbon-element-group.md)                     |
| [<span data-ttu-id="c12b4-163">功能表群組</span><span class="sxs-lookup"><span data-stu-id="c12b4-163">Menu Group</span></span>](windowsribbon-controls-menugroup.md)             | [<span data-ttu-id="c12b4-164">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="c12b4-164">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)             |
| [<span data-ttu-id="c12b4-165">分割按鈕</span><span class="sxs-lookup"><span data-stu-id="c12b4-165">Split Button</span></span>](windowsribbon-controls-splitbutton.md)         | [<span data-ttu-id="c12b4-166">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="c12b4-166">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)         |
| [<span data-ttu-id="c12b4-167">Tab</span><span class="sxs-lookup"><span data-stu-id="c12b4-167">Tab</span></span>](windowsribbon-controls-tab.md)                          | [<span data-ttu-id="c12b4-168">**索引標籤**</span><span class="sxs-lookup"><span data-stu-id="c12b4-168">**Tab**</span></span>](windowsribbon-element-tab.md)                         |
| [<span data-ttu-id="c12b4-169">Tab 群組</span><span class="sxs-lookup"><span data-stu-id="c12b4-169">Tab Group</span></span>](windowsribbon-controls-tabgroup.md)               | [<span data-ttu-id="c12b4-170">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="c12b4-170">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a><span data-ttu-id="c12b4-171">動態容器</span><span class="sxs-lookup"><span data-stu-id="c12b4-171">Dynamic Containers</span></span>

<span data-ttu-id="c12b4-172">動態容器是在功能區標記檔案中宣告的。</span><span class="sxs-lookup"><span data-stu-id="c12b4-172">Dynamic containers are declared in the Ribbon markup file.</span></span> <span data-ttu-id="c12b4-173">它們會提供在執行時間建立或修改的一組專案或命令。</span><span class="sxs-lookup"><span data-stu-id="c12b4-173">They feature a group of items or Commands that are created or modified at run time.</span></span>

<span data-ttu-id="c12b4-174">動態容器的子類別（稱為資源庫）是由其 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 介面的實作為區別。</span><span class="sxs-lookup"><span data-stu-id="c12b4-174">A subclass of dynamic containers, called galleries, are distinguished by their implementation of the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="c12b4-175">這個介面可讓控制項將其專案或命令清單公開為集合，並支援以使用者互動和執行時間條件為基礎的更新。</span><span class="sxs-lookup"><span data-stu-id="c12b4-175">This interface allows a control to expose its item or Command list as a collection, and to support updates based on both user interaction and run-time conditions.</span></span> <span data-ttu-id="c12b4-176">如需詳細資訊，請參閱 [使用資源庫](ribbon-controls-galleries.md)。</span><span class="sxs-lookup"><span data-stu-id="c12b4-176">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="c12b4-177">下表列出功能區架構中的動態容器控制項。</span><span class="sxs-lookup"><span data-stu-id="c12b4-177">The following table lists the dynamic container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="c12b4-178">控制</span><span class="sxs-lookup"><span data-stu-id="c12b4-178">Control</span></span>                                                               | <span data-ttu-id="c12b4-179">標記元素</span><span class="sxs-lookup"><span data-stu-id="c12b4-179">Markup Element</span></span>                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="c12b4-180">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="c12b4-180">Combo Box</span></span>](windowsribbon-controls-combobox.md)                      | [<span data-ttu-id="c12b4-181">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="c12b4-181">**ComboBox**</span></span>](windowsribbon-element-combobox.md)                     |
| [<span data-ttu-id="c12b4-182">下拉式圖庫</span><span class="sxs-lookup"><span data-stu-id="c12b4-182">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)       | [<span data-ttu-id="c12b4-183">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="c12b4-183">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       |
| [<span data-ttu-id="c12b4-184">功能區中的資源庫</span><span class="sxs-lookup"><span data-stu-id="c12b4-184">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)       | [<span data-ttu-id="c12b4-185">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="c12b4-185">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       |
| [<span data-ttu-id="c12b4-186">快速存取工具列</span><span class="sxs-lookup"><span data-stu-id="c12b4-186">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md) | [<span data-ttu-id="c12b4-187">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="c12b4-187">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md) |
| [<span data-ttu-id="c12b4-188">最近的項目</span><span class="sxs-lookup"><span data-stu-id="c12b4-188">Recent Items</span></span>](windowsribbon-controls-recentitems.md)                | [<span data-ttu-id="c12b4-189">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="c12b4-189">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)               |
| [<span data-ttu-id="c12b4-190">分割按鈕資源庫</span><span class="sxs-lookup"><span data-stu-id="c12b4-190">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md) | [<span data-ttu-id="c12b4-191">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="c12b4-191">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a><span data-ttu-id="c12b4-192">專用控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-192">Specialized Controls</span></span>

<span data-ttu-id="c12b4-193">功能區架構包含一些特定 UI 功能的專用控制項。</span><span class="sxs-lookup"><span data-stu-id="c12b4-193">The Ribbon framework contains a number of specialized controls for specific UI functionality.</span></span>

<span data-ttu-id="c12b4-194">下表列出功能區架構中的特殊控制項。</span><span class="sxs-lookup"><span data-stu-id="c12b4-194">The following table lists the specialized controls in the Ribbon framework.</span></span>



| <span data-ttu-id="c12b4-195">控制</span><span class="sxs-lookup"><span data-stu-id="c12b4-195">Control</span></span>                                                                  | <span data-ttu-id="c12b4-196">標記元素</span><span class="sxs-lookup"><span data-stu-id="c12b4-196">Markup Element</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="c12b4-197">下拉式色彩選擇器</span><span class="sxs-lookup"><span data-stu-id="c12b4-197">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | [<span data-ttu-id="c12b4-198">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="c12b4-198">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md) |
| [<span data-ttu-id="c12b4-199">字型控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-199">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | [<span data-ttu-id="c12b4-200">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="c12b4-200">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="c12b4-201">相關主題</span><span class="sxs-lookup"><span data-stu-id="c12b4-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c12b4-202">瞭解命令和控制項</span><span class="sxs-lookup"><span data-stu-id="c12b4-202">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 