---
title: 消費者介面自動化和 Active Accessibility
description: Microsoft Active Accessibility 是 Windows 95 中引進的舊版 API，其設計目的是讓 Windows 應用程式可供存取。
ms.assetid: 6fc92e67-b94b-4ba3-9f5d-42be6072f110
keywords:
- 消費者介面自動化，Microsoft Active Accessibility
- 消費者介面自動化，協助工具
- 消費者介面自動化，Active Accessibility
- 消費者介面自動化，程式設計語言
- 消費者介面自動化，樹狀檢視
- 消費者介面自動化，導覽
- 消費者介面自動化、控制項類型
- 協助工具
- Active Accessibility
- Microsoft Active Accessibility
- 控制項類型，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5e6b1ba80fb2c44b8c08753fa1fb43173843eb
ms.sourcegitcommit: b0bb3e2918aec9daae6a68bb03494f0c5cdf3902
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/02/2020
ms.locfileid: "106965676"
---
# <a name="ui-automation-and-active-accessibility"></a>消費者介面自動化和 Active Accessibility

Microsoft Active Accessibility 是 Windows 95 中引進的舊版 API，其設計目的是讓 Windows 應用程式可供存取。 Microsoft 消費者介面自動化是 Windows 的新協助工具模型，目的是要解決輔助技術產品和自動化測試控管的需求。 消費者介面自動化在 Microsoft Active Accessibility 方面提供了許多改進功能。 本主題說明這兩種技術之間的差異。

本主題包含下列各節。

-   [程式設計語言](#programming-languages)
-   [伺服器和用戶端](#servers-and-clients)
-   [UI 元素](#ui-elements)
-   [樹狀檢視和導覽](#tree-views-and-navigation)
-   [角色和控制項類型](#roles-and-control-types)
-   [狀態和屬性](#states-and-properties)
-   [事件](#events)
-   [從消費者介面自動化存取 Active Accessibility 屬性和物件](#accessing-active-accessibility-properties-and-objects-from-ui-automation)
-   [相關主題](#related-topics)

## <a name="programming-languages"></a>程式語言：

Microsoft Active Accessibility 是以元件物件模型為基礎， (COM) ，並支援雙重介面，因此可在 C/c + + 和指令碼語言中進行程式設計。

當導入消費者介面自動化時，用戶端 API 會限制為 managed 程式碼，而提供者 API 則包含受控和非受控的實作為。 在 Windows 7 中，引進了新的 COM 型用戶端 API，讓您更輕鬆地在 C/c + + 中編寫消費者介面自動化用戶端應用程式的程式。

## <a name="servers-and-clients"></a>伺服器和用戶端

在 Microsoft Active Accessibility 中，伺服器和用戶端會直接進行通訊，主要是透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的伺服器執行。

在消費者介面自動化中，核心服務位於伺服器 (提供者) 與用戶端之間。 核心服務會呼叫提供者所執行的介面，並提供其他服務，例如為 UI 專案產生唯一執行時間識別碼。 用戶端應用程式會藉由建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) 物件來取得此核心服務的存取權。 此物件支援一組與提供者介面不同的用戶端介面。 如需詳細資訊，請參閱 [建立 CUIAutomation 物件](uiauto-creatingcuiautomation.md)。

消費者介面自動化提供者可以提供資訊給 Microsoft Active Accessibility 用戶端，Microsoft Active Accessibility 伺服器可以提供資訊給消費者介面自動化用戶端應用程式。 不過，由於 Microsoft Active Accessibility 不會公開消費者介面自動化的資訊，因此這兩個模型並不完全相容。

## <a name="ui-elements"></a>UI 項目

Microsoft Active Accessibility 會將 UI 元素顯示為與子識別碼配對的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 很難比較兩個 **IAccessible** 指標，判斷它們是否參考相同的元素。

在消費者介面自動化中，每個元素都會以物件的形式呈現，以將 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面公開給用戶端。 您可以使用 [**IUIAutomationElement：： GetRuntimeId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getruntimeid)來比較專案，以其執行時間識別碼進行比較。

## <a name="tree-views-and-navigation"></a>樹狀檢視和導覽

畫面上的 UI 元素可視為樹狀結構，其中包含做為根的桌面、應用程式視窗為直屬子系，以及應用程式內的元素做為進一步的子系。

在 Microsoft Active Accessibility 中，會在樹狀結構中公開許多與使用者無關的 UI 元素。 用戶端應用程式必須檢查樹狀結構中的所有元素，以判斷哪些元素有意義。

消費者介面自動化用戶端應用程式會透過篩選視圖來查看 UI。 此視圖只包含可提供資訊給使用者的元素，或使用者可以與之互動的專案。 預先定義的視圖只包含 control 元素，而且只有 content 元素可用，而且用戶端應用程式可以定義自訂的視圖。 消費者介面自動化可讓您更輕鬆地向使用者描述 UI，以及協助使用者與應用程式互動。

在 Microsoft Active Accessibility 中，專案之間的導覽是空間，例如移至畫面左邊的元素，例如，將移至下一個功能表項目或對話方塊中定位順序的下一個專案，或階層式，例如移至容器中的第一個子專案，或從子項目移至其父元素。 階層式導覽很複雜，因為子項目不一定是可執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的物件。

在消費者介面自動化中，所有 UI 元素都是公開 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面並支援相同基本功能的 COM 物件。 從提供者的觀點來看，COM 物件會執行繼承自 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)的介面。 流覽主要是階層式;也就是說，從父代到子系，以及從一個同級到下一個。 不過，同級之間的導覽具有邏輯元素，因為它可能會遵循定位順序。 用戶端可以使用 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)，透過樹狀結構的任何篩選視圖，從任何起點進行導覽。 用戶端也可以使用 [**IUIAutomationElement：： FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) 和 [**IUIAutomationElement：： FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)，流覽至特定的子系或子系。 例如，您可以輕鬆地取出支援指定控制項模式之對話方塊中的所有元素。

消費者介面自動化中的導覽比 Microsoft Active Accessibility 更一致。 某些專案，例如下拉式清單和快顯視窗，會在 Microsoft Active Accessibility 樹狀結構中出現兩次，而從這些元素流覽可能會產生非預期的結果。 您很難針對 Rebar 控制項正確地執行 Microsoft Active Accessibility。 消費者介面自動化可進行 reparenting 和重新置放，讓專案可以放在樹狀結構中的任何位置，儘管階層的擁有權是由 windows 的擁有權組成。

## <a name="roles-and-control-types"></a>角色和控制項類型

Microsoft Active Accessibility 使用 accRole 屬性 ([**IAccessible：： get \_ AccRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)) 來抓取 UI 中的元素角色描述，例如 [**角色 \_ 系統 \_ 滑杆**](object-roles.md) 或 [**角色 \_ 系統 \_ MENUITEM**](object-roles.md)。 從項目的角色可以了解他所能使用的功能。 您可以使用固定方法（例如 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 和 [**IAccessible：： accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)）來與控制項互動。 用戶端應用程式和 UI 之間的互動僅限於可透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)完成的工作。

相反地，消費者介面自動化會將元素的控制項類型（由 [**IUIAutomationElement：： CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (或 [**IUIAutomationElement：： CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) 屬性所描述）從其預期的功能中分離出來。 功能是由提供者透過其特定介面實作所支援的控制項模式來判斷。 您可以結合控制項模式來描述特定 UI 元素所支援的完整功能集。 有些提供者必須支援特定的控制項模式。 例如，核取方塊的提供者必須支援 [切換](uiauto-implementingtoggle.md) 控制項模式。 需要有其他提供者，才能支援一或多個控制項模式。 例如，按鈕必須支援切換或叫 [用控制項模式](uiauto-implementinginvoke.md) 。 其他人仍不支援任何控制項模式。 例如，無法移動、調整大小或停駐的窗格都沒有控制項模式。

消費者介面自動化支援自訂控制項，這些控制項是由 [**UIA \_ CustomControlTypeId**](uiauto-controltype-ids.md) 常數所識別，並可透過 [**IUIAutomationElement：： CurrentLocalizedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentlocalizedcontroltype) (或 [**IUIAutomationElement：： CachedLocalizedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedlocalizedcontroltype)) 屬性來描述。

下表將 Microsoft Active Accessibility[物件角色](object-roles.md) 對應至消費者介面自動化控制項類型。



| Active Accessibility 角色                                                   | 消費者介面自動化控制項類型                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**角色 \_ 系統 \_ 按鍵**](object-roles.md)     | [按鈕](uiauto-supportbuttoncontroltype.md)                                                  |
| [**角色 \_ 系統 \_ 用戶端**](object-roles.md)             | [Calendar](uiauto-supportcalendarcontroltype.md)                                              |
| [**角色 \_ 系統 \_ CHECKBUTTON**](object-roles.md)   | [CheckBox](uiauto-supportcheckboxcontroltype.md)                                              |
| [**角色 \_ 系統 \_ COMBOBOX**](object-roles.md)         | [ComboBox](uiauto-supportcomboboxcontroltype.md)                                              |
| [**角色 \_ 系統 \_ 用戶端**](object-roles.md)             | 請參閱 [自訂控制項類型](uiauto-designingcustompropseventpatterns.md)。 |
| [**角色 \_ 系統 \_ 清單**](object-roles.md)                 | [DataGrid](uiauto-supportdatagridcontroltype.md)                                              |
| [**角色 \_ 系統 \_**](object-roles.md)         | [DataItem](uiauto-supportdataitemcontroltype.md)                                              |
| [**角色 \_ 系統 \_ 檔**](object-roles.md)         | [文件](uiauto-supportdocumentcontroltype.md)                                              |
| [**角色 \_ 系統 \_ 文字**](object-roles.md)                 | [編輯](uiauto-supporteditcontroltype.md)                                                      |
| [**角色 \_ 系統 \_ 群組**](object-roles.md)         | [群組](uiauto-supportgroupcontroltype.md)                                                    |
| [**角色 \_ 系統 \_ 清單**](object-roles.md)                 | [標頭](uiauto-supportheadercontroltype.md)                                                  |
| [**角色 \_ 系統 \_ COLUMNHEADER**](object-roles.md) | [HeaderItem](uiauto-supportheaderitemcontroltype.md)                                          |
| [**角色 \_ 系統 \_ 連結**](object-roles.md)                 | [超連結](uiauto-supporthyperlinkcontroltype.md)                                            |
| [**角色 \_ 系統 \_ 圖形**](object-roles.md)           | [影像](uiauto-supportimagecontroltype.md)                                                    |
| [**角色 \_ 系統 \_ 清單**](object-roles.md)                 | [清單](uiauto-supportlistcontroltype.md)                                                      |
| [**角色 \_ 系統 \_**](object-roles.md)         | [ListItem](uiauto-supportlistitemcontroltype.md)                                              |
| [**角色 \_ 系統 \_ MENUPOPUP**](object-roles.md)       | [功能表](uiauto-supportmenucontroltype.md)                                                      |
| [**角色 \_ 系統 \_ 功能表列**](object-roles.md)           | [MenuBar](uiauto-supportmenubarcontroltype.md)                                                |
| [**角色 \_ 系統 \_ MENUITEM**](object-roles.md)         | [MenuItem](uiauto-supportmenuitemcontroltype.md)                                              |
| [**角色 \_ 系統 \_ 窗格**](object-roles.md)                 | [窗格](uiauto-supportpanecontroltype.md)                                                      |
| [**角色 \_ 系統 \_ PROGRESSBAR**](object-roles.md)   | [進度列](uiauto-supportprogressbarcontroltype.md)                                        |
| [**角色 \_ 系統 \_ 選項按鈕**](object-roles.md)   | [RadioButton](uiauto-supportradiobuttoncontroltype.md)                                        |
| [**角色 \_ 系統 \_ 捲軸**](object-roles.md)       | [ScrollBar](uiauto-supportscrollbarcontroltype.md)                                            |
| [**角色 \_ 系統 \_ 分隔符號**](object-roles.md)       | [Separator](uiauto-supportseparatorcontroltype.md)                                            |
| [**角色 \_ 系統 \_ 滑杆**](object-roles.md)             | [滑桿](uiauto-supportslidercontroltype.md)                                                  |
| [**角色系統已進行數值 \_ \_ 調節**](object-roles.md)     | [Spinner](uiauto-supportspinnercontroltype.md)                                                |
| [**角色 \_ 系統 \_ SPLITBUTTON**](object-roles.md)   | [SplitButton](uiauto-supportsplitbuttoncontroltype.md)                                        |
| [**角色 \_ 系統 \_ 狀態列**](object-roles.md)       | [StatusBar](uiauto-supportstatusbarcontroltype.md)                                            |
| [**角色 \_ 系統 \_ PAGETABLIST**](object-roles.md)   | [Tab](uiauto-supporttabcontroltype.md)                                                        |
| [**角色 \_ 系統 \_ PAGETAB**](object-roles.md)           | [TabItem](uiauto-supporttabitemcontroltype.md)                                                |
| [**角色 \_ 系統 \_ 資料表**](object-roles.md)               | [資料表](uiauto-supporttablecontroltype.md)                                                    |
| [**角色 \_ 系統 \_ STATICTEXT**](object-roles.md)     | [Text](uiauto-supporttextcontroltype.md)                                                      |
| [**角色 \_ 系統 \_ 指標**](object-roles.md)       | [拇指](uiauto-supportthumbcontroltype.md)                                                    |
| [**角色 \_ 系統 \_ 標題列**](object-roles.md)         | [標題列](uiauto-supporttitlebarcontroltype.md)                                              |
| [**角色 \_ 系統 \_ 工具列**](object-roles.md)           | [工具 欄](uiauto-supporttoolbarcontroltype.md)                                                |
| [**角色 \_ 系統 \_ 工具提示**](object-roles.md)           | [ToolTip](uiauto-supporttooltipcontroltype.md)                                                |
| [**角色 \_ 系統 \_ 大綱**](object-roles.md)           | [樹狀結構](uiauto-supporttreecontroltype.md)                                                      |
| [**角色 \_ 系統 \_ OUTLINEITEM**](object-roles.md)   | [TreeItem](uiauto-supporttreeitemcontroltype.md)                                              |
| [**角色 \_ 系統 \_ 視窗**](object-roles.md)             | [Window](uiauto-supportwindowcontroltype.md)                                                  |



 

## <a name="states-and-properties"></a>狀態和屬性

Microsoft Active Accessibility 元素支援一組通用屬性。 某些屬性（例如 accState）必須根據元素角色來描述不同的條件。 伺服器必須執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 的所有方法，以傳回屬性，甚至是與元素無關的屬性。

消費者介面自動化定義額外的屬性，其中某些屬性會對應至 Microsoft Active Accessibility 中的狀態。 某些屬性通用於所有元素，但其他屬性則是控制項類型和控制項模式的特定屬性。 消費者介面自動化提供者不需要執行不相關的屬性，但可能會針對不支援的任何屬性傳回 null 值。 消費者介面自動化的核心服務可以從預設視窗提供者取得一些屬性，並使用提供者明確執行的屬性來合併這些屬性。

除了支援更多屬性之外，消費者介面自動化可讓您快取屬性，以提供更好的效能。

下表顯示兩個模型中某些屬性之間的對應。 如需消費者介面自動化屬性 Id 的描述，請參閱 [Automation 元素屬性識別碼](uiauto-automation-element-propids.md)。



| Active Accessibility 屬性存取子                                               | 消費者介面自動化屬性識別碼                                                                                                                                                                                | 備註                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | [**UIA \_AccessKeyPropertyId**](uiauto-automation-element-propids.md)或 [ **UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md) | [**UIA \_**](uiauto-automation-element-propids.md)如果兩者都存在，AccessKeyPropertyId 會優先使用。                                                                                                                                                                                                         |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                                                                                                      |                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                                                                                                        | 請參閱上表，以將角色對應至控制項類型。                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md)或 [ **UIA \_ RangeValueValuePropertyId**](uiauto-control-pattern-propids.md)   | 僅對支援 [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) 或 [**IUIAutomationRangeValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationrangevaluepattern)的控制項類型有效。 範圍值會正規化為0-100，以符合 Microsoft Active Accessibility 行為。 值會表示為字串。 |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                                                                                                              |                                                                                                                                                                                                                                                                                                                                             |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)                          | [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)                                                                                            |                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | 不支援。                                                                                                                                                                                           | accDescription 在 Microsoft Active Accessibility 中沒有明確的規格，導致伺服器將不同的資訊片段放在這個屬性中。                                                                                                                                                                    |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | 不支援。                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                             |



 

下表顯示對應至 Microsoft Active Accessibility [物件狀態常數](object-state-constants.md)的消費者介面自動化屬性識別碼。



| Active Accessibility 狀態                                                                    | 消費者介面自動化屬性                                                                                                                                                                                                                                                                                                                                                               | 觸發程式 New-winevent 狀態變更？ |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [**狀態 \_ 系統 \_ 已核取**](object-state-constants.md)                 | [**UIA \_[ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) ] 核取方塊。 [**UIA \_**](uiauto-control-pattern-propids.md)選項按鈕的 SelectionItemIsSelectedPropertyId。                                                                                                                   | Y                               |
| [**狀態系統已折迭 \_ \_**](object-state-constants.md)             | [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) (value = [**ExpandCollapseState \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-expandcollapsestate) 折迭的) 。                                                                                                                         | Y                               |
| [**狀態 \_ 系統已 \_ 展開**](object-state-constants.md)               | [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) (value = [**ExpandCollapseState \_ 加寬**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-expandcollapsestate) 或 [**ExpandCollapseState \_ PartiallyExpanded**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-expandcollapsestate)) 。 | Y                               |
| [**狀態 \_ 系統可 \_ 設定焦點**](object-state-constants.md)             | [**UIA \_IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)。                                                                                                                                                                                                                                                                   | N                               |
| [**以狀態 \_ 系統為 \_ 焦點**](object-state-constants.md)                 | [**UIA \_HasKeyboardFocusPropertyId**](uiauto-automation-element-propids.md)。                                                                                                                                                                                                                                                                         | N                               |
| [**狀態 \_ 系統 \_ HASPOPUP**](object-state-constants.md)               | [**UIA \_**](uiauto-control-pattern-propids.md)功能表項目的 ExpandCollapseExpandCollapseStatePropertyId。                                                                                                                                                                                                                           | N                               |
| [**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md)             | [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) (value = True， [**IUIAutomationElement：： GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)) 失敗。                                                                                                                                                         | N                               |
| [**狀態 \_ 系統 \_ 連結**](object-state-constants.md)                   | [**UIA \_ControlTypePropertyId**](uiauto-automation-element-propids.md) (value = [**UIA \_ HyperlinkControlTypeId**](uiauto-controltype-ids.md)) 。                                                                                                                                                                                | N                               |
| [**狀態 \_ 系統 \_ 混合**](object-state-constants.md)                     | [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) (值 = [**ToggleState \_ 不定**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)。                                                                                                                                                                              | N                               |
| [**狀態 \_ 系統 \_ 可移動**](object-state-constants.md)               | [**UIA \_TransformCanMovePropertyId**](uiauto-control-pattern-propids.md)。                                                                                                                                                                                                                                                                            | N                               |
| [**狀態 \_ 系統 \_ MULTISELECTABLE**](object-state-constants.md) | [**UIA \_SelectionCanSelectMultiplePropertyId**](uiauto-control-pattern-propids.md)。                                                                                                                                                                                                                                                        | N                               |
| [**狀態 \_ 系統 \_ 外**](object-state-constants.md)             | [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md)。                                                                                                                                                                                                                                                                                   | N                               |
| [**狀態 \_ 系統 \_ 受保護**](object-state-constants.md)             | [**UIA \_IsPasswordPropertyId**](uiauto-automation-element-propids.md)。                                                                                                                                                                                                                                                                                     | N                               |
| [**狀態 \_ 系統 \_ READONLY**](object-state-constants.md)               | [**UIA \_RangeValueIsReadOnlyPropertyId**](uiauto-control-pattern-propids.md) 和 [**UIA \_ ValueIsReadOnlyPropertyId**](uiauto-control-pattern-propids.md)。                                                                                                                                                         | N                               |
| [**狀態 \_ 系統可 \_ 選取**](object-state-constants.md)           | [**UIA \_IsSelectionItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) 。                                                                                                                                                                                                                                | N                               |
| [**選取的狀態 \_ 系統 \_**](object-state-constants.md)               | [**UIA \_SelectionItemIsSelectedPropertyId**](uiauto-control-pattern-propids.md)。                                                                                                                                                                                                                                                              | N                               |
| [**狀態 \_ 系統 \_ 相當大**](object-state-constants.md)               | [**UIA \_TransformCanResizePropertyId**](uiauto-control-pattern-propids.md)。                                                                                                                                                                                                                                                                        | N                               |
| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)         | [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md)。                                                                                                                                                                                                                                                                                       | Y                               |



 

如需屬性 Id 的完整清單，請參閱 [屬性識別碼](uiauto-entry-propids.md)。

## <a name="events"></a>事件

不同于 Microsoft Active Accessibility，消費者介面自動化中的事件機制並不依賴 Windows 事件路由（與視窗控制碼緊密系結），也不需要用戶端應用程式設定勾點。 事件的訂閱可以微調至樹狀結構的特定部分，而不只是針對特定的事件。 提供者也可以藉由追蹤要接聽的事件，來微調引發事件。

用戶端也可以更輕鬆地抓取引發事件的元素，因為這些專案會直接傳遞給事件回呼。 如果在用戶端訂閱事件時提供快取要求，則會自動預先提取專案的屬性。

下表顯示 Microsoft Active Accessibility [事件常數](event-constants.md) 和消費者介面自動化事件識別碼的對應。



| WinEvent                                                                                   | 消費者介面自動化事件識別碼                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**事件 \_ 物件 \_ ACCELERATORCHANGE**](event-constants.md) | [**UIA \_AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md) 屬性變更。                                                                                                                                                                                            |
| [**事件 \_ 物件 \_ CONTENTSCROLLED**](event-constants.md)     | [**UIA \_**](uiauto-control-pattern-propids.md)關聯捲軸上的 ScrollVerticalScrollPercentPropertyId 或 [**UIA \_ ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)屬性變更。 |
| [**\_建立事件物件 \_**](event-constants.md)                       | [**UIA \_StructureChangedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                               |
| [**事件 \_ 物件 \_ DEFACTIONCHANGE**](event-constants.md)     | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 物件 \_ DESCRIPTIONCHANGE**](event-constants.md) | 沒有完全相同的專案;可能是 [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md) 或 [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) 屬性變更。                                                    |
| [**事件 \_ 物件損 \_ 毀**](event-constants.md)                     | [**UIA \_StructureChangedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                               |
| [**事件 \_ 物件 \_ 焦點**](event-constants.md)                         | [**UIA \_AutomationFocusChangedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                   |
| [**事件 \_ 物件 \_ HELPCHANGE**](event-constants.md)               | [**UIA \_HelpTextPropertyId**](uiauto-automation-element-propids.md) 變更。                                                                                                                                                                                                                 |
| [**事件 \_ 物件 \_ 隱藏**](event-constants.md)                           | [**UIA \_StructureChangedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                               |
| [**事件 \_ 物件 \_ LOCATIONCHANGE**](event-constants.md)       | [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更。                                                                                                                                                                                      |
| [**事件 \_ 物件 \_ NAMECHANGE**](event-constants.md)               | [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更。                                                                                                                                                                                                                |
| [**事件 \_ 物件 \_ PARENTCHANGE**](event-constants.md)           | [**UIA \_StructureChangedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                               |
| [**事件 \_ 物件 \_ 重新排序**](event-constants.md)                     | Microsoft Active Accessibility 不一致地使用。 消費者介面自動化中未定義任何直接對應的事件。                                                                                                                                                                                               |
| [**事件 \_ 物件 \_ 選取範圍**](event-constants.md)                 | [**UIA \_SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                    |
| [**事件 \_ 物件 \_ SELECTIONADD**](event-constants.md)           | [**UIA \_SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)。                                                                                                                                                                                    |
| [**事件 \_ 物件 \_ SELECTIONREMOVE**](event-constants.md)     | [**UIA \_SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)。                                                                                                                                                                            |
| [**事件 \_ 物件 \_ SELECTIONWITHIN**](event-constants.md)     | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 物件 \_ 顯示**](event-constants.md)                           | [**UIA \_StructureChangedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                               |
| [**事件 \_ 物件 \_ STATECHANGE**](event-constants.md)             | 各種屬性變更的事件。                                                                                                                                                                                                                                                                                    |
| [**事件 \_ 物件 \_ VALUECHANGE**](event-constants.md)             | [**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 和 [**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md) 已變更。                                                                                                    |
| [**事件 \_ 系統 \_ 警示**](event-constants.md)                         | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ CAPTUREEND**](event-constants.md)               | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ CAPTURESTART**](event-constants.md)           | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ CONTEXTHELPEND**](event-constants.md)       | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ CONTEXTHELPSTART**](event-constants.md)   | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ DIALOGEND**](event-constants.md)                 | [**UIA \_視窗 \_ WindowClosedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                        |
| [**事件 \_ 系統 \_ DIALOGSTART**](event-constants.md)             | [**UIA \_視窗 \_ WindowOpenedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                        |
| [**事件 \_ 系統 \_ DRAGDROPEND**](event-constants.md)             | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ DRAGDROPSTART**](event-constants.md)         | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ 前景**](event-constants.md)               | [**UIA \_AutomationFocusChangedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                   |
| [**事件 \_ 系統 \_ MENUEND**](event-constants.md)                     | [**UIA \_MenuModeEndEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                                         |
| [**事件 \_ 系統 \_ MENUPOPUPEND**](event-constants.md)           | [**UIA \_MenuClosedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                                           |
| [**事件 \_ 系統 \_ MENUPOPUPSTART**](event-constants.md)       | [**UIA \_MenuOpenedEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                                           |
| [**事件 \_ 系統 \_ MENUSTART**](event-constants.md)                 | [**UIA \_MenuModeStartEventId**](uiauto-event-ids.md)。                                                                                                                                                                                                                                     |
| [**事件 \_ 系統 \_ MINIMIZEEND**](event-constants.md)             | [**UIA \_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                             |
| [**事件 \_ 系統 \_ MINIMIZESTART**](event-constants.md)         | [**UIA \_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                             |
| [**事件 \_ 系統 \_ MOVESIZEEND**](event-constants.md)             | [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更。                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ MOVESIZESTART**](event-constants.md)         | [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更。                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ SCROLLINGEND**](event-constants.md)           | [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 或 [**UIA \_ ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                               |
| [**事件 \_ 系統 \_ SCROLLINGSTART**](event-constants.md)       | [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 或 [**UIA \_ ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                               |
| [**事件 \_ 系統 \_ 音效**](event-constants.md)                         | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| [**事件 \_ 系統 \_ SWITCHEND**](event-constants.md)                 | 沒有對等專案，但 [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md) 事件表示新的應用程式已收到焦點。                                                                                                                                  |
| [**事件 \_ 系統 \_ SWITCHSTART**](event-constants.md)             | 沒有同等項目。                                                                                                                                                                                                                                                                                                      |
| 沒有同等項目。                                                                             | [**UIA \_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                             |
| 沒有同等項目。                                                                             | [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                   |
| 沒有同等項目。                                                                             | [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                       |
| 沒有同等項目。                                                                             | [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                 |
| 沒有同等項目。                                                                             | [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                     |
| 沒有同等項目。                                                                             | [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                           |
| 沒有同等項目。                                                                             | [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                               |
| 沒有同等項目。                                                                             | [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更。                                                                                                                                                                                         |
| 沒有同等項目。                                                                             | [**UIA \_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更                                                                                                                                                                              |
| 沒有同等項目。                                                                             | [**UIA \_AsyncContentLoadedEventId**](uiauto-event-ids.md) 事件。                                                                                                                                                                                                                     |
| 沒有同等項目。                                                                             | [**UIA \_ToolTipOpenedEventId**](uiauto-event-ids.md) 事件。                                                                                                                                                                                                                               |



 

## <a name="accessing-active-accessibility-properties-and-objects-from-ui-automation"></a>從消費者介面自動化存取 Active Accessibility 屬性和物件

Microsoft Active Accessibility 中未提供消費者介面自動化的主要功能是能夠以單一跨進程作業提取多個屬性。

現有 Microsoft Active Accessibility 用戶端可以使用 [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) 介面來利用這項功能。 這個介面代表 *控制項模式* ，可公開 UI 專案上的 Microsoft Active Accessibility 屬性和方法。 在抓取專案時，應用程式可以要求快取這個控制項模式及其屬性。

[**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) 也可讓用戶端從沒有 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)原生支援的元素取得 Microsoft Active Accessibility 屬性。

[**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)屬性中的變更不會引發消費者介面自動化事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將消費者介面自動化功能新增至 Active Accessibility 伺服器](uiauto-usingiaccessibleex.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> <dt>

[Microsoft Active Accessibility](microsoft-active-accessibility.md)
</dt> </dl>

 

 
