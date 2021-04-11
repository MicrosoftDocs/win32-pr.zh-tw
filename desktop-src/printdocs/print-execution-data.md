---
description: 包含呼叫 GetPrintExecutionData 之印表機驅動程式的執行內容。
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: 'PRINT_EXECUTION_DATA 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194135"
---
# <a name="print_execution_data-structure"></a><span data-ttu-id="4c902-103">列印 \_ 執行 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="4c902-103">PRINT\_EXECUTION\_DATA structure</span></span>

<span data-ttu-id="4c902-104">包含呼叫 [**GetPrintExecutionData**](getprintexecutiondata.md)之印表機驅動程式的執行內容。</span><span class="sxs-lookup"><span data-stu-id="4c902-104">Contains the execution context of the printer driver that calls [**GetPrintExecutionData**](getprintexecutiondata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c902-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c902-105">Syntax</span></span>


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a><span data-ttu-id="4c902-106">成員</span><span class="sxs-lookup"><span data-stu-id="4c902-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c902-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="4c902-107">**context**</span></span>
</dt> <dd>

<span data-ttu-id="4c902-108">[**列印 \_ 執行 \_ 內容**](print-execution-context.md)值，代表印表機驅動程式的目前執行內容。</span><span class="sxs-lookup"><span data-stu-id="4c902-108">The [**PRINT\_EXECUTION\_CONTEXT**](print-execution-context.md) value that represents the current execution context of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="4c902-109">**clientAppPID**</span><span class="sxs-lookup"><span data-stu-id="4c902-109">**clientAppPID**</span></span>
</dt> <dd>

<span data-ttu-id="4c902-110">如果 **coNtext** 的值是 **列印 \_ 執行 \_ 內容 \_ WOW64**， **clientAppPID** 會識別代表 splwow64.exe 進程載入印表機驅動程式的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="4c902-110">If the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** identifies the client application on whose behalf the splwow64.exe process loaded the printer driver.</span></span> <span data-ttu-id="4c902-111">如果 **內容** 的值不是 **列印 \_ 執行 \_ 內容 \_ WOW64**，則 **clientAppPID** 為零。</span><span class="sxs-lookup"><span data-stu-id="4c902-111">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** is zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c902-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c902-112">Requirements</span></span>



| <span data-ttu-id="4c902-113">需求</span><span class="sxs-lookup"><span data-stu-id="4c902-113">Requirement</span></span> | <span data-ttu-id="4c902-114">值</span><span class="sxs-lookup"><span data-stu-id="4c902-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c902-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c902-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4c902-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c902-116">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="4c902-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c902-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4c902-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c902-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="4c902-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4c902-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c902-120"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4c902-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c902-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c902-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c902-122">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="4c902-122">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="4c902-123">**列印 \_ 執行 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="4c902-123">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> </dl>

 

 




