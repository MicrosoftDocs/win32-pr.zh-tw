---
description: 表示每個影片物件單位的開頭 (VOBU) ，其長度為0.4 到1.0 秒的影片區段。
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: 'EC_DVD_CURRENT_TIME (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990192"
---
# <a name="ec_dvd_current_time"></a>EC \_ DVD \_ 目前 \_ 時間

表示每個影片物件單位的開頭 (VOBU) ，其長度為0.4 到1.0 秒的影片區段。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** 值，指出二進位編碼十進位 (BCD 中目前的播放時間碼，) 小時、分鐘、秒、框架 (HH： MM： SS： FF) 格式。 [**DVD 時間 \_ 碼**](/windows/win32/api/strmif/ns-strmif-dvd_timecode)結構的成員。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

布林值 (**BOOL**) 指出時間碼的值。 零 (0) 表示每秒25個畫面格，1表示每秒30個畫面格 (nondropped) 。 值為2表示無法判斷播放時間。

</dd> </dl>

## <a name="remarks"></a>備註

只有簡單的線性電影會發出此事件的信號。

此事件會在標題網域中引發。

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

 

 




