---
description: ScheduleJob 函式要求列印多工緩衝處理器排程指定的列印工作來進行列印。
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: 'ScheduleJob 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980552"
---
# <a name="schedulejob-function"></a><span data-ttu-id="69e56-103">ScheduleJob 函式</span><span class="sxs-lookup"><span data-stu-id="69e56-103">ScheduleJob function</span></span>

<span data-ttu-id="69e56-104">**ScheduleJob** 函式要求列印多工緩衝處理器排程指定的列印工作來進行列印。</span><span class="sxs-lookup"><span data-stu-id="69e56-104">The **ScheduleJob** function requests that the print spooler schedule a specified print job for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e56-105">語法</span><span class="sxs-lookup"><span data-stu-id="69e56-105">Syntax</span></span>


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a><span data-ttu-id="69e56-106">參數</span><span class="sxs-lookup"><span data-stu-id="69e56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69e56-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69e56-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e56-108">列印工作之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="69e56-108">A handle to the printer for the print job.</span></span> <span data-ttu-id="69e56-109">這必須是設定為多工緩衝處理印表機的本機印表機。</span><span class="sxs-lookup"><span data-stu-id="69e56-109">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="69e56-110">如果 *hPrinter* 是遠端印表機連線的控制碼，或印表機設定為直接列印，則 **ScheduleJob** 函式會失敗。</span><span class="sxs-lookup"><span data-stu-id="69e56-110">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **ScheduleJob** function fails.</span></span> <span data-ttu-id="69e56-111">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="69e56-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

<span data-ttu-id="69e56-112">*hPrinter* 必須與取得 *dwJobID* 列印工作識別碼的 [**system.printing.printqueue.addjob**](addjob.md)呼叫中指定的印表機控制碼相同。</span><span class="sxs-lookup"><span data-stu-id="69e56-112">*hPrinter* must be the same printer handle specified in the call to [**AddJob**](addjob.md) that obtained the *dwJobID* print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="69e56-113">*dwJobID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69e56-113">*dwJobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e56-114">要排程的列印工作。</span><span class="sxs-lookup"><span data-stu-id="69e56-114">The print job to be scheduled.</span></span> <span data-ttu-id="69e56-115">您可以藉由呼叫 [**system.printing.printqueue.addjob**](addjob.md) 函數來取得此列印工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="69e56-115">You obtain this print job identifier by calling the [**AddJob**](addjob.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69e56-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="69e56-116">Return value</span></span>

<span data-ttu-id="69e56-117">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="69e56-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="69e56-118">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="69e56-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="69e56-119">備註</span><span class="sxs-lookup"><span data-stu-id="69e56-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="69e56-120">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="69e56-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="69e56-121">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="69e56-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="69e56-122">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="69e56-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="69e56-123">您必須先成功呼叫 [**system.printing.printqueue.addjob**](addjob.md) 函式，才能呼叫 **ScheduleJob** 函數。</span><span class="sxs-lookup"><span data-stu-id="69e56-123">You must successfully call the [**AddJob**](addjob.md) function before calling the **ScheduleJob** function.</span></span> <span data-ttu-id="69e56-124">**System.printing.printqueue.addjob** 會取得您以 *dwJobID* 的形式傳遞至 **ScheduleJob** 的列印工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="69e56-124">**AddJob** obtains the print job identifier that you pass to **ScheduleJob** as *dwJobID*.</span></span> <span data-ttu-id="69e56-125">這兩個呼叫都必須使用相同的 *hPrinter* 值。</span><span class="sxs-lookup"><span data-stu-id="69e56-125">Both calls must use the same value for *hPrinter*.</span></span>

<span data-ttu-id="69e56-126">**ScheduleJob** 函式會檢查有效的多工緩衝處理檔案。</span><span class="sxs-lookup"><span data-stu-id="69e56-126">The **ScheduleJob** function checks for a valid spool file.</span></span> <span data-ttu-id="69e56-127">如果有不正確多工緩衝處理檔案，或如果是空的， **ScheduleJob** 會同時刪除多工緩衝處理檔案和列印多工緩衝處理器中對應的列印工作專案。</span><span class="sxs-lookup"><span data-stu-id="69e56-127">If there is an invalid spool file, or if it is empty, **ScheduleJob** deletes both the spool file and the corresponding print job entry in the print spooler.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e56-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="69e56-128">Requirements</span></span>



| <span data-ttu-id="69e56-129">需求</span><span class="sxs-lookup"><span data-stu-id="69e56-129">Requirement</span></span> | <span data-ttu-id="69e56-130">值</span><span class="sxs-lookup"><span data-stu-id="69e56-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e56-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69e56-131">Minimum supported client</span></span><br/> | <span data-ttu-id="69e56-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69e56-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="69e56-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69e56-133">Minimum supported server</span></span><br/> | <span data-ttu-id="69e56-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69e56-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="69e56-135">標頭</span><span class="sxs-lookup"><span data-stu-id="69e56-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="69e56-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="69e56-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="69e56-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="69e56-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="69e56-138"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="69e56-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="69e56-139">DLL</span><span class="sxs-lookup"><span data-stu-id="69e56-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69e56-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69e56-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="69e56-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69e56-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e56-142">列印</span><span class="sxs-lookup"><span data-stu-id="69e56-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="69e56-143">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="69e56-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="69e56-144">**System.printing.printqueue.addjob**</span><span class="sxs-lookup"><span data-stu-id="69e56-144">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="69e56-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="69e56-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




