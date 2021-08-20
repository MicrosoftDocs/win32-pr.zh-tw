---
title: WM/TrackNumber 屬性
description: WM/TrackNumber 屬性是原始發行的專輯上專案的曲目編號。
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- WM/TrackNumber 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4820ee1f8bf582705b00b6fa7d2ba37869d67835e69d5b9fd339c41bc0ce18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930824"
---
# <a name="wmtracknumber-attribute"></a>WM/TrackNumber 屬性

**WM/TrackNumber** 屬性是原始發行的專輯上專案的曲目編號。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

專輯的曲目編號從1開始。

**OriginalIndex** 和 **OriginalIndexLeft** 是這個屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMTrackNumber。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





