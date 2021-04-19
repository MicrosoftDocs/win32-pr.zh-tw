---
title: WM/導體屬性
description: WM/導體屬性是音樂的導線名稱。
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- WM/導體屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998779"
---
# <a name="wmconductor-attribute"></a>WM/導體屬性

**WM/導體** 屬性是音樂的導線名稱。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

這個屬性可以有多個值。 若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。

**導體** 是這個屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMConductor。

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

 

 





