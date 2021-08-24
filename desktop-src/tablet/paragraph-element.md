---
description: 包含段落。
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: 'Uments 的段落元素 (Windows.ui.xaml.doc.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: 877bede54ef714a011903424b1f323f004264affefedbcfae0ab44f2dcf58816
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843398"
---
# <a name="paragraph-element"></a>段落元素

包含段落。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>父項目

[**內容**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>子元素

[**折線圖**](line-element.md)

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>屬性



| 屬性       | 類型                      | 必要 | 描述                                                                             | 可能的值           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **離開**        | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最左邊點的距離。 | 任何整數。              |
| **前幾個**         | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最上方點的距離。  | 任何整數。              |
| **寬度**       | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的寬度。                                          | 任何非負整數。 |
| **高度**      | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的高度。                                         | 任何非負整數。 |
| **BlockNumber** | **xs:nonNegativeInteger** | 必要 | 區塊數目。                                                                           | 任何非負整數。 |
| **LineNumber**  | **xs:nonNegativeInteger** | 必要 | 段落開始的行。                                                 | 任何非負整數。 |



 

## <a name="element-information"></a>項目資訊



|  元素     | 值                                                     |
|--------------|-----------------------------------------------------------------|
| 項目類型 | [**ParagraphType**](paragraphtype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                      |
| 結構描述名稱  | 日誌讀者                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Windows.ui.xaml.documents。h</dt> </dl> |



 

 




