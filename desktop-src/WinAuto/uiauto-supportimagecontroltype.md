---
title: 影像控制項類型
description: 本主題提供影像控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: 439c708c-4fb4-481b-a2ff-3816d649f3ff
keywords:
- 消費者介面自動化，影像控制項類型的支援
- 消費者介面自動化，影像控制項類型
- 消費者介面自動化，影像控制項類型的樹狀結構
- 消費者介面自動化，影像控制項類型的屬性
- 消費者介面自動化，影像控制項類型的控制項模式
- 消費者介面自動化，影像控制項類型的事件
- 樹狀結構，影像控制項類型
- 屬性，影像控制項類型
- 控制項模式、影像控制項類型
- 事件，影像控制項類型
- 影像控制項類型的支援
- Image 控制項類型
- 控制項類型，影像控制項類型的樹狀結構
- 控制項類型、影像控制項類型的控制項模式
- 控制項類型，支援影像
- 控制項類型，影像
ms.topic: article
ms.date: 10/08/2019
ms.openlocfilehash: b91d55bf8e21813e180476146625172e3eab1a6d
ms.sourcegitcommit: da8cc3fb3c9f14cb768855502a2b6815ddee13b6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/10/2019
ms.locfileid: "106995558"
---
# <a name="image-control-type"></a>影像控制項類型

本主題提供 **影像** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。

當做圖示、參考圖形和圖表使用的影像控制項將支援 **影像** 控制項類型。 當做背景或浮水印影像使用的控制項將不支援 **影像** 控制項類型。

下列章節會定義 **影像** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有影像控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

- [一般樹狀結構](#typical-tree-structure)
- [相關屬性](#relevant-properties)
- [必要的控制項模式](#required-control-patterns)
- [必要的事件](#required-events)
- [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與影像控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。

| 控制項檢視 | 內容檢視 |
| ------------ | ------------ |
| Image | 影像 (根據 [ [Automation 元素屬性識別碼](uiauto-automation-element-propids.md) ] 屬性的值，取決於影像是否包含資訊)  |

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與影像控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。

| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 影像控制項的可按點必須是影像控制項周框內的點。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **影像**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。 | **HelpText** 屬性會公開當地語系化的字串，描述控制項的實際視覺外觀或與影像相關聯的其他工具提示資訊。 當需要較長的描述以傳達影像 (控制項的詳細資訊時，例如，如果影像是複雜的圖表或圖表) ，則必須支援此屬性。 這個屬性會對應至 HTML **LongDesc** 標記和可擴充的向量圖形 (SVG) **Desc** 標記。 使用影像控制項的開發人員必須支援屬性來允許在控制項設定視覺描述。 這個屬性必須對應至消費者介面自動化 **VisualDescription** 屬性。 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | 請參閱備註。 | 如果影像控制項包含尚未公開給使用者的有意義資訊，則必須包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 影像控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | 請參閱備註。 | 如果影像控制項是用來表示螢幕上特定項目的狀態資訊，則該控制項應包含在項目內。 當影像包含在專案內時，專案必須支援 status 屬性，並在狀態變更時引發適當的通知。 若影像為單獨控制項並傳達狀態資訊，則必須支援此屬性。                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 如果有靜態文字標籤，這個屬性必須公開該控制項的參考。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **影像** 控制項類型的當地語系化字串。 預設值為 "image" 代表 en-us 或英文 (美國) 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 包含資訊的所有影像控制項都必須公開 **Name** 屬性。 以程式設計方式存取此資訊時，必須提供相當於該圖形的文字。 如果影像控制項純粹是裝飾性的，則必須只顯示在消費者介面自動化樹狀結構的控制項視圖中，而且不需要有名稱 (請參閱 [備註](#remarks)) 。 使用者介面架構必須支援 ALT 或影像的替代文字屬性，其可由架構內設定。 然後，這個屬性會對應至消費者介面自動化名稱] 屬性。                                                                                                                                                     |

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出支援影像控制項所需的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。

| 控制項模式                                                 | 支援 | 注意                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)           | 相依 | 如果控制項在方格容器內，則影像控制項支援 [GridItem](uiauto-implementinggriditem.md) 控制項模式。                                                                                                                                                                                                                                                                                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | 永不   | 如果影像控制項是可按一下的物件，控制項就應該支援支援叫 [用控制項模式](uiauto-implementinginvoke.md) 的控制項類型，例如 [按鈕](uiauto-supportbuttoncontroltype.md) 控制項類型。 若為包含多個可點按物件的影像物件， (影像控制項類型的元素) 可能會在消費者介面自動化樹狀結構中裝載 ([Hyperlink](uiauto-supporthyperlinkcontroltype.md) 控制項) 類型的子連結。 |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | 永不   | 影像控制項不應支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式。 如果影像是可選取之容器的一部分，例如具有影像圖示作為內容的按鈕，則該容器支援模式，而不是內的影像。                                                                                                                                                                           |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)         | 相依 | 如果控制項在具有標題控制項的容器內，則影像控制項支援 [TableItem](uiauto-implementingtableitem.md) 控制項模式。                                                                                                                                                                                                                                                                                                |

## <a name="required-events"></a>必要的事件

下表列出支援的影像控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱

| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ItemStatusPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。               | 如果控制項支援 [**ItemStatus**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。  |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |

## <a name="remarks"></a>備註

全球資訊網協會 (W3C) 會將裝飾性影像定義為不會將資訊新增至頁面內容的影像。 如需詳細資訊，請參閱 W3C 主題的 [裝飾影像](https://www.w3.org/WAI/tutorials/images/decorative/)。

關於消費者介面自動化：

- 如果映射純粹是裝飾性的，則不是互動式，且不會傳達任何資訊，如下圖所示：
  - 可能或可能不在 UIA 樹狀結構中
  - 可能或可能不在 UIA 原始視圖中
  - 不得在 UIA 控制項視圖中
  - 不得在內容視圖中
  - 不一定會有名稱
- 如果影像傳達資訊，但是有清楚相關聯的文字可提供相同的資訊 (例如，包含左指向三角形圖形的 [播放] 按鈕，以及 [播放] ) 的文字，則影像會被視為裝飾性和影像：
  - 必須在原始視圖中
  - 必須在控制項視圖中
  - 不得在內容視圖中
  - 名稱屬性中不一定會有值
  - 也可傳達影像意義的文字必須在內容視圖中
- 如果影像是有資訊的，並且會傳達任何相關文字未提供的詳細資料，則影像：
  - 必須在原始視圖中
  - 必須在控制項視圖中
  - 必須在內容視圖中
  - 必須具有描述影像及其意義的名稱值

## <a name="related-topics"></a>相關主題

### <a name="conceptual"></a>概念

- [UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
- [UI 自動化概觀](uiauto-uiautomationoverview.md)
