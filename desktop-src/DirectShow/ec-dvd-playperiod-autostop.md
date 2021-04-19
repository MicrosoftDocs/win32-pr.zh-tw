---
description: 指出導覽器已完成播放 IDvdControl2：:P layPeriodInTitleAutoStop 呼叫中指定的區段。
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: 'EC_DVD_PLAYPERIOD_AUTOSTOP (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993296"
---
# <a name="ec_dvd_playperiod_autostop"></a>EC \_ DVD \_ PLAYPERIOD \_ AUTOSTOP

指出導覽器已完成播放 [**IDvdControl2：:P layperiodintitleautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)呼叫中指定的區段。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

零個。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="remarks"></a>備註

此事件會在標題網域中引發。

在導覽器完成播放指定的區段之前，也會一併傳送此事件。

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
</dt> <dt>

[**IDvdControl2：:P layPeriodInTitleAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 




