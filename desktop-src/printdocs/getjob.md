---
description: GetJob 函式會抓取指定列印工作的相關資訊。
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: 'GetJob 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192717"
---
# <a name="getjob-function"></a><span data-ttu-id="dce7d-103">GetJob 函式</span><span class="sxs-lookup"><span data-stu-id="dce7d-103">GetJob function</span></span>

<span data-ttu-id="dce7d-104">**GetJob** 函式會抓取指定列印工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dce7d-104">The **GetJob** function retrieves information about a specified print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce7d-105">語法</span><span class="sxs-lookup"><span data-stu-id="dce7d-105">Syntax</span></span>


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="dce7d-106">參數</span><span class="sxs-lookup"><span data-stu-id="dce7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce7d-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dce7d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce7d-108">要抓取列印工作資料之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dce7d-108">A handle to the printer for which the print-job data is retrieved.</span></span> <span data-ttu-id="dce7d-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="dce7d-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="dce7d-110">*JobId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dce7d-110">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce7d-111">識別要取出資料的列印工作。</span><span class="sxs-lookup"><span data-stu-id="dce7d-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="dce7d-112">您可以使用 [**system.printing.printqueue.addjob**](addjob.md) 函數或 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 函數來取得列印工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="dce7d-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dce7d-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dce7d-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce7d-114">*PJob* 緩衝區中傳回的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="dce7d-114">The type of information returned in the *pJob* buffer.</span></span> <span data-ttu-id="dce7d-115">如果 *層級* 為1， *PJob* 會接收 [**作業 \_ 資訊 \_ 1**](job-info-1.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="dce7d-115">If *Level* is 1, *pJob* receives a [**JOB\_INFO\_1**](job-info-1.md) structure.</span></span> <span data-ttu-id="dce7d-116">如果 *層級* 為2， *PJob* 會收到 [**工作 \_ 資訊 \_ 2**](job-info-2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="dce7d-116">If *Level* is 2, *pJob* receives a [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dce7d-117">*pJob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dce7d-117">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dce7d-118">緩衝區的指標，此緩衝區會接收 [**作業 \_ 資訊 \_ 1**](job-info-1.md) 或 [**作業 \_ 資訊 \_ 2**](job-info-2.md) 結構，其中包含作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dce7d-118">A pointer to a buffer that receives a [**JOB\_INFO\_1**](job-info-1.md) or a [**JOB\_INFO\_2**](job-info-2.md) structure containing information about the job.</span></span> <span data-ttu-id="dce7d-119">緩衝區必須夠大，才能儲存結構成員所指向的字串。</span><span class="sxs-lookup"><span data-stu-id="dce7d-119">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="dce7d-120">若要判斷所需的緩衝區大小，請呼叫 **GetJob** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="dce7d-120">To determine the required buffer size, call **GetJob** with *cbBuf* set to zero.</span></span> <span data-ttu-id="dce7d-121">**GetJob** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dce7d-121">**GetJob** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="dce7d-122">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dce7d-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce7d-123">陣列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dce7d-123">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="dce7d-124">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dce7d-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dce7d-125">值的指標，指定函式成功時所複製的位元組數目，或如果 *cbBuf* 太小，則為所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="dce7d-125">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce7d-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="dce7d-126">Return value</span></span>

<span data-ttu-id="dce7d-127">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="dce7d-127">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="dce7d-128">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="dce7d-128">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dce7d-129">備註</span><span class="sxs-lookup"><span data-stu-id="dce7d-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dce7d-130">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="dce7d-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="dce7d-131">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="dce7d-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="dce7d-132">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="dce7d-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dce7d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="dce7d-133">Requirements</span></span>



| <span data-ttu-id="dce7d-134">需求</span><span class="sxs-lookup"><span data-stu-id="dce7d-134">Requirement</span></span> | <span data-ttu-id="dce7d-135">值</span><span class="sxs-lookup"><span data-stu-id="dce7d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce7d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dce7d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dce7d-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dce7d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dce7d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dce7d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dce7d-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dce7d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dce7d-140">標頭</span><span class="sxs-lookup"><span data-stu-id="dce7d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce7d-141"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="dce7d-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dce7d-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="dce7d-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="dce7d-143"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dce7d-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="dce7d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dce7d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dce7d-145"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="dce7d-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="dce7d-146">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="dce7d-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dce7d-147">**GetJobW** (Unicode) 和 **GetJobA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="dce7d-147">**GetJobW** (Unicode) and **GetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="dce7d-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dce7d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce7d-149">列印</span><span class="sxs-lookup"><span data-stu-id="dce7d-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dce7d-150">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="dce7d-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="dce7d-151">**System.printing.printqueue.addjob**</span><span class="sxs-lookup"><span data-stu-id="dce7d-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="dce7d-152">**作業 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="dce7d-152">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="dce7d-153">**作業 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="dce7d-153">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="dce7d-154">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="dce7d-154">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="dce7d-155">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="dce7d-155">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

