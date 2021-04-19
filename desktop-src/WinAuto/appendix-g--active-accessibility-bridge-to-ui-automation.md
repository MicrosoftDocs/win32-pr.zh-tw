---
title: 附錄 G Active Accessibility 橋接器至消費者介面自動化
description: 本附錄包含 Microsoft Active Accessibility 橋接器的相關資訊。
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5fdc1ebc4d6e17781e383463974f78bb9334aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969852"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>附錄 G： Active Accessibility 橋接器至消費者介面自動化

本附錄包含 Microsoft Active Accessibility 橋接器的相關資訊。 Active Accessibility 橋接器可讓執行 Microsoft Active Accessibility 的應用程式存取可執行 Microsoft 消費者介面自動化的應用程式。 藉由橋接 Microsoft Active Accessibility 和消費者介面自動化，以 Microsoft Active Accessibility 為基礎的用戶端（例如 Windows XP 上的 screenreader）可以用程式設計方式與消費者介面自動化 Windows Presentation Foundation WPF (應用程式的消費者介面自動化型提供者互動。 它是消費者介面自動化原生核心 API (UIAutomationCore.dll) 的一部分。

Active Accessibility 橋接器會將消費者介面自動化的屬性和事件對應至 Microsoft Active Accessibility 的屬性和事件。 下表將 Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面方法和屬性對應至消費者介面自動化。 使用這些表格來判斷用於開發以 Microsoft Active Accessibility 為基礎之用戶端的適當程式碼撰寫做法。

### <a name="navigation-and-hierarchy-properties"></a>導覽和階層屬性



| IAccessible 屬性                                                     | 消費者介面自動化屬性          |
|--------------------------------------------------------------------------|---------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | 未實作                 |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | 衍生自消費者介面自動化樹狀結構 |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | 衍生自消費者介面自動化樹狀結構 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | 未實作                 |



 

### <a name="descriptive-properties-and-methods"></a>描述性屬性和方法



| IAccessible                                                                          | UI 自動化                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | 如需詳細資訊，請參閱控制項類型和 accRole 表。                                                                                                                                                                                                                                                                     |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | 如需詳細資訊，請參閱控制項類型和 accRole 表。                                                                                                                                                                                                                                                                     |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | AccessKeyPropertyor AcceleratorKeyProperty;如果兩者都存在，AccessKeyProperty 會優先使用。                                                                                                                                                                                                                         |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | ControlTypeProperty. 如需詳細資訊，請參閱控制項類型和 accRole 表。                                                                                                                                                                                                                                                |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | 如需詳細資訊，請參閱控制項類型和 accRole 表。                                                                                                                                                                                                                                                                     |
| [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | ValueProperty支援實 [值](uiauto-implementingvalue.md) 控制項模式或 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式控制項模式的控制項類型。 RangeValue 值與 Microsoft Active Accessibility 行為一致 (0 至 100) 。 值項目使用字串。 |
| [**put \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | ValueProperty支援實 [值](uiauto-implementingvalue.md) 控制項模式或 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式的控制項類型                                                                                                                                      |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | HelpTextProperty                                                                                                                                                                                                                                                                                                         |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | 未實作                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | 未實作                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>控制項類型和 accRole

Microsoft Active Accessibility 預設角色是 [**角色 \_ 系統 \_ 用戶端**](object-roles.md)。 如果找不到控制項類型的預設動作，Active Accessibility 橋接器也會使用下列可用的控制項模式： [Invoke](uiauto-implementinginvoke.md)、 [ExpandCollapse](uiauto-implementingexpandcollapse.md)和 [切換](uiauto-implementingtoggle.md)。 例如，[分組] 控制項沒有預設動作。 如果支援 ExpandCollapse，則 Active Accessibility 橋接器會將其用於預設動作。



| 消費者介面自動化控制項類型                              | accRole                                                                     | 預設動作                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [按鈕](uiauto-supportbuttoncontroltype.md)           | [**角色 \_ 系統 \_ 按鍵**](object-roles.md)     | 按鍵                                                    |
| [Calendar](uiauto-supportcalendarcontroltype.md)       | [**角色 \_ 系統 \_ 用戶端**](object-roles.md)             | 無                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**角色 \_ 系統 \_ CHECKBUTTON**](object-roles.md)   | 勾選/取消核取 (切換)                                    |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**角色 \_ 系統 \_ COMBOBOX**](object-roles.md)         | 無                                                     |
| 自訂                                                  | [**角色 \_ 系統 \_ 用戶端**](object-roles.md)             | 無                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**角色 \_ 系統 \_ 清單**](object-roles.md)                 | 無                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**角色 \_ 系統 \_**](object-roles.md)         | 無                                                     |
| [文件](uiauto-supportdocumentcontroltype.md)       | [**角色 \_ 系統 \_ 檔**](object-roles.md)         | 無                                                     |
| [編輯](uiauto-supporteditcontroltype.md)               | [**角色 \_ 系統 \_ 文字**](object-roles.md)                 | 無                                                     |
| [群組](uiauto-supportgroupcontroltype.md)             | [**角色 \_ 系統 \_ 群組**](object-roles.md)         | 無                                                     |
| [標頭](uiauto-supportheadercontroltype.md)           | [**角色 \_ 系統 \_ 清單**](object-roles.md)                 | 無                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**角色 \_ 系統 \_ COLUMNHEADER**](object-roles.md) | 按一下                                                    |
| [超連結](uiauto-supporthyperlinkcontroltype.md)     | [**角色 \_ 系統 \_ 連結**](object-roles.md)                 | 跳躍 (對應以叫用)                                     |
| [影像](uiauto-supportimagecontroltype.md)             | [**角色 \_ 系統 \_ 圖形**](object-roles.md)           | 無                                                     |
| [清單](uiauto-supportlistcontroltype.md)               | [**角色 \_ 系統 \_ 清單**](object-roles.md)                 | 無                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**角色 \_ 系統 \_**](object-roles.md)         | 按兩下                                             |
| [功能表](uiauto-supportmenucontroltype.md)               | [**角色 \_ 系統 \_ MENUPOPUP**](object-roles.md)       | 無                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**角色 \_ 系統 \_ 功能表列**](object-roles.md)           | 無                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**角色 \_ 系統 \_ MENUITEM**](object-roles.md)         | 針對具有子系的功能表項目執行或開啟/關閉。 |
| [窗格](uiauto-supportpanecontroltype.md)               | [**角色 \_ 系統 \_ 窗格**](object-roles.md)                 | 無                                                     |
| [進度列](uiauto-supportprogressbarcontroltype.md) | [**角色 \_ 系統 \_ PROGRESSBAR**](object-roles.md)   | 無                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**角色 \_ 系統 \_ 選項按鈕**](object-roles.md)   | 勾選                                                    |
| [ScrollBar](uiauto-supportscrollbarcontroltype.md)     | [**角色 \_ 系統 \_ 捲軸**](object-roles.md)       | 無                                                     |
| [滑桿](uiauto-supportslidercontroltype.md)           | [**角色 \_ 系統 \_ 滑杆**](object-roles.md)             | 無                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**角色系統已進行數值 \_ \_ 調節**](object-roles.md)     | 無                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**角色 \_ 系統 \_ SPLITBUTTON**](object-roles.md)   | 無                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**角色 \_ 系統 \_ 狀態列**](object-roles.md)       | 無                                                     |
| [Tab](uiauto-supporttabcontroltype.md)                 | [**角色 \_ 系統 \_ PAGETABLIST**](object-roles.md)   | 無                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**角色 \_ 系統 \_ PAGETAB**](object-roles.md)           | 參數                                                   |
| [資料表](uiauto-supporttablecontroltype.md)             | [**角色 \_ 系統 \_ 資料表**](object-roles.md)               | 無                                                     |
| [Text](uiauto-supporttextcontroltype.md)               | [**角色 \_ 系統 \_ STATICTEXT**](object-roles.md)     | 無                                                     |
| [拇指](uiauto-supportthumbcontroltype.md)             | [**角色 \_ 系統 \_ 指標**](object-roles.md)       | 無                                                     |
| [標題列](uiauto-supporttitlebarcontroltype.md)       | [**角色 \_ 系統 \_ 標題列**](object-roles.md)         | 無                                                     |
| [工具 欄](uiauto-supporttoolbarcontroltype.md)         | [**角色 \_ 系統 \_ 工具列**](object-roles.md)           | 無                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**角色 \_ 系統 \_ 工具提示**](object-roles.md)           | 無                                                     |
| [樹狀結構](uiauto-supporttreecontroltype.md)               | [**角色 \_ 系統 \_ 大綱**](object-roles.md)           | 無                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**角色 \_ 系統 \_ OUTLINEITEM**](object-roles.md)   | 展開或折迭                                       |
| [Window](uiauto-supportwindowcontroltype.md)           | [**角色 \_ 系統 \_ 視窗**](object-roles.md)             | 無                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>消費者介面自動化屬性和 accState



| accState                                                                                      | 消費者介面自動化屬性                                                                                                                                                        | 觸發狀態變更 |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**狀態 \_ 系統 \_ 已核取**](object-state-constants.md)                 | 若為 ControlType = "checkbox"，請使用 ToggleState。 針對「選項按鈕」，請使用 [ **SelectionItemPattern：： IsSelected**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Yes                   |
| [**狀態 \_ 系統可 \_ 設定焦點**](object-state-constants.md)             | IsKeyboardFocusableProperty                                                                                                                                                   | No                    |
| [**以狀態 \_ 系統為 \_ 焦點**](object-state-constants.md)                 | HasKeyboardFocusProperty                                                                                                                                                      | No                    |
| [**狀態 \_ 系統 \_ 受保護**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | No                    |
| [**狀態 \_ 系統 \_ READONLY**](object-state-constants.md)               | IsReadOnlyProperty (值控制項模式和 RangeValue 控制項模式)                                                                                                      | No                    |
| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Yes                   |
| [**狀態 \_ 系統 \_ 連結**](object-state-constants.md)                   | ControlTypeProperty = "hyperlink"                                                                                                                                             | No                    |
| [**狀態 \_ 系統可 \_ 選取**](object-state-constants.md)           | 支援 SelectionItemPattern                                                                                                                                             | No                    |
| [**選取的狀態 \_ 系統 \_**](object-state-constants.md)               | IsSelectedProperty (SelectionItem 控制項模式)                                                                                                                             | No                    |
| [**狀態系統已折迭 \_ \_**](object-state-constants.md)             | ExpandCollapseState = 折迭                                                                                                                                               | Yes                   |
| [**狀態 \_ 系統已 \_ 展開**](object-state-constants.md)               | ExpandCollapseState = 展開或 PartiallyExpanded                                                                                                                           | Yes                   |
| [**狀態 \_ 系統 \_ HASPOPUP**](object-state-constants.md)               | 支援展開/折迭的功能表項目                                                                                                                                       | No                    |
| [**狀態 \_ 系統 \_ 混合**](object-state-constants.md)                     | ToggleState = 不定                                                                                                                                                   | No                    |
| [**狀態 \_ 系統 \_ 相當大**](object-state-constants.md)               | [**IUIAutomationTransformPattern：： Graphicswindow.canresize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | No                    |
| [**狀態 \_ 系統 \_ 可移動**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanMove**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | No                    |
| [**狀態 \_ 系統 \_ MULTISELECTABLE**](object-state-constants.md) | [**IUIAutomationSelectionPattern::CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | No                    |



 

### <a name="selection-and-focus"></a>選取範圍和焦點



| IAccessible                                                            | UI 自動化                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**IUIAutomation：： System.windows.input.focusmanager.focusedelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | 如需詳細資訊，請參閱消費者介面自動化屬性和 accSelect SELFLAGs 資料表。             |
| [**取得 \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern::GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>消費者介面自動化屬性和 accSelect SELFLAGs



| accSelect SELFLAGs                                                  | 消費者介面自動化屬性                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**SELFLAG \_ 無**](selflag.md)                       | 無法使用                                                                                                                  |
| SELFLAG \_ TAKFOCUS                                                   | [**IUIAutomationElement：： SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**SELFLAG \_ TAKESELECTION**](selflag.md)     | [**IUIAutomationSelectionItemPattern：： Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**SELFLAG \_ ADDSELECTION**](selflag.md)       | [**IUIAutomationSelectionItemPattern::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| SELFLAG \_ TAKEREMOVESELECTION                                        | [**IUIAutomationSelectionItemPattern::RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**SELFLAG \_ EXTENDSELECTION**](selflag.md) | 無法使用                                                                                                                  |



 

### <a name="spatial-mapping"></a>空間對應



| IAccessible                                                 | UI 自動化                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | BoundingRectangleProperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot::ElementProviderFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>事件



| System-Level 事件常數                                                             | UI 自動化                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**事件 \_ 系統 \_ MENUPOPUPSTART**](event-constants.md)     | [**UIA \_MenuOpenedEventId**](uiauto-event-ids.md) (注意：必須檢查這是否為快顯視窗。 )  |
| [**事件 \_ 系統 \_ MENUPOPUPEND**](event-constants.md)         | [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                |
| [**事件 \_ 系統 \_ MENUSTART**](event-constants.md)               | [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md)                                          |
| [**事件 \_ 系統 \_ MENUEND**](event-constants.md)                   | [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md)                                              |
| [**事件 \_ 系統 \_ 音效**](event-constants.md)                       |                                                                                                                         |
| [**事件 \_ 系統 \_ 警示**](event-constants.md)                       |                                                                                                                         |
| [**事件 \_ 系統 \_ CAPTURESTART**](event-constants.md)         |                                                                                                                         |
| [**事件 \_ 系統 \_ CAPTUREEND**](event-constants.md)             |                                                                                                                         |
| [**事件 \_ 系統 \_ DIALOGSTART**](event-constants.md)           |                                                                                                                         |
| [**事件 \_ 系統 \_ DIALOGEND**](event-constants.md)               |                                                                                                                         |
| [**事件 \_ 系統 \_ MOVESIZESTART**](event-constants.md)       |                                                                                                                         |
| [**事件 \_ 系統 \_ MOVESIZEEND**](event-constants.md)           |                                                                                                                         |
| [**事件 \_ 系統 \_ CONTEXTHELPSTART**](event-constants.md) |                                                                                                                         |
| [**事件 \_ 系統 \_ CONTEXTHELPEND**](event-constants.md)     | 不相關                                                                                                            |
| [**事件 \_ 系統 \_ DRAGDROPSTART**](event-constants.md)       |                                                                                                                         |
| [**事件 \_ 系統 \_ DRAGDROPEND**](event-constants.md)           |                                                                                                                         |
| [**事件 \_ 系統 \_ SWITCHSTART**](event-constants.md)           | 不相關                                                                                                            |
| [**事件 \_ 系統 \_ SWITCHEND**](event-constants.md)               | 不相關                                                                                                            |
| [**事件 \_ 系統 \_ MINIMIZESTART**](event-constants.md)       |                                                                                                                         |
| [**事件 \_ 系統 \_ MINIMIZEEND**](event-constants.md)           |                                                                                                                         |
| [**事件 \_ 系統 \_ 前景**](event-constants.md)             |                                                                                                                         |
| [**事件 \_ 系統 \_ SCROLLINGSTART**](event-constants.md)     | 無法使用                                                                                                           |
| [**事件 \_ 系統 \_ SCROLLINGEND**](event-constants.md)         | 無法使用                                                                                                           |



 



| Object-Level 事件常數                                                           | UI 自動化                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**事件 \_ 物件 \_ 焦點**](event-constants.md)                     | AutomationFocusChangedEvent                                                            |
| [**事件 \_ 物件 \_ VALUECHANGE**](event-constants.md)         | ValueProperty (值控制項模式和 RangeValue 控制項模式)                    |
| [**事件 \_ 物件 \_ 選取範圍**](event-constants.md)             | ElementSelectedEvent (SelectionItem 控制項模式)                                    |
| [**事件 \_ 物件 \_ SELECTIONADD**](event-constants.md)       | ElementAddedToSelectionEvent (SelectionItem 控制項模式)                            |
| [**事件 \_ 物件 \_ SELECTIONREMOVE**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**事件 \_ 物件 \_ SELECTIONWITHIN**](event-constants.md) | EventsSelectionInvalidatedEvent                                                        |
| [**事件 \_ 物件 \_ STATECHANGE**](event-constants.md)         | 請參閱消費者介面自動化屬性和 accState 資料表，以瞭解觸發狀態變更的狀態 |



 

 

 




