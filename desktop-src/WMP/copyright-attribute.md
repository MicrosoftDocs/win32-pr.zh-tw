---
title: '著作權屬性 (Msfeeds .h) '
description: 著作權屬性是專案的著作權訊息。
ms.assetid: 617272cb-883f-46d6-b0a9-29ac32c63148
keywords:
- 著作權屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Copyright
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b42e68e0d3485824f502dea991048121e788dfbe574b8fa4921e93a3b7afb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651958"
---
# <a name="copyright-attribute"></a>著作權屬性

**著作權** 屬性是專案的著作權訊息。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用 Windows 媒體檔案](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMCopyright。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                    |
| 標頭<br/>  | <dl> <dt>Msfeeds。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





