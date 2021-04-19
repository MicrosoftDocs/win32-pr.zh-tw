---
title: Is_Protected 屬性
description: '\_受保護的屬性會指出內容是否使用數位版權管理 (DRM) 來保護。'
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Is_Protected 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980242"
---
# <a name="is_protected-attribute"></a>\_受保護的屬性

**\_ 受保護** 的屬性會指出內容是否使用數位版權管理 (DRM) 來保護。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用的 Windows Media 檔案](commonly-used-windows-media-file-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

**DigitallySecure** 是此屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMProtected。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





