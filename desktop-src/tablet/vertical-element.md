---
description: 包含描述筆記本便箋所用信紙中線條垂直元件的資訊。 例如，當便箋具有格線時使用。
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: 垂直元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6f05ab8a2160dbf6b987177957e8285385fe4db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479504"
---
# <a name="vertical-element"></a>垂直元素

包含描述筆記本便箋所用信紙中線條垂直元件的資訊。 例如，當便箋具有格線時使用。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
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



|  元素     | 值                                                         |
|--------------|---------------------------------------------------------------|
| 項目類型 | [**VerticalType**](verticaltype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                    |
| 結構描述名稱  | 日誌讀者                                                |



 

 

 




