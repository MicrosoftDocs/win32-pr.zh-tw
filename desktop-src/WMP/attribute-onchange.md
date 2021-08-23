---
title: attribute_onchange
description: 當外觀屬性變更值時，就會發生事件處理常式可以處理的事件。 事件處理常式的名稱是屬性的名稱，後面接著底線和 \ 0034; onchange \ 0034;，例如 \ 0034; value \_ onchange \ 0034;。
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c707b04587b6e975f81c8a0d0918b14c8e193d303f82c61b5220796bb6975b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573758"
---
# <a name="attribute_onchange"></a>屬性 \_ onchange

當外觀屬性變更值時，就會發生事件處理常式可以處理的事件。 事件處理常式的名稱是屬性的名稱，後面接著底線和 "onchange"，例如「值 \_ onchange」。

``` syntax
        attribute_onchange
```

## <a name="examples"></a>範例


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境事件處理常式**](ambient-event-handlers.md)
</dt> </dl>

 

 





