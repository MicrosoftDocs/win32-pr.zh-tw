---
description: 作業 \_ 資訊 \_ 2 結構描述與作業相關聯的一組完整值。
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: 'JOB_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_2
- _JOB_INFO_2A
- _JOB_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d6b582267afceb01fd7ced7d6d46144664bb9d2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194963"
---
# <a name="job_info_2-structure"></a><span data-ttu-id="27e96-103">作業 \_ 資訊 \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="27e96-103">JOB\_INFO\_2 structure</span></span>

<span data-ttu-id="27e96-104">**作業 \_ 資訊 \_ 2** 結構描述與作業相關聯的一組完整值。</span><span class="sxs-lookup"><span data-stu-id="27e96-104">The **JOB\_INFO\_2** structure describes a full set of values associated with a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e96-105">語法</span><span class="sxs-lookup"><span data-stu-id="27e96-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_2 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
} JOB_INFO_2, *PJOB_INFO_2;
```



## <a name="members"></a><span data-ttu-id="27e96-106">成員</span><span class="sxs-lookup"><span data-stu-id="27e96-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="27e96-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="27e96-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-108">作業識別碼值。</span><span class="sxs-lookup"><span data-stu-id="27e96-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="27e96-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-110">以 null 結束的字串指標，指定工作要進行多工緩衝處理的印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="27e96-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="27e96-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-112">以 null 結束的字串指標，指定建立列印工作的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="27e96-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="27e96-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-114">以 null 結束的字串指標，指定擁有列印工作之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e96-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="27e96-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-116">以 null 結束的字串指標，指定列印工作的名稱 (例如 "MS-WORD： Review.doc" ) 。</span><span class="sxs-lookup"><span data-stu-id="27e96-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="27e96-117">**pNotifyName**</span><span class="sxs-lookup"><span data-stu-id="27e96-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-118">以 null 結束的字串指標，指定在列印工作或列印工作時發生錯誤時，應通知的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="27e96-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-119">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="27e96-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-120">以 null 結束的字串指標，指定用來記錄列印工作的資料類型。</span><span class="sxs-lookup"><span data-stu-id="27e96-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-121">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="27e96-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-122">以 null 結束的字串指標，指定應該用來列印工作的列印處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="27e96-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="27e96-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-124">指定列印處理器參數之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="27e96-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-125">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="27e96-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-126">以 null 結束的字串指標，指定應該用來處理列印工作的印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="27e96-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-127">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="27e96-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-128">[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的指標，其中包含印表機驅動程式的裝置初始化和環境資料。</span><span class="sxs-lookup"><span data-stu-id="27e96-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-129">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="27e96-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-130">以 null 結束的字串指標，指定列印工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="27e96-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="27e96-131">此成員應在 **狀態** 之前檢查，而且如果 **pStatus** 為 **Null**，則狀態會由狀態成員的內容定義。</span><span class="sxs-lookup"><span data-stu-id="27e96-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-132">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="27e96-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-133">此成員的值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27e96-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="27e96-134">此版本不支援檔安全描述項的抓取和設定。</span><span class="sxs-lookup"><span data-stu-id="27e96-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-135">**狀態**</span><span class="sxs-lookup"><span data-stu-id="27e96-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-136">作業狀態。</span><span class="sxs-lookup"><span data-stu-id="27e96-136">The job status.</span></span> <span data-ttu-id="27e96-137">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="27e96-137">This member can be one or more of the following values.</span></span>

| <span data-ttu-id="27e96-138">值</span><span class="sxs-lookup"><span data-stu-id="27e96-138">Value</span></span>                           | <span data-ttu-id="27e96-139">意義</span><span class="sxs-lookup"><span data-stu-id="27e96-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="27e96-140">作業 \_ 狀態已 \_ 封鎖 \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="27e96-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="27e96-141">驅動程式無法列印工作。</span><span class="sxs-lookup"><span data-stu-id="27e96-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="27e96-142">作業 \_ 狀態 \_ 已刪除</span><span class="sxs-lookup"><span data-stu-id="27e96-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="27e96-143">作業已刪除。</span><span class="sxs-lookup"><span data-stu-id="27e96-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="27e96-144">作業 \_ 狀態 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="27e96-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="27e96-145">正在刪除工作。</span><span class="sxs-lookup"><span data-stu-id="27e96-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="27e96-146">作業 \_ 狀態 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="27e96-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="27e96-147">與作業相關聯的錯誤。</span><span class="sxs-lookup"><span data-stu-id="27e96-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="27e96-148">\_離線作業狀態 \_</span><span class="sxs-lookup"><span data-stu-id="27e96-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="27e96-149">印表機已離線。</span><span class="sxs-lookup"><span data-stu-id="27e96-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="27e96-150">作業 \_ 狀態 \_ PAPEROUT</span><span class="sxs-lookup"><span data-stu-id="27e96-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="27e96-151">印表機缺紙。</span><span class="sxs-lookup"><span data-stu-id="27e96-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="27e96-152">作業 \_ 狀態已 \_ 暫停</span><span class="sxs-lookup"><span data-stu-id="27e96-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="27e96-153">作業已暫停。</span><span class="sxs-lookup"><span data-stu-id="27e96-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="27e96-154">作業 \_ 狀態已 \_ 列印</span><span class="sxs-lookup"><span data-stu-id="27e96-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="27e96-155">作業已列印。</span><span class="sxs-lookup"><span data-stu-id="27e96-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="27e96-156">作業 \_ 狀態 \_ 列印</span><span class="sxs-lookup"><span data-stu-id="27e96-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="27e96-157">作業正在列印。</span><span class="sxs-lookup"><span data-stu-id="27e96-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="27e96-158">作業 \_ 狀態 \_ 重新開機</span><span class="sxs-lookup"><span data-stu-id="27e96-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="27e96-159">作業已重新開機。</span><span class="sxs-lookup"><span data-stu-id="27e96-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="27e96-160">作業 \_ 狀態 \_ 緩衝處理</span><span class="sxs-lookup"><span data-stu-id="27e96-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="27e96-161">作業已在幕後處理。</span><span class="sxs-lookup"><span data-stu-id="27e96-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="27e96-162">作業 \_ 狀態 \_ 使用者 \_ 介入</span><span class="sxs-lookup"><span data-stu-id="27e96-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="27e96-163">印表機有錯誤，需要使用者進行一些動作。</span><span class="sxs-lookup"><span data-stu-id="27e96-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="27e96-164">在 Windows XP 和更新版本的 Windows 中，也可以使用下列值：</span><span class="sxs-lookup"><span data-stu-id="27e96-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="27e96-165">值</span><span class="sxs-lookup"><span data-stu-id="27e96-165">Value</span></span>                 | <span data-ttu-id="27e96-166">意義</span><span class="sxs-lookup"><span data-stu-id="27e96-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27e96-167">作業 \_ 狀態 \_ 完成</span><span class="sxs-lookup"><span data-stu-id="27e96-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="27e96-168">作業會傳送至印表機，但可能尚未列印。</span><span class="sxs-lookup"><span data-stu-id="27e96-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="27e96-169">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="27e96-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="27e96-170">保留的作業 \_ 狀態 \_</span><span class="sxs-lookup"><span data-stu-id="27e96-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="27e96-171">作業已在列印後保留在列印佇列中。</span><span class="sxs-lookup"><span data-stu-id="27e96-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="27e96-172">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="27e96-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-173">作業優先權。</span><span class="sxs-lookup"><span data-stu-id="27e96-173">The job priority.</span></span> <span data-ttu-id="27e96-174">這個成員可以是下列其中一個值，或介於1到99之間的範圍 (最低優先順序 \_ 到最高 \_ 優先順序) 。</span><span class="sxs-lookup"><span data-stu-id="27e96-174">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="27e96-175">值</span><span class="sxs-lookup"><span data-stu-id="27e96-175">Value</span></span>         | <span data-ttu-id="27e96-176">意義</span><span class="sxs-lookup"><span data-stu-id="27e96-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="27e96-177">最小 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="27e96-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="27e96-178">最小優先權。</span><span class="sxs-lookup"><span data-stu-id="27e96-178">Minimum priority.</span></span> |
| <span data-ttu-id="27e96-179">最高 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="27e96-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="27e96-180">最高優先順序。</span><span class="sxs-lookup"><span data-stu-id="27e96-180">Maximum priority.</span></span> |
| <span data-ttu-id="27e96-181">DEF \_ 優先權</span><span class="sxs-lookup"><span data-stu-id="27e96-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="27e96-182">預設優先順序。</span><span class="sxs-lookup"><span data-stu-id="27e96-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="27e96-183">**位置**</span><span class="sxs-lookup"><span data-stu-id="27e96-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-184">工作在列印佇列中的位置。</span><span class="sxs-lookup"><span data-stu-id="27e96-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="27e96-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-186">作業可以列印的最早時間。</span><span class="sxs-lookup"><span data-stu-id="27e96-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="27e96-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-188">作業可以列印的最晚時間。</span><span class="sxs-lookup"><span data-stu-id="27e96-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="27e96-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-190">作業所需的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="27e96-190">The number of pages required for the job.</span></span> <span data-ttu-id="27e96-191">如果列印工作未包含以頁面分隔的資訊，則此值可能為零。</span><span class="sxs-lookup"><span data-stu-id="27e96-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-192">**大小**</span><span class="sxs-lookup"><span data-stu-id="27e96-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-193">作業的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="27e96-193">The size, in bytes, of the job.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-194">**已提交**</span><span class="sxs-lookup"><span data-stu-id="27e96-194">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-195">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構，指定提交作業的時間。</span><span class="sxs-lookup"><span data-stu-id="27e96-195">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="27e96-196">此時間值採用國際標準時間座標 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="27e96-196">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="27e96-197">您應該先將它轉換成當地時間值，再顯示它。</span><span class="sxs-lookup"><span data-stu-id="27e96-197">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="27e96-198">您可以使用 [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) 函數來執行轉換。</span><span class="sxs-lookup"><span data-stu-id="27e96-198">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-199">**Time**</span><span class="sxs-lookup"><span data-stu-id="27e96-199">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-200">自從作業開始列印以來經過的總時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="27e96-200">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="27e96-201">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="27e96-201">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="27e96-202">已列印的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="27e96-202">The number of pages that have printed.</span></span> <span data-ttu-id="27e96-203">如果列印工作未包含以頁面分隔的資訊，則此值可能為零。</span><span class="sxs-lookup"><span data-stu-id="27e96-203">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27e96-204">備註</span><span class="sxs-lookup"><span data-stu-id="27e96-204">Remarks</span></span>

<span data-ttu-id="27e96-205">不支援 TrueEndOfJob 的埠監視器，會將工作設定為在 \_ \_ 將作業提交至印表機之後列印的工作狀態。</span><span class="sxs-lookup"><span data-stu-id="27e96-205">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="27e96-206">規格需求</span><span class="sxs-lookup"><span data-stu-id="27e96-206">Requirements</span></span>



| <span data-ttu-id="27e96-207">需求</span><span class="sxs-lookup"><span data-stu-id="27e96-207">Requirement</span></span> | <span data-ttu-id="27e96-208">值</span><span class="sxs-lookup"><span data-stu-id="27e96-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27e96-209">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27e96-209">Minimum supported client</span></span><br/> | <span data-ttu-id="27e96-210">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27e96-210">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="27e96-211">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27e96-211">Minimum supported server</span></span><br/> | <span data-ttu-id="27e96-212">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27e96-212">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27e96-213">標頭</span><span class="sxs-lookup"><span data-stu-id="27e96-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="27e96-214"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="27e96-214"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="27e96-215">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="27e96-215">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="27e96-216">**\_ 作業 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 工作 \_ 資訊 \_ 2a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="27e96-216">**\_JOB\_INFO\_2W** (Unicode) and **\_JOB\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="27e96-217">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27e96-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e96-218">列印</span><span class="sxs-lookup"><span data-stu-id="27e96-218">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="27e96-219">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="27e96-219">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="27e96-220">**版**</span><span class="sxs-lookup"><span data-stu-id="27e96-220">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="27e96-221">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="27e96-221">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="27e96-222">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="27e96-222">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="27e96-223">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="27e96-223">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

