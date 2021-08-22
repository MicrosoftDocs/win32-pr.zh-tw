---
title: FileSize 屬性
description: FileSize 屬性是檔案的大小（以位元組為單位）。
ms.assetid: e845cc82-6975-4fd9-800f-a66f59a5fb39
keywords:
- FileSize 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- FileSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe1d3a1bed9bc5a8ca87991b910ffa3804267fc217ff8b500cae79f185cb8a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390908"
---
# <a name="filesize-attribute"></a>FileSize 屬性

**FileSize** 屬性是檔案的大小（以位元組為單位）。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案](commonly-used-windows-media-file-attributes.md)
-   [其他專案](other-item-attributes.md)
-   [相片專案](photo-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

**Size** 是這個屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMFileSize。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本 (只有 Windows Media Player 10 或更新版本才支援相片專案) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





