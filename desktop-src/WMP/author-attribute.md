---
title: Author 屬性
description: Author 屬性是與內容相關聯之媒體演出者或動作專案的名稱。
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Author 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976143"
---
# <a name="author-attribute"></a>Author 屬性

**Author** 屬性是與內容相關聯之媒體演出者或動作專案的名稱。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用的 Windows Media 檔案](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [GetItemInfoByType](media-getiteminfobytype.md)
-   [相片專案](photo-item-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [單選項目](radio-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和媒體檔案中。

這個屬性可以有多個值。 若要取得多重值屬性的所有值，您必須使用 *媒體*。**getItemInfoByType** 方法，而不是 *媒體*。**getItemInfo** 方法。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMAuthor。

**執行者** 和 **演出者** 是這個屬性的別名。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





