---
description: 在日誌檔中包含影像的編碼二進位資料（如果有的話）。
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Image 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975361"
---
# <a name="image-element"></a>Image 元素

在日誌檔中包含影像的編碼二進位資料（如果有的話）。

## <a name="definition"></a>定義

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
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



|              |                                                         |
|--------------|---------------------------------------------------------|
| 項目類型 | [**ImageType**](imagetype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink              |
| 結構描述名稱  | 日誌讀者                                          |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**背景**](background-element.md)
</dt> </dl>

 

 



