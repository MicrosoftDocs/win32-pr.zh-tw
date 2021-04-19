---
title: 播放清單。複製
description: 複製方法會從 CD 開始複製作業。
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- 播放清單。複製 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994291"
---
# <a name="playlistcopy"></a>播放清單。複製

**複製** 方法會從 CD 開始複製作業。

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法只會複製播放清單中的已核取專案，而且其運作方式與在 Windows Media Player 的完整模式中， **從 [從 CD 複製** ] 窗格的方式相同。 若要讓此方法運作，cd 必須位於 CD 光碟機中。 將 **checkboxesVisible** 屬性設定為 true，可讓使用者在複製前選取 CD 上的個別專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**播放清單。複製**](playlist-copying.md)
</dt> </dl>

 

 





