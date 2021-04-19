---
title: WM/WMCollectionGroupID 屬性
description: WM/WMCollectionGroupID 屬性是 GUID，可識別包含專案所屬集合的群組。
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- WM/WMCollectionGroupID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999278"
---
# <a name="wmwmcollectiongroupid-attribute"></a>WM/WMCollectionGroupID 屬性

**WM/WMCollectionGroupID** 屬性是 GUID，可識別包含專案所屬集合的群組。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

**WMCollectionGroupID** 是此屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMCollectionGroupID。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





