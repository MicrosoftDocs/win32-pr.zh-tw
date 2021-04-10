---
description: System.printing.printqueue.addjob 函式會將列印工作加入至可由列印多工緩衝處理器排程的列印工作清單。 函數會抓取您可用來儲存作業的檔案名。
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: 'System.printing.printqueue.addjob 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692915"
---
# <a name="addjob-function"></a><span data-ttu-id="e84c0-104">System.printing.printqueue.addjob 函式</span><span class="sxs-lookup"><span data-stu-id="e84c0-104">AddJob function</span></span>

<span data-ttu-id="e84c0-105">**System.printing.printqueue.addjob** 函式會將列印工作加入至可由列印多工緩衝處理器排程的列印工作清單。</span><span class="sxs-lookup"><span data-stu-id="e84c0-105">The **AddJob** function adds a print job to the list of print jobs that can be scheduled by the print spooler.</span></span> <span data-ttu-id="e84c0-106">函數會抓取您可用來儲存作業的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e84c0-106">The function retrieves the name of the file you can use to store the job.</span></span>

> [!NOTE]
> <span data-ttu-id="e84c0-107">在 Windows 8 和更新版本的作業系統中，我們不建議您直接使用 **system.printing.printqueue.addjob** ，因為在某些情況下 (，例如使用 File：或 PORTPROMPT： ) 列印到佇列， **system.printing.printqueue.addjob** 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e84c0-107">In Windows 8 and later operating systems, we do not recommended using **AddJob** directly because there are cases (such as printing to a queue using File: or PORTPROMPT:) where **AddJob** will fail.</span></span> <span data-ttu-id="e84c0-108">相反地，根據列印案例，建議您從 [**Windows. 列印**](/uwp/api/Windows.Graphics.Printing)命名空間使用 [GDI 列印 Api](gdi-printing.md)、 [XPS 列印 api](xps-printing.md)、 [**StartDocPrinter**](startdocprinter.md)或適當的方法。</span><span class="sxs-lookup"><span data-stu-id="e84c0-108">Instead, you are advised to use [GDI Print API](gdi-printing.md), [XPS Print API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md), or the appropriate method from the [**Windows.Graphics.Printing**](/uwp/api/Windows.Graphics.Printing) namespace, depending on the print scenario.</span></span>
>
> <span data-ttu-id="e84c0-109">如果您嘗試使用 **File：** 或 **PORTPROMPT：** 來列印至佇列， **System.printing.printqueue.addjob** 將會傳回不 \_ 支援的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e84c0-109">If you try to print to a queue using **File:** or **PORTPROMPT:**, **AddJob** will Return the NOT\_SUPPORTED error.</span></span>

## <a name="syntax"></a><span data-ttu-id="e84c0-110">語法</span><span class="sxs-lookup"><span data-stu-id="e84c0-110">Syntax</span></span>

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a><span data-ttu-id="e84c0-111">參數</span><span class="sxs-lookup"><span data-stu-id="e84c0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e84c0-112">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e84c0-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c0-113">指定列印工作之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e84c0-113">A handle that specifies the printer for the print job.</span></span> <span data-ttu-id="e84c0-114">這必須是設定為多工緩衝處理印表機的本機印表機。</span><span class="sxs-lookup"><span data-stu-id="e84c0-114">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="e84c0-115">如果 *hPrinter* 是遠端印表機連線的控制碼，或印表機設定為直接列印，則 **system.printing.printqueue.addjob** 函式會失敗。</span><span class="sxs-lookup"><span data-stu-id="e84c0-115">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **AddJob** function fails.</span></span> <span data-ttu-id="e84c0-116">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="e84c0-116">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e84c0-117">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e84c0-117">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c0-118">函數儲存在 *.pdata* 所指向之緩衝區中的列印工作資訊資料結構版本。</span><span class="sxs-lookup"><span data-stu-id="e84c0-118">The version of the print job information data structure that the function stores into the buffer pointed to by *pData*.</span></span> <span data-ttu-id="e84c0-119">將此參數設定為一個。</span><span class="sxs-lookup"><span data-stu-id="e84c0-119">Set this parameter to one.</span></span>

</dd> <dt>

<span data-ttu-id="e84c0-120">*.pdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e84c0-120">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c0-121">接收 [**System.printing.printqueue.addjob \_ INFO \_ 1**](addjob-info-1.md) 資料結構和路徑字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="e84c0-121">A pointer to a buffer that receives an [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="e84c0-122">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e84c0-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c0-123">*.Pdata* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e84c0-123">The size, in bytes, of the buffer pointed to by *pData*.</span></span> <span data-ttu-id="e84c0-124">緩衝區必須夠大，才能包含 [**System.printing.printqueue.addjob \_ INFO \_ 1**](addjob-info-1.md) 結構和路徑字串。</span><span class="sxs-lookup"><span data-stu-id="e84c0-124">The buffer needs to be large enough to contain an [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="e84c0-125">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e84c0-125">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c0-126">變數的指標，此變數會接收 [**System.printing.printqueue.addjob \_ INFO \_ 1**](addjob-info-1.md) 資料結構和路徑字串的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e84c0-126">A pointer to a variable that receives the total size, in bytes, of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure plus the path string.</span></span> <span data-ttu-id="e84c0-127">如果這個值小於或等於 *cbBuf* ，且函式成功，則這是寫入 *.pdata* 所指向之緩衝區的實際位元組數。</span><span class="sxs-lookup"><span data-stu-id="e84c0-127">If this value is less than or equal to *cbBuf* and the function succeeds, this is the actual number of bytes written to the buffer pointed to by *pData*.</span></span> <span data-ttu-id="e84c0-128">如果這個數位大於 *cbBuf*，緩衝區太小，而且您必須使用至少與 pcbNeeded 一樣的緩衝區大小來呼叫函式 \* \*\*。</span><span class="sxs-lookup"><span data-stu-id="e84c0-128">If this number is greater than *cbBuf*, the buffer is too small, and you must call the function again with a buffer size at least as large as \**pcbNeeded*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e84c0-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="e84c0-129">Return value</span></span>

<span data-ttu-id="e84c0-130">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="e84c0-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e84c0-131">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e84c0-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e84c0-132">備註</span><span class="sxs-lookup"><span data-stu-id="e84c0-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e84c0-133">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e84c0-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e84c0-134">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="e84c0-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e84c0-135">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="e84c0-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e84c0-136">您可以呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式來開啟 [**system.printing.printqueue.addjob \_ INFO \_ 1**](addjob-info-1.md)結構的 **Path** 成員所指定的多工緩衝處理檔案，然後呼叫 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)函數將列印工作資料寫入其中。</span><span class="sxs-lookup"><span data-stu-id="e84c0-136">You can call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the spool file specified by the **Path** member of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure, and then call the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to write print job data to it.</span></span> <span data-ttu-id="e84c0-137">完成之後，請呼叫 [**ScheduleJob**](schedulejob.md) 函式來通知列印多工緩衝處理器，列印工作現在可以由多工緩衝處理器排程來進行列印。</span><span class="sxs-lookup"><span data-stu-id="e84c0-137">After that is done, call the [**ScheduleJob**](schedulejob.md) function to notify the print spooler that the print job can now be scheduled by the spooler for printing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84c0-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="e84c0-138">Requirements</span></span>



| <span data-ttu-id="e84c0-139">需求</span><span class="sxs-lookup"><span data-stu-id="e84c0-139">Requirement</span></span> | <span data-ttu-id="e84c0-140">值</span><span class="sxs-lookup"><span data-stu-id="e84c0-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e84c0-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e84c0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e84c0-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e84c0-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e84c0-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e84c0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e84c0-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e84c0-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e84c0-145">標頭</span><span class="sxs-lookup"><span data-stu-id="e84c0-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e84c0-146"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e84c0-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e84c0-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="e84c0-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="e84c0-148"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e84c0-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e84c0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e84c0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e84c0-150"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="e84c0-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e84c0-151">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e84c0-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e84c0-152">**AddJobW** (Unicode) 和 **AddJobA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e84c0-152">**AddJobW** (Unicode) and **AddJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="e84c0-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e84c0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84c0-154">**SYSTEM.PRINTING.PRINTQUEUE.ADDJOB \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e84c0-154">**ADDJOB\_INFO\_1**</span></span>](addjob-info-1.md)
</dt> <dt>

[<span data-ttu-id="e84c0-155">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="e84c0-155">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="e84c0-156">GDI 列印 API</span><span class="sxs-lookup"><span data-stu-id="e84c0-156">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="e84c0-157">列印</span><span class="sxs-lookup"><span data-stu-id="e84c0-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e84c0-158">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="e84c0-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e84c0-159">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e84c0-159">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e84c0-160">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="e84c0-160">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="e84c0-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="e84c0-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="e84c0-162">**Windows. 列印**</span><span class="sxs-lookup"><span data-stu-id="e84c0-162">**Windows.Graphics.Printing**</span></span>](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[<span data-ttu-id="e84c0-163">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="e84c0-163">**WriteFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="e84c0-164">XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="e84c0-164">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

