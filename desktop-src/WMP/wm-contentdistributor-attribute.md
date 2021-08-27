---
title: WM/ContentDistributor 屬性
description: WM/ContentDistributor 屬性是專案的散發者名稱。
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- WM/ContentDistributor 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba79ab07b8579961db70038ef80f79da974ba5dff6d3ac88781be5d4f046f088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122707"
---
# <a name="wmcontentdistributor-attribute"></a>WM/ContentDistributor 屬性

**WM/ContentDistributor** 屬性是專案的散發者名稱。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

**ContentDistributor** 是此屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMContentDistributor。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





