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
# <a name="windows-ribbon-framework-control-library"></a>Windows 功能區架構控制項程式庫

本節所包含的主題描述 Windows 功能區架構所包含的一組控制項。 此處所列的控制項是功能區中公開命令功能的 UI 物件。

-   [簡介](#introduction)
-   [控制項](#windows-ribbon-framework-control-library)
    -   [基本控制項](#basic-controls)
    -   [容器控制項](#container-controls)
    -   [專用控制項](#specialized-controls)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

功能區架構是由索引標籤和[快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)[等元件](windowsribbon-controls-tab.md)所組成，這些元件會一起運作來提供豐富的 UI 體驗。 這些元件會個別公開不同類型的命令，讓客戶在功能區應用程式之間有組織、可預測的體驗。 例如，每個索引標籤都會公開與在應用程式工作區中的特定內容部分建立和操作相關的命令，而 [ [應用程式] 功能表](windowsribbon-controls-applicationmenu.md) 則會公開與完整專案相關的功能，例如整個檔、圖片或影片。

本主題提供功能區控制項的完整清單，其中包含每個控制項的簡短描述，並提供更詳細檔的連結（如果有的話）。

## <a name="the-controls"></a>控制項

功能區架構由兩個 [視圖](windowsribbon-reference-elements-view.md)組成： [**功能區**](windowsribbon-element-ribbon.md) 視圖和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 視圖。 每個視圖都可以裝載數個元件，作為架構所轉譯和管理之所有控制項的呈現容器。

當 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 裝載 [**CoNtextMenu**](windowsribbon-element-contextmenu.md)元素、[**浮動工具列**](windowsribbon-element-minitoolbar.md)元素或兩者時，[**功能區**](windowsribbon-element-ribbon.md)視圖會裝載 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)元素、 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)元素和功能區命令列。

每個 framework 控制項都是由與其 [**命令類型**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)相關聯的功能所區分。

### <a name="basic-controls"></a>基本控制項

基本控制項包含一或多個按鈕，只要按一下滑鼠，就能執行簡單的動作。

> [!Note]  
> [**微調**](windowsribbon-element-spinner.md)項是包含編輯控制項的例外狀況。

 

下表列出功能區架構中的基本控制項。



| 控制                                                  | 標記元素                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [按鈕](windowsribbon-controls-button.md)              | [**按鈕**](windowsribbon-element-button.md)             |
| [核取方塊](windowsribbon-controls-checkbox.md)         | [**相應**](windowsribbon-element-checkbox.md)         |
| [說明按鈕](windowsribbon-controls-helpbutton.md)     | [**HelpButton**](windowsribbon-element-helpbutton.md)     |
| [Spinner](windowsribbon-controls-spinner.md)            | [**Spinner**](windowsribbon-element-spinner.md)           |
| [切換按鈕](windowsribbon-controls-togglebutton.md) | [**ToggleButton**](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a>容器控制項

容器控制項是由控制項群組、功能表、清單或專案和命令集合所組成。

架構會區分兩種類型的容器，也就是靜態和動態。

### <a name="static-containers"></a>靜態容器

在功能區標記檔案中，會宣告和擴展靜態容器，以及所有相關聯的資源。 這些控制項無法在執行時間修改。

靜態控制項的優點包括下列各項：

-   快速建立原型。 靜態控制項可讓您快速建立功能區模擬，類似于最終的功能區設計，而不需要複雜的程式碼。
-   輕鬆修改。 靜態控制項的大部分元素、屬性、資源和配置都可以在標記中修改。
-   一致的 UI。 設計完善的應用程式提供一致且穩定的 UI，可避免在執行時間變更功能表和清單。

下表描述功能區架構中的靜態容器控制項。



| 控制                                                        | 標記元素                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [應用程式功能表](windowsribbon-controls-applicationmenu.md) | [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) |
| [內容快顯視窗](windowsribbon-controls-contextpopup.md)       | [**CoNtextPopup**](windowsribbon-element-contextpopup.md)       |
| [下拉式按鈕](windowsribbon-controls-dropdownbutton.md)  | [**DropDownButton**](windowsribbon-element-dropdownbutton.md)   |
| [群組](windowsribbon-controls-group.md)                      | [**Group**](windowsribbon-element-group.md)                     |
| [功能表群組](windowsribbon-controls-menugroup.md)             | [**MenuGroup**](windowsribbon-element-menugroup.md)             |
| [分割按鈕](windowsribbon-controls-splitbutton.md)         | [**SplitButton**](windowsribbon-element-splitbutton.md)         |
| [Tab](windowsribbon-controls-tab.md)                          | [**索引標籤**](windowsribbon-element-tab.md)                         |
| [Tab 群組](windowsribbon-controls-tabgroup.md)               | [**TabGroup**](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a>動態容器

動態容器是在功能區標記檔案中宣告的。 它們會提供在執行時間建立或修改的一組專案或命令。

動態容器的子類別（稱為資源庫）是由其 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 介面的實作為區別。 這個介面可讓控制項將其專案或命令清單公開為集合，並支援以使用者互動和執行時間條件為基礎的更新。 如需詳細資訊，請參閱 [使用資源庫](ribbon-controls-galleries.md)。

下表列出功能區架構中的動態容器控制項。



| 控制                                                               | 標記元素                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [下拉式方塊](windowsribbon-controls-combobox.md)                      | [**ComboBox**](windowsribbon-element-combobox.md)                     |
| [下拉式圖庫](windowsribbon-controls-dropdowngallery.md)       | [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       |
| [功能區中的資源庫](windowsribbon-controls-inribbongallery.md)       | [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       |
| [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) | [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) |
| [最近的項目](windowsribbon-controls-recentitems.md)                | [**RecentItems**](windowsribbon-element-recentitems.md)               |
| [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md) | [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a>專用控制項

功能區架構包含一些特定 UI 功能的專用控制項。

下表列出功能區架構中的特殊控制項。



| 控制                                                                  | 標記元素                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md) | [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) |
| [字型控制項](windowsribbon-controls-fontcontrol.md)                   | [**FontControl**](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解命令和控制項](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 