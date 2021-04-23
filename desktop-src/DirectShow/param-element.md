---
description: Param 元素會指定轉換、效果或其他子物件上的屬性值。
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: " (DirectShow) 的 param 元素"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909036"
---
# <a name="param-element"></a>param 元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`param`元素會指定轉換、效果或其他子物件上的屬性值。

## <a name="attributes"></a>屬性

[**名稱**](name-attribute.md)、 [**值**](value-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



| 標籤 | 值 |
|----------|----------------------------------------------------------------------------------------------------------|
| 父代   | [**剪輯**](clip-element.md)、 [**效果**](effect-element.md)、 [**轉換**](transition-element.md) |
| Children | [**at**](at-element.md)、 [**線性**](linear-element.md)                                               |



 

## <a name="remarks"></a>備註

**Value** 屬性會在轉換或效果開始時，指定屬性的值。 使用 **at** 或 **線性** 元素來指定變更值。 如果 **param** 元素包含 no 或 **線性** 元素，此值會在 **效果或轉換** 的持續時間內保持不變。

> [!Note]  
> **剪切** 元素內的 **param** 專案不 **能包含或****線性** 元素。

 

許多轉換支援標準 **進度** 屬性，範圍從0到1.0，指出輸出中反映的轉換百分比。 **進度**= 0.0，轉換會在其序列的開頭 (完全是) 的第一個影片影像。 **進行** 中 = 0.5 時，轉換是一半的完成。  (例如，在抹除 **過程** = 0.5，轉換界限位於影像的中央，) **正在進行** 中 = 1.0，則轉換已完成 (完全) 第二個影像。 根據預設，轉換會在轉換開始進行時，從 **進度** = 0.0 移至 **進度** = 1.0 結尾。

其他屬性通常專屬於特定的轉換或效果。 例如，抹除轉換支援可控制轉換區域寬度的 **GradientSize** 屬性。

若要回溯執行轉換，請在轉換開始時將 **進度** 屬性設為1.0，並使用 **線性** 元素將值變更為0.0，如下列範例所示：


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a>範例


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 元素](xtl-elements.md)
</dt> </dl>

 

 



