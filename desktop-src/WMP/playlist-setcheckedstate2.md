---
title: 播放清單。 setCheckedState2
description: SetCheckedState2 方法會使用播放清單元素中的指定索引來設定專案的已核取狀態。
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- 播放清單. setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6b95cb332c5f5a9d86e6f49484b27c1ab5802f28b18195f610395a1c732e369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336217"
---
# <a name="playlistsetcheckedstate2"></a>播放清單。 setCheckedState2

**SetCheckedState2** 方法會使用 **播放清單** 元素中的指定索引來設定專案的已核取狀態。

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*專案*
</dt> <dd>

**Number** (**long**) 指出要檢查或取消選取之播放清單專案的索引。

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*檢查*
</dt> <dd>

**布林值** ，指出是否要檢查指定的專案 (true) 或未核取 (false) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林值**。

## <a name="remarks"></a>備註

這個方法可以使用嵌套的播放清單，並取代 **setCheckedState** 方法。 您可以在 *專案* 參數中指定1，將所有專案設定為要求的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





