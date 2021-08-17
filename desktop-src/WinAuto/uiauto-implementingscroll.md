---
title: 捲軸控制項模式
description: 描述執行 IScrollProvider 的方針和慣例，包括屬性和方法的相關資訊。 捲軸控制項模式用來支援做為子物件集合之可滾動容器的控制項。
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- 消費者介面自動化，執行捲軸控制項模式
- 消費者介面自動化、捲軸控制項模式
- 消費者介面自動化、IScrollProvider
- IScrollProvider
- 執行消費者介面自動化捲軸控制項模式
- 捲軸控制項模式
- 控制項模式，IScrollProvider
- 控制項模式，執行消費者介面自動化捲軸
- 控制項模式、捲軸
- 介面，IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d1cf3c04be18f362a64e619ec4659fac58923f29e6105174057b18a580f8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324390"
---
# <a name="scroll-control-pattern"></a>捲軸控制項模式

描述執行 [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)的方針和慣例，包括屬性和方法的相關資訊。 **滾動** 條控制項模式用來支援做為子物件集合之可滾動容器的控制項。

控制項不一定要使用捲軸來支援滾動功能（雖然通常會這樣做）。 下圖顯示不使用捲軸的滾動控制項。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

![顯示沒有捲軸之滾動控制項的螢幕擷取畫面](images/uia-scrollpattern-without-scrollbars.jpg)

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IScrollProvider** 的必要成員](#required-members-for-iscrollprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在實行 **Scroll** 控制項模式時，請注意下列方針和慣例：

-   此控制項的子系必須執行 [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)。
-   容器控制項的捲軸不支援 **滾動** 條控制項模式。 它們必須改為支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。
-   若捲動是以百分比為單位，則與捲動刻度相關的所有值或數量必須標準化為 0 到 100 之間的範圍。
-   [**IScrollProvider：： HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)屬性和 [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)屬性與 **IsEnabled** 屬性無關。
-   如果 [**IScrollProvider：： HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) 屬性為 **FALSE**，則 [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) 屬性應設定為 100 (100% ) 而 [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) 屬性應設定為 **UIA \_ ScrollPatternNoScroll** (-1) 。 同樣地，如果 [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) 屬性為 **FALSE**，則 [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) 屬性應該設定為 100 (100% ) 而 [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) 屬性應設定為 **UIA \_ ScrollPatternNoScroll** (-1) 。 這可讓 Microsoft 消費者介面自動化用戶端在 [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) 方法中使用這些屬性值，同時避免在用戶端不感興趣的方向啟動時，才會發生競爭情況。
-   [**IScrollProvider：： HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent)屬性是地區設定特有的。 將 **HorizontalScrollPercent** 設定為100時，必須將控制項的滾動位置設定為對等語言的最右邊位置，例如從左至右讀取的英文。 或者，如果是由右至左的阿拉伯文語言，將 **HorizontalScrollPercent** 設定為100，就必須將滾動位置設定為最左邊的位置。

## <a name="required-members-for-iscrollprovider"></a>**IScrollProvider** 的必要成員

執行 [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) 介面需要下列屬性和方法。



| 必要成員                                                                  | 成員類型 | 備註 |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | 屬性    | 無  |
| [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | 屬性    | 無  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | 屬性    | 無  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | 屬性    | 無  |
| [**HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | 屬性    | 無  |
| [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | 屬性    | 無  |
| [**捲動**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | 方法      | 無  |
| [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




