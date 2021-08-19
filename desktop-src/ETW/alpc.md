---
description: 這個類別是 advanced local procedure 呼叫事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: ALPC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 435b55c44f06b6be062653a45e14a1a890e026371d8bd8e649c87ce3542118c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070288"
---
# <a name="alpc-class"></a>ALPC 類別

這個類別是 advanced local procedure 呼叫事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**ALPC** 類別未定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用 advanced local procedure 呼叫事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ ALPC** 旗標。

事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**ALPCGuid**](nt-kernel-logger-constants.md) 指定為 *PGUID* 參數，以針對 ALPC 事件執行特殊處理。 使用事件時，請使用下列事件種類來識別實際的 ALPC 事件。



| 事件類型           | 描述                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 事件種類值，33 | 傳送訊息事件。 [**ALPC \_ 傳送 \_ 訊息**](alpc-send-message.md)MOF 類別會定義此事件的事件資料。                           |
| 事件種類值，34 | 接收訊息事件。 [**ALPC \_ 接收 \_ 訊息**](alpc-receive-message.md)MOF 類別會定義此事件的事件資料。                  |
| 事件種類值，35 | 等候回復事件。 [**ALPC \_ 等候 \_ \_ 回復**](alpc-wait-for-reply.md)MOF 類別會定義此事件的事件資料。                    |
| 事件種類值，36 | 等候新的訊息事件。 [**ALPC \_ 等候 \_ \_ 新 \_ 訊息**](alpc-wait-for-new-message.md)MOF 類別定義此事件的事件資料。 |
| 事件種類值，37 | 停止等候事件。 [**ALPC \_ Unwait**](alpc-unwait.md) MOF 類別會定義此事件的事件資料。                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

