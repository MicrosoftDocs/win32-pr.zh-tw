---
description: 表示任何仍舊 (的 PGC、Cell 或 VOBU) 的開頭。
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: 'EC_DVD_STILL_ON (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977631"
---
# <a name="ec_dvd_still_on"></a>EC \_ DVD \_ 仍 \_ 在開啟

表示任何仍舊 (的 PGC、Cell 或 VOBU) 的開頭。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

布林值 (**BOOL**) 指出按鈕是否可用的值。 零 (0) 表示按鈕可供使用，因此 [**IDvdControl2：： StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) 方法將無法運作。 一個 (1) 表示沒有可用的按鈕，因此 **IDvdControl2：： StillOff** 可運作。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**DWORD** 值，指出仍會持續的秒數。 0xFFFFFFFF 表示仍無限制，這表示要等到使用者按下按鈕，或直到應用程式呼叫 [**IDvdControl2：： StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)為止。

</dd> </dl>

## <a name="remarks"></a>備註

所有按鈕的組合和仍可 (按鈕在上仍開啟的按鈕、具有仍然關閉的按鈕、按下 [開啟] 按鈕、按下 [開啟]、[仍關閉]) 。

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

 

 




