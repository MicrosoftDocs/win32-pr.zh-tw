---
title: 播放清單。 getNextCheckedItem
description: GetNextCheckedItem 方法會以指定的索引之後，抓取播放清單中下一個核取專案的索引。
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- 播放清單. getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54b6e598737d1aac09754b15c037c27a435deb5fff34c729aa48c51019e12982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571448"
---
# <a name="playlistgetnextcheckeditem"></a>播放清單。 getNextCheckedItem

**GetNextCheckedItem** 方法會以指定的索引之後，抓取播放清單中下一個核取專案的索引。

``` syntax
        elementID.getNextCheckedItem(item)
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

如果沒有進一步的核取專案，這個方法會傳回1。

這個方法已由 **getNextCheckedItem2** 所取代，支援嵌套播放清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





