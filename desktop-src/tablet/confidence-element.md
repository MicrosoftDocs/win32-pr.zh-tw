---
description: 包含 InkWord 的日記本筆墨分析器所傳回的信賴評等。
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: 信賴元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e4169767f3bf40d49e71e84214d50d3c0c0b4ecf5d3f7a9034ee6c8ea279d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936978"
---
# <a name="confidence-element"></a>信賴元素

包含 [**InkWord**](inkword-element.md)的日記本筆墨分析器所傳回的信賴評等。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>父項目

[**InkWord**](inkword-element.md)

## <a name="values"></a>值

此欄位的有效值包括 "0"、"1" 和 "2"。 0表示強烈的信賴度，1表示中繼信賴度，2表示不佳的信賴度。

## <a name="child-elements"></a>子元素

無。

## <a name="attributes"></a>屬性

無。

## <a name="element-information"></a>項目資訊



|                  | 值                                      |
|------------------|--------------------------------------------|
| **元素類型** | xs:string                                  |
| **Namespace**    | urn：架構-microsoft-com：平板電腦： richink |
| **結構描述名稱**  | 日誌讀者                             |



 

 

 



