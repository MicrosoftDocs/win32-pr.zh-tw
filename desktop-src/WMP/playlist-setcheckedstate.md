---
title: 播放清單。 setCheckedState
description: SetCheckedState 方法會指定檢查播放清單中的索引項目目。
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- 播放清單. setCheckedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93e143f738197524e1555f18aedf84aa606626de645a98149c65507b71291cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336245"
---
# <a name="playlistsetcheckedstate"></a>播放清單。 setCheckedState

**SetCheckedState** 方法會指定檢查播放清單中的索引項目目。

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*專案*
</dt> <dd>

**Number** (**long**) 表示要檢查之播放清單專案的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林值**。

## <a name="remarks"></a>備註

您可以在 *專案* 參數中指定1，將所有專案設定為已核取狀態。

這個方法已由 **setCheckedState2** 所取代，支援嵌套播放清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





