---
description: 當系統參數的值註冊 (SPRM) 變更時傳送。
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: 'EC_DVD_SPRM_Change (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 1af5b8637a197973bca2129a8b8a0198d20248eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994203"
---
# <a name="ec_dvd_sprm_change"></a>EC \_ DVD \_ SPRM \_ 變更

當系統參數的值註冊 (SPRM) 變更時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

已變更之 SPRM 值的以零為基底的索引。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

較低的16個位包含新的 SPRM 值。

</dd> </dl>

## <a name="remarks"></a>備註

此事件預設為停用。 若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。

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

[**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




