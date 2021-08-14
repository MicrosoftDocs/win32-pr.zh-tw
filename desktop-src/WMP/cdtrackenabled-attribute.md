---
title: CDTrackEnabled 屬性
description: CDTrackEnabled 屬性會指出是否已啟用播放軌。
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- CDTrackEnabled 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a86c94c2c1b44327cdbfb35544c3e0b5b34d25885215d78dbec0ec084d056e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342681"
---
# <a name="cdtrackenabled-attribute"></a>CDTrackEnabled 屬性

**CDTrackEnabled** 屬性會指出是否已啟用播放軌。

## <a name="applies-to"></a>套用至

-   [CD 曲目](cd-track-attributes.md)

## <a name="remarks"></a>備註

這個屬性只會儲存在程式庫快取中。

在 Windows Media Player 中播放 CD 時，使用者可以選取曲目並指定不應該播放。 如果可以播放此追蹤，這個屬性的值就是 True; 如果使用者指定不應該播放此播放軌，則為 False。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





