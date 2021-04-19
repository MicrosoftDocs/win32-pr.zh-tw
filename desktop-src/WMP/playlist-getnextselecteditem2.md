---
title: 播放清單。 getNextSelectedItem2
description: GetNextSelectedItem2 方法會以指定的索引之後，抓取播放清單中下一個選取專案的索引。
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- 播放清單. getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982509"
---
# <a name="playlistgetnextselecteditem2"></a>播放清單。 getNextSelectedItem2

**GetNextSelectedItem2** 方法會以指定的索引之後，抓取播放清單中下一個選取專案的索引。

``` syntax
        elementID.getNextSelectedItem2(item)
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

這個方法可以使用嵌套的播放清單，並取代 **getNextSelectedItem** 方法。 在 *item* 參數中傳遞1以尋找第一個選取的專案。 如果沒有其他選取的專案，則會傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





