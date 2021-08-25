---
description: 包含筆記本便箋中的文字資訊。
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae4e9fa123f1f43bd92d902158fc3fbc5b1c1de8e074b57aadeb339a0a7b6f15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819937"
---
# <a name="text-element"></a>Text 元素

包含筆記本便箋中的文字資訊。

## <a name="definition"></a>定義

搭配 [**內容**](content-element--journal-reader.md)使用時：

``` syntax
<xs:element name="Text" type="TextType" />
```

或者，搭配 [**TitleInfo**](titleinfo-element.md) 和 [**GroupNode**](groupnode-element.md)使用時：

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>父項目

[**內容**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>子元素

無。

## <a name="attributes"></a>屬性

搭配 [**TitleInfo**](titleinfo-element.md) 和 [**GroupNode**](groupnode-element.md)使用時，沒有任何屬性。 搭配 [**內容**](content-element--journal-reader.md)使用時，屬性如下所示。



| 屬性  | 類型                      | 必要 | 描述                                                                             | 可能的值           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **離開**   | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最左邊點的距離。 | 任何整數。              |
| **前幾個**    | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最上方點的距離。  | 任何整數。              |
| **寬度**  | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的寬度。                                          | 任何非負整數。 |
| **高度** | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的高度。                                         | 任何非負整數。 |



 

## <a name="element-information"></a>項目資訊



|   元素           |   值                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 項目類型 | 使用 [**GroupNode**](groupnode-element.md)和 [**TitleInfo**](titleinfo-element.md)元素的 Content 元素) 或 **xs： string** ([**TextType**](texttype-complex-type.md) complexType ()  |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink<br/>                                                                                                                                               |
| 結構描述名稱  | 日誌讀者<br/>                                                                                                                                                                           |



 

 

 




