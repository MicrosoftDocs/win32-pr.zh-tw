---
description: 作業 \_ 資訊 \_ 1 結構會指定列印工作資訊，例如工作識別碼值、工作要進行多工緩衝處理的印表機名稱、建立列印工作的電腦名稱稱、擁有列印工作的使用者名稱等，依此類推。
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: 'JOB_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320608"
---
# <a name="job_info_1-structure"></a><span data-ttu-id="7e6cf-103">作業 \_ 資訊 \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="7e6cf-103">JOB\_INFO\_1 structure</span></span>

<span data-ttu-id="7e6cf-104">**作業 \_ 資訊 \_ 1** 結構會指定列印工作資訊，例如工作識別碼值、工作要進行多工緩衝處理的印表機名稱、建立列印工作的電腦名稱稱、擁有列印工作的使用者名稱等，依此類推。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-104">The **JOB\_INFO\_1** structure specifies print-job information such as the job-identifier value, the name of the printer for which the job is spooled, the name of the machine that created the print job, the name of the user that owns the print job, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e6cf-105">語法</span><span class="sxs-lookup"><span data-stu-id="7e6cf-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="7e6cf-106">成員</span><span class="sxs-lookup"><span data-stu-id="7e6cf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e6cf-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-108">作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-108">A job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-110">以 null 結束的字串指標，指定工作要進行多工緩衝處理的印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-112">以 null 結束的字串指標，指定建立列印工作的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-114">以 null 結束的字串指標，指定擁有列印工作之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-114">A pointer to a null-terminated string that specifies the name of the user that owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-116">以 null 結束的字串指標，指定列印工作的名稱 (例如 "MS-WORD： Review.doc" ) 。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-117">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-117">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-118">以 null 結束的字串指標，指定用來記錄列印工作的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-118">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-119">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-119">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-120">以 null 結束的字串指標，指定列印工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-120">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="7e6cf-121">此成員應在 *狀態* 之前檢查，而且如果 *pStatus* 為 **Null**，則狀態會由狀態成員的內容定義。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-121">This member should be checked prior to *Status* and, if *pStatus* is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-122">**狀態**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-122">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-123">作業狀態。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-123">The job status.</span></span> <span data-ttu-id="7e6cf-124">此成員的值可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-124">The value of this member can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="7e6cf-125">值為零表示列印佇列在檔完成幕後處理之後暫停。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-125">A value of zero indicates that the print queue was paused after the document finished spooling.</span></span>



| <span data-ttu-id="7e6cf-126">值</span><span class="sxs-lookup"><span data-stu-id="7e6cf-126">Value</span></span>                           | <span data-ttu-id="7e6cf-127">意義</span><span class="sxs-lookup"><span data-stu-id="7e6cf-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6cf-128">作業 \_ 狀態已 \_ 封鎖 \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="7e6cf-128">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="7e6cf-129">驅動程式無法列印工作。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-129">The driver cannot print the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7e6cf-130">作業 \_ 狀態 \_ 完成</span><span class="sxs-lookup"><span data-stu-id="7e6cf-130">JOB\_STATUS\_COMPLETE</span></span>           | <span data-ttu-id="7e6cf-131">**WINDOWS XP 和更新版本：** 作業會傳送至印表機，但作業可能尚未列印。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-131">**Windows XP and later:** Job is sent to the printer, but the job may not be printed yet.</span></span><br/> <span data-ttu-id="7e6cf-132">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-132">See Remarks for more information.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7e6cf-133">作業 \_ 狀態 \_ 已刪除</span><span class="sxs-lookup"><span data-stu-id="7e6cf-133">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="7e6cf-134">作業已刪除。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-134">Job has been deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7e6cf-135">作業 \_ 狀態 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="7e6cf-135">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="7e6cf-136">正在刪除工作。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-136">Job is being deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7e6cf-137">作業 \_ 狀態 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="7e6cf-137">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="7e6cf-138">與作業相關聯的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-138">An error is associated with the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7e6cf-139">\_離線作業狀態 \_</span><span class="sxs-lookup"><span data-stu-id="7e6cf-139">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="7e6cf-140">印表機已離線。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-140">Printer is offline.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7e6cf-141">作業 \_ 狀態 \_ PAPEROUT</span><span class="sxs-lookup"><span data-stu-id="7e6cf-141">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="7e6cf-142">印表機缺紙。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-142">Printer is out of paper.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="7e6cf-143">作業 \_ 狀態已 \_ 暫停</span><span class="sxs-lookup"><span data-stu-id="7e6cf-143">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="7e6cf-144">作業已暫停。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-144">Job is paused.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7e6cf-145">作業 \_ 狀態已 \_ 列印</span><span class="sxs-lookup"><span data-stu-id="7e6cf-145">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="7e6cf-146">作業已列印。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-146">Job has printed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7e6cf-147">作業 \_ 狀態 \_ 列印</span><span class="sxs-lookup"><span data-stu-id="7e6cf-147">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="7e6cf-148">作業正在列印。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-148">Job is printing.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7e6cf-149">作業 \_ 狀態 \_ 重新開機</span><span class="sxs-lookup"><span data-stu-id="7e6cf-149">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="7e6cf-150">作業已重新開機。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-150">Job has been restarted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="7e6cf-151">保留的作業 \_ 狀態 \_</span><span class="sxs-lookup"><span data-stu-id="7e6cf-151">JOB\_STATUS\_RETAINED</span></span>           | <span data-ttu-id="7e6cf-152">**Windows Vista 和更新版本：** 作業已保留在列印佇列中，無法刪除。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-152">**Windows Vista and later:** Job has been retained in the print queue and cannot be deleted.</span></span> <span data-ttu-id="7e6cf-153">這可能是由下列問題所造成：</span><span class="sxs-lookup"><span data-stu-id="7e6cf-153">This can be caused by the following:</span></span><br/> <span data-ttu-id="7e6cf-154">1) 作業是透過呼叫 SetJob 來手動保留，而多工緩衝處理器正在等候作業釋放。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-154">1) The job was manually retained by a call to SetJob and the spooler is waiting for the job to be released.</span></span><br/> <span data-ttu-id="7e6cf-155">2) 工作尚未完成列印，必須先完成列印，才能自動將其刪除。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-155">2) The job has not finished printing and must finish printing before it can be automatically deleted.</span></span><br/> <span data-ttu-id="7e6cf-156">如需列印工作命令的詳細資訊，請參閱 [**SetJob**](setjob.md) 。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-156">See [**SetJob**](setjob.md) for more information about print job commands.</span></span><br/> |
| <span data-ttu-id="7e6cf-157">作業 \_ 狀態 \_ 緩衝處理</span><span class="sxs-lookup"><span data-stu-id="7e6cf-157">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="7e6cf-158">作業已在幕後處理。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-158">Job is spooling.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7e6cf-159">作業 \_ 狀態 \_ 使用者 \_ 介入</span><span class="sxs-lookup"><span data-stu-id="7e6cf-159">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="7e6cf-160">印表機有錯誤，需要使用者進行一些動作。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-160">Printer has an error that requires the user to do something.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="7e6cf-161">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-161">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-162">作業優先權。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-162">The job priority.</span></span> <span data-ttu-id="7e6cf-163">這個成員可以是下列其中一個值，或介於1到99之間的範圍 (最低優先順序 \_ 到最高 \_ 優先順序) 。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-163">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="7e6cf-164">值</span><span class="sxs-lookup"><span data-stu-id="7e6cf-164">Value</span></span>         | <span data-ttu-id="7e6cf-165">意義</span><span class="sxs-lookup"><span data-stu-id="7e6cf-165">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="7e6cf-166">最小 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="7e6cf-166">MIN\_PRIORITY</span></span> | <span data-ttu-id="7e6cf-167">最小優先權。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-167">Minimum priority.</span></span> |
| <span data-ttu-id="7e6cf-168">最高 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="7e6cf-168">MAX\_PRIORITY</span></span> | <span data-ttu-id="7e6cf-169">最高優先順序。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-169">Maximum priority.</span></span> |
| <span data-ttu-id="7e6cf-170">DEF \_ 優先權</span><span class="sxs-lookup"><span data-stu-id="7e6cf-170">DEF\_PRIORITY</span></span> | <span data-ttu-id="7e6cf-171">預設優先順序。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-171">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7e6cf-172">**位置**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-172">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-173">工作在列印佇列中的位置。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-173">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-174">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-174">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-175">檔包含的總頁數。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-175">The total number of pages that the document contains.</span></span> <span data-ttu-id="7e6cf-176">如果列印工作未包含以頁面分隔的資訊，則此值可能為零。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-176">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-177">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-177">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-178">已列印的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-178">The number of pages that have printed.</span></span> <span data-ttu-id="7e6cf-179">如果列印工作未包含以頁面分隔的資訊，則此值可能為零。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-179">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="7e6cf-180">**已提交**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-180">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="7e6cf-181">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構，指定此檔在多工緩衝處理的時間。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-181">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time that this document was spooled.</span></span>

<span data-ttu-id="7e6cf-182">此時間值採用國際標準時間座標 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-182">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="7e6cf-183">您應該先將它轉換成當地時間值，再顯示它。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-183">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="7e6cf-184">您可以使用 [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) 函數來執行轉換。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-184">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e6cf-185">備註</span><span class="sxs-lookup"><span data-stu-id="7e6cf-185">Remarks</span></span>

<span data-ttu-id="7e6cf-186">不支援 TrueEndOfJob 的埠監視器，會將工作設定為在 \_ \_ 將作業提交至印表機之後列印的工作狀態。</span><span class="sxs-lookup"><span data-stu-id="7e6cf-186">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e6cf-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e6cf-187">Requirements</span></span>



| <span data-ttu-id="7e6cf-188">需求</span><span class="sxs-lookup"><span data-stu-id="7e6cf-188">Requirement</span></span> | <span data-ttu-id="7e6cf-189">值</span><span class="sxs-lookup"><span data-stu-id="7e6cf-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6cf-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e6cf-190">Minimum supported client</span></span><br/> | <span data-ttu-id="7e6cf-191">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e6cf-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7e6cf-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e6cf-192">Minimum supported server</span></span><br/> | <span data-ttu-id="7e6cf-193">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e6cf-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7e6cf-194">標頭</span><span class="sxs-lookup"><span data-stu-id="7e6cf-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e6cf-195"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7e6cf-195"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7e6cf-196">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7e6cf-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7e6cf-197">**\_ 作業 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 作業 \_ 資訊 \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7e6cf-197">**\_JOB\_INFO\_1W** (Unicode) and **\_JOB\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="7e6cf-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e6cf-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e6cf-199">列印</span><span class="sxs-lookup"><span data-stu-id="7e6cf-199">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7e6cf-200">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="7e6cf-200">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7e6cf-201">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-201">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="7e6cf-202">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-202">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="7e6cf-203">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="7e6cf-203">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

