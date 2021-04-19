---
description: GetPrintExecutionData 會捕獲目前的列印內容。
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: 'GetPrintExecutionData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988434"
---
# <a name="getprintexecutiondata-function"></a><span data-ttu-id="e7dbb-103">GetPrintExecutionData 函式</span><span class="sxs-lookup"><span data-stu-id="e7dbb-103">GetPrintExecutionData function</span></span>

<span data-ttu-id="e7dbb-104">**GetPrintExecutionData** 會捕獲目前的列印內容。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-104">The **GetPrintExecutionData** retrieves the current print context.</span></span>

> [!Note]  
> <span data-ttu-id="e7dbb-105">這項功能的目的是要供在列印多工緩衝處理器內容中執行的印表機驅動程式使用。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-105">This function is intended for use by printer drivers that are running in the context of the print spooler.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e7dbb-106">語法</span><span class="sxs-lookup"><span data-stu-id="e7dbb-106">Syntax</span></span>


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a><span data-ttu-id="e7dbb-107">參數</span><span class="sxs-lookup"><span data-stu-id="e7dbb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7dbb-108">*.pdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e7dbb-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7dbb-109">變數的指標，此變數會接收 [**列印 \_ 執行 \_ 資料**](print-execution-data.md) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-109">A pointer to a variable that receives the address of the [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7dbb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7dbb-110">Return value</span></span>

<span data-ttu-id="e7dbb-111">如果函式成功，則傳回 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-111">Returns **TRUE** if the function succeeds; otherwise **FALSE**.</span></span> <span data-ttu-id="e7dbb-112">如果傳回值為 **FALSE**，則呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-112">If the return value is **FALSE**, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7dbb-113">備註</span><span class="sxs-lookup"><span data-stu-id="e7dbb-113">Remarks</span></span>

<span data-ttu-id="e7dbb-114">印表機驅動程式應該呼叫 winspool.drv. winspool.drv 模組上的 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 來取得 **GetPrintExecutionData** 函式的位址，因為 Windows Vista 或舊版 windows 不支援 **GetPrintExecutionData** 。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-114">Printer drivers should call [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) on the winspool.drv module to get the address of the **GetPrintExecutionData** function because **GetPrintExecutionData** is not supported on Windows Vista or earlier versions of Windows.</span></span>

<span data-ttu-id="e7dbb-115">只有當 *.pdata* 的值為 **Null** 時， **GetPrintExecutionData** 才會失敗。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-115">**GetPrintExecutionData** only fails if the value of *pData* is **NULL**.</span></span>

<span data-ttu-id="e7dbb-116">只有當 **coNtext** 的值是 **列印 \_ 執行 \_ 內容 \_ WOW64** 時，[**列印 \_ 執行 \_ 資料**](print-execution-data.md)的 **clientAppPID** 成員值才有意義。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-116">The value of the **clientAppPID** member of [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) is only meaningful if the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**.</span></span> <span data-ttu-id="e7dbb-117">如果 **內容** 的值不是 **列印 \_ 執行 \_ 內容 \_ WOW64**，則 **clientAppPID** 的值為0。</span><span class="sxs-lookup"><span data-stu-id="e7dbb-117">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, the value of **clientAppPID** is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7dbb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7dbb-118">Requirements</span></span>



| <span data-ttu-id="e7dbb-119">需求</span><span class="sxs-lookup"><span data-stu-id="e7dbb-119">Requirement</span></span> | <span data-ttu-id="e7dbb-120">值</span><span class="sxs-lookup"><span data-stu-id="e7dbb-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7dbb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7dbb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e7dbb-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7dbb-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="e7dbb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7dbb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e7dbb-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7dbb-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="e7dbb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e7dbb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7dbb-126"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e7dbb-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e7dbb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e7dbb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7dbb-128"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="e7dbb-128"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="e7dbb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7dbb-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7dbb-130">[**3]。Getlasterror**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="e7dbb-130">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>
</dt> <dt>

[<span data-ttu-id="e7dbb-131">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="e7dbb-131">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="e7dbb-132">**列印 \_ 執行 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="e7dbb-132">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> <dt>

[<span data-ttu-id="e7dbb-133">**列印 \_ 執行 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="e7dbb-133">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

