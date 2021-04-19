---
description: 參與者 \_ 事件列舉描述參與者事件。
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: 'PARTICIPANT_EVENT 列舉 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990195"
---
# <a name="participant_event-enumeration"></a>參與者 \_ 事件列舉

\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**參與者 \_ 事件** 列舉描述參與者事件。 [**ITParticipantEvent：： get \_ 事件**](itparticipantevent-get-event.md)方法會傳回這個列舉的成員，以表示發生的會議參與者事件種類。 存取 [IPCONF MSP](ipconf-msp.md)的應用程式會使用這個列舉。

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE \_ 新 \_ 參與者**
</dt> <dd>

會議已加入新的參與者。

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE \_ 資訊 \_ 變更**
</dt> <dd>

參與者的資訊已變更。

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE \_ 參與者 \_ 離開**
</dt> <dd>

參與者已離開會議。

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE \_ 新的子 \_ 流**
</dt> <dd>

參與者已加入新的子流。

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_ \_ 已移除 PE 子流**
</dt> <dd>

已從參與者移除新的子流。

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE 子 \_ 流 \_ 對應**
</dt> <dd>

參與者已對應到子流。

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE 子流未對應 \_ \_**
</dt> <dd>

已從子流取消對應參與者。

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE \_ 參與者 \_ 超時**
</dt> <dd>

因為有超時時間，所以已從會議中移除參與者。

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**已 \_ 復原 PE 參與者 \_**
</dt> <dd>

已移除的參與者也會再次顯示。 通常，這是已超時但現在收到信號的參與者。

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**使用中的 PE \_ 參與者 \_**
</dt> <dd>

參與者已在會議中生效。

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE \_ 參與者 \_ 非使用中**
</dt> <dd>

參與者在會議中已變成非使用中。

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE \_ 本機 \_ 交談**
</dt> <dd>

本機參與者已開始交談。

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ 本機 \_ 無訊息**
</dt> <dd>

本機參與者在會議中已變成無訊息。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                              |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipantEvent：： get \_ 事件**](itparticipantevent-get-event.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf MSP 介面](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




