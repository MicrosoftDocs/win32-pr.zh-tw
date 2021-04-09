---
title: 'MM_MOM_POSITIONCB 訊息 (Mmsystem .h) '
description: 當您 \_ \_ \_ \_ 在 MIDI 輸出資料流程中到達 MEVT F 回呼事件時，會將 MM MOM POSITIONCB 訊息傳送至視窗。
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933979"
---
# <a name="mm_mom_positioncb-message"></a>MM \_ MOM \_ POSITIONCB 訊息

當 **您 \_ \_** \_ \_ 在 MIDI 輸出資料流程中到達 MEVT F 回呼事件時，會將 MM MOM POSITIONCB 訊息傳送至視窗。


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

[**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的指標，可識別造成回呼的事件。 **DwOffset** 成員會提供事件的位移。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

保護請勿使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

即使在執行回呼函式時，也會繼續播放資料流程緩衝區。 在 \_ 緩衝區中 MEVT F 回呼事件之後的任何事件 \_ 都會排程，並在一段時間內傳送，不論回呼函數中花費了多少時間。

如果要產生的位置回呼比您的應用程式可以處理的還要快， [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwOffset** 成員可能會參考您的應用程式尚未處理的事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDI 訊息](midi-messages.md)
</dt> </dl>

 

