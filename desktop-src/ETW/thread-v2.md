---
description: Thread_V2 類別-這個類別是執行緒事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Thread_V2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: d057f80d5cf29f6660ee3a2ebd651c468496529a56a11147225ebd504451184c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069388"
---
# <a name="thread_v2-class"></a>執行緒 \_ V2 類別

這個類別是執行緒事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**執行緒 \_ V2** 類別未定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用執行緒事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 執行緒** 旗標。 您也可以指定下列旗標：

-   **事件 \_ 追蹤 \_ 旗標 \_ CSWITCH**
-   **事件 \_ 追蹤 \_ 旗標 \_ 發送器**

事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**ThreadGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以針對執行緒事件執行特殊處理。 使用下列事件種類來識別使用事件時的實際執行緒事件。



| 事件類型                                                      | 描述                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ END** (事件種類值為 2) <br/>   | 結束執行緒事件。 [**執行緒 \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                        |
| **活動 \_追蹤 \_ 類型 \_ 開始** (事件種類值為 1) <br/> | 啟動執行緒事件。 [**執行緒 \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                      |
| 事件種類值、3                                             | 開始資料收集執行緒事件。 列舉核心會話開始時正在執行的執行緒。 [**執行緒 \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF 類別會定義此事件的事件資料。 |
| 事件種類值，4                                             | 結束資料收集執行緒事件。 列舉核心會話結束時目前正在執行的執行緒。 [**執行緒 \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF 類別會定義此事件的事件資料。     |
| 事件種類值，36                                            | 內容切換事件。 [**CSwitch**](cswitch.md) MOF 類別會定義此事件的事件資料。                                                                                                                                |
| 事件種類值，50                                            | 就緒的執行緒事件。 [**ReadyThread**](readythread.md) MOF 類別會定義此事件的事件資料。                                                                                                                          |



 

進程和執行緒啟動事件可能會記錄在父進程或執行緒的內容中。 因此，[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員可能不會對應到正在建立的進程和執行緒。 這就是為什麼這些事件包含事件資料 (中的進程和執行緒識別碼，以及事件標頭) 中的識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**CSwitch**](cswitch.md)
</dt> <dt>

[**執行緒**](thread.md)
</dt> <dt>

[**執行緒 \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**執行緒 \_ V0**](thread-v0.md)
</dt> <dt>

[**執行緒 \_ V1**](thread-v1.md)
</dt> </dl>

 

 
