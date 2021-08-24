---
description: 定義應對應命名空間的前置詞，以便讓 XML 更容易讀取。
ms.assetid: 955f4785-5657-4a89-9728-bce99a0a4234
title: preferredPrefix 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e82caf0558ff3ffc1079d3773453673bcbe916a518f6196670f37744fdf8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756868"
---
# <a name="preferredprefix-element"></a>preferredPrefix 元素

定義應對應命名空間的前置詞，以便讓 XML 更容易讀取。

## <a name="usage"></a>使用方式

``` syntax
<preferredPrefix/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                   | 描述                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**命名 空間**](namespace.md)<br/> | 要用於產生程式碼的命名空間。<br/> <br/> |



## <a name="remarks"></a>備註

這個元素會覆寫用於產生之程式碼的預設 URI 前置詞。 例如，媒體相關的命名空間可能會有適用于音訊/視覺效果) 的慣用首碼 "av" (。

根據預設，產生的程式碼會從 URI 建立慣用的前置詞。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




