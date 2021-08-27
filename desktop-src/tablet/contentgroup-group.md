---
description: 定義在筆記本便箋中包含一組分組內容的群組。
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: ContentGroup 群組
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0085cc52a8fc29d3a51f4d1e1c8f42128b63db9e166a7a1c436dc15bff70a36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009008"
---
# <a name="contentgroup-group"></a>ContentGroup 群組

定義在筆記本便箋中包含一組分組內容的群組。

## <a name="definition"></a>定義

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>子元素

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**繪圖**](drawing-element.md)

[**Text**](text-element.md)

[**映像**](docimage-element.md)

[**旗標**](flag-element.md)

## <a name="attributes"></a>屬性



| 屬性  | 類型                      | 必要 | 描述                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **離開**   | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最左邊點的距離。<br/> | 任何整數。<br/>              |
| **前幾個**    | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最上方點的距離。<br/>  | 任何整數。<br/>              |
| **寬度**  | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的寬度。<br/>                                          | 任何非負整數。<br/> |
| **高度** | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的高度。<br/>                                         | 任何非負整數。<br/> |



 

## <a name="type-information"></a>類型資訊



|  元素     | 值                                                     |
|-------------|--------------------------------------------|
| 命名空間   | urn：架構-microsoft-com：平板電腦： richink |
| 結構描述名稱 | 日誌讀者                             |



 

 

 




