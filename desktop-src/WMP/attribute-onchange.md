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
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000426"
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

 

 





