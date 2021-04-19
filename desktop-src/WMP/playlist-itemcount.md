---
title: 播放清單。 itemCount
description: ItemCount 屬性會抓取播放清單元素目前所顯示的專案數。
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- 播放清單. itemCount Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999503"
---
# <a name="playlistitemcount"></a>播放清單。 itemCount

**ItemCount** 屬性會抓取 **播放清單** 元素目前所顯示的專案數。

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

**ItemCount** 屬性將會計算展開專案的總數。 例如，如果有兩個包含三個媒體專案的播放清單，則如果沒有展開播放清單，則 **itemCount** 會傳回2。 如果只展開第一個播放清單，則 **itemCount** 會傳回4。 如果這兩個播放清單都已展開， **itemCount** 會傳回6。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> </dl>

 

 





