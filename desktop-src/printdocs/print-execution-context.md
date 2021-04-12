---
description: 表示呼叫 GetPrintExecutionData 時的執行內容。
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: 'PRINT_EXECUTION_CONTEXT 列舉 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192712"
---
# <a name="print_execution_context-enumeration"></a>列印 \_ 執行 \_ 內容列舉

表示呼叫 [**GetPrintExecutionData**](getprintexecutiondata.md) 時的執行內容。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**列印 \_ 執行 \_ 內容 \_ 應用程式**
</dt> <dd>

呼叫端正在應用程式中執行。

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**列印 \_ 執行 \_ 內容 \_ 多工緩衝處理程式 \_ 服務**
</dt> <dd>

呼叫端在多工緩衝處理器服務中執行 (spoolsv.exe) 。

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**列印 \_ 執行 \_ 內容 \_ 多工緩衝處理程式 \_ 隔離 \_ 主機**
</dt> <dd>

呼叫端正在列印隔離主機 (PrintIsolationHost.exe 中執行) 

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**列印 \_ 執行 \_ 內容 \_ 篩選 \_ 管線**
</dt> <dd>

呼叫端會在列印篩選管線 (printfilterpipelinesvc.exe 中執行) 

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**列印 \_ 執行 \_ 內容 \_ WOW64**
</dt> <dd>

呼叫端正在 splwow64.exe

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**列印 \_ 執行 \_ 資料**](print-execution-data.md)
</dt> </dl>

 

 




