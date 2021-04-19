---
title: WM/WMCollectionID 屬性
description: WM/WMCollectionID 屬性是識別專案所屬集合的 GUID。
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- WM/WMCollectionID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bce21196e1da9583db293dab004812265c85308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978771"
---
# <a name="wmwmcollectionid-attribute"></a>WM/WMCollectionID 屬性

**WM/WMCollectionID** 屬性是識別專案所屬集合的 GUID。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和媒體檔案中。

**WMCollectionID** 是此屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMCollectionID。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





