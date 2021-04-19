---
description: 包含與筆記本便箋區段相關聯之旗標的 base64 編碼點陣圖。
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: 旗標元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971018"
---
# <a name="flag-element"></a>旗標元素

包含與筆記本便箋區段相關聯之旗標的 base64 編碼點陣圖。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>父項目

[**內容**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

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



|              |                                                       |
|--------------|-------------------------------------------------------|
| 項目類型 | [**FlagType**](flagtype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink            |
| 結構描述名稱  | 日誌讀者                                        |



 

 

 



