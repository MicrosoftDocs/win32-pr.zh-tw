---
description: 在設定部分印表機選項時，抓取列印子系統中指定之印表機、列印伺服器或其他類型之控制碼的控制碼。
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: 'OpenPrinter2 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849752"
---
# <a name="openprinter2-function"></a><span data-ttu-id="36e92-103">OpenPrinter2 函式</span><span class="sxs-lookup"><span data-stu-id="36e92-103">OpenPrinter2 function</span></span>

<span data-ttu-id="36e92-104">在設定部分印表機選項時，抓取列印子系統中指定之印表機、列印伺服器或其他類型之控制碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36e92-104">Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="36e92-105">語法</span><span class="sxs-lookup"><span data-stu-id="36e92-105">Syntax</span></span>


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a><span data-ttu-id="36e92-106">參數</span><span class="sxs-lookup"><span data-stu-id="36e92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36e92-107">*pPrinterName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36e92-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36e92-108">常數以 null 終止的字串指標，指定印表機或列印伺服器的名稱、印表機物件、XcvMonitor 或 XcvPort。</span><span class="sxs-lookup"><span data-stu-id="36e92-108">A pointer to a constant null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="36e92-109">若為印表機物件，請使用： PrinterName、Job xxxx。</span><span class="sxs-lookup"><span data-stu-id="36e92-109">For a printer object, use: PrinterName,Job xxxx.</span></span> <span data-ttu-id="36e92-110">若為 XcvMonitor，請使用： ServerName，XcvMonitor MonitorName。</span><span class="sxs-lookup"><span data-stu-id="36e92-110">For an XcvMonitor, use: ServerName,XcvMonitor MonitorName.</span></span> <span data-ttu-id="36e92-111">若為 XcvPort，請使用： ServerName，XcvPort PortName。</span><span class="sxs-lookup"><span data-stu-id="36e92-111">For an XcvPort, use: ServerName,XcvPort PortName.</span></span>

<span data-ttu-id="36e92-112">**Windows Vista：** 如果是 **Null**，則表示本機列印伺服器。</span><span class="sxs-lookup"><span data-stu-id="36e92-112">**Windows Vista:** If **NULL**, it indicates the local print server.</span></span>

</dd> <dt>

<span data-ttu-id="36e92-113">*phPrinter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="36e92-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36e92-114">變數的指標，此變數會接收開啟的印表機或列印伺服器物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36e92-114">A pointer to a variable that receives a handle to the open printer or print server object.</span></span>

</dd> <dt>

<span data-ttu-id="36e92-115">*pDefault* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36e92-115">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36e92-116">[**印表機 \_ 預設**](printer-defaults.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="36e92-116">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="36e92-117">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="36e92-117">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="36e92-118">*pOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36e92-118">*pOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36e92-119">[**印表機 \_ 選項**](printer-options.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="36e92-119">A pointer to a [**PRINTER\_OPTIONS**](printer-options.md) structure.</span></span> <span data-ttu-id="36e92-120">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="36e92-120">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36e92-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="36e92-121">Return value</span></span>

<span data-ttu-id="36e92-122">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="36e92-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="36e92-123">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="36e92-123">If the function fails, the return value is zero.</span></span> <span data-ttu-id="36e92-124">如需擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="36e92-124">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="36e92-125">備註</span><span class="sxs-lookup"><span data-stu-id="36e92-125">Remarks</span></span>

<span data-ttu-id="36e92-126">請勿在 [**DllMain**](/windows/desktop/Dlls/dllmain)中呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="36e92-126">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="36e92-127">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="36e92-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="36e92-128">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="36e92-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="36e92-129">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="36e92-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="36e92-130">此函式的 ANSI 版本不會實作為函式，並傳回 \_ 不支援的錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36e92-130">The ANSI version of this function is not implemented and returns ERROR\_NOT\_SUPPORTED.</span></span>

<span data-ttu-id="36e92-131">*PDefault* 參數可讓您指定用來列印 [**StartDocPrinter**](startdocprinter.md)函數所提交檔的資料類型和裝置模式值。</span><span class="sxs-lookup"><span data-stu-id="36e92-131">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="36e92-132">不過，您可以在檔啟動後使用 [**SetJob**](setjob.md) 函式來覆寫這些值。</span><span class="sxs-lookup"><span data-stu-id="36e92-132">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="36e92-133">您可以呼叫 **OpenPrinter2** 函數來開啟列印伺服器的控制碼，或判斷列印伺服器的用戶端存取許可權。</span><span class="sxs-lookup"><span data-stu-id="36e92-133">You can call the **OpenPrinter2** function to open a handle to a print server or to determine client access rights to a print server.</span></span> <span data-ttu-id="36e92-134">若要這樣做，請在 *pPrinterName* 參數中指定列印伺服器的名稱，將 [**印表機 \_ 預設**](printer-defaults.md)結構的 **PDatatype** 和 **PDevMode** 成員設為 **Null**，並設定 **DesiredAccess** 成員以指定伺服器存取遮罩值，例如 [伺服器 \_ 所有存取] \_ 。</span><span class="sxs-lookup"><span data-stu-id="36e92-134">To do this, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="36e92-135">當您完成控制碼時，請將它傳遞至 [**ClosePrinter**](closeprinter.md) 函式來關閉它。</span><span class="sxs-lookup"><span data-stu-id="36e92-135">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="36e92-136">使用 [**印表機 \_ 預設**](printer-defaults.md)結構的 **DesiredAccess** 成員來指定所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="36e92-136">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the necessary access rights.</span></span> <span data-ttu-id="36e92-137">存取權限可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="36e92-137">The access rights can be one of the following.</span></span>



| <span data-ttu-id="36e92-138">所需的存取值</span><span class="sxs-lookup"><span data-stu-id="36e92-138">Desired Access value</span></span>                        | <span data-ttu-id="36e92-139">意義</span><span class="sxs-lookup"><span data-stu-id="36e92-139">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36e92-140">印表機 \_ 存取 \_ 管理</span><span class="sxs-lookup"><span data-stu-id="36e92-140">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="36e92-141">執行管理工作，例如 [**SetPrinter**](setprinter.md)所提供的工作。</span><span class="sxs-lookup"><span data-stu-id="36e92-141">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="36e92-142">印表機 \_ 存取 \_ 使用</span><span class="sxs-lookup"><span data-stu-id="36e92-142">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="36e92-143">執行基本列印工作。</span><span class="sxs-lookup"><span data-stu-id="36e92-143">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="36e92-144">印表機 \_ 所有 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="36e92-144">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="36e92-145">執行所有管理工作和基本列印工作（同步處理除外）。</span><span class="sxs-lookup"><span data-stu-id="36e92-145">To perform all administrative tasks and basic printing operations except SYNCHRONIZE.</span></span> <span data-ttu-id="36e92-146">請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="36e92-146">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                         |
| <span data-ttu-id="36e92-147">印表機 \_ 存取 \_ 管理 \_ 受限</span><span class="sxs-lookup"><span data-stu-id="36e92-147">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="36e92-148">執行管理工作，例如 [**SetPrinter**](setprinter.md) 和 [**SetPrinterData**](setprinterdata.md)所提供的工作。</span><span class="sxs-lookup"><span data-stu-id="36e92-148">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="36e92-149">從 Windows 8.1 開始，可以使用這個值。</span><span class="sxs-lookup"><span data-stu-id="36e92-149">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="36e92-150">一般安全性值，例如寫入 \_ DAC</span><span class="sxs-lookup"><span data-stu-id="36e92-150">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="36e92-151">允許特定的控制存取權限。</span><span class="sxs-lookup"><span data-stu-id="36e92-151">To allow specific control access rights.</span></span> <span data-ttu-id="36e92-152">請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="36e92-152">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="36e92-153">如果使用者沒有許可權可使用所需的存取權開啟指定的印表機或列印伺服器，則 **OpenPrinter2** 呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回拒絕存取的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="36e92-153">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter2** call will fail, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="36e92-154">當 *pPrinterName* 是本機印表機時， **OpenPrinter2** 會忽略 [**印表機 \_ 選項**](printer-options.md)結構指向使用 *pOptions* 的所有 **dwFlags** 值，但印表機 \_ 選項 \_ 用戶端 \_ 變更除外。</span><span class="sxs-lookup"><span data-stu-id="36e92-154">When *pPrinterName* is a local printer, then **OpenPrinter2** ignores all values of the **dwFlags** that the [**PRINTER\_OPTIONS**](printer-options.md) structure pointed to using *pOptions*, except PRINTER\_OPTION\_CLIENT\_CHANGE.</span></span> <span data-ttu-id="36e92-155">如果傳遞後者，則 **OpenPrinter2** 會傳回 \_ 拒絕存取錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36e92-155">If the latter is passed, then **OpenPrinter2** will return ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="36e92-156">因此，開啟本機印表機時， **OpenPrinter2** 不會比 [**OpenPrinter**](openprinter.md)更具優勢。</span><span class="sxs-lookup"><span data-stu-id="36e92-156">Accordingly, when opening a local printer, **OpenPrinter2** provides no advantage over [**OpenPrinter**](openprinter.md).</span></span>

<span data-ttu-id="36e92-157">**Windows Vista：\*\*\*\*OpenPrinter2** 傳回的印表機資料是從本機快取中取出，除非 *POptions* 所參考 [**印表機 \_ 選項**](printer-options.md)結構的 **dwFlags** 欄位中未設定 [**印表機] \_ \_ \_ 選項**。</span><span class="sxs-lookup"><span data-stu-id="36e92-157">**Windows Vista:** The printer data returned by **OpenPrinter2** is retrieved from a local cache unless the **PRINTER\_OPTION\_NO\_CACHE** flag is set in the **dwFlags** field of the [**PRINTER\_OPTIONS**](printer-options.md) structure referenced by *pOptions*.</span></span>

## <a name="examples"></a><span data-ttu-id="36e92-158">範例</span><span class="sxs-lookup"><span data-stu-id="36e92-158">Examples</span></span>

<span data-ttu-id="36e92-159">在此範例中 ，當印表機 \_ 存取 \_ 管理 \_ 限制傳遞到 [**印表機 \_ 預設**](printer-defaults.md)結構，且使用者沒有適當的許可權時，OpenPrinter2 就會失敗。</span><span class="sxs-lookup"><span data-stu-id="36e92-159">In this example, **OpenPrinter2** fails when PRINTER\_ACCESS\_MANAGE\_LIMITED is passed to the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure, and the user does not have the appropriate permission.</span></span>


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



<span data-ttu-id="36e92-160">如需示範如何使用此函式的範例程式，請參閱 [如何：使用 GDI 列印 API 進行列印](how-to--print-using-the-gdi-print-api.md)。</span><span class="sxs-lookup"><span data-stu-id="36e92-160">For a sample program that shows how to use this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36e92-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="36e92-161">Requirements</span></span>



| <span data-ttu-id="36e92-162">需求</span><span class="sxs-lookup"><span data-stu-id="36e92-162">Requirement</span></span> | <span data-ttu-id="36e92-163">值</span><span class="sxs-lookup"><span data-stu-id="36e92-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36e92-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36e92-164">Minimum supported client</span></span><br/> | <span data-ttu-id="36e92-165">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36e92-165">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="36e92-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36e92-166">Minimum supported server</span></span><br/> | <span data-ttu-id="36e92-167">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36e92-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="36e92-168">標頭</span><span class="sxs-lookup"><span data-stu-id="36e92-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="36e92-169"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="36e92-169"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="36e92-170">程式庫</span><span class="sxs-lookup"><span data-stu-id="36e92-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="36e92-171"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="36e92-171"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="36e92-172">DLL</span><span class="sxs-lookup"><span data-stu-id="36e92-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36e92-173"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36e92-173"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="36e92-174">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="36e92-174">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="36e92-175">**OpenPrinter2W** (Unicode) 和 **OpenPrinter2A** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="36e92-175">**OpenPrinter2W** (Unicode) and **OpenPrinter2A** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="36e92-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36e92-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e92-177">列印</span><span class="sxs-lookup"><span data-stu-id="36e92-177">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="36e92-178">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="36e92-178">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="36e92-179">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="36e92-179">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="36e92-180">**印表機 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="36e92-180">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="36e92-181">**印表機 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="36e92-181">**PRINTER\_OPTIONS**</span></span>](printer-options.md)
</dt> <dt>

[<span data-ttu-id="36e92-182">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="36e92-182">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="36e92-183">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="36e92-183">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="36e92-184">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="36e92-184">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="36e92-185">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="36e92-185">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

