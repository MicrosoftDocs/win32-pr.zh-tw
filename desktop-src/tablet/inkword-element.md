---
description: 包含筆記本便箋中指定筆墨單字的相關資訊，包括位置、替代項和實際筆墨資料。
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: InkWord 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979011"
---
# <a name="inkword-element"></a>InkWord 元素

包含筆記本便箋中指定筆墨單字的相關資訊，包括位置、替代項和實際筆墨資料。

## <a name="definition"></a>定義

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>父項目

[**GroupNode**](groupnode-element.md)

[**線條**](line-element.md)

## <a name="child-elements"></a>子元素

[**ScalarTransform**](scalartransform-element.md)

[**AlternateList**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**信賴度**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>屬性



| 屬性  | 類型                      | 必要 | 描述                                                                             | 可能的值           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **離開**   | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最左邊點的距離。 | 任何整數。              |
| **前幾個**    | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最上方點的距離。  | 任何整數。              |
| **寬度**  | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的寬度。                                          | 任何非負整數。 |
| **高度** | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的高度。                                         | 任何非負整數。 |



 

> [!WARNING]
> 筆墨單字的內部座標組應為英文計量單位，而您的應用程式必須使用2.54 的乘數，將寬度和高度值轉換為 Tablet PC 平臺 Api 所使用的 HIMETRIC 單位。

 

## <a name="element-information"></a>項目資訊



|              |                                                             |
|--------------|-------------------------------------------------------------|
| 項目類型 | [**InkWordType**](inkwordtype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                  |
| 結構描述名稱  | 日誌讀者                                              |



 

 

 



