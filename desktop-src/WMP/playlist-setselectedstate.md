---
title: 播放清單。 setSelectedState
description: SetSelectedState 方法會指定選取播放清單中的索引項目目。
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- 播放清單. setSelectedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982702"
---
# <a name="playlistsetselectedstate"></a>播放清單。 setSelectedState

**SetSelectedState** 方法會指定選取播放清單中的索引項目目。

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*專案*
</dt> <dd>

**數位** (**long**) 指出播放清單中專案的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

您可以在 *專案* 參數中指定1，將所有專案設定為選取的狀態。

這個方法已由 **setSelectedState2** 所取代，支援嵌套播放清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 setSelectedState2**](playlist-setselectedstate2.md)
</dt> </dl>

 

 





