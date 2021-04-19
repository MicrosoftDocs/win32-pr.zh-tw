---
description: 印表機 \_ 資訊 \_ 5 結構會指定詳細的印表機資訊。
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: 'PRINTER_INFO_5 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988884"
---
# <a name="printer_info_5-structure"></a><span data-ttu-id="7b624-103">印表機 \_ 資訊 \_ 5 結構</span><span class="sxs-lookup"><span data-stu-id="7b624-103">PRINTER\_INFO\_5 structure</span></span>

<span data-ttu-id="7b624-104">**印表機 \_ 資訊 \_ 5** 結構會指定詳細的印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="7b624-104">The **PRINTER\_INFO\_5** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b624-105">語法</span><span class="sxs-lookup"><span data-stu-id="7b624-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="7b624-106">成員</span><span class="sxs-lookup"><span data-stu-id="7b624-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b624-107">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="7b624-107">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="7b624-108">指定印表機名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="7b624-108">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="7b624-109">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="7b624-109">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="7b624-110">以 null 結束的字串指標，識別用來將資料傳輸至印表機的埠 (s) 。</span><span class="sxs-lookup"><span data-stu-id="7b624-110">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="7b624-111">如果印表機連線到一個以上的埠，每個埠的名稱必須以逗號分隔 (例如，"LPT1：，LPT2：，LPT3：" ) 。</span><span class="sxs-lookup"><span data-stu-id="7b624-111">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="7b624-112">**屬性**</span><span class="sxs-lookup"><span data-stu-id="7b624-112">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="7b624-113">印表機屬性。</span><span class="sxs-lookup"><span data-stu-id="7b624-113">The printer attributes.</span></span> <span data-ttu-id="7b624-114">這個成員可以是下列值的任何合理組合。</span><span class="sxs-lookup"><span data-stu-id="7b624-114">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="7b624-115">值</span><span class="sxs-lookup"><span data-stu-id="7b624-115">Value</span></span>                                   | <span data-ttu-id="7b624-116">意義</span><span class="sxs-lookup"><span data-stu-id="7b624-116">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b624-117">印表機 \_ 屬性 \_ 直接</span><span class="sxs-lookup"><span data-stu-id="7b624-117">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="7b624-118">作業會直接傳送到印表機 (不會) 。</span><span class="sxs-lookup"><span data-stu-id="7b624-118">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="7b624-119">印表機 \_ 屬性 \_ \_ 先完成 \_</span><span class="sxs-lookup"><span data-stu-id="7b624-119">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="7b624-120">如果設定和印表機設定為列印時進行列印，則任何已完成的幕後處理作業都會排定在未完成幕後處理的作業之前列印。</span><span class="sxs-lookup"><span data-stu-id="7b624-120">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="7b624-121">印表機 \_ 屬性 \_ 啟用 \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="7b624-121">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="7b624-122">如果設定，則會呼叫 **DevQueryPrint** 。</span><span class="sxs-lookup"><span data-stu-id="7b624-122">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="7b624-123">如果檔和印表機的設置不符， **DevQueryPrint** 可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="7b624-123">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="7b624-124">設定此旗標會使不相符的檔保留在佇列中。</span><span class="sxs-lookup"><span data-stu-id="7b624-124">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="7b624-125">印表機 \_ 屬性 \_ 隱藏</span><span class="sxs-lookup"><span data-stu-id="7b624-125">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="7b624-126">保留的。</span><span class="sxs-lookup"><span data-stu-id="7b624-126">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="7b624-127">印表機 \_ 屬性 \_ KEEPPRINTEDJOBS</span><span class="sxs-lookup"><span data-stu-id="7b624-127">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="7b624-128">如果設定，則會在列印工作之後保留工作。</span><span class="sxs-lookup"><span data-stu-id="7b624-128">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="7b624-129">如果未設定，則會刪除作業。</span><span class="sxs-lookup"><span data-stu-id="7b624-129">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="7b624-130">\_本機印表機屬性 \_</span><span class="sxs-lookup"><span data-stu-id="7b624-130">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="7b624-131">印表機是本機印表機。</span><span class="sxs-lookup"><span data-stu-id="7b624-131">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="7b624-132">印表機 \_ 屬性 \_ 網路</span><span class="sxs-lookup"><span data-stu-id="7b624-132">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="7b624-133">印表機是網路印表機連接。</span><span class="sxs-lookup"><span data-stu-id="7b624-133">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="7b624-134">\_ \_ 已發佈印表機屬性</span><span class="sxs-lookup"><span data-stu-id="7b624-134">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="7b624-135">指出是否要在目錄服務中發佈印表機。</span><span class="sxs-lookup"><span data-stu-id="7b624-135">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="7b624-136">印表機 \_ 屬性已 \_ 排入佇列</span><span class="sxs-lookup"><span data-stu-id="7b624-136">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="7b624-137">如果設定，印表機會在最後一頁進行多工緩衝處理之後，再開始列印。</span><span class="sxs-lookup"><span data-stu-id="7b624-137">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="7b624-138">如果未設定，且 \_ \_ 未設定印表機屬性 DIRECT，則印表機會在幕後處理時進行幕後處理和列印。</span><span class="sxs-lookup"><span data-stu-id="7b624-138">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="7b624-139">\_ \_ 僅限原始印表機屬性 \_</span><span class="sxs-lookup"><span data-stu-id="7b624-139">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="7b624-140">指出只有原始資料類型列印工作可以進行多工緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="7b624-140">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="7b624-141">印表機 \_ 屬性 \_ 共用</span><span class="sxs-lookup"><span data-stu-id="7b624-141">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="7b624-142">印表機是共用的。</span><span class="sxs-lookup"><span data-stu-id="7b624-142">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="7b624-143">在 Windows XP 和更新版本的 Windows 中，也可以使用下列值。</span><span class="sxs-lookup"><span data-stu-id="7b624-143">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="7b624-144">值</span><span class="sxs-lookup"><span data-stu-id="7b624-144">Value</span></span>                   | <span data-ttu-id="7b624-145">意義</span><span class="sxs-lookup"><span data-stu-id="7b624-145">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b624-146">印表機 \_ 屬性 \_ 傳真</span><span class="sxs-lookup"><span data-stu-id="7b624-146">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="7b624-147">如果設定，印表機就是傳真印表機。</span><span class="sxs-lookup"><span data-stu-id="7b624-147">If set, printer is a fax printer.</span></span> <span data-ttu-id="7b624-148">這只能由 [**interactivesession.addprinter**](addprinter.md)設定，但可由 [**>enumprinters**](enumprinters.md) 和 [**GetPrinter**](getprinter.md)來抓取。</span><span class="sxs-lookup"><span data-stu-id="7b624-148">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="7b624-149">在 Windows Vista 和更新版本的 Windows 中，也可以使用下列值。</span><span class="sxs-lookup"><span data-stu-id="7b624-149">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="7b624-150">值</span><span class="sxs-lookup"><span data-stu-id="7b624-150">Value</span></span>                               | <span data-ttu-id="7b624-151">意義</span><span class="sxs-lookup"><span data-stu-id="7b624-151">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7b624-152">印表機 \_ 屬性 \_ 易記 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="7b624-152">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="7b624-153">電腦已連線到此印表機，並將其命名為易記名稱。</span><span class="sxs-lookup"><span data-stu-id="7b624-153">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="7b624-154">印表機 \_ 屬性 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="7b624-154">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="7b624-155">印表機是一台電腦的連線。</span><span class="sxs-lookup"><span data-stu-id="7b624-155">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="7b624-156">已 \_ 推入印表機屬性的 \_ \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="7b624-156">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="7b624-157">印表機是使用 [推播印表機連線] 使用者原則安裝的。</span><span class="sxs-lookup"><span data-stu-id="7b624-157">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="7b624-158">印表機 \_ 屬性已 \_ 推送 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="7b624-158">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="7b624-159">印表機是使用 [推播印表機連線] 電腦原則安裝的。</span><span class="sxs-lookup"><span data-stu-id="7b624-159">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7b624-160">**DeviceNotSelectedTimeout**</span><span class="sxs-lookup"><span data-stu-id="7b624-160">**DeviceNotSelectedTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="7b624-161">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="7b624-161">This value is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7b624-162">**TransmissionRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="7b624-162">**TransmissionRetryTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="7b624-163">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="7b624-163">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b624-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b624-164">Requirements</span></span>



| <span data-ttu-id="7b624-165">需求</span><span class="sxs-lookup"><span data-stu-id="7b624-165">Requirement</span></span> | <span data-ttu-id="7b624-166">值</span><span class="sxs-lookup"><span data-stu-id="7b624-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b624-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b624-167">Minimum supported client</span></span><br/> | <span data-ttu-id="7b624-168">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b624-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7b624-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b624-169">Minimum supported server</span></span><br/> | <span data-ttu-id="7b624-170">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b624-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7b624-171">標頭</span><span class="sxs-lookup"><span data-stu-id="7b624-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b624-172"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7b624-172"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7b624-173">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7b624-173">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7b624-174">**\_ 印表機 \_ 資訊 \_** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 5a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7b624-174">**\_PRINTER\_INFO\_5W** (Unicode) and **\_PRINTER\_INFO\_5A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="7b624-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b624-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b624-176">列印</span><span class="sxs-lookup"><span data-stu-id="7b624-176">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7b624-177">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="7b624-177">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7b624-178">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="7b624-178">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="7b624-179">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="7b624-179">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="7b624-180">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="7b624-180">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="7b624-181">**印表機 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7b624-181">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="7b624-182">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7b624-182">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="7b624-183">**印表機 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="7b624-183">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="7b624-184">**印表機 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="7b624-184">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




