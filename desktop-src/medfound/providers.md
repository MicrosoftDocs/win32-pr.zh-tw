---
description: 包含 MFTrace 的追蹤提供者清單。
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: providers 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191760"
---
# <a name="providers-element"></a>providers 元素

包含 [MFTrace](mftrace.md)的追蹤提供者清單。

## <a name="usage"></a>使用方式

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> | 指定媒體基礎繞道提供者，此提供者會追蹤媒體基礎的 API 呼叫。<br/> <br/> |
| [**供應商**](provider.md)<br/>   | 指定追蹤提供者 (ETW 或 WPP) 。<br/> <br/>                                                  |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a>父元素

沒有父元素。

## <a name="element-information"></a>項目資訊



|              |     |
|--------------|-----|
| 可以是空的 | Yes |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MFTrace 設定檔](mftrace-configuration-file.md)
</dt> </dl>

 

 




