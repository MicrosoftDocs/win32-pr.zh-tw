---
title: WM/Period 屬性
description: WM/Period 屬性是內容的期間。
ms.assetid: fb154ef7-c8bc-4468-8f3f-4b716291fd0a
keywords:
- WM/Period 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Period
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a46be5c66fb2dc6f9f6739a57778deef04b113f174208c5d56fe0712589aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053806"
---
# <a name="wmperiod-attribute"></a>WM/Period 屬性

**WM/period** 屬性是內容的期間。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

**Period** 是這個屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMPeriod。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





