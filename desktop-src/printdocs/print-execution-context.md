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
# <a name="print_execution_context-enumeration"></a><span data-ttu-id="4018e-103">列印 \_ 執行 \_ 內容列舉</span><span class="sxs-lookup"><span data-stu-id="4018e-103">PRINT\_EXECUTION\_CONTEXT enumeration</span></span>

<span data-ttu-id="4018e-104">表示呼叫 [**GetPrintExecutionData**](getprintexecutiondata.md) 時的執行內容。</span><span class="sxs-lookup"><span data-stu-id="4018e-104">Represents the execution context when [**GetPrintExecutionData**](getprintexecutiondata.md) is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="4018e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4018e-105">Syntax</span></span>


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="4018e-106">常數</span><span class="sxs-lookup"><span data-stu-id="4018e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4018e-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**列印 \_ 執行 \_ 內容 \_ 應用程式**</span><span class="sxs-lookup"><span data-stu-id="4018e-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**PRINT\_EXECUTION\_CONTEXT\_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="4018e-108">呼叫端正在應用程式中執行。</span><span class="sxs-lookup"><span data-stu-id="4018e-108">The caller is running in an application.</span></span>

</dd> <dt>

<span data-ttu-id="4018e-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**列印 \_ 執行 \_ 內容 \_ 多工緩衝處理程式 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="4018e-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="4018e-110">呼叫端在多工緩衝處理器服務中執行 (spoolsv.exe) 。</span><span class="sxs-lookup"><span data-stu-id="4018e-110">The caller is running in the spooler service (spoolsv.exe).</span></span>

</dd> <dt>

<span data-ttu-id="4018e-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**列印 \_ 執行 \_ 內容 \_ 多工緩衝處理程式 \_ 隔離 \_ 主機**</span><span class="sxs-lookup"><span data-stu-id="4018e-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_ISOLATION\_HOST**</span></span>
</dt> <dd>

<span data-ttu-id="4018e-112">呼叫端正在列印隔離主機 (PrintIsolationHost.exe 中執行) </span><span class="sxs-lookup"><span data-stu-id="4018e-112">The caller is running in the print isolation host (PrintIsolationHost.exe)</span></span>

</dd> <dt>

<span data-ttu-id="4018e-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**列印 \_ 執行 \_ 內容 \_ 篩選 \_ 管線**</span><span class="sxs-lookup"><span data-stu-id="4018e-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**PRINT\_EXECUTION\_CONTEXT\_FILTER\_PIPELINE**</span></span>
</dt> <dd>

<span data-ttu-id="4018e-114">呼叫端會在列印篩選管線 (printfilterpipelinesvc.exe 中執行) </span><span class="sxs-lookup"><span data-stu-id="4018e-114">The caller is running in the print filter pipeline (printfilterpipelinesvc.exe)</span></span>

</dd> <dt>

<span data-ttu-id="4018e-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**列印 \_ 執行 \_ 內容 \_ WOW64**</span><span class="sxs-lookup"><span data-stu-id="4018e-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**PRINT\_EXECUTION\_CONTEXT\_WOW64**</span></span>
</dt> <dd>

<span data-ttu-id="4018e-116">呼叫端正在 splwow64.exe</span><span class="sxs-lookup"><span data-stu-id="4018e-116">The caller is running in splwow64.exe</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4018e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4018e-117">Requirements</span></span>



| <span data-ttu-id="4018e-118">需求</span><span class="sxs-lookup"><span data-stu-id="4018e-118">Requirement</span></span> | <span data-ttu-id="4018e-119">值</span><span class="sxs-lookup"><span data-stu-id="4018e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4018e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4018e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4018e-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4018e-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="4018e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4018e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4018e-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4018e-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="4018e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4018e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4018e-125"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4018e-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4018e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4018e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4018e-127">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="4018e-127">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="4018e-128">**列印 \_ 執行 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="4018e-128">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

 




