---
description: 包含筆記本便箋的標題資訊。
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title 項目
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05661be8566cf4136194af4e08d8f9774d3413dc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473134"
---
# <a name="title-element"></a>Title 項目

包含筆記本便箋的標題資訊。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>父項目

[**信箋**](stationery-element.md)

## <a name="child-elements"></a>子元素

[**TitleArea**](titlearea-element.md)

## <a name="attributes"></a>屬性




| 屬性 | 類型 | 必要 | 描述 | 可能的值 | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | <strong>xs:string</strong> | 必要 | 指定附注標題周圍的框線類型。 | <ul><li>無</li><li>SolidSquare</li><li>OutlineSquare</li><li>SolidRoundRect</li><li>OutlineRoundRect</li><li>SolidRoundRectDottedBaseline</li></ul> | 
| <strong>DateStyle</strong> | <strong>xs:string</strong> | 必要 | 定義標題是否包含日期。 | <ul><li>無</li><li>Short</li></ul> | 
| <strong>色彩</strong> | <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a> | 選擇性 | 指定背景的色彩。 | 請參閱 <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>。 | 




 

## <a name="element-information"></a>項目資訊



| 元素      | 值                                                   |
|--------------|---------------------------------------------------------|
| 項目類型 | [**TitleType**](titletype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink              |
| 結構描述名稱  | 日誌讀者                                          |



 

 

 



