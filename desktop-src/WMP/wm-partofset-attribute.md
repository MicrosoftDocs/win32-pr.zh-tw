---
title: WM/PartOfSet 屬性
description: WM/PartOfSet 屬性是專案所屬之集合的部分編號和總數。
ms.assetid: c6827c31-c625-4283-a50d-f08eccf87271
keywords:
- WM/PartOfSet 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/PartOfSet
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27d6297931c503c95c8ef0462bf7b119a0ffb75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999654"
---
# <a name="wmpartofset-attribute"></a>WM/PartOfSet 屬性

**WM/PartOfSet** 屬性是專案所屬之集合的部分編號和總數。

## <a name="applies-to"></a>套用至

-   [音樂檔案](music-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性只會儲存在不在文件庫中的音樂檔案中。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMPartOfSet。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





