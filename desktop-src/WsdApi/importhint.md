---
description: 指定未明確指定位置之 <wsdl： import> 指示詞的下載位置。
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importHint 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983424"
---
# <a name="importhint-element"></a>importHint 元素

指定未明確指定位置之 <wsdl： import> 指示詞的下載位置。

## <a name="usage"></a>使用方式

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**位置**](location.md)<br/>   | 要匯入之檔案的位置。 位置可以是相對路徑、絕對路徑或 HTTP URL。<br/> <br/> |
| [**命名 空間**](namespace.md)<br/> | 要匯入的命名空間。 這應該符合 <wsdl： import> 元素中指定的命名空間。<br/> <br/>     |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | 指定要針對合約資訊處理的 WSDL 檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




