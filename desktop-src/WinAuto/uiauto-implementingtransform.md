---
title: 轉換控制項模式
description: 描述執行 ITransformProvider 和 ITransformProvider2 的指導方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- 消費者介面自動化，執行轉換控制項模式
- 消費者介面自動化，轉換控制項模式
- 消費者介面自動化、ITransformProvider
- ITransformProvider
- 執行消費者介面自動化轉換控制項模式
- 轉換控制項模式
- 控制項模式，ITransformProvider
- 控制模式，實施消費者介面自動化轉換
- 控制項模式，轉換
- 介面，ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5aceefa7d482cbbe6d9b1612c1fb9c65081796113e527d5122274ce5d8f8215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826834"
---
# <a name="transform-control-pattern"></a>轉換控制項模式

描述執行 [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 和 [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2)的指導方針和慣例，包括屬性和方法的相關資訊。 轉換控制項模式用來支援可在二維空間內移動、調整大小或旋轉的控制項。

如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ITransformProvider** 的必要成員](#required-members-for-itransformprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **轉換** 控制項模式時，請注意下列方針和慣例：

-   此控制項模式的支援不限於桌面上的物件。 若容器物件的子項可以自由在容器的範圍內移動、調整大小或旋轉，則這些子項也必須支援此控制項模式。
-   如果物件最後在螢幕上的位置完全在其容器的座標以外，而鍵盤或滑鼠存取不到的話，就無法移動、調整大小或旋轉物件 (例如，最上層的視窗移離螢幕，或是子物件移到容器檢視區範圍以外的地方)。 在這種情況下，物件會放置到最接近所要求螢幕座標的地方，其上方或左方座標會覆寫成容器範圍內的座標。
-   針對多監視器系統，若物件移動、調整大小或旋轉後的位置完全超出合併桌面螢幕座標的範圍，物件就會移至主要監視器上最接近所要求座標的位置。
-   所有參數和屬性值都是絕對值，不受地區設定影響。

## <a name="required-members-for-itransformprovider"></a>**ITransformProvider** 的必要成員

執行 [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 介面需要下列屬性和方法。



| 必要成員                                         | 成員類型 | 備註 |
|----------------------------------------------------------|-------------|-------|
| [**CanMove**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | 屬性    | 無  |
| [**Graphicswindow.canresize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | 屬性    | 無  |
| [**CanRotate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | 屬性    | 無  |
| [**移動**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | 方法      | 無  |
| [**調整大小**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | 方法      | 無  |
| [**旋轉**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | 方法      | 無  |



 

執行 [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 介面需要下列其他屬性和方法。



| 必要成員                                              | 成員類型 | 備註 |
|---------------------------------------------------------------|-------------|-------|
| [**CanZoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | 屬性    | 無  |
| [**Zoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | 方法      | 無  |
| [**ZoomByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | 方法      | 無  |
| [**ZoomLevel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | 屬性    | 無  |
| [**ZoomMaximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | 屬性    | 無  |
| [**ZoomMinimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | 屬性    | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 