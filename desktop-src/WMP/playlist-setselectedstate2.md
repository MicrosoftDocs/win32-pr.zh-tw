---
title: 播放清單。 setSelectedState2
description: SetSelectedState2 方法會使用播放清單元素中的指定索引來設定專案的選取狀態。
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- 播放清單. setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f952d00486fe2419ab48592c7624299ef466c5dfa2b96d53fefb308fc537488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335810"
---
# <a name="playlistsetselectedstate2"></a>播放清單。 setSelectedState2

**SetSelectedState2** 方法會使用 **播放清單** 元素中的指定索引來設定專案的選取狀態。

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*專案*
</dt> <dd>

**數位** (**long**) 指出播放清單中專案的索引。

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*選擇*
</dt> <dd>

**布林值** ，指出是否要選取指定的專案 (true) 或未選取 (false) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法可以使用嵌套的播放清單，並取代無法使用的 **setSelectedState** 方法。 您可以在 *專案* 參數中指定1，將所有專案設定為要求的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 setSelectedState**](playlist-setselectedstate.md)
</dt> </dl>

 

 





