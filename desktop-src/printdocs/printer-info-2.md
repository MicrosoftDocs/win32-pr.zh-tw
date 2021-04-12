---
description: 印表機 \_ 資訊 \_ 2 結構會指定詳細的印表機資訊。
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: 'PRINTER_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513832"
---
# <a name="printer_info_2-structure"></a><span data-ttu-id="4ee99-103">印表機 \_ 資訊 \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="4ee99-103">PRINTER\_INFO\_2 structure</span></span>

<span data-ttu-id="4ee99-104">**印表機 \_ 資訊 \_ 2** 結構會指定詳細的印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="4ee99-104">The **PRINTER\_INFO\_2** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee99-105">語法</span><span class="sxs-lookup"><span data-stu-id="4ee99-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="4ee99-106">成員</span><span class="sxs-lookup"><span data-stu-id="4ee99-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ee99-107">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="4ee99-107">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-108">以 null 結束的字串指標，識別控制印表機的伺服器。</span><span class="sxs-lookup"><span data-stu-id="4ee99-108">A pointer to a null-terminated string identifying the server that controls the printer.</span></span> <span data-ttu-id="4ee99-109">如果這個字串是 **Null**，則會在本機控制印表機。</span><span class="sxs-lookup"><span data-stu-id="4ee99-109">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-110">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="4ee99-110">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-111">指定印表機名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="4ee99-111">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-112">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="4ee99-112">**pShareName**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-113">以 null 結束的字串指標，可識別印表機的共用點。</span><span class="sxs-lookup"><span data-stu-id="4ee99-113">A pointer to a null-terminated string that identifies the share point for the printer.</span></span> <span data-ttu-id="4ee99-114"> (只有在 \_ \_ 已設定 **屬性** 成員的印表機屬性共用常數時，才會使用此字串。 ) </span><span class="sxs-lookup"><span data-stu-id="4ee99-114">(This string is used only if the PRINTER\_ATTRIBUTE\_SHARED constant was set for the **Attributes** member.)</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-115">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="4ee99-115">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-116">以 null 結束的字串指標，識別用來將資料傳輸至印表機的埠 (s) 。</span><span class="sxs-lookup"><span data-stu-id="4ee99-116">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="4ee99-117">如果印表機連線到一個以上的埠，每個埠的名稱必須以逗號分隔 (例如，"LPT1：，LPT2：，LPT3：" ) 。</span><span class="sxs-lookup"><span data-stu-id="4ee99-117">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-118">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="4ee99-118">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-119">以 null 結束的字串指標，指定印表機驅動程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ee99-119">A pointer to a null-terminated string that specifies the name of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-120">**pComment**</span><span class="sxs-lookup"><span data-stu-id="4ee99-120">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-121">以 null 結束的字串指標，提供印表機的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="4ee99-121">A pointer to a null-terminated string that provides a brief description of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-122">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="4ee99-122">**pLocation**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-123">以 null 結束的字串指標，指定印表機 (的實體位置，例如 "Bldg"。</span><span class="sxs-lookup"><span data-stu-id="4ee99-123">A pointer to a null-terminated string that specifies the physical location of the printer (for example, "Bldg.</span></span> <span data-ttu-id="4ee99-124">38，房間1164」 ) 。</span><span class="sxs-lookup"><span data-stu-id="4ee99-124">38, Room 1164").</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-125">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="4ee99-125">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-126">用來定義預設印表機資料的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標，例如紙張方向和解析度。</span><span class="sxs-lookup"><span data-stu-id="4ee99-126">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines default printer data such as the paper orientation and the resolution.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-127">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="4ee99-127">**pSepFile**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-128">以 null 結束的字串指標，指定用來建立分隔符號頁面的檔案名。</span><span class="sxs-lookup"><span data-stu-id="4ee99-128">A pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="4ee99-129">此頁面是用來分隔傳送至印表機的列印工作。</span><span class="sxs-lookup"><span data-stu-id="4ee99-129">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-130">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="4ee99-130">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-131">以 null 結束的字串指標，指定印表機所使用的列印處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="4ee99-131">A pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span> <span data-ttu-id="4ee99-132">您可以使用 [**EnumPrintProcessors**](enumprintprocessors.md) 函數來取得伺服器上所安裝之列印處理器的清單。</span><span class="sxs-lookup"><span data-stu-id="4ee99-132">You can use the [**EnumPrintProcessors**](enumprintprocessors.md) function to obtain a list of print processors installed on a server.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-133">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="4ee99-133">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-134">以 null 結束的字串指標，指定用來記錄列印工作的資料類型。</span><span class="sxs-lookup"><span data-stu-id="4ee99-134">A pointer to a null-terminated string that specifies the data type used to record the print job.</span></span> <span data-ttu-id="4ee99-135">您可以使用 [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) 函數來取得特定列印處理器所支援的資料類型清單。</span><span class="sxs-lookup"><span data-stu-id="4ee99-135">You can use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to obtain a list of data types supported by a specific print processor.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-136">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="4ee99-136">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-137">指定預設列印處理器參數之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="4ee99-137">A pointer to a null-terminated string that specifies the default print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-138">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4ee99-138">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-139">印表機的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="4ee99-139">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure for the printer.</span></span> <span data-ttu-id="4ee99-140">這個成員可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ee99-140">This member may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-141">**屬性**</span><span class="sxs-lookup"><span data-stu-id="4ee99-141">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-142">印表機屬性。</span><span class="sxs-lookup"><span data-stu-id="4ee99-142">The printer attributes.</span></span> <span data-ttu-id="4ee99-143">這個成員可以是下列值的任何合理組合。</span><span class="sxs-lookup"><span data-stu-id="4ee99-143">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="4ee99-144">值</span><span class="sxs-lookup"><span data-stu-id="4ee99-144">Value</span></span>                                   | <span data-ttu-id="4ee99-145">意義</span><span class="sxs-lookup"><span data-stu-id="4ee99-145">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee99-146">印表機 \_ 屬性 \_ 直接</span><span class="sxs-lookup"><span data-stu-id="4ee99-146">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="4ee99-147">作業會直接傳送到印表機 (不會) 。</span><span class="sxs-lookup"><span data-stu-id="4ee99-147">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="4ee99-148">印表機 \_ 屬性 \_ \_ 先完成 \_</span><span class="sxs-lookup"><span data-stu-id="4ee99-148">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="4ee99-149">如果設定和印表機設定為列印時進行列印，則任何已完成的幕後處理作業都會排定在未完成幕後處理的作業之前列印。</span><span class="sxs-lookup"><span data-stu-id="4ee99-149">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="4ee99-150">印表機 \_ 屬性 \_ 啟用 \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="4ee99-150">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="4ee99-151">如果設定，則會呼叫 **DevQueryPrint** 。</span><span class="sxs-lookup"><span data-stu-id="4ee99-151">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="4ee99-152">如果檔和印表機的設置不符， **DevQueryPrint** 可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="4ee99-152">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="4ee99-153">設定此旗標會使不相符的檔保留在佇列中。</span><span class="sxs-lookup"><span data-stu-id="4ee99-153">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="4ee99-154">印表機 \_ 屬性 \_ 隱藏</span><span class="sxs-lookup"><span data-stu-id="4ee99-154">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="4ee99-155">保留的。</span><span class="sxs-lookup"><span data-stu-id="4ee99-155">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="4ee99-156">印表機 \_ 屬性 \_ KEEPPRINTEDJOBS</span><span class="sxs-lookup"><span data-stu-id="4ee99-156">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="4ee99-157">如果設定，則會在列印工作之後保留工作。</span><span class="sxs-lookup"><span data-stu-id="4ee99-157">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="4ee99-158">如果未設定，則會刪除作業。</span><span class="sxs-lookup"><span data-stu-id="4ee99-158">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="4ee99-159">\_本機印表機屬性 \_</span><span class="sxs-lookup"><span data-stu-id="4ee99-159">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="4ee99-160">印表機是本機印表機。</span><span class="sxs-lookup"><span data-stu-id="4ee99-160">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="4ee99-161">印表機 \_ 屬性 \_ 網路</span><span class="sxs-lookup"><span data-stu-id="4ee99-161">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="4ee99-162">印表機是網路印表機連接。</span><span class="sxs-lookup"><span data-stu-id="4ee99-162">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="4ee99-163">\_ \_ 已發佈印表機屬性</span><span class="sxs-lookup"><span data-stu-id="4ee99-163">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="4ee99-164">指出是否要在目錄服務中發佈印表機。</span><span class="sxs-lookup"><span data-stu-id="4ee99-164">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="4ee99-165">印表機 \_ 屬性已 \_ 排入佇列</span><span class="sxs-lookup"><span data-stu-id="4ee99-165">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="4ee99-166">如果設定，印表機會在最後一頁進行多工緩衝處理之後，再開始列印。</span><span class="sxs-lookup"><span data-stu-id="4ee99-166">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="4ee99-167">如果未設定，且 \_ \_ 未設定印表機屬性 DIRECT，則印表機會在幕後處理時進行幕後處理和列印。</span><span class="sxs-lookup"><span data-stu-id="4ee99-167">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="4ee99-168">\_ \_ 僅限原始印表機屬性 \_</span><span class="sxs-lookup"><span data-stu-id="4ee99-168">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="4ee99-169">指出只有原始資料類型列印工作可以進行多工緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="4ee99-169">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="4ee99-170">印表機 \_ 屬性 \_ 共用</span><span class="sxs-lookup"><span data-stu-id="4ee99-170">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="4ee99-171">印表機是共用的。</span><span class="sxs-lookup"><span data-stu-id="4ee99-171">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="4ee99-172">在 Windows XP 和更新版本的 Windows 中，也可以使用下列值。</span><span class="sxs-lookup"><span data-stu-id="4ee99-172">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="4ee99-173">值</span><span class="sxs-lookup"><span data-stu-id="4ee99-173">Value</span></span>                   | <span data-ttu-id="4ee99-174">意義</span><span class="sxs-lookup"><span data-stu-id="4ee99-174">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee99-175">印表機 \_ 屬性 \_ 傳真</span><span class="sxs-lookup"><span data-stu-id="4ee99-175">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="4ee99-176">如果設定，印表機就是傳真印表機。</span><span class="sxs-lookup"><span data-stu-id="4ee99-176">If set, printer is a fax printer.</span></span> <span data-ttu-id="4ee99-177">這只能由 [**interactivesession.addprinter**](addprinter.md)設定，但可由 [**>enumprinters**](enumprinters.md) 和 [**GetPrinter**](getprinter.md)來抓取。</span><span class="sxs-lookup"><span data-stu-id="4ee99-177">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="4ee99-178">在 Windows Vista 和更新版本的 Windows 中，也可以使用下列值。</span><span class="sxs-lookup"><span data-stu-id="4ee99-178">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="4ee99-179">值</span><span class="sxs-lookup"><span data-stu-id="4ee99-179">Value</span></span>                               | <span data-ttu-id="4ee99-180">意義</span><span class="sxs-lookup"><span data-stu-id="4ee99-180">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4ee99-181">印表機 \_ 屬性 \_ 易記 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="4ee99-181">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="4ee99-182">電腦已連線到此印表機，並將其命名為易記名稱。</span><span class="sxs-lookup"><span data-stu-id="4ee99-182">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="4ee99-183">印表機 \_ 屬性 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="4ee99-183">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="4ee99-184">印表機是一台電腦的連線。</span><span class="sxs-lookup"><span data-stu-id="4ee99-184">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="4ee99-185">已 \_ 推入印表機屬性的 \_ \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="4ee99-185">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="4ee99-186">印表機是使用 [推播印表機連線] 使用者原則安裝的。</span><span class="sxs-lookup"><span data-stu-id="4ee99-186">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="4ee99-187">印表機 \_ 屬性已 \_ 推送 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="4ee99-187">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="4ee99-188">印表機是使用 [推播印表機連線] 電腦原則安裝的。</span><span class="sxs-lookup"><span data-stu-id="4ee99-188">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

<span data-ttu-id="4ee99-189">在 Windows Server 2003 中，也可以使用下列值。</span><span class="sxs-lookup"><span data-stu-id="4ee99-189">In Windows Server 2003, the following value can also be used.</span></span>

| <span data-ttu-id="4ee99-190">值</span><span class="sxs-lookup"><span data-stu-id="4ee99-190">Value</span></span>                  | <span data-ttu-id="4ee99-191">意義</span><span class="sxs-lookup"><span data-stu-id="4ee99-191">Meaning</span></span>                                                                 |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4ee99-192">印表機 \_ 屬性 \_ TS</span><span class="sxs-lookup"><span data-stu-id="4ee99-192">PRINTER\_ATTRIBUTE\_TS</span></span> | <span data-ttu-id="4ee99-193">指出印表機目前透過終端機伺服器連線。</span><span class="sxs-lookup"><span data-stu-id="4ee99-193">Indicates the printer is currently connected through a terminal server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="4ee99-194">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="4ee99-194">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-195">多工緩衝處理器用來路由列印工作的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="4ee99-195">A priority value that the spooler uses to route print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-196">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="4ee99-196">**DefaultPriority**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-197">指派給每個列印工作的預設優先權值。</span><span class="sxs-lookup"><span data-stu-id="4ee99-197">The default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-198">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4ee99-198">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-199">印表機將列印工作的最早時間。</span><span class="sxs-lookup"><span data-stu-id="4ee99-199">The earliest time at which the printer will print a job.</span></span> <span data-ttu-id="4ee99-200">此值的表示方式為自 12:00 AM GMT 起的經過時間， (格林尼治平均時間) 。</span><span class="sxs-lookup"><span data-stu-id="4ee99-200">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-201">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4ee99-201">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-202">印表機將列印工作的最新時間。</span><span class="sxs-lookup"><span data-stu-id="4ee99-202">The latest time at which the printer will print a job.</span></span> <span data-ttu-id="4ee99-203">此值的表示方式為自 12:00 AM GMT 起的經過時間， (格林尼治平均時間) 。</span><span class="sxs-lookup"><span data-stu-id="4ee99-203">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-204">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4ee99-204">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-205">印表機狀態。</span><span class="sxs-lookup"><span data-stu-id="4ee99-205">The printer status.</span></span> <span data-ttu-id="4ee99-206">這個成員可以是下列值的任何合理組合。</span><span class="sxs-lookup"><span data-stu-id="4ee99-206">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="4ee99-207">值</span><span class="sxs-lookup"><span data-stu-id="4ee99-207">Value</span></span>                               | <span data-ttu-id="4ee99-208">意義</span><span class="sxs-lookup"><span data-stu-id="4ee99-208">Meaning</span></span>                                                          |
|-------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4ee99-209">印表機 \_ 狀態 \_ 忙碌中</span><span class="sxs-lookup"><span data-stu-id="4ee99-209">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="4ee99-210">印表機忙碌中。</span><span class="sxs-lookup"><span data-stu-id="4ee99-210">The printer is busy.</span></span>                                             |
| <span data-ttu-id="4ee99-211">印表機 \_ 狀態 \_ 門 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="4ee99-211">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="4ee99-212">印表機門已開啟。</span><span class="sxs-lookup"><span data-stu-id="4ee99-212">The printer door is open.</span></span>                                        |
| <span data-ttu-id="4ee99-213">印表機 \_ 狀態 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="4ee99-213">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="4ee99-214">印表機處於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="4ee99-214">The printer is in an error state.</span></span>                                |
| <span data-ttu-id="4ee99-215">印表機 \_ 狀態 \_ 初始化</span><span class="sxs-lookup"><span data-stu-id="4ee99-215">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="4ee99-216">印表機初始化中。</span><span class="sxs-lookup"><span data-stu-id="4ee99-216">The printer is initializing.</span></span>                                     |
| <span data-ttu-id="4ee99-217">印表機 \_ 狀態 \_ IO 使用中 \_</span><span class="sxs-lookup"><span data-stu-id="4ee99-217">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="4ee99-218">印表機處於作用中的輸入/輸出狀態</span><span class="sxs-lookup"><span data-stu-id="4ee99-218">The printer is in an active input/output state</span></span>                   |
| <span data-ttu-id="4ee99-219">印表機 \_ 狀態 \_ 手動 \_ 饋送</span><span class="sxs-lookup"><span data-stu-id="4ee99-219">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="4ee99-220">印表機處於手動摘要狀態。</span><span class="sxs-lookup"><span data-stu-id="4ee99-220">The printer is in a manual feed state.</span></span>                           |
| <span data-ttu-id="4ee99-221">印表機 \_ 狀態 \_ 無 \_ 墨粉</span><span class="sxs-lookup"><span data-stu-id="4ee99-221">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="4ee99-222">印表機的碳粉已用完。</span><span class="sxs-lookup"><span data-stu-id="4ee99-222">The printer is out of toner.</span></span>                                     |
| <span data-ttu-id="4ee99-223">印表機 \_ 狀態 \_ 無法 \_ 使用</span><span class="sxs-lookup"><span data-stu-id="4ee99-223">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="4ee99-224">印表機無法列印。</span><span class="sxs-lookup"><span data-stu-id="4ee99-224">The printer is not available for printing.</span></span>                       |
| <span data-ttu-id="4ee99-225">印表機 \_ 狀態 \_ 離線</span><span class="sxs-lookup"><span data-stu-id="4ee99-225">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="4ee99-226">印表機為離線。</span><span class="sxs-lookup"><span data-stu-id="4ee99-226">The printer is offline.</span></span>                                          |
| <span data-ttu-id="4ee99-227">印表機 \_ 狀態 \_ \_ 記憶體不足 \_</span><span class="sxs-lookup"><span data-stu-id="4ee99-227">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="4ee99-228">印表機的記憶體用盡。</span><span class="sxs-lookup"><span data-stu-id="4ee99-228">The printer has run out of memory.</span></span>                               |
| <span data-ttu-id="4ee99-229">印表機 \_ 狀態 \_ 輸出 \_ 紙匣已 \_ 滿</span><span class="sxs-lookup"><span data-stu-id="4ee99-229">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="4ee99-230">印表機的輸出紙匣已滿。</span><span class="sxs-lookup"><span data-stu-id="4ee99-230">The printer's output bin is full.</span></span>                                |
| <span data-ttu-id="4ee99-231">印表機 \_ 狀態 \_ 頁面 \_</span><span class="sxs-lookup"><span data-stu-id="4ee99-231">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="4ee99-232">印表機無法列印目前的頁面。</span><span class="sxs-lookup"><span data-stu-id="4ee99-232">The printer cannot print the current page.</span></span>                       |
| <span data-ttu-id="4ee99-233">印表機 \_ 狀態 \_ 紙 \_ 紙</span><span class="sxs-lookup"><span data-stu-id="4ee99-233">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="4ee99-234">印表機中的紙張已卡住</span><span class="sxs-lookup"><span data-stu-id="4ee99-234">Paper is jammed in the printer</span></span>                                   |
| <span data-ttu-id="4ee99-235">印表機 \_ 狀態 \_ 紙張 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="4ee99-235">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="4ee99-236">印表機紙張用完。</span><span class="sxs-lookup"><span data-stu-id="4ee99-236">The printer is out of paper.</span></span>                                     |
| <span data-ttu-id="4ee99-237">印表機 \_ 狀態 \_ 紙張 \_ 問題</span><span class="sxs-lookup"><span data-stu-id="4ee99-237">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="4ee99-238">印表機有紙張問題。</span><span class="sxs-lookup"><span data-stu-id="4ee99-238">The printer has a paper problem.</span></span>                                 |
| <span data-ttu-id="4ee99-239">印表機 \_ 狀態已 \_ 暫停</span><span class="sxs-lookup"><span data-stu-id="4ee99-239">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="4ee99-240">印表機已暫停。</span><span class="sxs-lookup"><span data-stu-id="4ee99-240">The printer is paused.</span></span>                                           |
| <span data-ttu-id="4ee99-241">印表機 \_ 狀態 \_ 暫止 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="4ee99-241">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="4ee99-242">正在刪除印表機。</span><span class="sxs-lookup"><span data-stu-id="4ee99-242">The printer is being deleted.</span></span>                                    |
| <span data-ttu-id="4ee99-243">印表機 \_ 狀態 \_ \_ 省電</span><span class="sxs-lookup"><span data-stu-id="4ee99-243">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="4ee99-244">印表機處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="4ee99-244">The printer is in power save mode.</span></span>                               |
| <span data-ttu-id="4ee99-245">印表機 \_ 狀態 \_ 列印</span><span class="sxs-lookup"><span data-stu-id="4ee99-245">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="4ee99-246">印表機正在列印。</span><span class="sxs-lookup"><span data-stu-id="4ee99-246">The printer is printing.</span></span>                                         |
| <span data-ttu-id="4ee99-247">印表機 \_ 狀態 \_ 處理</span><span class="sxs-lookup"><span data-stu-id="4ee99-247">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="4ee99-248">印表機正在處理列印工作。</span><span class="sxs-lookup"><span data-stu-id="4ee99-248">The printer is processing a print job.</span></span>                           |
| <span data-ttu-id="4ee99-249">印表機 \_ 狀態 \_ 伺服器 \_ 不明</span><span class="sxs-lookup"><span data-stu-id="4ee99-249">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="4ee99-250">印表機狀態不明。</span><span class="sxs-lookup"><span data-stu-id="4ee99-250">The printer status is unknown.</span></span>                                   |
| <span data-ttu-id="4ee99-251">印表機 \_ 狀態 \_ 墨粉 \_ 低</span><span class="sxs-lookup"><span data-stu-id="4ee99-251">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="4ee99-252">印表機碳粉不足。</span><span class="sxs-lookup"><span data-stu-id="4ee99-252">The printer is low on toner.</span></span>                                     |
| <span data-ttu-id="4ee99-253">印表機 \_ 狀態 \_ 使用者 \_ 介入</span><span class="sxs-lookup"><span data-stu-id="4ee99-253">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="4ee99-254">印表機有錯誤，需要使用者進行一些動作。</span><span class="sxs-lookup"><span data-stu-id="4ee99-254">The printer has an error that requires the user to do something.</span></span> |
| <span data-ttu-id="4ee99-255">印表機 \_ 狀態 \_ 等候中</span><span class="sxs-lookup"><span data-stu-id="4ee99-255">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="4ee99-256">印表機正在等候。</span><span class="sxs-lookup"><span data-stu-id="4ee99-256">The printer is waiting.</span></span>                                          |
| <span data-ttu-id="4ee99-257">印表機 \_ 狀態 \_ 預熱 \_</span><span class="sxs-lookup"><span data-stu-id="4ee99-257">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="4ee99-258">印表機準備中。</span><span class="sxs-lookup"><span data-stu-id="4ee99-258">The printer is warming up.</span></span>                                       |



 

</dd> <dt>

<span data-ttu-id="4ee99-259">**cJobs**</span><span class="sxs-lookup"><span data-stu-id="4ee99-259">**cJobs**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-260">已排入印表機佇列的列印工作數目。</span><span class="sxs-lookup"><span data-stu-id="4ee99-260">The number of print jobs that have been queued for the printer.</span></span>

</dd> <dt>

<span data-ttu-id="4ee99-261">**AveragePPM**</span><span class="sxs-lookup"><span data-stu-id="4ee99-261">**AveragePPM**</span></span>
</dt> <dd>

<span data-ttu-id="4ee99-262">印表機上每分鐘列印的平均頁數。</span><span class="sxs-lookup"><span data-stu-id="4ee99-262">The average number of pages per minute that have been printed on the printer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ee99-263">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ee99-263">Requirements</span></span>



| <span data-ttu-id="4ee99-264">需求</span><span class="sxs-lookup"><span data-stu-id="4ee99-264">Requirement</span></span> | <span data-ttu-id="4ee99-265">值</span><span class="sxs-lookup"><span data-stu-id="4ee99-265">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee99-266">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ee99-266">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee99-267">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ee99-267">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4ee99-268">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ee99-268">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee99-269">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ee99-269">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4ee99-270">標頭</span><span class="sxs-lookup"><span data-stu-id="4ee99-270">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ee99-271"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4ee99-271"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4ee99-272">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4ee99-272">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4ee99-273">**\_ 印表機 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 2a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4ee99-273">**\_PRINTER\_INFO\_2W** (Unicode) and **\_PRINTER\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="4ee99-274">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ee99-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee99-275">列印</span><span class="sxs-lookup"><span data-stu-id="4ee99-275">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4ee99-276">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="4ee99-276">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4ee99-277">**版**</span><span class="sxs-lookup"><span data-stu-id="4ee99-277">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="4ee99-278">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="4ee99-278">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="4ee99-279">**印表機 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4ee99-279">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="4ee99-280">**印表機 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4ee99-280">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="4ee99-281">**印表機 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4ee99-281">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="4ee99-282">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="4ee99-282">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

