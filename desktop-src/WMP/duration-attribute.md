---
title: Duration 屬性
description: Duration 屬性是專案的播放持續時間（以秒為單位）。
ms.assetid: 0a59a7b6-4536-4197-9f4a-1877ef42f828
keywords:
- Duration 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Duration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50e57a58eb1a2343230fd91757de1aa09901ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982703"
---
# <a name="duration-attribute"></a>Duration 屬性

**Duration** 屬性是專案的播放持續時間（以秒為單位）。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用的 Windows Media 檔案](commonly-used-windows-media-file-attributes.md)
-   [其他專案](other-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMDuration。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





