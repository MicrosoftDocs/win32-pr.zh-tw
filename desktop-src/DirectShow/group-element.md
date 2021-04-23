---
description: Group 元素會定義一個群組，也就是時間軸中的最上層物件。
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: " (DirectShow) 的群組元素"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909246"
---
# <a name="group-element"></a>group 元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**Group** 元素會定義一個群組，也就是時間軸中的最上層物件。

## <a name="attributes"></a>屬性

[**bitdepth**](bitdepth-attribute.md)、 [**緩衝**](buffering-attribute.md)、 [**畫面播放速率**](framerate-attribute.md)、 [**高度**](height-attribute.md)、 [**鎖定**](lock-attribute.md)、 [**靜音**](mute-attribute.md)、 [**name**](name-attribute.md)、 [**previewmode**](previewmode-attribute.md)、 [**samplingrate**](samplingrate-attribute.md)、 [**type**](type-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)、 [**width**](width-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



| 標籤 | 值 |
|----------|----------------------------------------------------------------------------------------------------------|
| 父代   | [**時程表**](timeline-element.md)                                                                     |
| Children | [**複合**](composite-element.md)、 [**效果**](effect-element.md)、 [**追蹤**](track-element.md) |



 

## <a name="remarks"></a>備註

在專案中 `group` ，嵌套層的優先順序是由它們出現在元素內的順序隱含決定。 第一個圖層的優先順序為0，而後續層級的優先順序值也會增加。

## <a name="examples"></a>範例


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 元素](xtl-elements.md)
</dt> </dl>

 

 



