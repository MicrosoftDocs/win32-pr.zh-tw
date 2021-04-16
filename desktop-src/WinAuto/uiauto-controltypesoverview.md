---
title: UI 自動化控制項類型概觀
description: Microsoft 消費者介面自動化控制項類型是可做為已知識別碼的屬性，表示特定 UI 專案所代表的控制項類型，例如下拉式方塊或按鈕。
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- 消費者介面自動化，控制項類型總覽
- 消費者介面自動化，UIA_LocalizedControlTypePropertyId 屬性
- 控制項類型，關於
- 控制項類型，先決條件
- 控制項類型，必要條件
- 控制項類型，預先定義
- 控制項類型，UIA_LocalizedControlTypePropertyId 屬性
- 預先定義的控制項類型
- UIA_LocalizedControlTypePropertyId 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507939"
---
# <a name="ui-automation-control-types-overview"></a>UI 自動化控制項類型概觀

Microsoft 消費者介面自動化控制項類型是可做為已知識別碼的屬性，表示特定 UI 專案所代表的控制項類型，例如下拉式方塊或按鈕。 用戶端應用程式會使用類型來識別控制項的功能，以及判斷如何與其互動。

本主題包含下列幾節：

-   [UI 自動化控制項類型必要條件](#ui-automation-control-type-requisites)
-   [LocalizedControlType 屬性](#the-localizedcontroltype-property)
-   [目前 UI 自動化控制項類型](#current-ui-automation-control-types)
-   [相關主題](#related-topics)

## <a name="ui-automation-control-type-requisites"></a>UI 自動化控制項類型必要條件

每個消費者介面自動化控制項類型都有一組相關聯的條件。 當提供者將控制項類型指派給控制項時，提供者必須確保控制項符合與該控制項類型相關聯的所有條件。 這些條件包括下列各項：

-   消費者介面自動化控制項模式：每個控制項類型都有一組控制項必須支援的控制項模式、選擇性的集合，以及控制項不能支援的集合。
-   使用者介面自動化屬性值：每個控制項類型都有一組控制項必須支援的屬性。
-   使用者介面自動化事件：每個控制項類型都有一組控制項必須支援的事件。
-   使用者介面自動化樹狀結構：每個控制項類型皆定義控制項在使用者介面自動化樹狀結構中必須如何顯示。

當控制項符合特定控制項類型的條件時， [**IUIAutomationElement：： CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (或 [**IUIAutomationElement：：) CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype) 屬性值會指出該控制項類型。

如果您的控制項不符合特定控制項類型的規格，請使用 [**UIA \_ CustomControlTypeId**](uiauto-controltype-ids.md) 做為控制項類型識別碼，並使用相關的控制項模式和屬性來完全描述控制項。 您也可以將 [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) 屬性設定為最能描述控制項類型的字串。

## <a name="the-localizedcontroltype-property"></a>LocalizedControlType 屬性

如果您使用預先定義的控制項類型來描述您的控制項，請使用 [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) 屬性的預設值，並允許消費者介面自動化提供當地語系化的字串，讓提供者正確公開。 如果您無法使用預先定義的控制項類型來描述您的控制項，請將 **UIA \_ LocalizedControlTypePropertyId** 屬性設定為可精確描述控制項類型的當地語系化字串。 此字串應該很簡潔，但其精確度足以讓輔助技術（例如螢幕讀取器）可以在 UI 中使用它來通知使用者控制項的型別。

## <a name="current-ui-automation-control-types"></a>目前 UI 自動化控制項類型

下列主題描述消費者介面自動化控制項類型。 針對每個控制項類型，描述包含指定類型的控制項必須支援的一組條件：

-   AppBar 控制項類型
-   [Button 控制項類型](uiauto-supportbuttoncontroltype.md)
-   [行事曆控制項類型](uiauto-supportcalendarcontroltype.md)
-   [CheckBox 控制項類型](uiauto-supportcheckboxcontroltype.md)
-   [ComboBox 控制項類型](uiauto-supportcomboboxcontroltype.md)
-   [DataGrid 控制項類型](uiauto-supportdatagridcontroltype.md)
-   [DataItem 控制項類型](uiauto-supportdataitemcontroltype.md)
-   [檔控制項類型](uiauto-supportdocumentcontroltype.md)
-   [編輯控制項類型](uiauto-supporteditcontroltype.md)
-   [群組控制項類型](uiauto-supportgroupcontroltype.md)
-   [標題控制項類型](uiauto-supportheadercontroltype.md)
-   [HeaderItem 控制項類型](uiauto-supportheaderitemcontroltype.md)
-   [Hyperlink 控制項類型](uiauto-supporthyperlinkcontroltype.md)
-   [影像控制項類型](uiauto-supportimagecontroltype.md)
-   [清單控制項類型](uiauto-supportlistcontroltype.md)
-   [[類型] 控制項類型](uiauto-supportlistitemcontroltype.md)
-   [Menu 控制項類型](uiauto-supportmenucontroltype.md)
-   [功能表列控制項類型](uiauto-supportmenubarcontroltype.md)
-   [MenuItem 控制項類型](uiauto-supportmenuitemcontroltype.md)
-   [窗格控制項類型](uiauto-supportpanecontroltype.md)
-   [ProgressBar 控制項類型](uiauto-supportprogressbarcontroltype.md)
-   [選項按鈕控制項類型](uiauto-supportradiobuttoncontroltype.md)
-   [捲軸控制項類型](uiauto-supportscrollbarcontroltype.md)
-   [SemanticZoom 控制項類型](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [分隔符號控制項類型](uiauto-supportseparatorcontroltype.md)
-   [滑杆控制項類型](uiauto-supportslidercontroltype.md)
-   [微調控制項類型](uiauto-supportspinnercontroltype.md)
-   [SplitButton 控制項類型](uiauto-supportsplitbuttoncontroltype.md)
-   [狀態列控制項類型](uiauto-supportstatusbarcontroltype.md)
-   [索引標籤控制項類型](uiauto-supporttabcontroltype.md)
-   [TabItem 控制項類型](uiauto-supporttabitemcontroltype.md)
-   [Table 控制項類型](uiauto-supporttablecontroltype.md)
-   [Text 控制項類型](uiauto-supporttextcontroltype.md)
-   [Thumb 控制項類型](uiauto-supportthumbcontroltype.md)
-   [標題列控制項類型](uiauto-supporttitlebarcontroltype.md)
-   [ToolBar 控制項類型](uiauto-supporttoolbarcontroltype.md)
-   [ToolTip 控制項類型](uiauto-supporttooltipcontroltype.md)
-   [樹狀目錄控制項類型](uiauto-supporttreecontroltype.md)
-   [TreeItem 控制項類型](uiauto-supporttreeitemcontroltype.md)
-   [Window 控制項類型](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[控制項類型識別碼](uiauto-controltype-ids.md)
</dt> <dt>

**概念**
</dt> <dt>

[支援消費者介面自動化控制項類型](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[標準控制項的 UI 自動化支援](uiauto-controlsupport.md)
</dt> <dt>

[UI 自動化基礎](entry-uiautocore-overview.md)
</dt> </dl>

 

 