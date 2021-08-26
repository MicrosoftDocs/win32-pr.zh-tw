---
title: ExpandCollapse 控制項模式
description: 描述執行 IExpandCollapseProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- 消費者介面自動化，執行 ExpandCollapse 控制項模式
- 消費者介面自動化，ExpandCollapse 控制項模式
- 消費者介面自動化、IExpandCollapseProvider
- IExpandCollapseProvider
- 執行消費者介面自動化 ExpandCollapse 控制項模式
- ExpandCollapse 控制項模式
- 控制項模式，IExpandCollapseProvider
- 控制模式，消費者介面自動化執行 ExpandCollapse
- 控制項模式，ExpandCollapse
- 介面，IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7fa1461110a7fcdee83b8b3c20c15653e7bd5740187b89337620f5410b2bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998038"
---
# <a name="expandcollapse-control-pattern"></a>ExpandCollapse 控制項模式

描述執行 [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。 **ExpandCollapse** 控制項模式是用來支援以視覺化方式展開以顯示更多內容和折迭以隱藏內容的控制項。

如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IExpandCollapseProvider** 的必要成員](#required-members-for-iexpandcollapseprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **ExpandCollapse** 控制項模式時，請注意下列方針和慣例：

-   匯總控制項（以提供 UI 擴充/折迭功能的子物件所建立）必須支援 **ExpandCollapse** 控制項模式，而其子項目則否。 例如，下拉式方塊控制項是使用清單方塊、按鈕和編輯控制項的組合所建立，但它只是必須支援 **ExpandCollapse** 控制項模式的父下拉式方塊。
    > [!Note]  
    > 例外狀況是功能表控制項，這是個別功能表項目物件的匯總。 功能表項目物件可以支援 **ExpandCollapse** 控制項模式，但是父功能表控制項則不能。 樹狀結構和樹狀目錄專案控制項會套用類似的例外狀況。

     

-   當控制項的 [**IExpandCollapseProvider：： ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) 設定為 **ExpandCollapseState \_ LeafNode** 時，控制項的任何 **ExpandCollapse** 功能目前為非使用中狀態，而且可以使用此控制項模式取得的唯一資訊是 **ExpandCollapseState**。 如果後續新增任何子物件，則會啟用 **ExpandCollapseState** 變更和 **ExpandCollapse** 功能。
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) 只是指直屬子物件的可見度;它不會參考所有子系物件的可見度。
-   [**IExpandCollapseProvider：： Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) 和 [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) 功能是控制項特定的。 以下是此行為的範例：
    -   Office 的個人功能表可以是三個狀態的功能表項目 ( 「展開」、「折迭」和「PartiallyExpanded」 ) 其中控制項指定在呼叫 [**展開**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)[**或折迭時要**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)採用的狀態。
    -   在樹狀目錄專案上呼叫 [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) 可能會顯示所有子系或只顯示立即的子系。
    -   如果呼叫控制項的 [**展開**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)[**或折**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)迭維持其子系的狀態，則應該傳送可見度變更事件，而不是狀態變更事件。 如果父控制項在折迭時不維持其子系的狀態，控制項可能會損毀所有不再可見的子系，並引發終結的事件;或者，它可能會變更每個子代的 [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) ，並引發可見度變更事件。
-   為了保證導覽，在 Microsoft 消費者介面自動化樹狀結構 (中，不論其父系 [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)為何，都需要有適當的可見度狀態) 的物件。 如果子系是依需求產生的，則它們可能只會在第一次顯示時出現在消費者介面自動化樹狀結構中，或只在顯示時出現。

## <a name="required-members-for-iexpandcollapseprovider"></a>**IExpandCollapseProvider** 的必要成員

執行 [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) 介面需要下列屬性、方法和事件。



| 必要成員                                                                                    | 成員類型 | 備註                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | 屬性    | 無                                                                   |
| [**展開**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | 方法      | 無                                                                   |
| [**摺疊**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | 方法      | 無                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | 事件       | 此控制項沒有相關聯的事件;使用這個一般事件處理常式。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




