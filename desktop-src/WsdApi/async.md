---
description: 指定產生的 proxy 函數中是否包含非同步作業。
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: async 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027347"
---
# <a name="async-element"></a>async 元素

指定產生的 proxy 函數中是否包含非同步作業。

## <a name="usage"></a>使用方式

``` syntax
<async/>
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



## <a name="remarks"></a>備註

可能的值為 1 (包含) 的非同步作業，而 0 (預設值) 排除非同步作業。

Proxy 可以有相同作業的非同步和同步版本。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




