---
title: 'MOM_POSITIONCB 訊息 (Mmsystem .h) '
description: 當您 \_ \_ \_ 在 MIDI 輸出資料流程中到達 MEVT F 回呼事件時，會傳送 MOM 位置訊息。
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d403d9d913628f6b00a7b36dba96d0f4d491f486ef9c3edf7a5c3d5a30c345f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806998"
---
# <a name="mom_positioncb-message"></a>MOM \_ POSITIONCB 訊息

當您在 MIDI 輸出資料流程中到達 **MEVT \_ F \_ 回呼** 事件時，會傳送 **MOM \_ 位置** 訊息。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

識別輸入緩衝區之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的指標。

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

即使在執行回呼函式時，也會繼續播放資料流程緩衝區。 在緩衝區中 **MEVT \_ F \_ 回呼** 事件之後的任何事件都會排程，並在一段時間內傳送，不論回呼函數中花費了多少時間。

如果要產生的位置回呼比您的應用程式可以處理的還要快， [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwOffset** 成員可能會參考您的應用程式尚未處理的事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDI 訊息](midi-messages.md)
</dt> </dl>

 

