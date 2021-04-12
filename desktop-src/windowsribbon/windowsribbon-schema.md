---
title: 使用功能區標記宣告命令和控制項
description: Windows 功能區架構會根據 Extensible Application Markup Language (XAML) 以宣告方式來執行功能區應用程式的外觀。
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows 功能區，標記結構
- 功能區，標記結構
- Windows 功能區，從命令邏輯分隔簡報
- 從命令邏輯分隔簡報的功能區
- Windows 功能區，元件
- 功能區、元件
- Windows 功能區的命令系統
- Windows 功能區的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376160"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a><span data-ttu-id="0ad15-111">使用功能區標記宣告命令和控制項</span><span class="sxs-lookup"><span data-stu-id="0ad15-111">Declaring Commands and Controls with Ribbon Markup</span></span>

<span data-ttu-id="0ad15-112">Windows 功能區架構會根據 Extensible Application Markup Language (XAML) 以宣告方式來執行功能區應用程式的外觀。</span><span class="sxs-lookup"><span data-stu-id="0ad15-112">The Windows Ribbon framework uses a markup language based on Extensible Application Markup Language (XAML) to declaratively implement the appearance of a Ribbon application.</span></span>

-   [<span data-ttu-id="0ad15-113">分隔來自命令邏輯的簡報</span><span class="sxs-lookup"><span data-stu-id="0ad15-113">Separating Presentation from Command Logic</span></span>](#separating-presentation-from-command-logic)
-   [<span data-ttu-id="0ad15-114">標記結構</span><span class="sxs-lookup"><span data-stu-id="0ad15-114">Markup Structure</span></span>](#markup-structure)
-   [<span data-ttu-id="0ad15-115">功能區元件</span><span class="sxs-lookup"><span data-stu-id="0ad15-115">Ribbon Components</span></span>](#ribbon-components)
-   [<span data-ttu-id="0ad15-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ad15-116">Related topics</span></span>](#related-topics)

## <a name="separating-presentation-from-command-logic"></a><span data-ttu-id="0ad15-117">分隔來自命令邏輯的簡報</span><span class="sxs-lookup"><span data-stu-id="0ad15-117">Separating Presentation from Command Logic</span></span>

<span data-ttu-id="0ad15-118">您可以透過兩個不同但相依的開發平臺，從功能區架構中的命令邏輯分隔展示和視覺化屬性。</span><span class="sxs-lookup"><span data-stu-id="0ad15-118">The separation of presentation and visual attributes from command logic in the Ribbon framework is accomplished through two distinct, but dependent, development platforms.</span></span> <span data-ttu-id="0ad15-119">控制項版面配置、調整行為、命令宣告和資源規格是宣告式標記語法的設計階段網域，以 [Extensible Application Markup Language (XAML) ](/dotnet/framework/wpf/advanced/xaml-in-wpf) 規格為基礎。</span><span class="sxs-lookup"><span data-stu-id="0ad15-119">Control layouts, scaling behaviors, Command declarations, and resource specifications are the design time domain of a declarative markup syntax based on the [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) specification.</span></span> <span data-ttu-id="0ad15-120">低層級功能、應用程式勾點和命令處理常式都是在元件物件模型中定義 (COM) 型介面執行。</span><span class="sxs-lookup"><span data-stu-id="0ad15-120">Low level functionality, application hooks, and Command handlers are defined in Component Object Model (COM)-based interface implementations.</span></span>

<span data-ttu-id="0ad15-121">這種展示和邏輯的分隔可提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="0ad15-121">This separation of presentation and logic provides the following benefits:</span></span>

-   <span data-ttu-id="0ad15-122">更有效率的應用程式開發週期，可讓使用者介面開發人員和設計人員獨立于核心應用程式功能，來執行功能區應用程式的 GUI。</span><span class="sxs-lookup"><span data-stu-id="0ad15-122">A more efficient application development cycle which allows UI developers and designers to implement the GUI of the Ribbon application independently from the core application functionality.</span></span> <span data-ttu-id="0ad15-123">這些核心功能可留給專用軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="0ad15-123">This core functionality can be left to dedicated software developers.</span></span>
-   <span data-ttu-id="0ad15-124">維護成本較低，因為對 GUI 的變更可能不會變更核心功能 (，反之亦然) 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-124">Less costly maintenance because changes to the GUI are possible without changes to core functionality (and vice versa).</span></span>
-   <span data-ttu-id="0ad15-125">透過標記的字串和影像資源的簡單規格。</span><span class="sxs-lookup"><span data-stu-id="0ad15-125">Simple specification of string and image resources through markup.</span></span>
-   <span data-ttu-id="0ad15-126">簡化原型設計。</span><span class="sxs-lookup"><span data-stu-id="0ad15-126">Ease of prototyping.</span></span>

## <a name="markup-structure"></a><span data-ttu-id="0ad15-127">標記結構</span><span class="sxs-lookup"><span data-stu-id="0ad15-127">Markup Structure</span></span>

<span data-ttu-id="0ad15-128">功能區架構標記的結構中有兩個不同的分支。</span><span class="sxs-lookup"><span data-stu-id="0ad15-128">Two distinct branches exist within the structure of Ribbon framework markup.</span></span>

<span data-ttu-id="0ad15-129">第一個分支包含命令和資源宣告的資訊清單， (字串和影像) 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-129">The first branch contains a manifest of Command and resource declarations (strings and images).</span></span> <span data-ttu-id="0ad15-130">架構會使用每個命令專案，透過命令識別碼將功能區控制項系結至應用程式程式碼中定義的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-130">Each Command entry is used by the framework to bind a Ribbon control, through a Command ID, to a Command handler defined in the application code.</span></span>

<span data-ttu-id="0ad15-131">第二個分支包含實際的控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="0ad15-131">The second branch contains the actual control declarations.</span></span> <span data-ttu-id="0ad15-132">每個控制項都會透過 *CommandName* 屬性與命令相關聯，該屬性會對應到每個命令宣告中指定的 *名稱* 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ad15-132">Each control is associated with a Command through a *CommandName* attribute that maps to a *Name* attribute specified in each Command declaration.</span></span>

## <a name="ribbon-components"></a><span data-ttu-id="0ad15-133">功能區元件</span><span class="sxs-lookup"><span data-stu-id="0ad15-133">Ribbon Components</span></span>

<span data-ttu-id="0ad15-134">功能區架構 UI 功能是透過 [視圖](windowsribbon-reference-elements-view.md)來公開。</span><span class="sxs-lookup"><span data-stu-id="0ad15-134">Ribbon framework UI functionality is exposed through [Views](windowsribbon-reference-elements-view.md).</span></span> <span data-ttu-id="0ad15-135">視圖基本上是一個容器（例如 [**功能區**](windowsribbon-element-ribbon.md) 和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)），可用來呈現 framework 控制項及其系結的命令。</span><span class="sxs-lookup"><span data-stu-id="0ad15-135">A View is essentially a container, such as the [**Ribbon**](windowsribbon-element-ribbon.md) and [**ContextPopup**](windowsribbon-element-contextpopup.md), that is used to present framework controls and the Commands they are bound to.</span></span>

<span data-ttu-id="0ad15-136">[**功能區**](windowsribbon-element-ribbon.md)視圖是由數個元件所組成，其中包含 [應用程式功能表](windowsribbon-controls-applicationmenu.md)、[快速存取工具列 (QAT)](windowsribbon-controls-quickaccesstoolbar.md) ，以顯示功能區 UI 中常用的命令、包含控制項 [群組](windowsribbon-controls-group.md)[的核心](windowsribbon-controls-tab.md)和內容索引標籤，以及 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)的豐富內容功能表系統。</span><span class="sxs-lookup"><span data-stu-id="0ad15-136">The [**Ribbon**](windowsribbon-element-ribbon.md) View is composed of several components that include an [Application Menu](windowsribbon-controls-applicationmenu.md), the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md) for displaying commonly used Commands from the ribbon UI, core and contextual [tabs](windowsribbon-controls-tab.md) that contain [groups](windowsribbon-controls-group.md) of controls, and the rich context menu system of the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="0ad15-137">所有功能區元件都是在獨立的標記檔案中宣告：</span><span class="sxs-lookup"><span data-stu-id="0ad15-137">All Ribbon components are declared in a standalone markup file that:</span></span>

-   <span data-ttu-id="0ad15-138">指定每個元素的基本屬性。</span><span class="sxs-lookup"><span data-stu-id="0ad15-138">Specifies the basic properties for each element.</span></span>
-   <span data-ttu-id="0ad15-139">清楚地顯示階層式關聯性。</span><span class="sxs-lookup"><span data-stu-id="0ad15-139">Shows hierarchical relationships clearly.</span></span>
-   <span data-ttu-id="0ad15-140">提供版面配置喜好設定和縮放提示。</span><span class="sxs-lookup"><span data-stu-id="0ad15-140">Supplies layout preferences and scaling hints.</span></span> <span data-ttu-id="0ad15-141">如需功能區架構版面配置範本的詳細資訊，請參閱 [透過大小定義自訂功能區和調整原則](windowsribbon-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="0ad15-141">For more information on Ribbon framework layout templates, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>
-   <span data-ttu-id="0ad15-142">提供一種方式來定義資源，例如影像和標籤。</span><span class="sxs-lookup"><span data-stu-id="0ad15-142">Provides a way to define resources such as images and labels.</span></span> <span data-ttu-id="0ad15-143">如需映射資源的詳細資訊，請參閱 [指定功能區影像資源](windowsribbon-imageformats.md)。</span><span class="sxs-lookup"><span data-stu-id="0ad15-143">For more information on image resources, see [Specifying Ribbon Image Resources](windowsribbon-imageformats.md).</span></span>

<span data-ttu-id="0ad15-144">下列兩個功能區標記範例示範一組功能區應用程式功能表項目如何與命令名稱和識別碼相關聯。</span><span class="sxs-lookup"><span data-stu-id="0ad15-144">The following two Ribbon markup examples demonstrate how a set of Ribbon Application Menu items are each associated with a Command name and ID.</span></span>

1.  <span data-ttu-id="0ad15-145">本節顯示具有基本命令的應用程式功能表所需的命令宣告，例如 [新增]、[開啟] 和 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="0ad15-145">This section shows the Command declarations required for an Application Menu with basic commands such as New, Open, and Save.</span></span>
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  <span data-ttu-id="0ad15-146">此區段會顯示相關聯的控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="0ad15-146">This section shows the associated Control declarations.</span></span>
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

<span data-ttu-id="0ad15-147">使用 UI 命令編譯器 (UICC) 工具編譯標記時，命令名稱和識別碼會放入功能區主機應用程式所使用的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-147">When the markup is compiled with the UI Command Compiler (UICC) tool, the Command names and IDs are placed into a header file used by the Ribbon host application.</span></span>

<span data-ttu-id="0ad15-148">以下是 UICC 所產生的標頭檔範例。</span><span class="sxs-lookup"><span data-stu-id="0ad15-148">The following is an example of a header file generated by UICC.</span></span>


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a><span data-ttu-id="0ad15-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ad15-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ad15-150">Extensible Application Markup Language (XAML) </span><span class="sxs-lookup"><span data-stu-id="0ad15-150">Extensible Application Markup Language (XAML)</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[<span data-ttu-id="0ad15-151">編譯功能區標記</span><span class="sxs-lookup"><span data-stu-id="0ad15-151">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)
</dt> </dl>

 

 