---
description: OpenPrinter 函式會抓取指定之印表機或列印伺服器或列印子系統中其他類型之控制碼的控制碼。
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: 'OpenPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969386"
---
# <a name="openprinter-function"></a><span data-ttu-id="985ba-103">OpenPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="985ba-103">OpenPrinter function</span></span>

<span data-ttu-id="985ba-104">**OpenPrinter** 函式會抓取指定之印表機或列印伺服器或列印子系統中其他類型之控制碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="985ba-104">The **OpenPrinter** function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="985ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="985ba-105">Syntax</span></span>


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="985ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="985ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="985ba-107">*pPrinterName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="985ba-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="985ba-108">以 null 結束的字串指標，指定印表機或列印伺服器的名稱、印表機物件、XcvMonitor 或 XcvPort。</span><span class="sxs-lookup"><span data-stu-id="985ba-108">A pointer to a null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="985ba-109">若為印表機物件，請使用： PrinterName、Job xxxx。</span><span class="sxs-lookup"><span data-stu-id="985ba-109">For a printer object use: PrinterName, Job xxxx.</span></span> <span data-ttu-id="985ba-110">若為 XcvMonitor，請使用： ServerName，XcvMonitor MonitorName。</span><span class="sxs-lookup"><span data-stu-id="985ba-110">For an XcvMonitor, use: ServerName, XcvMonitor MonitorName.</span></span> <span data-ttu-id="985ba-111">若為 XcvPort，請使用： ServerName，XcvPort PortName。</span><span class="sxs-lookup"><span data-stu-id="985ba-111">For an XcvPort, use: ServerName, XcvPort PortName.</span></span>

<span data-ttu-id="985ba-112">如果是 **Null**，則表示本機印表機伺服器。</span><span class="sxs-lookup"><span data-stu-id="985ba-112">If **NULL**, it indicates the local printer server.</span></span>

</dd> <dt>

<span data-ttu-id="985ba-113">*phPrinter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="985ba-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="985ba-114">變數的指標，此變數會接收控制碼 (不會) 開啟的印表機或列印伺服器物件的安全線程。</span><span class="sxs-lookup"><span data-stu-id="985ba-114">A pointer to a variable that receives a handle (not thread safe) to the open printer or print server object.</span></span>

<span data-ttu-id="985ba-115">*PhPrinter* 參數可以傳回 Xcv 控制碼，以搭配 XcvData 函式使用。</span><span class="sxs-lookup"><span data-stu-id="985ba-115">The *phPrinter* parameter can return an Xcv handle for use with the XcvData function.</span></span> <span data-ttu-id="985ba-116">如需 XcvData 的詳細資訊，請參閱 DDK。</span><span class="sxs-lookup"><span data-stu-id="985ba-116">For more information about XcvData, see the DDK.</span></span>

</dd> <dt>

<span data-ttu-id="985ba-117">*pDefault* \[在\]</span><span class="sxs-lookup"><span data-stu-id="985ba-117">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="985ba-118">[**印表機 \_ 預設**](printer-defaults.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="985ba-118">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="985ba-119">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="985ba-119">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="985ba-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="985ba-120">Return value</span></span>

<span data-ttu-id="985ba-121">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="985ba-121">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="985ba-122">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="985ba-122">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="985ba-123">備註</span><span class="sxs-lookup"><span data-stu-id="985ba-123">Remarks</span></span>

<span data-ttu-id="985ba-124">請勿在 [**DllMain**](/windows/desktop/Dlls/dllmain)中呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="985ba-124">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="985ba-125">針對遠端印表機的 **OpenPrinter** 呼叫所取得的控制碼，會透過「列印多工緩衝處理器」服務的本機快取來存取印表機。</span><span class="sxs-lookup"><span data-stu-id="985ba-125">A handle obtained for a remote printer by a call to **OpenPrinter** for a remote printer accesses the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="985ba-126">此快取不是即時精確。</span><span class="sxs-lookup"><span data-stu-id="985ba-126">This cache isn't real-time accurate.</span></span> <span data-ttu-id="985ba-127">若要取得準確的資料，請將 OpenPrinter 呼叫取代為 [**OpenPrinter2**](openprinter2.md) ，並將 pOptions 設定為印表機 \_ 選項 \_ NO \_ CACHE。</span><span class="sxs-lookup"><span data-stu-id="985ba-127">To obtain accurate data, replace the OpenPrinter call with [**OpenPrinter2**](openprinter2.md) with pOptions.dwFlags set to PRINTER\_OPTION\_NO\_CACHE.</span></span> <span data-ttu-id="985ba-128">請注意，只有 OpenPrinter2W 可正常運作。</span><span class="sxs-lookup"><span data-stu-id="985ba-128">Note that only OpenPrinter2W is functional.</span></span> <span data-ttu-id="985ba-129">函數會傳回使用其他列印 API 呼叫的印表機控制碼，並略過本機快取。</span><span class="sxs-lookup"><span data-stu-id="985ba-129">The function returns a printer handle that uses other Printing API calls and bypasses the local cache.</span></span> <span data-ttu-id="985ba-130">這個方法會在等候與遠端印表機的網路通訊時封鎖，所以它可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="985ba-130">This method blocks while waiting for network communication with the remote printer, so it might not return immediately.</span></span> <span data-ttu-id="985ba-131">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="985ba-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="985ba-132">從管理使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="985ba-132">Calling this function from a thread that manages user interface interaction might make the application appear unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="985ba-133">針對遠端印表機呼叫 **OpenPrinter** 所取得的控制碼，將會透過列印多工緩衝處理器服務中的本機快取來存取印表機。</span><span class="sxs-lookup"><span data-stu-id="985ba-133">A handle obtained by a call to **OpenPrinter** for a remote printer will access the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="985ba-134">這種快取的設計並不是即時精確。</span><span class="sxs-lookup"><span data-stu-id="985ba-134">This cache is, by design, not real time accurate.</span></span> <span data-ttu-id="985ba-135">如果您需要取得精確的資料，請將 **OpenPrinter** 呼叫取代為 [**OpenPrinter2**](openprinter2.md) ，並將 *pOptions* 設定為 [**印表機 \_ 選項 \_ NO \_ CACHE**](printer-options.md)。</span><span class="sxs-lookup"><span data-stu-id="985ba-135">If you need to obtain accurate data, replace the **OpenPrinter** call with [**OpenPrinter2**](openprinter2.md) with *pOptions.dwFlags* set to [**PRINTER\_OPTION\_NO\_CACHE**](printer-options.md).</span></span> <span data-ttu-id="985ba-136">請注意，只有 **OpenPrinter2W** 可正常運作。</span><span class="sxs-lookup"><span data-stu-id="985ba-136">Note that only **OpenPrinter2W** is functional.</span></span> <span data-ttu-id="985ba-137">如此一來，函式就會傳回印表機控制碼，讓其他的列印 API 呼叫略過本機快取。</span><span class="sxs-lookup"><span data-stu-id="985ba-137">Doing so the function returns a printer handle that makes other Printing API calls to bypass the local cache.</span></span> <span data-ttu-id="985ba-138">請注意，這種方法會在等候遠端印表機的往返網路通訊時封鎖，所以它可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="985ba-138">Note that this approach will block while waiting for the round-trip network communication to the remote printer, so it may not return immediately.</span></span> <span data-ttu-id="985ba-139">此函式傳回的速度取決於執行時間因素，例如網路狀態、列印伺服器設定，以及印表機驅動程式的執行因素。撰寫應用程式時，難以預測的因素。</span><span class="sxs-lookup"><span data-stu-id="985ba-139">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation - factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="985ba-140">因此，從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="985ba-140">Therefore calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="985ba-141">*PhPrinter* 所指向的控制碼不是安全線程。</span><span class="sxs-lookup"><span data-stu-id="985ba-141">The handle pointed to by *phPrinter* is not thread safe.</span></span> <span data-ttu-id="985ba-142">如果呼叫端需要在多個執行緒上同時使用它，則必須使用 [同步](/windows/desktop/Sync/synchronization-functions)處理函式提供對印表機控制碼的自訂同步存取。</span><span class="sxs-lookup"><span data-stu-id="985ba-142">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="985ba-143">為了避免撰寫自訂程式碼，應用程式可以視需要開啟每個執行緒上的印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="985ba-143">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="985ba-144">*PDefault* 參數可讓您指定用來列印 [**StartDocPrinter**](startdocprinter.md)函數所提交檔的資料類型和裝置模式值。</span><span class="sxs-lookup"><span data-stu-id="985ba-144">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="985ba-145">不過，您可以在檔啟動後使用 [**SetJob**](setjob.md) 函式來覆寫這些值。</span><span class="sxs-lookup"><span data-stu-id="985ba-145">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="985ba-146">當在 [**StartDocPrinter**](startdocprinter.md)呼叫的 *pDocInfo* 參數中傳遞的 [**DOC \_ INFO \_ 1**](doc-info-1.md)結構的 *pDatatype* 成員值為 "RAW" 時，不會使用 *PDefault* 參數的 [**印表機 \_ 預設**](printer-defaults.md)值結構中所定義的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)設定。</span><span class="sxs-lookup"><span data-stu-id="985ba-146">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) settings defined in the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure of the *pDefault* parameter are not used when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW".</span></span> <span data-ttu-id="985ba-147">當高階檔 (例如 Adobe PDF 或 Microsoft Word 檔案) 或其他印表機資料 (這類 PCL、PS 或 HPGL) 直接傳送至 *pDatatype* 設定為「原始」的印表機時，檔必須完整地以硬體理解的語言描述 **DEVMODE** 樣式的列印工作設定。</span><span class="sxs-lookup"><span data-stu-id="985ba-147">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer with *pDatatype* set to "RAW", the document must fully describe the **DEVMODE**-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="985ba-148">您可以呼叫 **OpenPrinter** 函數來開啟列印伺服器的控制碼，或判斷用戶端對列印伺服器的存取權限。</span><span class="sxs-lookup"><span data-stu-id="985ba-148">You can call the **OpenPrinter** function to open a handle to a print server or to determine the access rights that a client has to a print server.</span></span> <span data-ttu-id="985ba-149">若要這樣做，請在 *pPrinterName* 參數中指定列印伺服器的名稱，將 [**印表機 \_ 預設**](printer-defaults.md)結構的 **PDatatype** 和 **PDevMode** 成員設為 **Null**，並設定 **DesiredAccess** 成員以指定伺服器存取遮罩值，例如 [伺服器 \_ 所有存取] \_ 。</span><span class="sxs-lookup"><span data-stu-id="985ba-149">To do so, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="985ba-150">當您完成控制碼時，請將它傳遞至 [**ClosePrinter**](closeprinter.md) 函式來關閉它。</span><span class="sxs-lookup"><span data-stu-id="985ba-150">When you finish with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="985ba-151">使用 [**印表機 \_ 預設**](printer-defaults.md)結構的 **DesiredAccess** 成員，指定印表機所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="985ba-151">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the access rights that you need to the printer.</span></span> <span data-ttu-id="985ba-152">存取權限可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="985ba-152">The access rights can be one of the following.</span></span> <span data-ttu-id="985ba-153"> (如果 *pDefault* 為 **Null**，則存取權限會是印表機 \_ 存取 \_ 使用。 ) </span><span class="sxs-lookup"><span data-stu-id="985ba-153">(If *pDefault* is **NULL**, then the access rights are PRINTER\_ACCESS\_USE.)</span></span>



| <span data-ttu-id="985ba-154">所需的存取值</span><span class="sxs-lookup"><span data-stu-id="985ba-154">Desired Access value</span></span>                        | <span data-ttu-id="985ba-155">意義</span><span class="sxs-lookup"><span data-stu-id="985ba-155">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985ba-156">印表機 \_ 存取 \_ 管理</span><span class="sxs-lookup"><span data-stu-id="985ba-156">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="985ba-157">執行管理工作，例如 [**SetPrinter**](setprinter.md)所提供的工作。</span><span class="sxs-lookup"><span data-stu-id="985ba-157">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="985ba-158">印表機 \_ 存取 \_ 使用</span><span class="sxs-lookup"><span data-stu-id="985ba-158">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="985ba-159">執行基本列印工作。</span><span class="sxs-lookup"><span data-stu-id="985ba-159">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="985ba-160">印表機 \_ 所有 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="985ba-160">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="985ba-161">若要執行所有管理工作和基本列印工作，除了同步處理 (請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="985ba-161">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                     |
| <span data-ttu-id="985ba-162">印表機 \_ 存取 \_ 管理 \_ 受限</span><span class="sxs-lookup"><span data-stu-id="985ba-162">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="985ba-163">執行管理工作，例如 [**SetPrinter**](setprinter.md) 和 [**SetPrinterData**](setprinterdata.md)所提供的工作。</span><span class="sxs-lookup"><span data-stu-id="985ba-163">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="985ba-164">從 Windows 8.1 開始，可以使用這個值。</span><span class="sxs-lookup"><span data-stu-id="985ba-164">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="985ba-165">一般安全性值，例如寫入 \_ DAC</span><span class="sxs-lookup"><span data-stu-id="985ba-165">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="985ba-166">允許特定的控制存取權限。</span><span class="sxs-lookup"><span data-stu-id="985ba-166">To allow specific control access rights.</span></span> <span data-ttu-id="985ba-167">請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="985ba-167">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="985ba-168">如果使用者沒有許可權可使用所需的存取權開啟指定的印表機或列印伺服器，則 **OpenPrinter** 呼叫會失敗，並傳回值為零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回值 \_ 拒絕存取的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="985ba-168">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter** call will fail with a return value of zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

## <a name="examples"></a><span data-ttu-id="985ba-169">範例</span><span class="sxs-lookup"><span data-stu-id="985ba-169">Examples</span></span>

<span data-ttu-id="985ba-170">如需使用此函式的範例程式，請參閱 [如何：使用 GDI 列印 API 進行列印](how-to--print-using-the-gdi-print-api.md)。</span><span class="sxs-lookup"><span data-stu-id="985ba-170">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="985ba-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="985ba-171">Requirements</span></span>



| <span data-ttu-id="985ba-172">需求</span><span class="sxs-lookup"><span data-stu-id="985ba-172">Requirement</span></span> | <span data-ttu-id="985ba-173">值</span><span class="sxs-lookup"><span data-stu-id="985ba-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985ba-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="985ba-174">Minimum supported client</span></span><br/> | <span data-ttu-id="985ba-175">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="985ba-175">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="985ba-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="985ba-176">Minimum supported server</span></span><br/> | <span data-ttu-id="985ba-177">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="985ba-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="985ba-178">標頭</span><span class="sxs-lookup"><span data-stu-id="985ba-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="985ba-179"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="985ba-179"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="985ba-180">程式庫</span><span class="sxs-lookup"><span data-stu-id="985ba-180">Library</span></span><br/>                  | <dl> <span data-ttu-id="985ba-181"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="985ba-181"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="985ba-182">DLL</span><span class="sxs-lookup"><span data-stu-id="985ba-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="985ba-183"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="985ba-183"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="985ba-184">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="985ba-184">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="985ba-185">**OpenPrinterW** (Unicode) 和 **OpenPrinterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="985ba-185">**OpenPrinterW** (Unicode) and **OpenPrinterA** (ANSI)</span></span><br/>                                         |



## <a name="see-also"></a><span data-ttu-id="985ba-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="985ba-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985ba-187">列印</span><span class="sxs-lookup"><span data-stu-id="985ba-187">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="985ba-188">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="985ba-188">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="985ba-189">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="985ba-189">**WritePrinter**</span></span>](writeprinter.md)
</dt> <dt>

[<span data-ttu-id="985ba-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="985ba-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="985ba-191">**印表機 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="985ba-191">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="985ba-192">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="985ba-192">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="985ba-193">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="985ba-193">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="985ba-194">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="985ba-194">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

