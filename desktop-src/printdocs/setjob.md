---
description: SetJob 函式會在指定的印表機上暫停、繼續、取消或重新開機列印工作。 您也可以使用 SetJob 函數來設定列印工作參數，例如列印工作優先順序和檔案名稱。
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: 'SetJob 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975185"
---
# <a name="setjob-function"></a><span data-ttu-id="1f13e-104">SetJob 函式</span><span class="sxs-lookup"><span data-stu-id="1f13e-104">SetJob function</span></span>

<span data-ttu-id="1f13e-105">**SetJob** 函式會在指定的印表機上暫停、繼續、取消或重新開機列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-105">The **SetJob** function pauses, resumes, cancels, or restarts a print job on a specified printer.</span></span> <span data-ttu-id="1f13e-106">您也可以使用 **SetJob** 函數來設定列印工作參數，例如列印工作優先順序和檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="1f13e-106">You can also use the **SetJob** function to set print job parameters, such as the print job priority and the document name.</span></span>

<span data-ttu-id="1f13e-107">您可以使用 **SetJob** 函式，將命令提供給列印工作，或設定列印工作參數，或在相同的呼叫中執行這兩個動作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-107">You can use the **SetJob** function to give a command to a print job, or to set print job parameters, or to do both in the same call.</span></span> <span data-ttu-id="1f13e-108">*Command* 參數的值不會影響函式使用 *Level* 和 *pJob* 參數的方式。</span><span class="sxs-lookup"><span data-stu-id="1f13e-108">The value of the *Command* parameter does not affect how the function uses the *Level* and *pJob* parameters.</span></span> <span data-ttu-id="1f13e-109">此外，您也可以搭配使用 **SetJob** 與 [**工作 \_ 資訊 \_ 3**](job-info-3.md) ，將一組列印工作連結在一起。</span><span class="sxs-lookup"><span data-stu-id="1f13e-109">Also, you can use **SetJob** with [**JOB\_INFO\_3**](job-info-3.md) to link together a set of print jobs.</span></span> <span data-ttu-id="1f13e-110">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="1f13e-110">See Remarks for more information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f13e-111">語法</span><span class="sxs-lookup"><span data-stu-id="1f13e-111">Syntax</span></span>


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="1f13e-112">參數</span><span class="sxs-lookup"><span data-stu-id="1f13e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f13e-113">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f13e-113">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f13e-114">感興趣的印表機物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="1f13e-114">A handle to the printer object of interest.</span></span> <span data-ttu-id="1f13e-115">使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="1f13e-115">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="1f13e-116">*JobId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f13e-116">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f13e-117">指定列印工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f13e-117">Identifier that specifies the print job.</span></span> <span data-ttu-id="1f13e-118">您可以藉由呼叫 [**system.printing.printqueue.addjob**](addjob.md) 函式或 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 函數來取得列印工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f13e-118">You obtain a print job identifier by calling the [**AddJob**](addjob.md) function or the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function.</span></span>

<span data-ttu-id="1f13e-119">如果 *Level* 參數設定為3，則 *JobId* 參數必須符合 *pJob* 所指向之 [**作業 \_ 資訊 \_ 3**](job-info-3.md)結構的 **jobid** 成員</span><span class="sxs-lookup"><span data-stu-id="1f13e-119">If the *Level* parameter is set to 3, the *JobId* parameter must match the **JobId** member of the [**JOB\_INFO\_3**](job-info-3.md) structure pointed to by *pJob*</span></span>

</dd> <dt>

<span data-ttu-id="1f13e-120">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f13e-120">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f13e-121">*PJob* 參數所指向的作業資訊結構類型。</span><span class="sxs-lookup"><span data-stu-id="1f13e-121">The type of job information structure pointed to by the *pJob* parameter.</span></span>

<span data-ttu-id="1f13e-122">**所有版本的 Windows**：您可以將 *Level* 參數設定為0、1或2。</span><span class="sxs-lookup"><span data-stu-id="1f13e-122">**All versions of Windows**: You can set the *Level* parameter to 0, 1, or 2.</span></span> <span data-ttu-id="1f13e-123">當您將 *層級* 設定為0時， *PJob* 應該是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1f13e-123">When you set *Level* to 0, *pJob* should be **NULL**.</span></span> <span data-ttu-id="1f13e-124">當您未設定任何列印工作參數時，請使用這些值。</span><span class="sxs-lookup"><span data-stu-id="1f13e-124">Use these values when you are not setting any print job parameters.</span></span>

<span data-ttu-id="1f13e-125">您也可以將 *Level* 參數設為3。</span><span class="sxs-lookup"><span data-stu-id="1f13e-125">You can also set the *Level* parameter to 3.</span></span>

<span data-ttu-id="1f13e-126">從 **Windows Vista** 開始：您也可以將 *Level* 參數設定為4。</span><span class="sxs-lookup"><span data-stu-id="1f13e-126">Starting with **Windows Vista**: You can also set the *Level* parameter to 4.</span></span>

</dd> <dt>

<span data-ttu-id="1f13e-127">*pJob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f13e-127">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f13e-128">設定列印工作參數之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1f13e-128">A pointer to a structure that sets the print job parameters.</span></span>

<span data-ttu-id="1f13e-129">**所有版本的 Windows**： *PJob* 可指向 [**作業 \_ 資訊 \_ 1**](job-info-1.md) 或 [**作業 \_ 資訊 \_ 2**](job-info-2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="1f13e-129">**All versions of Windows**: *pJob* can point to a [**JOB\_INFO\_1**](job-info-1.md) or [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

<span data-ttu-id="1f13e-130">*pJob* 也可以指向 [**作業 \_ 資訊 \_ 3**](job-info-3.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="1f13e-130">*pJob* can also point to a [**JOB\_INFO\_3**](job-info-3.md) structure.</span></span> <span data-ttu-id="1f13e-131">您必須擁有作業 **\_ 資訊 \_ 3** 結構的 **JobId** 和 **NextJobId** 成員所指定之作業的 **作業存取權 \_ \_ 管理** 存取權限。</span><span class="sxs-lookup"><span data-stu-id="1f13e-131">You must have **JOB\_ACCESS\_ADMINISTER** access permission for the jobs specified by the **JobId** and **NextJobId** members of the **JOB\_INFO\_3** structure.</span></span>

<span data-ttu-id="1f13e-132">從 **Windows Vista** 開始： *pJob* 也可以指向 [**工作 \_ 資訊 \_ 4**](job-info-4.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="1f13e-132">Starting with **Windows Vista**: *pJob* can also point to a [**JOB\_INFO\_4**](job-info-4.md) structure.</span></span>

<span data-ttu-id="1f13e-133">如果 *Level* 參數為0，則 *PJob* 應該是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1f13e-133">If the *Level* parameter is 0, *pJob* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1f13e-134">*命令* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f13e-134">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f13e-135">要執行的列印工作作業。</span><span class="sxs-lookup"><span data-stu-id="1f13e-135">The print job operation to perform.</span></span> <span data-ttu-id="1f13e-136">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1f13e-136">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1f13e-137">值</span><span class="sxs-lookup"><span data-stu-id="1f13e-137">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="1f13e-138">意義</span><span class="sxs-lookup"><span data-stu-id="1f13e-138">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <span data-ttu-id="1f13e-139"><dt>**作業 \_ 控制 \_ 取消**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-139"><dt>**JOB\_CONTROL\_CANCEL**</dt></span></span> </dl>                                    | <span data-ttu-id="1f13e-140">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="1f13e-140">Do not use.</span></span> <span data-ttu-id="1f13e-141">若要刪除列印工作，請使用 **工作 \_ 控制 \_ 刪除**。</span><span class="sxs-lookup"><span data-stu-id="1f13e-141">To delete a print job, use **JOB\_CONTROL\_DELETE**.</span></span><br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <span data-ttu-id="1f13e-142"><dt>**作業 \_ 控制 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-142"><dt>**JOB\_CONTROL\_PAUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="1f13e-143">暫停列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-143">Pause the print job.</span></span><br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <span data-ttu-id="1f13e-144"><dt>**作業 \_ 控制項 \_ 重新開機**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-144"><dt>**JOB\_CONTROL\_RESTART**</dt></span></span> </dl>                                 | <span data-ttu-id="1f13e-145">重新開機列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-145">Restart the print job.</span></span> <span data-ttu-id="1f13e-146">只有在列印時才能重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="1f13e-146">A job can only be restarted if it was printing.</span></span><br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <span data-ttu-id="1f13e-147"><dt>**作業 \_ 控制 \_ 繼續**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-147"><dt>**JOB\_CONTROL\_RESUME**</dt></span></span> </dl>                                    | <span data-ttu-id="1f13e-148">繼續暫停的列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-148">Resume a paused print job.</span></span><br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <span data-ttu-id="1f13e-149"><dt>**作業 \_ 控制 \_ 刪除**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-149"><dt>**JOB\_CONTROL\_DELETE**</dt></span></span> </dl>                                    | <span data-ttu-id="1f13e-150">刪除列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-150">Delete the print job.</span></span><br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <span data-ttu-id="1f13e-151"><dt>**\_ \_ 傳送 \_ 至印表機的作業控制 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-151"><dt>**JOB\_CONTROL\_SENT\_TO\_PRINTER**</dt></span></span> </dl>       | <span data-ttu-id="1f13e-152">由埠監視器用來結束列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-152">Used by port monitors to end the print job.</span></span><br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <span data-ttu-id="1f13e-153"><dt>**工作 \_ 控制 \_ 最後一 \_ 頁已 \_ 退出**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-153"><dt>**JOB\_CONTROL\_LAST\_PAGE\_EJECTED**</dt></span></span> </dl> | <span data-ttu-id="1f13e-154">供語言監視器用來結束列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-154">Used by language monitors to end the print job.</span></span><br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <span data-ttu-id="1f13e-155"><dt>**工作 \_ 控制 \_ 保留**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-155"><dt>**JOB\_CONTROL\_RETAIN**</dt></span></span> </dl>                                    | <span data-ttu-id="1f13e-156">**Windows Vista 和更新版本**：在列印後將工作保留在佇列中。</span><span class="sxs-lookup"><span data-stu-id="1f13e-156">**Windows Vista and later**: Keep the job in the queue after it prints.</span></span><br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <span data-ttu-id="1f13e-157"><dt>**作業 \_ 控制 \_ 發行**</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-157"><dt>**JOB\_CONTROL\_RELEASE**</dt></span></span> </dl>                                 | <span data-ttu-id="1f13e-158">**Windows Vista 和更新版本**：發行列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-158">**Windows Vista and later**: Release the print job.</span></span><br/>                     |



 

<span data-ttu-id="1f13e-159">您可以使用 **SetJob** 函數的相同呼叫來設定列印工作參數，以及提供命令給列印工作。</span><span class="sxs-lookup"><span data-stu-id="1f13e-159">You can use the same call to the **SetJob** function to set print job parameters and to give a command to a print job.</span></span> <span data-ttu-id="1f13e-160">因此，如果您要設定列印工作參數， *命令* 就不需要是0，雖然它可以是。</span><span class="sxs-lookup"><span data-stu-id="1f13e-160">Thus, *Command* does not need to be 0 if you are setting print job parameters, although it can be.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f13e-161">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f13e-161">Return value</span></span>

<span data-ttu-id="1f13e-162">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="1f13e-162">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1f13e-163">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="1f13e-163">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f13e-164">備註</span><span class="sxs-lookup"><span data-stu-id="1f13e-164">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1f13e-165">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="1f13e-165">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1f13e-166">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="1f13e-166">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1f13e-167">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="1f13e-167">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="1f13e-168">您可以使用 **SetJob** 函式來設定各種列印工作參數，方法是提供 [**工作 \_ 資訊 \_ 1**](job-info-1.md)、 [**作業 \_ 資訊 \_ 2**](job-info-2.md)、 [**作業 \_ 資訊 \_ 3**](job-info-3.md)的指標，或包含所需資料的 [**工作 \_ 資訊 \_ 4**](job-info-4.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="1f13e-168">You can use the **SetJob** function to set various print job parameters by supplying a pointer to a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), [**JOB\_INFO\_3**](job-info-3.md), or [**JOB\_INFO\_4**](job-info-4.md) structure that contains the necessary data.</span></span>

<span data-ttu-id="1f13e-169">若要移除或刪除特定印表機的所有列印工作，請呼叫 [**SetPrinter**](setprinter.md) 函式，並將其 *命令* 參數設定為 **印表機 \_ 控制項 \_ 清除**。</span><span class="sxs-lookup"><span data-stu-id="1f13e-169">To remove or delete all of the print jobs for a particular printer, call the [**SetPrinter**](setprinter.md) function with its *Command* parameter set to **PRINTER\_CONTROL\_PURGE**.</span></span>

<span data-ttu-id="1f13e-170">呼叫 **SetJob**： **JobId**、 **pPrinterName**、 **pMachineName**、 **pUserName**、 **pDrivername**、 **Size**、已 **提交**、 **Time** 和 **TotalPages** 時，會忽略 [**作業 \_ 資訊 \_ 1**](job-info-1.md)、[**作業 \_ 資訊 \_ 2**](job-info-2.md)或 [**作業 \_ 資訊 \_ 4**](job-info-4.md)結構的下列成員。</span><span class="sxs-lookup"><span data-stu-id="1f13e-170">The following members of a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure are ignored on a call to **SetJob**: **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time**, and **TotalPages**.</span></span>

<span data-ttu-id="1f13e-171">您必須擁有印表機的 **印表機 \_ 存取權 \_ 管理** 存取權限，才能在列印佇列中變更列印工作的位置。</span><span class="sxs-lookup"><span data-stu-id="1f13e-171">You must have **PRINTER\_ACCESS\_ADMINISTER** access permission for a printer in order to change a print job's position in the print queue.</span></span>

<span data-ttu-id="1f13e-172">如果您不想要在列印佇列中設定列印工作的位置，則應該將 [**作業 \_ 資訊 \_ 1**](job-info-1.md)、[**作業 \_ 資訊 \_ 2**](job-info-2.md)或 [**工作 \_ 資訊 \_ 4**](job-info-4.md)結構的 **位置** 成員設定為 **\_ \_ 未指定的工作位置**。</span><span class="sxs-lookup"><span data-stu-id="1f13e-172">If you do not want to set a print job's position in the print queue, you should set the **Position** member of the [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure to **JOB\_POSITION\_UNSPECIFIED**.</span></span>

<span data-ttu-id="1f13e-173">使用 **SetJob** 函式搭配 [**作業 \_ 資訊 \_ 3**](job-info-3.md) 結構，將一組列印工作連結 (也稱為鏈) 。</span><span class="sxs-lookup"><span data-stu-id="1f13e-173">Use the **SetJob** function with the [**JOB\_INFO\_3**](job-info-3.md) structure to link together a set of print jobs (also known as a chain).</span></span> <span data-ttu-id="1f13e-174">當單一檔是由數個您想要個別轉譯的部分所組成時，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="1f13e-174">This is useful in situations where a single document consists of several parts that you want to render separately.</span></span> <span data-ttu-id="1f13e-175">若要依序列印 A、B、C 和 D 等作業，請使用 [**工作 \_ 資訊 \_ 4**](job-info-4.md)呼叫 **SetJob** ，將 A 連結至 b、b 至 C 和 c 到 D。</span><span class="sxs-lookup"><span data-stu-id="1f13e-175">To print jobs A, B, C, and D in order, call **SetJob** with [**JOB\_INFO\_4**](job-info-4.md) to link A to B, B to C, and C to D.</span></span>

<span data-ttu-id="1f13e-176">如果您連結列印工作，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="1f13e-176">If you link print jobs, note the following:</span></span>

-   <span data-ttu-id="1f13e-177">作業可以新增至鏈的開頭或結尾。</span><span class="sxs-lookup"><span data-stu-id="1f13e-177">Jobs can be added to the beginning or end of a chain.</span></span>
-   <span data-ttu-id="1f13e-178">鏈中的所有工作都必須具有相同的資料類型。</span><span class="sxs-lookup"><span data-stu-id="1f13e-178">All jobs in the chain must have the same data type.</span></span>
-   <span data-ttu-id="1f13e-179">在幕後處理開始之前，必須完整連結鏈，否則，多工緩衝處理器可能會列印和刪除多工緩衝處理作業，然後才能將它們全部連結。</span><span class="sxs-lookup"><span data-stu-id="1f13e-179">The chain must be completely linked before spooling begins, otherwise the spooler may print and delete spooled jobs before you link them all.</span></span> <span data-ttu-id="1f13e-180">有兩種方式可以讓鏈保持不上列印：</span><span class="sxs-lookup"><span data-stu-id="1f13e-180">There are two ways to keep the chain from printing prematurely:</span></span>

    -   <span data-ttu-id="1f13e-181">暫停鏈中的第一個工作，直到鏈完全連結為止。</span><span class="sxs-lookup"><span data-stu-id="1f13e-181">Pause the first job in the chain until the chain is completely linked.</span></span> <span data-ttu-id="1f13e-182">第一個工作的暫停狀態會控制鏈中所有工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="1f13e-182">The paused state of the first job governs the state of all jobs in the chain.</span></span>
    -   <span data-ttu-id="1f13e-183">讓第一個工作不完整，也就是不針對第一個作業呼叫 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) 或 [**ScheduleJob**](schedulejob.md) 。</span><span class="sxs-lookup"><span data-stu-id="1f13e-183">Keep the first job incomplete, that is, do not call [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) or [**ScheduleJob**](schedulejob.md) for the first job.</span></span> <span data-ttu-id="1f13e-184">但是，如果已啟用 (預設) 的「在幕後列印時列印」，這個方法會在建立鏈時封鎖埠，這也會防止列印非相關的作業。</span><span class="sxs-lookup"><span data-stu-id="1f13e-184">However, if 'print while spooling' is enabled (the default), this method blocks the port while the chain is built, which also prevents the printing of non-related jobs.</span></span>

-   <span data-ttu-id="1f13e-185">應用程式必須處理在鏈完成列印之前，使用者在鏈中刪除工作的情況。</span><span class="sxs-lookup"><span data-stu-id="1f13e-185">The application must handle the case where the user deletes a job in the chain before the chain finishes printing.</span></span> <span data-ttu-id="1f13e-186">當 JobID 不存在時， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)會傳回 **不正確 \_ 參數**。</span><span class="sxs-lookup"><span data-stu-id="1f13e-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **INVALID\_PARAMETER** when a JobID does not exist.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f13e-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f13e-187">Requirements</span></span>



| <span data-ttu-id="1f13e-188">需求</span><span class="sxs-lookup"><span data-stu-id="1f13e-188">Requirement</span></span> | <span data-ttu-id="1f13e-189">值</span><span class="sxs-lookup"><span data-stu-id="1f13e-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f13e-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f13e-190">Minimum supported client</span></span><br/> | <span data-ttu-id="1f13e-191">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f13e-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1f13e-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f13e-192">Minimum supported server</span></span><br/> | <span data-ttu-id="1f13e-193">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f13e-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1f13e-194">標頭</span><span class="sxs-lookup"><span data-stu-id="1f13e-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f13e-195"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-195"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1f13e-196">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f13e-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f13e-197"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-197"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1f13e-198">DLL</span><span class="sxs-lookup"><span data-stu-id="1f13e-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f13e-199"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="1f13e-199"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1f13e-200">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1f13e-200">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1f13e-201">**SetJobW** (Unicode) 和 **SetJobA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1f13e-201">**SetJobW** (Unicode) and **SetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="1f13e-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f13e-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f13e-203">列印</span><span class="sxs-lookup"><span data-stu-id="1f13e-203">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1f13e-204">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="1f13e-204">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1f13e-205">**System.printing.printqueue.addjob**</span><span class="sxs-lookup"><span data-stu-id="1f13e-205">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="1f13e-206">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="1f13e-206">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="1f13e-207">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="1f13e-207">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="1f13e-208">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="1f13e-208">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="1f13e-209">**作業 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="1f13e-209">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="1f13e-210">**作業 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1f13e-210">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="1f13e-211">**作業 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="1f13e-211">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="1f13e-212">**作業 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1f13e-212">**JOB\_INFO\_4**</span></span>](job-info-4.md)
</dt> </dl>

 

