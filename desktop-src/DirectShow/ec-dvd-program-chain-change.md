---
description: 當目前的程式鏈 (PGC) 變更時傳送。
ms.assetid: 80fcd059-6ab4-4116-ac3a-012c451237b3
title: 'EC_DVD_PROGRAM_CHAIN_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CHAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: eefd45ac1d147a0409417f215e56a4db490dfdbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992160"
---
# <a name="ec_dvd_program_chain_change"></a>EC \_ DVD \_ 程式 \_ 鏈 \_ 變更

當目前的程式鏈 (PGC) 變更時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

新的程式鏈號 (PGCN) 。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

地區設定識別碼 (為音訊語言的 LCID) 。

</dd> </dl>

## <a name="remarks"></a>備註

此事件預設為停用。 若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ NotifyPositionChange** 選項設定為 **TRUE**。

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

 

 




