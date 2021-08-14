---
title: TextChild 控制項模式
description: 介紹執行 ITextChildProvider 的指導方針和慣例，包括屬性和方法的相關資訊。 TextChild 控制項模式可用來存取專案的最接近支援文字控制項模式的上階。
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- 消費者介面自動化，執行 TextChild 控制項模式
- 消費者介面自動化，TextChild 控制項模式
- 消費者介面自動化、ITextChildProvider
- ITextChildProvider
- 執行消費者介面自動化 TextChild 控制項模式
- TextChild 控制項模式
- 控制項模式，ITextChildProvider
- 控制模式，消費者介面自動化執行 TextChild
- 控制項模式，TextChild
- 介面，ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c7bfb1852a02efc7baa789e137a4c05e2c2e85a65606109b26a622dfafcf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929035"
---
# <a name="textchild-control-pattern"></a>TextChild 控制項模式

介紹執行 [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)的指導方針和慣例，包括屬性和方法的相關資訊。 **TextChild** 控制項模式可用來存取專案的最接近支援 [文字](uiauto-implementingtextandtextrange.md)控制項模式的上階。

例如，假設檔中的文字包含內嵌影像以及如下圖所示的超連結。

![顯示包含內嵌影像和超連結之文字的螢幕擷取畫面](images/textchild-pattern.png)

如果您使用 Microsoft 消費者介面自動化工具來檢查這份檔內容的消費者介面自動化樹狀結構，它可能會顯示一個檔元素，其中包含代表影像的一個子項目，另一個代表超連結的子專案。 例如：

![顯示檢查報表範例 ui 自動化元素樹狀結構的螢幕擷取畫面](images/textchild-pattern-tree.png)

一般來說，上述範例中的 document 元素支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，但 document 專案的兩個子系則不支援。 如果消費者介面自動化用戶端應用程式有影像元素或超連結元素的參考，則用戶端可以使用 **TextChild** 控制項模式，以方便存取包含檔專案所公開的 Textcontrol 模式。

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) 介面時，請注意下列方針和慣例：

-   [**ITextChildProvider：： TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer)屬性應指定最接近的上階元素，以支援 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)介面，不論上階鏈中較高的元素是否也支援 **ITextProvider**。
-   元素不應同時支援 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 和 [ITextChildProvider * *](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) 介面。
- 實 [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) 的專案必須是可執行 [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)之專案的子系（或子項目）。 此元素不需要同時執行 [文字控制項模式](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange)。
-   [**ITextChildProvider：： TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)屬性所指定的文字範圍必須與包含文字提供者專案所傳回的文字範圍相同，因為它的 [**ITextProvider：： RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)函式是以文字子項目做為括住的子專案來呼叫時。

## <a name="required-members-for-itextchildprovider"></a>**ITextChildProvider** 的必要成員

執行 [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) 介面時需要這些屬性和方法。



| 必要成員                                                     | 成員類型 | 備註 |
|----------------------------------------------------------------------|-------------|-------|
| [**TextContainer**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | 屬性    | 無  |
| [**TextRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | 屬性    | 無  |



 

此控制項模式沒有任何相關聯的方法或事件。

## <a name="related-topics"></a>相關主題

**概念**

- [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
- [UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
- [UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)