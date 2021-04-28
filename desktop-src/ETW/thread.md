---
description: Thread 類別-這個類別是執行緒事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105526"
---
# <a name="thread-class"></a>Thread 類別

這個類別是執行緒事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**Thread** 類別未定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用執行緒事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 執行緒** 旗標。

事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**ThreadGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以針對執行緒事件執行特殊處理。 使用下列事件種類來識別使用事件時的實際執行緒事件。



| 事件類型                                                      | 描述                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ END** (事件種類值為 2) <br/>   | 結束執行緒事件。 [**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                        |
| **活動 \_追蹤 \_ 類型 \_ 開始** (事件種類值為 1) <br/> | 啟動執行緒事件。 [**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                      |
| 事件種類值、3                                             | 開始資料收集執行緒事件。 列舉核心會話開始時正在執行的執行緒。 [**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF 類別會定義此事件的事件資料。 |
| 事件種類值，4                                             | 結束資料收集執行緒事件。 列舉核心會話結束時目前正在執行的執行緒。 [**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF 類別會定義此事件的事件資料。     |



 

進程和執行緒啟動事件可能會記錄在父進程或執行緒的內容中。 因此，[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員可能不會對應到正在建立的進程和執行緒。 這就是為什麼這些事件包含事件資料 (中的進程和執行緒識別碼，以及事件標頭) 中的識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**執行緒 \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**執行緒 \_ V0**](thread-v0.md)
</dt> <dt>

[**執行緒 \_ V1**](thread-v1.md)
</dt> <dt>

[**執行緒 \_ V2**](thread-v2.md)
</dt> </dl>

 

 
