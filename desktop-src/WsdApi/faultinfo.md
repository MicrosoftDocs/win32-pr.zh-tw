---
description: 指定產生的函式中是否包含用來傳遞錯誤資訊的參數。
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: faultInfo 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193257"
---
# <a name="faultinfo-element"></a>faultInfo 元素

指定產生的函式中是否包含用來傳遞錯誤資訊的參數。

## <a name="usage"></a>使用方式

``` syntax
<faultInfo/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                         | 描述                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                 | 針對埠類型作業產生 proxy 函式的實作為宣告。<br/> <br/> |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>           | 針對埠類型作業產生 proxy 函式的 IDL 宣告。<br/> <br/>            |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/> | 針對埠類型作業產生 proxy 函式的執行。<br/> <br/>             |
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | 針對埠類型作業產生存根函式的實作為。<br/> <br/>              |



## <a name="remarks"></a>備註

可能的值為 1 (包含的錯誤參數) 和 0 (排除) 的錯誤參數。 預設會排除錯誤參數。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




