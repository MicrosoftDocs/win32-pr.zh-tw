---
description: 包含一組&8212 的元素 \# ;在筆記本便箋中群組在一起的段落、InkWord、繪圖、文字、影像或旗標&\# 郵件;。
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: GroupNode 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992413"
---
# <a name="groupnode-element"></a>GroupNode 元素

包含在筆記本便箋中群組在一起的一組元素（[**段落**](paragraph-element.md)、 [**InkWord**](inkword-element.md)、 [**繪圖**](drawing-element.md)、 [**文字**](text-element.md)、 [**影像**](image-element.md)或 [**旗**](flag-element.md)標）。

## <a name="definition"></a>定義

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a>父項目

[**內容**](content-element--journal-reader.md)

## <a name="child-elements"></a>子元素

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**繪圖**](drawing-element.md)

[**Text**](text-element.md)

[**Image**](docimage-element.md)

[**旗標**](flag-element.md)

## <a name="attributes"></a>屬性



| 屬性  | 類型                      | 必要 | 描述                                                                             | 可能的值           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **離開**   | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最左邊點的距離。 | 任何整數。              |
| **前幾個**    | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最上方點的距離。  | 任何整數。              |
| **寬度**  | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的寬度。                                          | 任何非負整數。 |
| **高度** | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的高度。                                         | 任何非負整數。 |



 

## <a name="element-information"></a>項目資訊



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| 項目類型 | [**GroupNodeType**](groupnodetype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                      |
| 結構描述名稱  | 日誌讀者                                                  |



 

 

 



