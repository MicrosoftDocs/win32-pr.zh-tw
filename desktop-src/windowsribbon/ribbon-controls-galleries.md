---
title: 使用資源庫
description: Windows 功能區架構為開發人員提供健全且一致的模型，以管理各種集合型控制項的動態內容。
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows 功能區，資源庫
- 功能區，資源庫
- Windows 功能區，DropDownGallery 控制項
- 功能區，DropDownGallery 控制項
- Windows 功能區，SplitButtonGallery 控制項
- 功能區，SplitButtonGallery 控制項
- DropDownGallery 控制項
- SplitButtonGallery 控制項
- Windows 功能區的資源庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682840"
---
# <a name="working-with-galleries"></a><span data-ttu-id="b74a1-112">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="b74a1-112">Working with Galleries</span></span>

<span data-ttu-id="b74a1-113">Windows 功能區架構為開發人員提供健全且一致的模型，以管理各種集合型控制項的動態內容。</span><span class="sxs-lookup"><span data-stu-id="b74a1-113">The Windows Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="b74a1-114">藉由調整並重新設定功能區 UI，這些動態控制項可讓架構在主應用程式和功能區本身中回應使用者互動，並提供彈性來處理各種執行時間環境。</span><span class="sxs-lookup"><span data-stu-id="b74a1-114">By adapting and reconfiguring the Ribbon UI, these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

-   [<span data-ttu-id="b74a1-115">簡介</span><span class="sxs-lookup"><span data-stu-id="b74a1-115">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b74a1-116">畫廊</span><span class="sxs-lookup"><span data-stu-id="b74a1-116">Galleries</span></span>](#working-with-galleries)
    -   [<span data-ttu-id="b74a1-117">專案資源庫</span><span class="sxs-lookup"><span data-stu-id="b74a1-117">Item Galleries</span></span>](#item-galleries)
    -   [<span data-ttu-id="b74a1-118">命令資源庫</span><span class="sxs-lookup"><span data-stu-id="b74a1-118">Command Galleries</span></span>](#command-galleries)
    -   [<span data-ttu-id="b74a1-119">圖庫控制項</span><span class="sxs-lookup"><span data-stu-id="b74a1-119">Gallery Controls</span></span>](#working-with-galleries)
-   [<span data-ttu-id="b74a1-120">如何執行資源庫</span><span class="sxs-lookup"><span data-stu-id="b74a1-120">How to Implement a Gallery</span></span>](#how-to-implement-a-gallery)
    -   [<span data-ttu-id="b74a1-121">基本元件</span><span class="sxs-lookup"><span data-stu-id="b74a1-121">The Basic Components</span></span>](#the-basic-components)
    -   [<span data-ttu-id="b74a1-122">在標記中宣告控制項</span><span class="sxs-lookup"><span data-stu-id="b74a1-122">Declare the Controls in Markup</span></span>](#declare-the-controls-in-markup)
    -   [<span data-ttu-id="b74a1-123">建立命令處理常式</span><span class="sxs-lookup"><span data-stu-id="b74a1-123">Create a Command Handler</span></span>](#create-a-command-handler)
    -   [<span data-ttu-id="b74a1-124">系結命令處理常式</span><span class="sxs-lookup"><span data-stu-id="b74a1-124">Bind the Command Handler</span></span>](#bind-the-command-handler)
    -   [<span data-ttu-id="b74a1-125">初始化集合</span><span class="sxs-lookup"><span data-stu-id="b74a1-125">Initialize a Collection</span></span>](#initialize-a-collection)
    -   [<span data-ttu-id="b74a1-126">處理收集事件</span><span class="sxs-lookup"><span data-stu-id="b74a1-126">Handle Collection Events</span></span>](#handle-collection-events)
-   [<span data-ttu-id="b74a1-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="b74a1-127">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="b74a1-128">簡介</span><span class="sxs-lookup"><span data-stu-id="b74a1-128">Introduction</span></span>

<span data-ttu-id="b74a1-129">功能區架構可動態適應執行時間條件、應用程式需求和使用者輸入的這項功能，強調架構的豐富 UI 功能，並為開發人員提供彈性來滿足廣泛的客戶需求。</span><span class="sxs-lookup"><span data-stu-id="b74a1-129">This ability of the Ribbon framework to dynamically adapt to run-time conditions, application requirements, and end-user input highlights the rich UI capabilities of the framework, and provides developers with the flexibility to cater to a broad range of customer needs.</span></span>

<span data-ttu-id="b74a1-130">本指南的重點在於描述架構所支援的動態資源庫控制項、說明其差異、討論其最適合的使用時間和位置，並示範如何將這些控制項併入功能區應用程式。</span><span class="sxs-lookup"><span data-stu-id="b74a1-130">The focus of this guide is to describe the dynamic gallery controls supported by the framework, explain their differences, discuss when and where they may best be used, and demonstrate how they can be incorporated into a Ribbon application.</span></span>

## <a name="galleries"></a><span data-ttu-id="b74a1-131">資源庫</span><span class="sxs-lookup"><span data-stu-id="b74a1-131">Galleries</span></span>

<span data-ttu-id="b74a1-132">資源庫是功能強大的清單方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="b74a1-132">Galleries are functionally and graphically rich list box controls.</span></span> <span data-ttu-id="b74a1-133">資源庫的專案集合可以依分類來組織，這些類別會顯示在彈性資料行和資料列型配置中（以影像和文字表示），並視資源庫類型而定，支援即時預覽。</span><span class="sxs-lookup"><span data-stu-id="b74a1-133">The item collection of a gallery can be organized by categories, displayed in flexible column and row-based layouts, represented with images and text, and depending on the type of gallery, support live previewing.</span></span>

<span data-ttu-id="b74a1-134">資源庫與其他動態功能區控制項的功能不同，原因如下：</span><span class="sxs-lookup"><span data-stu-id="b74a1-134">Galleries are functionally distinct from other dynamic Ribbon controls for the following reasons:</span></span>

-   <span data-ttu-id="b74a1-135">資源庫會執行 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 介面，以定義各種操作主機庫專案集合的方法。</span><span class="sxs-lookup"><span data-stu-id="b74a1-135">Galleries implement the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface that defines the various methods for manipulating gallery item collections.</span></span>
-   <span data-ttu-id="b74a1-136">您可以在執行時間根據直接出現在功能區中的活動更新資源庫，例如，當使用者將命令新增至快速存取工具列時 (QAT) 。</span><span class="sxs-lookup"><span data-stu-id="b74a1-136">Galleries can be updated at run time, based on activity that occurs directly in the Ribbon, such as when a user adds a Command to the Quick Access Toolbar (QAT).</span></span>
-   <span data-ttu-id="b74a1-137">您可以在執行時間根據在執行時間環境中間接發生的活動來更新資源庫，例如，當印表機驅動程式僅支援直向頁面配置時。</span><span class="sxs-lookup"><span data-stu-id="b74a1-137">Galleries can be updated at run time, based on activity that occurs indirectly from the run-time environment, such as when a printer driver supports portrait page layouts only.</span></span>
-   <span data-ttu-id="b74a1-138">您可以在執行時間根據在主應用程式中間接發生的活動（例如，當使用者在檔中選取專案時）來更新資源庫。</span><span class="sxs-lookup"><span data-stu-id="b74a1-138">Galleries can be updated at run time, based on activity that occurs indirectly in the host application, such as when a user selects an item in a document.</span></span>

<span data-ttu-id="b74a1-139">功能區架構會公開兩種類型的資源庫：專案資源庫和命令資源庫。</span><span class="sxs-lookup"><span data-stu-id="b74a1-139">The Ribbon framework exposes two types of galleries: item galleries and Command galleries.</span></span>

### <a name="item-galleries"></a><span data-ttu-id="b74a1-140">專案資源庫</span><span class="sxs-lookup"><span data-stu-id="b74a1-140">Item Galleries</span></span>

<span data-ttu-id="b74a1-141">專案圖庫包含以索引為基礎的相關專案集合，其中每個專案都以影像、字串或兩者表示。</span><span class="sxs-lookup"><span data-stu-id="b74a1-141">Item galleries contain an index-based collection of related items where each item is represented by an image, a string, or both.</span></span> <span data-ttu-id="b74a1-142">控制項系結至單一命令處理常式，該處理常式依賴 [UI \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) 屬性所識別的索引值。</span><span class="sxs-lookup"><span data-stu-id="b74a1-142">The control is bound to a single Command handler that relies on the index value that is identified by the [UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) property.</span></span>

<span data-ttu-id="b74a1-143">專案圖庫支援即時預覽，這表示會根據滑鼠停駐或焦點顯示命令結果，而不需要認可或實際叫用命令。</span><span class="sxs-lookup"><span data-stu-id="b74a1-143">Item galleries support live previewing, which means displaying a Command result, based on mouseover or focus, without committing to or actually invoking the Command.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b74a1-144">此架構不支援在 [應用程式] 功能表中裝載專案資源庫。</span><span class="sxs-lookup"><span data-stu-id="b74a1-144">The framework does not support hosting item galleries in the Application Menu.</span></span>

 

### <a name="command-galleries"></a><span data-ttu-id="b74a1-145">命令資源庫</span><span class="sxs-lookup"><span data-stu-id="b74a1-145">Command Galleries</span></span>

<span data-ttu-id="b74a1-146">命令資源庫包含相異、非索引項目目的集合。</span><span class="sxs-lookup"><span data-stu-id="b74a1-146">Command galleries contain a collection of distinct, non-indexed items.</span></span> <span data-ttu-id="b74a1-147">每個專案都是以透過命令識別碼系結至命令處理常式的單一控制項來表示。</span><span class="sxs-lookup"><span data-stu-id="b74a1-147">Each item is represented by a single control bound to a Command handler through a Command ID.</span></span> <span data-ttu-id="b74a1-148">就像獨立控制項一樣，命令資源庫中的每個專案都會將輸入事件路由傳送至相關聯的命令處理常式，而命令資源庫本身不會接聽事件。</span><span class="sxs-lookup"><span data-stu-id="b74a1-148">Like standalone controls, each item in a Command gallery routes input events to an associated Command handler—the Command gallery itself does not listen for events.</span></span>

<span data-ttu-id="b74a1-149">命令資源庫不支援即時預覽。</span><span class="sxs-lookup"><span data-stu-id="b74a1-149">Command galleries do not support live previewing.</span></span>

### <a name="gallery-controls"></a><span data-ttu-id="b74a1-150">圖庫控制項</span><span class="sxs-lookup"><span data-stu-id="b74a1-150">Gallery Controls</span></span>

<span data-ttu-id="b74a1-151">功能區架構中有四個資源庫控制項： [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)、 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)和 [**ComboBox**](windowsribbon-element-combobox.md)。</span><span class="sxs-lookup"><span data-stu-id="b74a1-151">There are four gallery controls in the Ribbon framework: the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), and the [**ComboBox**](windowsribbon-element-combobox.md).</span></span> <span data-ttu-id="b74a1-152">**ComboBox** 以外的所有專案都可以實作為專案資源庫或命令資源庫。</span><span class="sxs-lookup"><span data-stu-id="b74a1-152">All except the **ComboBox** can be implemented as either an item gallery or a Command gallery.</span></span>

### <a name="dropdowngallery"></a><span data-ttu-id="b74a1-153">DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="b74a1-153">DropDownGallery</span></span>

<span data-ttu-id="b74a1-154">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)是一個按鈕，顯示包含互斥專案或命令集合的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="b74a1-154">A [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) is a button that displays a drop-down list that contains a collection of mutually exclusive items or Commands.</span></span>

<span data-ttu-id="b74a1-155">下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中的功能區 [下拉式圖庫](windowsribbon-controls-dropdowngallery.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="b74a1-155">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![適用于 windows 7 的 microsoft 油漆中，下拉式圖庫控制項的螢幕擷取畫面。](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a><span data-ttu-id="b74a1-157">SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="b74a1-157">SplitButtonGallery</span></span>

<span data-ttu-id="b74a1-158">[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)是複合控制項，會在主要按鈕上從其集合公開單一預設專案或命令，並在按一下次要按鈕時顯示的互斥下拉式清單中顯示其他專案或命令。</span><span class="sxs-lookup"><span data-stu-id="b74a1-158">A [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) is a composite control that exposes a single default item or Command from its collection on a primary button, and displays other items or commands in a mutually exclusive drop-down list that is displayed when a secondary button is clicked.</span></span>

<span data-ttu-id="b74a1-159">下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中的功能區 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="b74a1-159">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![適用于 windows 7 的 microsoft 油漆中分割按鈕圖庫控制項的螢幕擷取畫面。](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a><span data-ttu-id="b74a1-161">InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="b74a1-161">InRibbonGallery</span></span>

<span data-ttu-id="b74a1-162">[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)是一個資源庫，可在功能區中顯示相關專案或命令的集合。</span><span class="sxs-lookup"><span data-stu-id="b74a1-162">An [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is a gallery that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="b74a1-163">如果資源庫中有太多專案，則會提供展開箭號，以在展開的窗格中顯示集合的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="b74a1-163">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

<span data-ttu-id="b74a1-164">下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中功能區元件 [庫](windowsribbon-controls-inribbongallery.md) 控制項的功能區。</span><span class="sxs-lookup"><span data-stu-id="b74a1-164">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![microsoft 油漆功能區中功能區資源庫控制項的螢幕擷取畫面。](images/controls/inribbongallery.png)

### <a name="combobox"></a><span data-ttu-id="b74a1-166">ComboBox</span><span class="sxs-lookup"><span data-stu-id="b74a1-166">ComboBox</span></span>

<span data-ttu-id="b74a1-167">[**ComboBox**](windowsribbon-element-combobox.md)是單一資料行清單方塊，其中包含具有靜態控制項或編輯控制項和下拉式箭號的專案集合。</span><span class="sxs-lookup"><span data-stu-id="b74a1-167">A [**ComboBox**](windowsribbon-element-combobox.md) is a single-column list box that contains a collection of items with either a static control or edit control and dropdown arrow.</span></span> <span data-ttu-id="b74a1-168">當使用者按一下下拉式箭號時，就會顯示控制項的清單方塊部分。</span><span class="sxs-lookup"><span data-stu-id="b74a1-168">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

<span data-ttu-id="b74a1-169">下列螢幕擷取畫面說明 Windows Live Movie Maker 的功能區 [下拉式列示方塊](windowsribbon-controls-combobox.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="b74a1-169">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![microsoft 油漆功能區中 combobox 控制項的螢幕擷取畫面。](images/controls/combobox.png)

<span data-ttu-id="b74a1-171">因為 [**ComboBox**](windowsribbon-element-combobox.md) 只是一個專案資源庫，所以不支援命令專案。</span><span class="sxs-lookup"><span data-stu-id="b74a1-171">Because the [**ComboBox**](windowsribbon-element-combobox.md) is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="b74a1-172">它也是唯一不支援命令空間的資源庫控制項。</span><span class="sxs-lookup"><span data-stu-id="b74a1-172">It is also the only gallery control that does not support a Command Space.</span></span> <span data-ttu-id="b74a1-173"> (命令空間是在標記中宣告的命令集合，並列在專案庫或命令資源庫底部。 ) </span><span class="sxs-lookup"><span data-stu-id="b74a1-173">(A Command Space is a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery.)</span></span>

<span data-ttu-id="b74a1-174">下列程式碼範例顯示在 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)中宣告三個按鈕命令空間所需的標記。</span><span class="sxs-lookup"><span data-stu-id="b74a1-174">The following code example shows the markup required to declare a three-button Command Space in a [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



<span data-ttu-id="b74a1-175">下列螢幕擷取畫面說明上述程式碼範例的三個按鈕命令空間。</span><span class="sxs-lookup"><span data-stu-id="b74a1-175">The following screen shot illustrates the three-button Command Space of the preceding code example.</span></span>

![dropdowngallery 中三個按鈕命令空間的螢幕擷取畫面。](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a><span data-ttu-id="b74a1-177">如何執行資源庫</span><span class="sxs-lookup"><span data-stu-id="b74a1-177">How to Implement a Gallery</span></span>

<span data-ttu-id="b74a1-178">本節將討論功能區元件庫的執行詳細資料，並逐步解說如何將它們併入功能區應用程式中。</span><span class="sxs-lookup"><span data-stu-id="b74a1-178">This section discusses the implementation details of Ribbon galleries and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="the-basic-components"></a><span data-ttu-id="b74a1-179">基本元件</span><span class="sxs-lookup"><span data-stu-id="b74a1-179">The Basic Components</span></span>

<span data-ttu-id="b74a1-180">本節說明在功能區架構中形成動態內容骨幹的一組屬性和方法，並支援在執行時間新增、刪除、更新和操作功能區圖庫的內容和視覺化配置。</span><span class="sxs-lookup"><span data-stu-id="b74a1-180">This section describes the set of properties and methods that form the backbone of dynamic content in the Ribbon framework and support adding, deleting, updating, and otherwise manipulating the content and visual layout of Ribbon galleries at run time.</span></span>

### <a name="iuicollection"></a><span data-ttu-id="b74a1-181">IUICollection</span><span class="sxs-lookup"><span data-stu-id="b74a1-181">IUICollection</span></span>

<span data-ttu-id="b74a1-182">資源庫需要一組基本的方法來存取和操作其集合中的個別專案。</span><span class="sxs-lookup"><span data-stu-id="b74a1-182">Galleries require a basic set of methods to access and manipulate the individual items in their collections.</span></span>

<span data-ttu-id="b74a1-183">[IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown)介面會定義這些方法，而架構會以 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)介面中所定義的其他方法來補充其功能。</span><span class="sxs-lookup"><span data-stu-id="b74a1-183">The [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) interface defines these methods, and the framework supplements their functionality with additional methods that are defined in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="b74a1-184">**IUICollection** 是由功能區標記中每個資源庫宣告的架構所執行。</span><span class="sxs-lookup"><span data-stu-id="b74a1-184">**IUICollection** is implemented by the framework for each gallery declaration in the Ribbon markup.</span></span>

<span data-ttu-id="b74a1-185">如果 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 介面未提供其他需要的功能，則由主應用程式所執行且衍生自 [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) 的自訂集合物件可以取代為架構集合。</span><span class="sxs-lookup"><span data-stu-id="b74a1-185">If additional functionality is required that is not provided by the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface, then a custom collection object that is implemented by the host application and derived from [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) can be substituted for the framework collection.</span></span>

### <a name="iuicollectionchangedevent"></a><span data-ttu-id="b74a1-186">IUICollectionChangedEvent</span><span class="sxs-lookup"><span data-stu-id="b74a1-186">IUICollectionChangedEvent</span></span>

<span data-ttu-id="b74a1-187">若要讓應用程式回應資源庫集合中的變更，則必須執行 [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) 介面。</span><span class="sxs-lookup"><span data-stu-id="b74a1-187">For an application to respond to changes in a gallery collection, it must implement the [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) interface.</span></span> <span data-ttu-id="b74a1-188">應用程式可以透過 [**IUICollectionChangedEvent：： OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged)事件接聽程式，訂閱來自 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)物件的通知。</span><span class="sxs-lookup"><span data-stu-id="b74a1-188">Applications can subscribe to notifications from an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [**IUICollectionChangedEvent::OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) event listener.</span></span>

<span data-ttu-id="b74a1-189">當應用程式將架構所提供的資源庫集合取代為自訂集合時，應用程式應該會執行 [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) 介面。</span><span class="sxs-lookup"><span data-stu-id="b74a1-189">When the application replaces the gallery collection provided by the framework with a custom collection, the application should implement the [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface.</span></span> <span data-ttu-id="b74a1-190">如果未執行 [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) ，則應用程式無法在需要動態更新資源庫控制項的自訂集合中通知架構變更。</span><span class="sxs-lookup"><span data-stu-id="b74a1-190">If [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, then the application is unable to notify the framework of changes in the custom collection that require dynamic updates to the gallery control.</span></span>

<span data-ttu-id="b74a1-191">在未執行 [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) 的情況下，資源庫控制項只能透過 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 和 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)的失效，或藉由呼叫 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)來更新。</span><span class="sxs-lookup"><span data-stu-id="b74a1-191">In those cases where [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, the gallery control can be updated only by invalidation through [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) and [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), or by calling [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>

### <a name="iuisimplepropertyset"></a><span data-ttu-id="b74a1-192">IUISimplePropertySet</span><span class="sxs-lookup"><span data-stu-id="b74a1-192">IUISimplePropertySet</span></span>

<span data-ttu-id="b74a1-193">應用程式必須針對資源庫集合中的每個專案或命令執行 IUISimplePropertySet。</span><span class="sxs-lookup"><span data-stu-id="b74a1-193">Applications must implement IUISimplePropertySet for each item or Command in a gallery collection.</span></span> <span data-ttu-id="b74a1-194">但是，可使用 [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) 要求的屬性會有所不同。</span><span class="sxs-lookup"><span data-stu-id="b74a1-194">However, the properties that can be requested with [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) vary.</span></span>

<span data-ttu-id="b74a1-195">專案會透過 [UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) 屬性索引鍵來定義並系結至資源庫，並使用 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件來公開屬性。</span><span class="sxs-lookup"><span data-stu-id="b74a1-195">Items are defined and bound to a gallery through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key and expose properties with an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="b74a1-196">下表描述專案圖庫中專案 ([**UI \_ COMMANDTYPE \_ 集合**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) 的有效屬性。</span><span class="sxs-lookup"><span data-stu-id="b74a1-196">The valid properties for items in item galleries ([**UI\_COMMANDTYPE\_COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="b74a1-197">某些專案屬性（例如 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)）可以在標記中定義。</span><span class="sxs-lookup"><span data-stu-id="b74a1-197">Some item properties, such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), can be defined in markup.</span></span> <span data-ttu-id="b74a1-198">如需詳細資訊，請參閱 [屬性索引鍵](windowsribbon-reference-properties.md) 參考檔。</span><span class="sxs-lookup"><span data-stu-id="b74a1-198">For more detail, see the [Property Keys](windowsribbon-reference-properties.md) reference documentation.</span></span>

 



<span data-ttu-id="b74a1-199">控制</span><span class="sxs-lookup"><span data-stu-id="b74a1-199">Control</span></span>

<span data-ttu-id="b74a1-200">屬性</span><span class="sxs-lookup"><span data-stu-id="b74a1-200">Properties</span></span>

[<span data-ttu-id="b74a1-201">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="b74a1-201">**ComboBox**</span></span>](windowsribbon-element-combobox.md)

<span data-ttu-id="b74a1-202">[UI \_PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)， [UI \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b74a1-202">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="b74a1-203">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="b74a1-203">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)

<span data-ttu-id="b74a1-204">[UI \_PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)、 [ui \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) 、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b74a1-204">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="b74a1-205">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="b74a1-205">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)

<span data-ttu-id="b74a1-206">[UI \_PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)、 [ui \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) 、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b74a1-206">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="b74a1-207">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="b74a1-207">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)

<span data-ttu-id="b74a1-208">[UI \_PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)、 [ui \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md)、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b74a1-208">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

<span data-ttu-id="b74a1-209">[UI \_PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) 是專案資源庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="b74a1-209">[UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) is a property of the item gallery.</span></span>



 

<span data-ttu-id="b74a1-210">下表說明命令資源庫 ([**UI \_ COMMANDTYPE \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) 的有效專案屬性。</span><span class="sxs-lookup"><span data-stu-id="b74a1-210">The valid item properties for Command galleries ([**UI\_COMMANDTYPE\_COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>



| <span data-ttu-id="b74a1-211">控制</span><span class="sxs-lookup"><span data-stu-id="b74a1-211">Control</span></span>                                                                | <span data-ttu-id="b74a1-212">屬性</span><span class="sxs-lookup"><span data-stu-id="b74a1-212">Properties</span></span>                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b74a1-213">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="b74a1-213">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       | <span data-ttu-id="b74a1-214">[UI \_PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md)、 [ui \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) 、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b74a1-214">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="b74a1-215">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="b74a1-215">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       | <span data-ttu-id="b74a1-216">[UI \_PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md)、 [ui \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) 、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b74a1-216">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="b74a1-217">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="b74a1-217">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) | <span data-ttu-id="b74a1-218">[UI \_PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md)、 [ui \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="b74a1-218">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>  |



 

<span data-ttu-id="b74a1-219">類別目錄是用來組織資源庫中的專案與命令。</span><span class="sxs-lookup"><span data-stu-id="b74a1-219">Categories are used to organize items and Commands in galleries.</span></span> <span data-ttu-id="b74a1-220">類別目錄會透過 [UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-categories.md) category 屬性索引鍵來定義並系結至資源庫，並以類別特定的 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件來公開屬性。</span><span class="sxs-lookup"><span data-stu-id="b74a1-220">Categories are defined and bound to a gallery through the [UI\_PKEY\_Categories](windowsribbon-reference-properties-uipkey-categories.md) property key and expose properties with a category-specific [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="b74a1-221">類別沒有 CommandType，且不支援使用者互動。</span><span class="sxs-lookup"><span data-stu-id="b74a1-221">Categories do not have a CommandType and do not support user interaction.</span></span> <span data-ttu-id="b74a1-222">例如，類別目錄不能成為專案資源庫中的 SelectedItem，而且它們不會系結至命令庫中的命令。</span><span class="sxs-lookup"><span data-stu-id="b74a1-222">For example, categories cannot become the SelectedItem in an item gallery, and they are not bound to a Command in a Command gallery.</span></span> <span data-ttu-id="b74a1-223">如同其他主機庫專案屬性，可以藉由呼叫 [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)來取出類別目錄屬性，例如 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)和 [ui \_ PKEY \_](windowsribbon-reference-properties-uipkey-categoryid.md)類別目錄。</span><span class="sxs-lookup"><span data-stu-id="b74a1-223">Like other gallery item properties, category properties such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) and [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) can be retrieved by calling [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b74a1-224">當針對沒有相關聯類別的專案要求 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)目錄時， [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)應該會傳回 [**ui \_ 集合 \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) 。</span><span class="sxs-lookup"><span data-stu-id="b74a1-224">[**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) should return [**UI\_COLLECTION\_INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) when [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) is requested for an item that does not have an associated category.</span></span>

 

### <a name="declare-the-controls-in-markup"></a><span data-ttu-id="b74a1-225">在標記中宣告控制項</span><span class="sxs-lookup"><span data-stu-id="b74a1-225">Declare the Controls in Markup</span></span>

<span data-ttu-id="b74a1-226">資源庫（例如所有功能區控制項）必須在標記中宣告。</span><span class="sxs-lookup"><span data-stu-id="b74a1-226">Galleries, like all Ribbon controls, must be declared in markup.</span></span> <span data-ttu-id="b74a1-227">資源庫會在標記中識別為專案資源庫或命令資源庫，並宣告各種展示詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b74a1-227">A gallery is identified in markup as an item gallery or Command gallery, and various presentation details are declared.</span></span> <span data-ttu-id="b74a1-228">不同于其他控制項，資源庫需要在標記中宣告基底控制項或集合容器。</span><span class="sxs-lookup"><span data-stu-id="b74a1-228">Unlike other controls, galleries require the base control only, or collection container, to be declared in markup.</span></span> <span data-ttu-id="b74a1-229">實際的集合會在執行時間填入。</span><span class="sxs-lookup"><span data-stu-id="b74a1-229">The actual collections are populated at run time.</span></span> <span data-ttu-id="b74a1-230">在標記中宣告資源庫時，會使用 *Type* 屬性來指定資源庫是否為命令資源庫的專案圖庫。</span><span class="sxs-lookup"><span data-stu-id="b74a1-230">When a gallery is declared in markup, the *Type* attribute is used to specify whether the gallery is an item gallery of a Command gallery.</span></span>

<span data-ttu-id="b74a1-231">這裡討論的每個控制項都有一些選擇性的版面配置屬性可用。</span><span class="sxs-lookup"><span data-stu-id="b74a1-231">There are a number of optional layout attributes available for each of the controls discussed here.</span></span> <span data-ttu-id="b74a1-232">這些屬性會提供開發人員喜好設定，讓架構直接影響控制項在功能區中的填入和顯示方式。</span><span class="sxs-lookup"><span data-stu-id="b74a1-232">These attributes provide developer preferences for the framework to follow that directly affect how a control is populated and displayed in a ribbon.</span></span> <span data-ttu-id="b74a1-233">標記中適用的喜好設定，與 [透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)中所討論的顯示和版面配置範本和行為有關。</span><span class="sxs-lookup"><span data-stu-id="b74a1-233">The preferences applicable in markup are related to the display and layout templates and behaviors discussed in [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="b74a1-234">如果特定控制項不允許直接在標記中使用版面配置喜好設定，或未指定配置喜好設定，則架構會根據可用的螢幕空間量來定義控制項特定的顯示慣例。</span><span class="sxs-lookup"><span data-stu-id="b74a1-234">If a particular control does not allow layout preferences directly in markup, or the layout preferences are not specified, then the framework defines control-specific display conventions based on the amount of screen space available.</span></span>

<span data-ttu-id="b74a1-235">下列範例示範如何將一組資源庫納入功能區中。</span><span class="sxs-lookup"><span data-stu-id="b74a1-235">The following examples demonstrate how to incorporate a set of galleries into a Ribbon.</span></span>

### <a name="command-declarations"></a><span data-ttu-id="b74a1-236">命令聲明</span><span class="sxs-lookup"><span data-stu-id="b74a1-236">Command Declarations</span></span>

<span data-ttu-id="b74a1-237">命令應該以用來將控制項或控制項集合與命令相關聯的 *CommandName* 屬性來宣告。</span><span class="sxs-lookup"><span data-stu-id="b74a1-237">Commands should be declared with a *CommandName* attribute that is used to associate a control, or set of controls, with the Command.</span></span>

<span data-ttu-id="b74a1-238">在編譯標記時，用來將命令系結至命令處理常式的 *CommandId* 屬性也可以在這裡指定。</span><span class="sxs-lookup"><span data-stu-id="b74a1-238">A *CommandId* attribute used to bind a Command to a Command handler when the markup is compiled can also be specified here.</span></span> <span data-ttu-id="b74a1-239">如果未提供任何識別碼，則架構會產生一個識別碼。</span><span class="sxs-lookup"><span data-stu-id="b74a1-239">If no ID is provided, then one is generated by the framework.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a><span data-ttu-id="b74a1-240">控制項宣告</span><span class="sxs-lookup"><span data-stu-id="b74a1-240">Control Declarations</span></span>

<span data-ttu-id="b74a1-241">本章節包含的範例會示範各種資源庫類型所需的基本控制項標記。</span><span class="sxs-lookup"><span data-stu-id="b74a1-241">This section contains examples that demonstrate the basic control markup required for the various gallery types.</span></span> <span data-ttu-id="b74a1-242">它們示範如何宣告資源庫控制項，並透過 *CommandName* 屬性將它們與命令建立關聯。</span><span class="sxs-lookup"><span data-stu-id="b74a1-242">They show how to declare the gallery controls and associate them with a Command through the *CommandName* attribute.</span></span>

<span data-ttu-id="b74a1-243">下列範例顯示 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) 的控制項宣告，其中 *Type* 屬性用來指定這是命令資源庫。</span><span class="sxs-lookup"><span data-stu-id="b74a1-243">The following example shows a control declaration for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) where the *Type* attribute is used to specify that this is a Command gallery.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



<span data-ttu-id="b74a1-244">下列範例顯示 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)的控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="b74a1-244">The following example shows a control declaration for the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



<span data-ttu-id="b74a1-245">下列範例顯示 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)的控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="b74a1-245">The following example shows a control declaration for the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span></span>

> [!Note]  
> <span data-ttu-id="b74a1-246">由於 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 的設計是要在功能區中顯示其專案集合的子集，而不啟動下拉式功能表，所以它提供了一些選擇性屬性，可在功能區初始化時管理其大小和專案版面配置。</span><span class="sxs-lookup"><span data-stu-id="b74a1-246">Because the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is designed to display a subset of its item collection in the Ribbon without activating a drop-down menu, it provides a number of optional attributes that govern its size and item layout on Ribbon initialization.</span></span> <span data-ttu-id="b74a1-247">這些屬性對 **InRibbonGallery** 而言是唯一的，而且無法從其他動態控制項使用。</span><span class="sxs-lookup"><span data-stu-id="b74a1-247">These attributes are unique to the **InRibbonGallery** and are not available from the other dynamic controls.</span></span>

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



<span data-ttu-id="b74a1-248">下列範例顯示 [**ComboBox**](windowsribbon-element-combobox.md)的控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="b74a1-248">The following example shows a control declaration for the [**ComboBox**](windowsribbon-element-combobox.md).</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a><span data-ttu-id="b74a1-249">建立命令處理常式</span><span class="sxs-lookup"><span data-stu-id="b74a1-249">Create a Command Handler</span></span>

<span data-ttu-id="b74a1-250">針對每個命令，功能區架構都需要主應用程式中對應的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="b74a1-250">For each Command, the Ribbon framework requires a corresponding Command handler in the host application.</span></span> <span data-ttu-id="b74a1-251">命令處理常式是由功能區主機應用程式所執行，並且衍生自 [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) 介面。</span><span class="sxs-lookup"><span data-stu-id="b74a1-251">Command handlers are implemented by the Ribbon host application and are derived from the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span>

> [!Note]  
> <span data-ttu-id="b74a1-252">多個命令可以系結至單一命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="b74a1-252">Multiple Commands can be bound to a single Command handler.</span></span>

 

<span data-ttu-id="b74a1-253">命令處理常式有兩個用途：</span><span class="sxs-lookup"><span data-stu-id="b74a1-253">A Command handler serves two purposes:</span></span>

-   <span data-ttu-id="b74a1-254">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 會回應屬性更新要求。</span><span class="sxs-lookup"><span data-stu-id="b74a1-254">[**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responds to property update requests.</span></span> <span data-ttu-id="b74a1-255">您可以透過呼叫 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)或 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)，將命令屬性的值（例如 [ui \_ PKEY \_ 啟用](windowsribbon-reference-properties-uipkey-enabled.md)或 [ui \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)）設定為。</span><span class="sxs-lookup"><span data-stu-id="b74a1-255">The values of Command properties, such as [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), are set through calls to [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) or [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span>
-   <span data-ttu-id="b74a1-256">[**IUICommandHandler：： execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 會回應 execute 事件。</span><span class="sxs-lookup"><span data-stu-id="b74a1-256">[**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responds to execute events.</span></span> <span data-ttu-id="b74a1-257">這個方法支援 [**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) 參數所指定的下列三個執行狀態。</span><span class="sxs-lookup"><span data-stu-id="b74a1-257">This method supports the following three execution states that are specified by the [**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) parameter.</span></span>
    -   <span data-ttu-id="b74a1-258">執行狀態會執行或認可至處理常式所系結的任何命令。</span><span class="sxs-lookup"><span data-stu-id="b74a1-258">The Execute state executes, or commits to, any commands to which the handler is bound.</span></span>
    -   <span data-ttu-id="b74a1-259">預覽狀態會預覽處理常式所系結的任何命令。</span><span class="sxs-lookup"><span data-stu-id="b74a1-259">The Preview state previews any commands to which the handler is bound.</span></span> <span data-ttu-id="b74a1-260">這基本上會執行命令，而不會認可結果。</span><span class="sxs-lookup"><span data-stu-id="b74a1-260">This essentially executes the commands without committing to the result.</span></span>
    -   <span data-ttu-id="b74a1-261">CancelPreview 狀態會取消任何預覽的命令。</span><span class="sxs-lookup"><span data-stu-id="b74a1-261">The CancelPreview state cancels any previewed Commands.</span></span> <span data-ttu-id="b74a1-262">這是支援透過功能表或清單進行遍歷的必要步驟，並可依需要順序預覽及復原結果。</span><span class="sxs-lookup"><span data-stu-id="b74a1-262">This is required to support traversal through a menu or list and sequentially preview and undo the results as required.</span></span>

<span data-ttu-id="b74a1-263">下列範例示範資源庫命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="b74a1-263">The following example demonstrates a gallery command handler.</span></span>


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a><span data-ttu-id="b74a1-264">系結命令處理常式</span><span class="sxs-lookup"><span data-stu-id="b74a1-264">Bind the Command Handler</span></span>

<span data-ttu-id="b74a1-265">在您定義命令處理常式之後，命令必須系結至處理常式。</span><span class="sxs-lookup"><span data-stu-id="b74a1-265">After you define a Command handler, the Command must be bound to the handler.</span></span>

<span data-ttu-id="b74a1-266">下列範例示範如何將資源庫命令系結至特定的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="b74a1-266">The following example demonstrates how to bind a gallery Command to a specific Command handler.</span></span> <span data-ttu-id="b74a1-267">在此情況下， [**ComboBox**](windowsribbon-element-combobox.md) 和圖庫控制項都會系結至各自的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="b74a1-267">In this case, both the [**ComboBox**](windowsribbon-element-combobox.md) and gallery controls are bound to their respective Command handlers.</span></span>


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a><span data-ttu-id="b74a1-268">初始化集合</span><span class="sxs-lookup"><span data-stu-id="b74a1-268">Initialize a Collection</span></span>

<span data-ttu-id="b74a1-269">下列範例示範針對專案和命令資源庫， [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) 的自訂執行。</span><span class="sxs-lookup"><span data-stu-id="b74a1-269">The following example demonstrates a custom implementation of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) for both item and Command galleries.</span></span>

<span data-ttu-id="b74a1-270">此範例中的 CItemProperties 類別衍生自 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)。</span><span class="sxs-lookup"><span data-stu-id="b74a1-270">The CItemProperties class in this example is derived from [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span></span> <span data-ttu-id="b74a1-271">除了所需的方法 [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)之外，CItemProperties 類別還會執行一組 helper 函式來進行初始化和索引追蹤。</span><span class="sxs-lookup"><span data-stu-id="b74a1-271">In addition to the required method [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), the CItemProperties class implements a set of helper functions for initialization and index tracking.</span></span>


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a><span data-ttu-id="b74a1-272">處理收集事件</span><span class="sxs-lookup"><span data-stu-id="b74a1-272">Handle Collection Events</span></span>

<span data-ttu-id="b74a1-273">下列範例示範 IUICollectionChangedEvent 的執行。</span><span class="sxs-lookup"><span data-stu-id="b74a1-273">The following example demonstrates an IUICollectionChangedEvent implementation.</span></span>


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="b74a1-274">相關主題</span><span class="sxs-lookup"><span data-stu-id="b74a1-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b74a1-275">集合屬性</span><span class="sxs-lookup"><span data-stu-id="b74a1-275">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="b74a1-276">建立功能區應用程式</span><span class="sxs-lookup"><span data-stu-id="b74a1-276">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="b74a1-277">瞭解命令和控制項</span><span class="sxs-lookup"><span data-stu-id="b74a1-277">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> <dt>

[<span data-ttu-id="b74a1-278">功能區使用者體驗指導方針</span><span class="sxs-lookup"><span data-stu-id="b74a1-278">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="b74a1-279">功能區設計流程</span><span class="sxs-lookup"><span data-stu-id="b74a1-279">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[<span data-ttu-id="b74a1-280">資源庫範例</span><span class="sxs-lookup"><span data-stu-id="b74a1-280">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 