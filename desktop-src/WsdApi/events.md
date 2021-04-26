---
description: 指定產生的函數中是否包含相關事件。
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: events 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995925"
---
# <a name="events-element"></a>events 元素

指定產生的函數中是否包含相關事件。

## <a name="usage"></a>使用方式

``` syntax
<events/>
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
| [**stubDeclarations**](stubdeclarations.md)<br/>                         | 針對埠類型作業產生存根函式的宣告。<br/> <br/>                 |
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | 針對埠類型作業產生存根函式的實作為。<br/> <br/>              |



## <a name="remarks"></a>備註

可能的值為 1 (包含的事件) 和 0 (預設值) 排除的事件。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




