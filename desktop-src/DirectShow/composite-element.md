---
description: 複合元素定義了組合、追蹤的容器物件，以及其他的嵌套組合。
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: 複合元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106976995"
---
# <a name="composite-element"></a>複合元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`composite`元素會定義組合、追蹤的容器物件，以及其他的嵌套組合。

## <a name="attributes"></a>屬性

[**鎖定**](lock-attribute.md)、 [**靜音**](mute-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| 父代   | `composite`、 [**群組**](group-element.md)                                                                             |
| Children | `composite`、 [**效果**](effect-element.md)、 [**追蹤**](track-element.md)、 [**轉換**](transition-element.md) |



 

## <a name="remarks"></a>備註

在專案中 `composite` ，嵌套層的優先順序是由它們出現在元素內的順序隱含決定。 第一個圖層的優先順序為0，而後續層級的優先順序值也會增加。

## <a name="examples"></a>範例


```XML
<composite> </composite>
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 元素](xtl-elements.md)
</dt> </dl>

 

 



