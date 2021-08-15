---
title: 播放清單。 getNextCheckedItem2
description: GetNextCheckedItem2 方法會以指定的索引之後，抓取播放清單中下一個核取專案的索引。
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- 播放清單. getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9bd39ba95aff88bccfa43885f8c15fba6bb0beef20d51dd3ca4cf6f36bda05b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118834865"
---
# <a name="playlistgetnextcheckeditem2"></a>播放清單。 getNextCheckedItem2

**GetNextCheckedItem2** 方法會以指定的索引之後，抓取播放清單中下一個核取專案的索引。

``` syntax
        elementID.getNextCheckedItem2(item)
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

這個方法可以使用嵌套的播放清單，並取代 **getNextCheckedItem** 方法。 在 *item* 參數中傳遞1以找出第一個選取的專案。 如果沒有進一步的核取專案，這個方法會傳回1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 getNextCheckedItem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





