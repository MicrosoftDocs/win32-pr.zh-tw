---
title: WM/內容類型屬性
description: WM/內容屬性是內容的內容類型。
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- WM/內容類型屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0ef67b0b41ff59f644b0d52376428ae7a2330d388aa62f9765cb4842eeb561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000978"
---
# <a name="wmgenre-attribute"></a>WM/內容類型屬性

**WM/** 內容屬性是內容的內容類型。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [其他專案](other-item-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

這個屬性可以有多個值。 若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。

內容 **類型是此** 屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMGenre。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**GetItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





