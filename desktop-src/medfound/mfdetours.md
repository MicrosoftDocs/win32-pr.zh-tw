---
description: 指定 Microsoft 媒體基礎繞道提供者，此提供者會追蹤媒體基礎的 API 呼叫。
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: mfdetours 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a0215d9d065bd27f0ad98ebea23abec8f7ecbbfc2223d522e0ddd1887990c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113638"
---
# <a name="mfdetours-element"></a>mfdetours 元素

指定 Microsoft 媒體基礎繞道提供者，此提供者會追蹤媒體基礎的 API 呼叫。

## <a name="usage"></a>使用方式

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>屬性



| 屬性            | 類型             | 必要       | 描述                             |
|----------------------|------------------|----------------|-----------------------------------------|
| **level**<br/> | CDATA<br/> | Yes<br/> | 追蹤層級。<br/> <br/> |



## <a name="child-elements"></a>子元素



| 元素                               |
|---------------------------------------|
| [**關鍵 字**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
keyword+
```

## <a name="parent-elements"></a>父元素

| 元素                                   |
|-------------------------------------------|
| [**供應商**](providers.md)<br/> |



## <a name="element-information"></a>項目資訊

:::row:::
    :::column:::
        可以是空的
    :::column-end:::
    :::column span="2":::
        否
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MFTrace 設定檔](mftrace-configuration-file.md)
</dt> </dl>

 

 




