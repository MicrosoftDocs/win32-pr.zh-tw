---
description: 包含在筆記本便箋中用於信紙的水平線格式資訊。
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: 水準元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b66e8557d73570ce1a0b7eb7217c02435c51a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482684"
---
# <a name="horizontal-element"></a>水準元素

包含在筆記本便箋中用於信紙的水平線格式資訊。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>父項目

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>子元素

無。

## <a name="attributes"></a>屬性




| 屬性 | 類型 | 必要 | 描述 | 可能的值 | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType | 必要 | 指定要繪製的線條類型。 | <ul><li>無</li><li>實線</li><li>虛線</li><li>點</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>色彩</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | 選擇性 | 元素的色彩。 | 十六進位的 RGB 值。 符合下列正則運算式： # [0-9a-南非-Z] {6} 。 例如，#4a79B5。<br /> | 
| <strong>SpacingBefore</strong> | <strong>xs:nonNegativeInteger</strong> | 選擇性 | 元素之前的間距。 | 任何非負整數。 | 
| <strong>SpacingBetween</strong> | <strong>xs:nonNegativeInteger</strong> | 選擇性 | 此元素與周圍元素之間的間距。 | 任何非負整數。 | 




 

## <a name="element-information"></a>項目資訊



|  元素     | 值                                                     |
|--------------|-------------------------------------------------------------------|
| 項目類型 | [**HorizontalType complexType**](horizontaltype-complex-type.md) |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                        |
| 結構描述名稱  | 日誌讀者                                                    |



 

 

 




