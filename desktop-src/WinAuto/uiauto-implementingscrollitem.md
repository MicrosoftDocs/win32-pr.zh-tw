---
title: ScrollItem 控制項模式
description: 描述執行 IScrollItemProvider 的方針和慣例，包括方法的相關資訊。
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- 消費者介面自動化，執行 ScrollItem 控制項模式
- 消費者介面自動化，ScrollItem 控制項模式
- 消費者介面自動化、IScrollItemProvider
- IScrollItemProvider
- 執行消費者介面自動化 ScrollItem 控制項模式
- ScrollItem 控制項模式
- 控制項模式，IScrollItemProvider
- 控制模式，消費者介面自動化執行 ScrollItem
- 控制項模式，ScrollItem
- 介面，IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a677a761c01afb5ad6feaf04df0197299a528a22741c0bd8ff72c02f45c74b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826888"
---
# <a name="scrollitem-control-pattern"></a>ScrollItem 控制項模式

描述執行 [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)的方針和慣例，包括方法的相關資訊。 **ScrollItem** 控制項模式用來支援執行 [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)之容器的個別子控制項。 控制項的 **ScrollItem** 控制項模式是否存在，並不表示其容器或任何上階都必須執行 **滾動** 條控制項模式。

當容器執行的是 **滾動** 條控制項模式時， **ScrollItem** 控制項模式會作為子控制項與其容器之間的通道，以確保容器可以變更其區域內的目前可見內容 (或區域) ，以顯示子控制項。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IScrollItemProvider** 的必要成員](#required-members-for-iscrollitemprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **ScrollItem** 控制項模式時，請注意下列方針和慣例：

-   不需要 [視窗](uiauto-supportwindowcontroltype.md) 或 **畫布** 控制項內所含的專案來執行 [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) 介面。 不過，您也必須公開 [**IUIAutomationElement：： CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (或 [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) 屬性的有效位置。 這可讓 Microsoft 消費者介面自動化用戶端應用程式使用容器上的 [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) 控制項模式方法來顯示子專案。

## <a name="required-members-for-iscrollitemprovider"></a>**IScrollItemProvider** 的必要成員

以下是執行 [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) 介面的必要方法。



| 必要成員                                                    | 成員類型 | 備註 |
|---------------------------------------------------------------------|-------------|-------|
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | 方法      | 無  |



 

此控制項模式沒有任何相關聯的屬性或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[選取控制項模式](uiauto-implementingselection.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




