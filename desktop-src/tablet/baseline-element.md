---
description: 針對筆記本檔中段落基準的起始點和結束點，提供 (x，y) 資訊。 這些值所使用的座標空間是 HIMETRIC。
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: 基準元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bc64f332608b4bd0281ae2a7f29db96101e9d2e
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436563"
---
# <a name="baseline-element"></a>基準元素

針對筆記本檔中段落基準的起始點和結束點，提供 (x，y) 資訊。 這些值所使用的座標空間是 **HIMETRIC**。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a>父項目

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="child-elements"></a>子元素

無。

## <a name="attributes"></a>屬性



| 屬性  | 類型                      | 必要 | 描述                                                      | 可能的值           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **StartX** | **xs:nonNegativeInteger** | 必要 | 標示基準開頭的點 X 值。 | 任何非負整數。 |
| **StartY** | **xs:nonNegativeInteger** | 必要 | 標示基準開頭的點 Y 值。 | 任何非負整數。 |
| **EndX**   | **xs:nonNegativeInteger** | 必要 | 標示基準結尾之點的 X 值。       | 任何非負整數。 |



 

## <a name="element-information"></a>項目資訊



|                  | 值                                                         |
|------------------|---------------------------------------------------------------|
| **元素類型** | [**BaselineType**](baselinetype-complex-type.md) complexType |
| **Namespace**    | urn：架構-microsoft-com：平板電腦： richink                    |
| **結構描述名稱**  | 日誌讀者                                                |



 

 

 



