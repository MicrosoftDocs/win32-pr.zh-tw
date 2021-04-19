---
description: 以 DVD \_ HMSF 時間 \_ 碼格式，表示與標題開頭相關的目前時間。 此事件會在每個 VOBU 的開頭觸發，每隔0.4 到1.0 秒就會發生一次。
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: 'EC_DVD_CURRENT_HMSF_TIME (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997633"
---
# <a name="ec_dvd_current_hmsf_time"></a>EC \_ DVD \_ 目前 \_ HMSF \_ 時間

以 [**DVD \_ HMSF 時間 \_ 碼**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) 格式，表示與標題開頭相關的目前時間。 此事件會在每個 VOBU 的開頭觸發，每隔0.4 到1.0 秒就會發生一次。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

包含 DVD HMSF 時間碼結構的 ULONG 值 \_ \_ 。 將 lParam1 指派給 ULONG 變數，然後將該變數轉換成 DVD \_ HMSF 時間 \_ 碼，以存取其值。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

包含 [**DVD 時間 \_ 碼 \_ 旗標**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)聯集的 ULONG 值。

</dd> </dl>

## <a name="remarks"></a>備註

DVD \_ HMSF \_ 時間碼格式的目的是要取代在 EC \_ DVD \_ 目前時間事件中傳回的舊 BCD 格式 \_ 。 HMSF 的時間碼比較容易使用。 若要讓 Navigator 傳送 EC \_ dvd \_ 目前 \_ HMSF \_ 時間事件，而不是 ec \_ dvd \_ 目前 \_ 時間事件，應用程式必須呼叫 `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` 。 設定此旗標時，導覽器也會預期 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 和 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) 方法中的所有時間參數都必須以 DVD HMSF 時間 \_ 碼傳遞 \_ 。

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

 

 




