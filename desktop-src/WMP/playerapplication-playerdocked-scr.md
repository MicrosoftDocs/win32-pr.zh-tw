---
title: PLAYERAPPLICATION. playerDocked 屬性
description: playerDocked 屬性會抓取值，指出 Windows Media Player 是否處於停駐狀態。
ms.assetid: 8b95da72-037b-4179-a564-fc9bc63368ac
keywords:
- PLAYERAPPLICATION. playerDocked Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.playerDocked
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e05d186ab8123dcd4a03eff6c282cec4f7884225d8271540eebb8dc2e73eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571785"
---
# <a name="playerapplicationplayerdocked"></a>PLAYERAPPLICATION.playerDocked

**playerDocked** 屬性會抓取值，指出 Windows Media Player 是否處於停駐狀態。

``` syntax
        elementID.playerDocked
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林值**。



| 值 | 描述                       |
|-------|-----------------------------------|
| True  | Windows Media Player 固定。   |
| 否 | Windows Media Player 未移除。 |



 

## <a name="remarks"></a>備註

只有在遠端 Windows Media Player 控制項時，才會使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PLAYERAPPLICATION 元素**](playerapplication-element.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





