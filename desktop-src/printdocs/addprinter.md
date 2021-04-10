---
description: Interactivesession.addprinter 函式會將印表機新增至指定伺服器支援的印表機清單。
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: 'Interactivesession.addprinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192610"
---
# <a name="addprinter-function"></a><span data-ttu-id="64abf-103">Interactivesession.addprinter 函式</span><span class="sxs-lookup"><span data-stu-id="64abf-103">AddPrinter function</span></span>

<span data-ttu-id="64abf-104">**Interactivesession.addprinter** 函式會將印表機新增至指定伺服器支援的印表機清單。</span><span class="sxs-lookup"><span data-stu-id="64abf-104">The **AddPrinter** function adds a printer to the list of supported printers for a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="64abf-105">語法</span><span class="sxs-lookup"><span data-stu-id="64abf-105">Syntax</span></span>


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="64abf-106">參數</span><span class="sxs-lookup"><span data-stu-id="64abf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64abf-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64abf-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64abf-108">以 null 結束的字串指標，指定應該安裝印表機之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="64abf-108">A pointer to a null-terminated string that specifies the name of the server on which the printer should be installed.</span></span> <span data-ttu-id="64abf-109">如果這個字串為 **Null**，則印表機會安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="64abf-109">If this string is **NULL**, the printer is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="64abf-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64abf-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64abf-111">*PPrinter* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="64abf-111">The version of the structure to which *pPrinter* points.</span></span> <span data-ttu-id="64abf-112">此值必須是2。</span><span class="sxs-lookup"><span data-stu-id="64abf-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="64abf-113">*pPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64abf-113">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64abf-114">[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構的指標，其中包含印表機的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="64abf-114">A pointer to a [**PRINTER\_INFO\_2**](printer-info-2.md) structure that contains information about the printer.</span></span> <span data-ttu-id="64abf-115">在呼叫 **interactivesession.addprinter** 之前，您必須為此結構的 **pPrinterName**、 **pPortName**、 **pDriverName** 和 **pPrintProcessor** 成員指定非 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="64abf-115">You must specify non-**NULL** values for the **pPrinterName**, **pPortName**, **pDriverName**, and **pPrintProcessor** members of this structure before calling **AddPrinter**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64abf-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="64abf-116">Return value</span></span>

<span data-ttu-id="64abf-117">如果函式成功，則傳回值會是控制碼 (不會) 至新的印表機物件的執行緒安全。</span><span class="sxs-lookup"><span data-stu-id="64abf-117">If the function succeeds, the return value is a handle (not thread safe) to a new printer object.</span></span> <span data-ttu-id="64abf-118">當您完成控制碼時，請將它傳遞至 [**ClosePrinter**](closeprinter.md) 函式來關閉它。</span><span class="sxs-lookup"><span data-stu-id="64abf-118">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="64abf-119">如果函式失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="64abf-119">If the function fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="64abf-120">備註</span><span class="sxs-lookup"><span data-stu-id="64abf-120">Remarks</span></span>

<span data-ttu-id="64abf-121">請勿在 [**DllMain**](/windows/desktop/Dlls/dllmain)中呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="64abf-121">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="64abf-122">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="64abf-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="64abf-123">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="64abf-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="64abf-124">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="64abf-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="64abf-125">呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="64abf-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="64abf-126">傳回的控制碼不是安全線程。</span><span class="sxs-lookup"><span data-stu-id="64abf-126">The returned handle is not thread safe.</span></span> <span data-ttu-id="64abf-127">如果呼叫端需要在多個執行緒上同時使用它，則必須使用 [同步](/windows/desktop/Sync/synchronization-functions)處理函式提供對印表機控制碼的自訂同步存取。</span><span class="sxs-lookup"><span data-stu-id="64abf-127">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="64abf-128">為了避免撰寫自訂程式碼，應用程式可以視需要開啟每個執行緒上的印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="64abf-128">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="64abf-129">以下是在呼叫 **interactivesession.addprinter** 函式之前可以設定的 [**印表機 \_ INFO \_ 2**](printer-info-2.md)結構的成員：</span><span class="sxs-lookup"><span data-stu-id="64abf-129">The following are the members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure that can be set before the **AddPrinter** function is called:</span></span>

-   <span data-ttu-id="64abf-130">**屬性**</span><span class="sxs-lookup"><span data-stu-id="64abf-130">**Attributes**</span></span>
-   <span data-ttu-id="64abf-131">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="64abf-131">**pPrintProcessor**</span></span>
-   <span data-ttu-id="64abf-132">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="64abf-132">**DefaultPriority**</span></span>
-   <span data-ttu-id="64abf-133">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="64abf-133">**Priority**</span></span>
-   <span data-ttu-id="64abf-134">**pComment**</span><span class="sxs-lookup"><span data-stu-id="64abf-134">**pComment**</span></span>
-   <span data-ttu-id="64abf-135">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="64abf-135">**pSecurityDescriptor**</span></span>
-   <span data-ttu-id="64abf-136">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="64abf-136">**pDatatype**</span></span>
-   <span data-ttu-id="64abf-137">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="64abf-137">**pSepFile**</span></span>
-   <span data-ttu-id="64abf-138">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="64abf-138">**pDevMode**</span></span>
-   <span data-ttu-id="64abf-139">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="64abf-139">**pShareName**</span></span>
-   <span data-ttu-id="64abf-140">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="64abf-140">**pLocation**</span></span>
-   <span data-ttu-id="64abf-141">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="64abf-141">**StartTime**</span></span>
-   <span data-ttu-id="64abf-142">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="64abf-142">**pParameters**</span></span>
-   <span data-ttu-id="64abf-143">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="64abf-143">**UntilTime**</span></span>

<span data-ttu-id="64abf-144">[**印表機 \_ INFO \_ 2**](printer-info-2.md)結構的 **Status**、 **CJobs** 和 **AveragePPM** 成員是保留供 [**GetPrinter**](getprinter.md)函式使用。</span><span class="sxs-lookup"><span data-stu-id="64abf-144">The **Status**, **cJobs**, and **AveragePPM** members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure are reserved for use by the [**GetPrinter**](getprinter.md) function.</span></span> <span data-ttu-id="64abf-145">它們必須在呼叫 **interactivesession.addprinter** 之前設定。</span><span class="sxs-lookup"><span data-stu-id="64abf-145">They must not be set before calling **AddPrinter**.</span></span>

<span data-ttu-id="64abf-146">如果 **pSecurityDescriptor** 為 **Null**，系統會將預設安全描述項指派給印表機。</span><span class="sxs-lookup"><span data-stu-id="64abf-146">If **pSecurityDescriptor** is **NULL**, the system assigns a default security descriptor to the printer.</span></span> <span data-ttu-id="64abf-147">預設安全描述項具有下列許可權。</span><span class="sxs-lookup"><span data-stu-id="64abf-147">The default security descriptor has the following permissions.</span></span>



| <span data-ttu-id="64abf-148">值</span><span class="sxs-lookup"><span data-stu-id="64abf-148">Value</span></span>                          | <span data-ttu-id="64abf-149">描述</span><span class="sxs-lookup"><span data-stu-id="64abf-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64abf-150">系統管理員與進階使用者</span><span class="sxs-lookup"><span data-stu-id="64abf-150">Administrators and Power Users</span></span> | <span data-ttu-id="64abf-151">完整控制列印佇列。</span><span class="sxs-lookup"><span data-stu-id="64abf-151">Full control on the print queue.</span></span> <span data-ttu-id="64abf-152">這表示這些群組的成員可以列印、管理佇列 (可以刪除佇列、變更佇列的任何設定，包括安全描述項) ，以及管理所有使用者的列印工作 (刪除、暫停、繼續、重新開機作業) 。請注意，Windows XP Professional 之前不存在 Power 使用者。</span><span class="sxs-lookup"><span data-stu-id="64abf-152">This means members of these groups can print, manage the queue (can delete the queue, change any setting of the queue, including the security descriptor), and manage the print jobs of all users (delete, pause, resume, restart jobs).Note that Power Users do not exist before Windows XP Professional.</span></span><br/> |
| <span data-ttu-id="64abf-153">建立者/擁有者</span><span class="sxs-lookup"><span data-stu-id="64abf-153">Creator/Owner</span></span>                  | <span data-ttu-id="64abf-154">可以管理自己的作業。</span><span class="sxs-lookup"><span data-stu-id="64abf-154">Can manage own jobs.</span></span> <span data-ttu-id="64abf-155">這表示提交工作的使用者可以管理 (刪除、暫停、繼續、重新開機) 自己的作業。</span><span class="sxs-lookup"><span data-stu-id="64abf-155">This means that user who submit jobs can manage (delete, pause, resume, restart) their own jobs.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="64abf-156">所有人</span><span class="sxs-lookup"><span data-stu-id="64abf-156">Everyone</span></span>                       | <span data-ttu-id="64abf-157">Execute 和 standard read control。</span><span class="sxs-lookup"><span data-stu-id="64abf-157">Execute and standard read control.</span></span> <span data-ttu-id="64abf-158">這表示 everyone 群組的成員可以列印和讀取列印佇列的屬性。</span><span class="sxs-lookup"><span data-stu-id="64abf-158">This means that members of the everyone group can print and read properties of the print queue.</span></span>                                                                                                                                                                                                                     |



 

<span data-ttu-id="64abf-159">應用程式使用 **interactivesession.addprinter** 函式建立印表機物件之後，必須使用 [**PrinterProperties**](printerproperties.md) 函式來指定與印表機物件相關聯之印表機驅動程式的正確設定。</span><span class="sxs-lookup"><span data-stu-id="64abf-159">After an application creates a printer object with the **AddPrinter** function, it must use the [**PrinterProperties**](printerproperties.md) function to specify the correct settings for the printer driver associated with the printer object.</span></span>

<span data-ttu-id="64abf-160">如果已經存在具有相同名稱的印表機物件， **interactivesession.addprinter** 函式會傳回錯誤，除非該物件標示為待刪除。</span><span class="sxs-lookup"><span data-stu-id="64abf-160">The **AddPrinter** function returns an error if a printer object with the same name already exists, unless that object is marked as pending deletion.</span></span> <span data-ttu-id="64abf-161">在此情況下，不會刪除現有的印表機，而且會使用 **interactivesession.addprinter** 建立參數來變更現有印表機設定 (如同應用程式已使用 [**SetPrinter**](setprinter.md) 函式) 。</span><span class="sxs-lookup"><span data-stu-id="64abf-161">In that case, the existing printer is not deleted, and the **AddPrinter** creation parameters are used to change the existing printer settings (as if the application had used the [**SetPrinter**](setprinter.md) function).</span></span>

<span data-ttu-id="64abf-162">您可以使用 [**EnumPrintProcessors**](enumprintprocessors.md) 函式來列舉安裝在伺服器上的列印處理器組。</span><span class="sxs-lookup"><span data-stu-id="64abf-162">Use the [**EnumPrintProcessors**](enumprintprocessors.md) function to enumerate the set of print processors installed on a server.</span></span> <span data-ttu-id="64abf-163">您可以使用 [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) 函式來列舉列印處理器所支援的一組資料類型。</span><span class="sxs-lookup"><span data-stu-id="64abf-163">Use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to enumerate the set of data types that a print processor supports.</span></span> <span data-ttu-id="64abf-164">使用 [**EnumPorts**](enumports.md) 函式來列舉可用的埠集合。</span><span class="sxs-lookup"><span data-stu-id="64abf-164">Use the [**EnumPorts**](enumports.md) function to enumerate the set of available ports.</span></span> <span data-ttu-id="64abf-165">使用 [**EnumPrinterDrivers**](enumprinterdrivers.md) 函式來列舉已安裝的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="64abf-165">Use the [**EnumPrinterDrivers**](enumprinterdrivers.md) function to enumerate the installed printer drivers.</span></span>

<span data-ttu-id="64abf-166">**Interactivesession.addprinter** 函式的呼叫端必須具有伺服器 \_ 存取權 \_ ，才能管理要在其上建立印表機的伺服器。</span><span class="sxs-lookup"><span data-stu-id="64abf-166">The caller of the **AddPrinter** function must have SERVER\_ACCESS\_ADMINISTER access to the server on which the printer is to be created.</span></span> <span data-ttu-id="64abf-167">此函式所傳回的控制碼會有 [印表機 \_ 所有 \_ 存取權限]，可用來執行印表機的系統管理操作。</span><span class="sxs-lookup"><span data-stu-id="64abf-167">The handle returned by the function will have PRINTER\_ALL\_ACCESS permission, and can be used to perform administrative operations on the printer.</span></span>

<span data-ttu-id="64abf-168">如果傳遞了 **DrvPrinterEvent** 函式的印表機 \_ 事件 \_ 旗標 \_ 沒有 \_ ui 旗標，則驅動程式不應在 **DrvPrinterEvent** 期間使用 ui 呼叫。</span><span class="sxs-lookup"><span data-stu-id="64abf-168">If the **DrvPrinterEvent** function is passed the PRINTER\_EVENT\_FLAG\_NO\_UI flag, the driver should not use a UI call during **DrvPrinterEvent**.</span></span> <span data-ttu-id="64abf-169">若要執行 UI 相關的工作，安裝程式應該使用印表機的 .inf 檔案中的 **VendorSetup** 專案，或針對隨插即用的裝置，安裝程式可以使用裝置特定的共同安裝程式。</span><span class="sxs-lookup"><span data-stu-id="64abf-169">To do UI-related jobs, the installer should either use the **VendorSetup** entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="64abf-170">如需有關 **VendorSetup** 的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組 (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="64abf-170">For more information about **VendorSetup**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="64abf-171">網際網路連線防火牆 (ICF) 預設會封鎖印表機埠，但是當您執行 **interactivesession.addprinter** 時，會啟用檔案和列印共用的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="64abf-171">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing is enabled when you run **AddPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="64abf-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="64abf-172">Requirements</span></span>



| <span data-ttu-id="64abf-173">需求</span><span class="sxs-lookup"><span data-stu-id="64abf-173">Requirement</span></span> | <span data-ttu-id="64abf-174">值</span><span class="sxs-lookup"><span data-stu-id="64abf-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64abf-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64abf-175">Minimum supported client</span></span><br/> | <span data-ttu-id="64abf-176">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64abf-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="64abf-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64abf-177">Minimum supported server</span></span><br/> | <span data-ttu-id="64abf-178">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64abf-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="64abf-179">標頭</span><span class="sxs-lookup"><span data-stu-id="64abf-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="64abf-180"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="64abf-180"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="64abf-181">程式庫</span><span class="sxs-lookup"><span data-stu-id="64abf-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="64abf-182"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="64abf-182"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="64abf-183">DLL</span><span class="sxs-lookup"><span data-stu-id="64abf-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64abf-184"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="64abf-184"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="64abf-185">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="64abf-185">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="64abf-186">**AddPrinterW** (Unicode) 和 **AddPrinterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="64abf-186">**AddPrinterW** (Unicode) and **AddPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="64abf-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64abf-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64abf-188">列印</span><span class="sxs-lookup"><span data-stu-id="64abf-188">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="64abf-189">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="64abf-189">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="64abf-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="64abf-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="64abf-191">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="64abf-191">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="64abf-192">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="64abf-192">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="64abf-193">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="64abf-193">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="64abf-194">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="64abf-194">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="64abf-195">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="64abf-195">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="64abf-196">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="64abf-196">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="64abf-197">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="64abf-197">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="64abf-198">**PrinterProperties**</span><span class="sxs-lookup"><span data-stu-id="64abf-198">**PrinterProperties**</span></span>](printerproperties.md)
</dt> <dt>

[<span data-ttu-id="64abf-199">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="64abf-199">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

