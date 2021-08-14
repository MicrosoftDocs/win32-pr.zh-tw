---
title: 使用功能區標記宣告命令和控制項
description: Windows 功能區架構會根據 Extensible Application Markup Language (XAML) ，使用以宣告方式執行功能區應用程式外觀的標記語言。
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows功能區，標記結構
- 功能區，標記結構
- Windows從命令邏輯分隔簡報的功能區
- 從命令邏輯分隔簡報的功能區
- Windows功能區、元件
- 功能區、元件
- Windows 功能區的命令系統
- Windows 功能區的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ae6c8d62012fac240c6d044c688295d89d8d5899e3673a3b914d8d142111d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201320"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>使用功能區標記宣告命令和控制項

Windows 功能區架構會根據 Extensible Application Markup Language (XAML) ，使用以宣告方式執行功能區應用程式外觀的標記語言。

-   [分隔來自命令邏輯的簡報](#separating-presentation-from-command-logic)
-   [標記結構](#markup-structure)
-   [功能區元件](#ribbon-components)
-   [相關主題](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>分隔來自命令邏輯的簡報

您可以透過兩個不同但相依的開發平臺，從功能區架構中的命令邏輯分隔展示和視覺化屬性。 控制項版面配置、調整行為、命令宣告和資源規格是宣告式標記語法的設計階段網域，以 [Extensible Application Markup Language (XAML) ](/dotnet/framework/wpf/advanced/xaml-in-wpf) 規格為基礎。 低層級功能、應用程式勾點和命令處理常式都是在元件物件模型中定義 (COM) 型介面執行。

這種展示和邏輯的分隔可提供下列優點：

-   更有效率的應用程式開發週期，可讓使用者介面開發人員和設計人員獨立于核心應用程式功能，來執行功能區應用程式的 GUI。 這些核心功能可留給專用軟體發展人員。
-   維護成本較低，因為對 GUI 的變更可能不會變更核心功能 (，反之亦然) 。
-   透過標記的字串和影像資源的簡單規格。
-   簡化原型設計。

## <a name="markup-structure"></a>標記結構

功能區架構標記的結構中有兩個不同的分支。

第一個分支包含命令和資源宣告的資訊清單， (字串和影像) 。 架構會使用每個命令專案，透過命令識別碼將功能區控制項系結至應用程式程式碼中定義的命令處理常式。

第二個分支包含實際的控制項宣告。 每個控制項都會透過 *CommandName* 屬性與命令相關聯，該屬性會對應到每個命令宣告中指定的 *名稱* 屬性。

## <a name="ribbon-components"></a>功能區元件

功能區架構 UI 功能是透過 [視圖](windowsribbon-reference-elements-view.md)來公開。 視圖基本上是一個容器（例如 [**功能區**](windowsribbon-element-ribbon.md) 和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)），可用來呈現 framework 控制項及其系結的命令。

[**功能區**](windowsribbon-element-ribbon.md)視圖是由數個元件所組成，其中包含 [應用程式功能表](windowsribbon-controls-applicationmenu.md)、[快速存取工具列 (QAT)](windowsribbon-controls-quickaccesstoolbar.md) ，以顯示功能區 UI 中常用的命令、包含控制項 [群組](windowsribbon-controls-group.md)[的核心](windowsribbon-controls-tab.md)和內容索引標籤，以及 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)的豐富內容功能表系統。

所有功能區元件都是在獨立的標記檔案中宣告：

-   指定每個元素的基本屬性。
-   清楚地顯示階層式關聯性。
-   提供版面配置喜好設定和縮放提示。 如需功能區架構版面配置範本的詳細資訊，請參閱 [透過大小定義自訂功能區和調整原則](windowsribbon-templates.md)。
-   提供一種方式來定義資源，例如影像和標籤。 如需映射資源的詳細資訊，請參閱 [指定功能區影像資源](windowsribbon-imageformats.md)。

下列兩個功能區標記範例示範一組功能區應用程式功能表項目如何與命令名稱和識別碼相關聯。

1.  本節顯示具有基本命令的應用程式功能表所需的命令宣告，例如 [新增]、[開啟] 和 [儲存]。
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

    

2.  此區段會顯示相關聯的控制項宣告。
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

    

使用 UI 命令編譯器 (UICC) 工具編譯標記時，命令名稱和識別碼會放入功能區主機應用程式所使用的標頭檔中。

以下是 UICC 所產生的標頭檔範例。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Extensible Application Markup Language (XAML) ](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[編譯功能區標記](windowsribbon-intentcl.md)
</dt> </dl>

 

 