---
description: EnumJobs 函式會抓取指定印表機的一組指定列印工作的相關資訊。
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: 'EnumJobs 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193763"
---
# <a name="enumjobs-function"></a><span data-ttu-id="403a1-103">EnumJobs 函式</span><span class="sxs-lookup"><span data-stu-id="403a1-103">EnumJobs function</span></span>

<span data-ttu-id="403a1-104">**EnumJobs** 函式會抓取指定印表機的一組指定列印工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="403a1-104">The **EnumJobs** function retrieves information about a specified set of print jobs for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="403a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="403a1-105">Syntax</span></span>


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="403a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="403a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403a1-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403a1-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403a1-108">此函式會列舉其列印工作的印表機物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="403a1-108">A handle to the printer object whose print jobs the function enumerates.</span></span> <span data-ttu-id="403a1-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="403a1-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="403a1-110">*FirstJob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403a1-110">*FirstJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403a1-111">第一個要列舉之列印工作的列印佇列中，以零為基底的位置。</span><span class="sxs-lookup"><span data-stu-id="403a1-111">The zero-based position within the print queue of the first print job to enumerate.</span></span> <span data-ttu-id="403a1-112">例如，值為0會指定列舉應該從列印佇列中的第一個列印工作開始;值為9時，會指定在列印佇列中的第十個列印工作開始列舉。</span><span class="sxs-lookup"><span data-stu-id="403a1-112">For example, a value of 0 specifies that enumeration should begin at the first print job in the print queue; a value of 9 specifies that enumeration should begin at the tenth print job in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="403a1-113">*NoJobs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403a1-113">*NoJobs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403a1-114">要列舉的列印工作總數。</span><span class="sxs-lookup"><span data-stu-id="403a1-114">The total number of print jobs to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="403a1-115">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403a1-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403a1-116">*PJob* 緩衝區中傳回的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="403a1-116">The type of information returned in the *pJob* buffer.</span></span>



| <span data-ttu-id="403a1-117">值</span><span class="sxs-lookup"><span data-stu-id="403a1-117">Value</span></span>                                                                                                | <span data-ttu-id="403a1-118">意義</span><span class="sxs-lookup"><span data-stu-id="403a1-118">Meaning</span></span>                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="403a1-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="403a1-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="403a1-120">*pJob* 接收 [**作業 \_ 資訊 \_ 1**](job-info-1.md) 結構的陣列</span><span class="sxs-lookup"><span data-stu-id="403a1-120">*pJob* receives an array of [**JOB\_INFO\_1**](job-info-1.md) structures</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="403a1-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="403a1-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="403a1-122">*pJob* 接收 [**作業 \_ 資訊 \_ 2**](job-info-2.md) 結構的陣列</span><span class="sxs-lookup"><span data-stu-id="403a1-122">*pJob* receives an array of [**JOB\_INFO\_2**](job-info-2.md) structures</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="403a1-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="403a1-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="403a1-124">*pJob* 接收 [**作業 \_ 資訊 \_ 3**](job-info-3.md) 結構的陣列</span><span class="sxs-lookup"><span data-stu-id="403a1-124">*pJob* receives an array of [**JOB\_INFO\_3**](job-info-3.md) structures</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="403a1-125">*pJob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="403a1-125">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="403a1-126">緩衝區的指標，此緩衝區會接收 [**作業 \_ 資訊 \_ 1**](job-info-1.md)、 [**作業 \_ 資訊 \_ 2**](job-info-2.md)或 [**作業 \_ 資訊 \_ 3**](job-info-3.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="403a1-126">A pointer to a buffer that receives an array of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures.</span></span> <span data-ttu-id="403a1-127">緩衝區必須夠大，才能接收結構的陣列，以及結構成員指向的任何字串或其他資料。</span><span class="sxs-lookup"><span data-stu-id="403a1-127">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="403a1-128">若要判斷所需的緩衝區大小，請呼叫 **EnumJobs** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="403a1-128">To determine the required buffer size, call **EnumJobs** with *cbBuf* set to zero.</span></span> <span data-ttu-id="403a1-129">**EnumJobs** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="403a1-129">**EnumJobs** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="403a1-130">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="403a1-130">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403a1-131">*PJob* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="403a1-131">The size, in bytes, of the *pJob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="403a1-132">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="403a1-132">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="403a1-133">變數的指標，此變數會接收函式成功時所複製的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="403a1-133">A pointer to a variable that receives the number of bytes copied if the function succeeds.</span></span> <span data-ttu-id="403a1-134">如果函式失敗，則變數會收到所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="403a1-134">If the function fails, the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="403a1-135">*pcReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="403a1-135">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="403a1-136">變數的指標，此變數會接收 *pJob* 緩衝區中傳回的 [**作業 \_ 資訊 \_ 1**](job-info-1.md)、[**作業 \_ 資訊 \_ 2**](job-info-2.md)或 [**作業 \_ 資訊 \_ 3**](job-info-3.md)結構的數目。</span><span class="sxs-lookup"><span data-stu-id="403a1-136">A pointer to a variable that receives the number of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures returned in the *pJob* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="403a1-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="403a1-137">Return value</span></span>

<span data-ttu-id="403a1-138">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="403a1-138">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="403a1-139">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="403a1-139">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="403a1-140">備註</span><span class="sxs-lookup"><span data-stu-id="403a1-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="403a1-141">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="403a1-141">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="403a1-142">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="403a1-142">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="403a1-143">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="403a1-143">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="403a1-144">[**作業 \_ 資訊 \_ 1**](job-info-1.md)結構包含一般列印工作資訊，[**作業 \_ 資訊 \_ 2**](job-info-2.md)結構有更詳細的資訊。</span><span class="sxs-lookup"><span data-stu-id="403a1-144">The [**JOB\_INFO\_1**](job-info-1.md) structure contains general print-job information; the [**JOB\_INFO\_2**](job-info-2.md) structure has much more detailed information.</span></span> <span data-ttu-id="403a1-145">[**作業 \_ 資訊 \_ 3**](job-info-3.md)結構包含如何連結作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="403a1-145">The [**JOB\_INFO\_3**](job-info-3.md) structure contains information about how jobs are linked.</span></span>

<span data-ttu-id="403a1-146">若要判斷印表機佇列中的列印工作數目，請呼叫 [**GetPrinter**](getprinter.md) 函數，並將 *Level* 參數設定為2。</span><span class="sxs-lookup"><span data-stu-id="403a1-146">To determine the number of print jobs in the printer queue, call the [**GetPrinter**](getprinter.md) function with the *Level* parameter set to 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="403a1-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="403a1-147">Requirements</span></span>



| <span data-ttu-id="403a1-148">需求</span><span class="sxs-lookup"><span data-stu-id="403a1-148">Requirement</span></span> | <span data-ttu-id="403a1-149">值</span><span class="sxs-lookup"><span data-stu-id="403a1-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="403a1-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="403a1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="403a1-151">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="403a1-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="403a1-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="403a1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="403a1-153">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="403a1-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="403a1-154">標頭</span><span class="sxs-lookup"><span data-stu-id="403a1-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="403a1-155"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="403a1-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="403a1-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="403a1-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="403a1-157"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="403a1-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="403a1-158">DLL</span><span class="sxs-lookup"><span data-stu-id="403a1-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="403a1-159"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="403a1-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="403a1-160">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="403a1-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="403a1-161">**EnumJobsW** (Unicode) 和 **EnumJobsA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="403a1-161">**EnumJobsW** (Unicode) and **EnumJobsA** (ANSI)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="403a1-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="403a1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403a1-163">列印</span><span class="sxs-lookup"><span data-stu-id="403a1-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="403a1-164">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="403a1-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="403a1-165">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="403a1-165">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="403a1-166">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="403a1-166">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="403a1-167">**作業 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="403a1-167">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="403a1-168">**作業 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="403a1-168">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="403a1-169">**作業 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="403a1-169">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="403a1-170">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="403a1-170">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="403a1-171">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="403a1-171">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

