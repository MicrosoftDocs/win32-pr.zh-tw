---
description: 表示 DVD 播放已停止。 當標題或章節完成，而且 DVD 導覽器找不到任何其他分支指示以進行後續播放時，就會傳送此事件。 當應用程式停止播放時，不會傳送此事件。
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: 'EC_DVD_PLAYBACK_STOPPED (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000749"
---
# <a name="ec_dvd_playback_stopped"></a>EC \_ DVD \_ 播放 \_ 已停止

表示 DVD 播放已停止。 當標題或章節完成，而且 [DVD 導覽器](dvd-navigator-filter.md) 找不到任何其他分支指示以進行後續播放時，就會傳送此事件。 當應用程式停止播放時，不會傳送此事件。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

[**DVD \_ PB \_ 已停止**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped)列舉的成員，表示播放停止的原因。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="remarks"></a>備註

此事件會在所有網域中引發。

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

 

 




