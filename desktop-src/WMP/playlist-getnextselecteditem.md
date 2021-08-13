---
title: 播放清單。 getNextSelectedItem
description: GetNextSelectedItem 方法會以指定的索引之後，抓取播放清單中下一個選取專案的索引。
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- 播放清單. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 872dd31694384dfa35d7ce98c2f26756ede14539f4e788cbb6f699d17ca78a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467748"
---
# <a name="playlistgetnextselecteditem"></a>播放清單。 getNextSelectedItem

**GetNextSelectedItem** 方法會以指定的索引之後，抓取播放清單中下一個選取專案的索引。

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*專案*
</dt> <dd>

**Number** (**Long**) ，指出要在其後搜尋的專案索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**long**) 。

## <a name="remarks"></a>備註

如果沒有其他選取的專案，這個方法會傳回1。

這個方法已由 **getNextSelectedItem2** 所取代，支援嵌套播放清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





