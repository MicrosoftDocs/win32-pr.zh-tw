---
description: 表示已起始 DVD 播放的速率變更。
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: 'EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8de40dc8fd7f70dda522f4d1faf34f8c05059c6928f80a141d7ac9ae1889ecec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823678"
---
# <a name="ec_dvd_playback_rate_change"></a>EC \_ DVD \_ 播放 \_ 速率 \_ 變更

表示已起始 DVD 播放的速率變更。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

長時程表示新的播放速率。 值是實際的播放率乘以10000，因此播放速率等於 10000.0/ *lParam1*。 小於零的值表示反向播放模式，而大於零的值表示向前播放模式。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="remarks"></a>備註

此事件會在標題網域中引發。

播放 *速率* 是播放 *速度* 的反向。 例如，如果播放速度為2x，則速率為0.5。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdevcode (包含 Dshow) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> <dt>

[DVD 事件通知碼](dvd-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 




