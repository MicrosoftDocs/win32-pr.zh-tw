---
title: MediaContentTypes 屬性
description: MediaContentTypes 屬性會指定專案中的內容類型。
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- MediaContentTypes 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca3c422083954554db76657a0bb9cc10062fd878a9ebf4b31f4dc88734ac1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996238"
---
# <a name="mediacontenttypes-attribute"></a>MediaContentTypes 屬性

**MediaContentTypes** 屬性會指定專案中的內容類型。

## <a name="applies-to"></a>套用至

-   [播放清單](playlist-attributes-ref.md)

## <a name="remarks"></a>備註

這個屬性可以是下列其中一個值：



| 值 | 意義                                |
|-------|----------------------------------------|
| 1     | 播放清單包含音訊內容。   |
| 2     | 提供。                        |
| 3     | 播放清單包含音訊內容。   |
| 4     | 播放清單包含影片內容。   |
| 5     | 播放清單包含圖片內容。 |
| 6     | 播放清單包含電視內容。      |



 

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





