---
description: '>NETWORKSTATUS 結構描述 NPP 的目前狀態。'
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: '>NETWORKSTATUS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514145"
---
# <a name="networkstatus-structure"></a>>NETWORKSTATUS 結構

**>networkstatus** 結構描述 NPP 的目前狀態。

## <a name="syntax"></a>語法


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a>成員

<dl> <dt>

**State**
</dt> <dd>

表示 NPP 的目前狀態。



| 值                                                                                                                                                                                                          | 意義                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**>NETWORKSTATUS \_ 狀態 \_ VOID**</dt> </dl>                | NPP 未連接或已連線，且未啟動 capture。<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**>NETWORKSTATUS \_ 狀態 \_ 捕獲**</dt> </dl> | NPP 正在捕獲資料。<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**>NETWORKSTATUS \_ 狀態已 \_ 暫停**</dt> </dl>          | NPP 已在捕獲資料時暫停。<br/>                                     |



 

</dd> <dt>

**旗標**
</dt> <dd>

描述 NPP 目前狀態的旗標。



| 值                                                                                                                                                                                                                             | 意義                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**>NETWORKSTATUS \_ 旗標 \_ 觸發程式 \_ 暫止**</dt> </dl> | NPP 有暫止的觸發程式。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

使用這個結構時，您必須先配置結構的記憶體，才能使用它，並在不再需要結構時釋放記憶體。

本主題底部的 [另請參閱] 清單會列出使用此結構的所有方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDelaydC：： QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP：： QueryStatus](iesp-querystatus.md)
</dt> <dt>

[IRTC：： QueryStatus](irtc-querystatus.md)
</dt> <dt>

[IStats：： QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 




