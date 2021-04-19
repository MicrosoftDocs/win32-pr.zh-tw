---
description: 定義針對命名空間中的宏名稱所產生的程式碼中所使用的前置詞。
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroPrefix 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985634"
---
# <a name="macroprefix-element"></a>macroPrefix 元素

定義針對命名空間中的宏名稱所產生的程式碼中所使用的前置詞。

## <a name="usage"></a>使用方式

``` syntax
<macroPrefix/>
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

這個元素會覆寫用於產生之宏的預設 URI 前置詞。 例如，如果宏前置詞為 "AV \_ " 且名稱為 "調諧器"，則為限定名稱產生的宏將會是 "av \_ 調諧器"。

根據預設，產生的程式碼會從 URI 建立慣用的宏前置詞。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




