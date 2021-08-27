---
description: 定義在頁面上繪製的邊界線。
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c264c2470d070353d1fd19340a161cf765bc05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478664"
---
# <a name="margin-element"></a>Margin 元素

定義在頁面上繪製的邊界線。

## <a name="definition"></a>定義

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>父項目

無。

## <a name="child-elements"></a>子元素

沒有。。

## <a name="attributes"></a>屬性




| 屬性 | 類型 | 必要 | 描述 | 可能的值 | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType | 必要 | 指定要繪製的線條類型。 | <ul><li>無</li><li>實線</li><li>虛線</li><li>點</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>色彩</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | 選擇性 | 元素的色彩。 | 十六進位的 RGB 值。 符合下列正則運算式： # [0-9a-南非-Z] {6} 。 例如，#4a79B5。<br /> | 
| <strong>類型</strong> | <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType | 選擇性 | 表示左邊界或右邊界。 | <ul><li>Left</li><li>Right</li></ul> | 
| <strong>間距</strong> | <strong>xs:nonNegativeInteger</strong> | 選擇性 | 頁面邊緣和邊界之間的間距。 | 任何非負整數。 | 




 

## <a name="element-information"></a>項目資訊



|  元素     | 值                                                     |
|--------------|-----------------------------------------------------------|
| 項目類型 | [**MarginType**](margintype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                |
| 結構描述名稱  | 日誌讀者                                            |



 

 

 




