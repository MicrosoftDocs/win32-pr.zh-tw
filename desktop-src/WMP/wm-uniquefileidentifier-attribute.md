---
title: WM/UniqueFileIdentifier 屬性
description: WM/UniqueFileIdentifier 屬性是可唯一識別專案的字串。
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- WM/UniqueFileIdentifier 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a4297f299f6e7df64088066b3137d844a0c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977784"
---
# <a name="wmuniquefileidentifier-attribute"></a>WM/UniqueFileIdentifier 屬性

**WM/UniqueFileIdentifier** 屬性是可唯一識別專案的字串。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

**UniqueFileIdentifier** 是此屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMUniqueFileIdentifier。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





