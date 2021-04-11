---
title: 選取控制項模式
description: 描述執行 ISelectionProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- 消費者介面自動化，執行選取控制項模式
- 消費者介面自動化，選取控制項模式
- 消費者介面自動化、ISelectionProvider
- ISelectionProvider
- 執行消費者介面自動化選取控制項模式
- 選取控制項模式
- 控制項模式，ISelectionProvider
- 控制項模式，執行消費者介面自動化選取專案
- 控制項模式，選取
- 介面，ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021507"
---
# <a name="selection-control-pattern"></a>選取控制項模式

描述執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。 **選取** 控制項模式用來支援控制項，這些控制項可作為可選取之子專案集合的容器。 這個元素的子系必須執行 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)。

如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ISelectionProvider** 的必要成員](#required-members-for-iselectionprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **選取** 控制項模式時，請注意下列方針和慣例：

-   執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 的控制項允許選取單一或多個子專案。 例如，清單方塊、清單視圖和樹狀檢視支援多重選取，而下拉式方塊、滑杆和選項按鈕群組則支援單一選取。
-   具有最小值、最大值和連續範圍的控制項（例如媒體播放機的 **音量** 滑杆控制項）應該執行 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) ，而不是 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)。
-   單一選取控制項，可管理執行 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)的子控制項，例如 Windows 的 [**顯示內容**] 對話方塊中的 [**螢幕解析度**] 滑杆，或 Microsoft Word (的 **色彩選擇器** 選取控制項，請參閱下列影像) ，應執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider);其子系應同時執行 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)和 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)。

    ![顯示色樣字串對應範例的影像](images/uia-valuepattern-colorpicker.jpg)

-   功能表不支援 **選取** 控制項模式。 如果您使用的功能表項目包括圖形和文字 (例如 Microsoft Outlook 的 [ **View** ] 功能表中的 [**預覽] 窗格** 專案) 而且需要傳達狀態，則您應該執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)。

## <a name="required-members-for-iselectionprovider"></a>**ISelectionProvider** 的必要成員

執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 介面需要下列屬性、方法和事件。



| 必要成員                                                                                | 成員類型 | 備註                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | 屬性    | 無                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | 屬性    | 無                                                                        |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | 方法      | 無                                                                        |
| [**UIA \_ 選取專案 \_ InvalidatedEventId**](uiauto-event-ids.md) | 事件       | 當容器中的選取範圍大幅變更時，引發此事件。 |



 

[**ISelectionProvider：： IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)和 [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)屬性可以是動態的。 例如，控制項的初始狀態可能沒有任何預設選取的專案，表示 **IsSelectionRequired** 為 false。 不過，在選取項目之後，控制項就必須至少有一個項目一律保持為選取。 同樣地，在極少數的情況下，控制項可能會允許最初選取多個項目，但之後就只允許單一選取。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[SelectionItem 控制項模式](uiauto-implementingselectionitem.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




