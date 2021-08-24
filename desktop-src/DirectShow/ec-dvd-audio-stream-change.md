---
description: 表示 DVD 主要標題的目前音訊串流號碼已變更。
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: 'EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2ad6015ef132a98d02dc207cb9d43b6324ea3a05c541f43e295e75d13b5bb7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998128"
---
# <a name="ec_dvd_audio_stream_change"></a>EC \_ DVD \_ 音訊 \_ 串流 \_ 變更

表示 DVD 主要標題的目前音訊串流號碼已變更。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** 值，指出新的使用者音訊串流號碼。 音訊串流數位的範圍是從0到7。 Stream 0xFFFFFFFF 表示未選取任何資料流程。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="remarks"></a>備註

目前的音訊串流可以使用在光碟上撰寫的流覽命令，以及透過使用 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面的應用程式控制，自動變更。

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

 

 




