---
description: 包含便箋標題的位置和周框資訊（如果有的話）。
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: TitleArea 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f95c06e6aabe7c73cdc02a7fdb66c60f220adfbe72ea565b73cbc2c3f1a88bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589308"
---
# <a name="titlearea-element"></a>TitleArea 元素

包含便箋標題的位置和周框資訊（如果有的話）。

## <a name="definition"></a>定義

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a>父項目

[**標題**](title-element.md)

## <a name="child-elements"></a>子元素

無。

## <a name="attributes"></a>屬性



| 屬性  | 類型                      | 必要 | 描述                                                                             | 可能的值           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **離開**   | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最左邊點的距離。 | 任何整數。              |
| **前幾個**    | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最上方點的距離。  | 任何整數。              |
| **寬度**  | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的寬度。                                          | 任何非負整數。 |
| **高度** | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的高度。                                         | 任何非負整數。 |



 

## <a name="element-information"></a>項目資訊



|   元素    | 值                                                           |
|--------------|-----------------------------------------------------------------|
| 項目類型 | [**TitleAreaType**](titleareatype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                      |
| 結構描述名稱  | 日誌讀者                                                  |



 

 

 



