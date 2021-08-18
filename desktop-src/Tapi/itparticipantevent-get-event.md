---
description: Get \_ 事件方法 \_ 會取得已發生之事件種類的參與者事件描述元。
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'ITParticipantEvent：： get_Event 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d45e8f6aab556eb1b6f5c6dc1b4b0cbadf9653e06fd77f4fb806b7ef89d7813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864699"
---
# <a name="itparticipanteventget_event-method"></a>ITParticipantEvent：： get \_ 事件方法

\[**取得 \_事件** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ 事件** 方法會取得已發生之事件種類的 [**參與者 \_ 事件**](participant-event.md)描述元。

## <a name="syntax"></a>語法


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pParticipantEvent* \[擴展\]
</dt> <dd>

事件 [**參與者 \_ 事件**](participant-event.md) 描述項的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>      |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PParticipantEvent* 參數不是有效的指標。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**參與者 \_ 活動**](participant-event.md)
</dt> </dl>

 

 




