---
description: GetPrinterData 函式會抓取指定印表機或列印伺服器的設定資料。
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: 'GetPrinterData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996844"
---
# <a name="getprinterdata-function"></a><span data-ttu-id="16580-103">GetPrinterData 函式</span><span class="sxs-lookup"><span data-stu-id="16580-103">GetPrinterData function</span></span>

<span data-ttu-id="16580-104">**GetPrinterData** 函式會抓取指定印表機或列印伺服器的設定資料。</span><span class="sxs-lookup"><span data-stu-id="16580-104">The **GetPrinterData** function retrieves configuration data for the specified printer or print server.</span></span>

<span data-ttu-id="16580-105">在 Windows 2000 和更新版本的 Windows 中，呼叫 **GetPrinterData** 相當於呼叫 [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) ，並將 *PKeyName* 參數設定為 "PrinterDriverData"。</span><span class="sxs-lookup"><span data-stu-id="16580-105">In Windows 2000 and later versions of Windows, calling **GetPrinterData** is equivalent to calling [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="16580-106">語法</span><span class="sxs-lookup"><span data-stu-id="16580-106">Syntax</span></span>


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="16580-107">參數</span><span class="sxs-lookup"><span data-stu-id="16580-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16580-108">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16580-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16580-109">由函式抓取設定資料之印表機或列印伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="16580-109">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="16580-110">使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="16580-110">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="16580-111">*pValueName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16580-111">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16580-112">以 null 結束的字串指標，可識別要取出的資料。</span><span class="sxs-lookup"><span data-stu-id="16580-112">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="16580-113">針對印表機，此字串是登錄中印表機 "PrinterDriverData" 機碼下的登錄值名稱。</span><span class="sxs-lookup"><span data-stu-id="16580-113">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="16580-114">針對列印伺服器，這個字串是下列 [備註] 區段中所列的其中一個預先定義的字串。</span><span class="sxs-lookup"><span data-stu-id="16580-114">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="16580-115">*pType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16580-115">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16580-116">變數的指標，此變數會接收表示在 *.pdata* 中取出之資料類型的值。</span><span class="sxs-lookup"><span data-stu-id="16580-116">A pointer to a variable that receives a value that indicates the type of data retrieved in *pData*.</span></span> <span data-ttu-id="16580-117">函數會傳回儲存資料的 [**SetPrinterData**](setprinterdata.md) 或 [**SetPrinterDataEx**](setprinterdataex.md) 呼叫中指定的型別。</span><span class="sxs-lookup"><span data-stu-id="16580-117">The function returns the type specified in the [**SetPrinterData**](setprinterdata.md) or [**SetPrinterDataEx**](setprinterdataex.md) call that stored the data.</span></span> <span data-ttu-id="16580-118">如果您不需要資料類型，請將此參數設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="16580-118">Set this parameter to **NULL** if you don't need the data type.</span></span>

</dd> <dt>

<span data-ttu-id="16580-119">*.pdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16580-119">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16580-120">接收設定資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="16580-120">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="16580-121">*nSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16580-121">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16580-122">*.Pdata* 指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="16580-122">The size, in bytes, of the buffer that *pData* points to.</span></span>

</dd> <dt>

<span data-ttu-id="16580-123">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16580-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16580-124">變數的指標，此變數會接收設定資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="16580-124">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="16580-125">如果 *nSize* 所指定的緩衝區大小太小，則函式會傳回 **錯誤的 \_ \_ 資料**，而 *pcbNeeded* 會指出所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="16580-125">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16580-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="16580-126">Return value</span></span>

<span data-ttu-id="16580-127">如果函式成功，則傳回值為「 **錯誤 \_ 成功**」。</span><span class="sxs-lookup"><span data-stu-id="16580-127">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="16580-128">如果函式失敗，則傳回值會是錯誤值。</span><span class="sxs-lookup"><span data-stu-id="16580-128">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16580-129">備註</span><span class="sxs-lookup"><span data-stu-id="16580-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="16580-130">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="16580-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="16580-131">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="16580-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="16580-132">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="16580-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="16580-133">**GetPrinterData** 會抓取 [**SetPrinterDataEx**](setprinterdataex.md) 或 [**SetPrinterData**](setprinterdata.md) 函數所設定的印表機設定資料。</span><span class="sxs-lookup"><span data-stu-id="16580-133">**GetPrinterData** retrieves printer configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) or [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="16580-134">**GetPrinterData** 可能會觸發對 [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85))的 Windows 呼叫，這可能會寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="16580-134">**GetPrinterData** might trigger a Windows call to [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), which might write to the registry.</span></span> <span data-ttu-id="16580-135">如果有的話，就會發生副作用，例如，如果在網路上共用印表機，則會在用戶端中觸發更新或升級印表機事件識別碼20。</span><span class="sxs-lookup"><span data-stu-id="16580-135">If it does, side effects can occur, such as triggering an update or upgrade printer event ID 20 in the client, if the printer is shared in a network.</span></span>

<span data-ttu-id="16580-136">如果 *hPrinter* 是列印伺服器的控制碼， *pValueName* 可以指定下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="16580-136">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="16580-137">值</span><span class="sxs-lookup"><span data-stu-id="16580-137">Value</span></span>                                                               | <span data-ttu-id="16580-138">註解</span><span class="sxs-lookup"><span data-stu-id="16580-138">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16580-139">**SPLREG \_ 允許 \_ 使用者 \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="16580-139">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="16580-140">Windows XP Service Pack 2 (SP2) 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-140">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="16580-141">Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-141">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="16580-142">**SPLREG \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="16580-142">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-143">**SPLREG \_ 嗶聲 \_ 已啟用**</span><span class="sxs-lookup"><span data-stu-id="16580-143">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-144">**SPLREG \_ 預設多工 \_ 緩衝處理 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="16580-144">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-145">**SPLREG \_ DNS \_ 電腦 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="16580-145">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-146">**\_存在 SPLREG DS \_**</span><span class="sxs-lookup"><span data-stu-id="16580-146">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="16580-147">在成功傳回時，如果電腦位於 DS 網域， *.pdata* 會包含0x0001，否則為0。</span><span class="sxs-lookup"><span data-stu-id="16580-147">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="16580-148">**\_ \_ \_ 為 \_ 使用者提供 SPLREG DS**</span><span class="sxs-lookup"><span data-stu-id="16580-148">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="16580-149">在成功傳回時，如果使用者登入 DS 網域， *.pdata* 會包含0x0001，否則為0。</span><span class="sxs-lookup"><span data-stu-id="16580-149">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="16580-150">**SPLREG \_ 事件 \_ 記錄檔**</span><span class="sxs-lookup"><span data-stu-id="16580-150">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-151">**SPLREG \_ 主要 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="16580-151">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-152">**SPLREG \_ 次要 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="16580-152">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-153">**SPLREG \_ NET \_ 快顯視窗**</span><span class="sxs-lookup"><span data-stu-id="16580-153">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="16580-154">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="16580-154">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="16580-155">**SPLREG \_ NET \_ POPUP \_ 至 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="16580-155">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="16580-156">在成功傳回時，如果工作通知應該傳送至用戶端電腦， *.pdata* 會包含 1; 如果要將工作通知傳送給使用者，則為0。</span><span class="sxs-lookup"><span data-stu-id="16580-156">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="16580-157">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="16580-157">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="16580-158">**SPLREG \_ OS \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="16580-158">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="16580-159">Windows XP 及更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-159">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="16580-160">**SPLREG \_ OS \_ VERSIONEX**</span><span class="sxs-lookup"><span data-stu-id="16580-160">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-161">**SPLREG \_ 埠 \_ 執行緒 \_ 優先順序 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="16580-161">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-162">**SPLREG \_ 埠 \_ 執行緒 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="16580-162">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-163">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="16580-163">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="16580-164">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-164">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="16580-165">**\_回收前的 SPLREG 列印 \_ 驅動程式 \_ 隔離 \_ 時間 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="16580-165">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="16580-166">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-166">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="16580-167">**SPLREG \_ 列印 \_ 驅動 \_ 程式 \_ \_ \_ 在回收前隔離的最大物件 \_**</span><span class="sxs-lookup"><span data-stu-id="16580-167">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="16580-168">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-168">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="16580-169">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 空閒 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="16580-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="16580-170">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="16580-171">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 執行 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="16580-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="16580-172">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="16580-173">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離覆 \_ 寫 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="16580-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="16580-174">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="16580-175">**SPLREG \_ 遠端 \_ 傳真**</span><span class="sxs-lookup"><span data-stu-id="16580-175">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="16580-176">在成功傳回時，如果傳真服務支援遠端用戶端， *.pdata* 會包含0x0001，否則為0。</span><span class="sxs-lookup"><span data-stu-id="16580-176">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="16580-177">**SPLREG \_ 重試 \_ 快顯視窗**</span><span class="sxs-lookup"><span data-stu-id="16580-177">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="16580-178">在成功傳回時，如果伺服器設定為所有作業的 [重試] 快顯視窗， *.pdata* 會包含 1; 如果伺服器不會針對所有作業重試快顯視窗，則為0。</span><span class="sxs-lookup"><span data-stu-id="16580-178">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="16580-179">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="16580-179">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="16580-180">**SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="16580-180">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-181">**SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="16580-181">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="16580-182">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="16580-182">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="16580-183">Windows Server 2003 和更新版本</span><span class="sxs-lookup"><span data-stu-id="16580-183">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="16580-184">下列 *pValueName* 值指出發生錯誤時的集區列印行為。</span><span class="sxs-lookup"><span data-stu-id="16580-184">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="16580-185">值</span><span class="sxs-lookup"><span data-stu-id="16580-185">Value</span></span>                                       | <span data-ttu-id="16580-186">註解</span><span class="sxs-lookup"><span data-stu-id="16580-186">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16580-187">**\_集區 \_ 上的 SPLREG 重新開機作業 \_ \_ \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="16580-187">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="16580-188">*.Pdata* 的值表示在發生錯誤之後，于另一個埠上重新開機作業的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="16580-188">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="16580-189">這項設定會 **\_ \_ \_ 在 \_ \_ 已啟用集區的 SPLREG 重新開機作業** 時使用。</span><span class="sxs-lookup"><span data-stu-id="16580-189">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="16580-190">**\_ \_ \_ \_ 已啟用集區上的 SPLREG 重新開機作業 \_**</span><span class="sxs-lookup"><span data-stu-id="16580-190">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="16580-191">*.Pdata* 中的非零值表示已啟用 **集區 \_ \_ \_ \_ \_ 錯誤的 SPLREG 重新開機作業**。</span><span class="sxs-lookup"><span data-stu-id="16580-191">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="16580-192">在 **\_ 集區 \_ \_ \_ \_ 錯誤的 SPLREG 重新開機作業** 中指定的時間是最短時間。</span><span class="sxs-lookup"><span data-stu-id="16580-192">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="16580-193">實際的時間可能會比較長，取決於下列埠監視器設定，這些設定是此登錄機碼下的登錄值：</span><span class="sxs-lookup"><span data-stu-id="16580-193">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="16580-194">**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ monitor \\ < *MonitorName* > \\ 埠**</span><span class="sxs-lookup"><span data-stu-id="16580-194">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="16580-195">呼叫 [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) 函數來查詢這些值。</span><span class="sxs-lookup"><span data-stu-id="16580-195">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="16580-196">埠監視器設定</span><span class="sxs-lookup"><span data-stu-id="16580-196">Port monitor setting</span></span>     | <span data-ttu-id="16580-197">資料類型</span><span class="sxs-lookup"><span data-stu-id="16580-197">Data type</span></span>      | <span data-ttu-id="16580-198">意義</span><span class="sxs-lookup"><span data-stu-id="16580-198">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16580-199">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="16580-199">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="16580-200">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="16580-200">**REG\_DWORD**</span></span> | <span data-ttu-id="16580-201">如果非零值，可讓埠監視器以埠狀態更新多工緩衝處理器。</span><span class="sxs-lookup"><span data-stu-id="16580-201">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="16580-202">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="16580-202">**StatusUpdateInterval**</span></span> | <span data-ttu-id="16580-203">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="16580-203">**REG\_DWORD**</span></span> | <span data-ttu-id="16580-204">指定埠監視器以埠狀態更新多工緩衝處理器時的間隔（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="16580-204">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="16580-205">在 Windows 7 和更新版本的 Windows 中，預設會在用戶端上轉譯傳送至列印伺服器的列印工作。</span><span class="sxs-lookup"><span data-stu-id="16580-205">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="16580-206">下列值會設定列印工作的用戶端轉譯，如果您在 *pValueName* 中設定下列值，就可以讀取這些值。</span><span class="sxs-lookup"><span data-stu-id="16580-206">The following values configure client-side rendering of a print jobs and can be read if you set the following values in *pValueName*.</span></span>



| <span data-ttu-id="16580-207">設定</span><span class="sxs-lookup"><span data-stu-id="16580-207">Setting</span></span>                      | <span data-ttu-id="16580-208">資料類型</span><span class="sxs-lookup"><span data-stu-id="16580-208">Data type</span></span>      | <span data-ttu-id="16580-209">描述</span><span class="sxs-lookup"><span data-stu-id="16580-209">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16580-210">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="16580-210">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="16580-211">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="16580-211">**REG\_DWORD**</span></span> | <span data-ttu-id="16580-212">值為0，或如果此值不存在於登錄中，則會啟用列印工作的預設用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="16580-212">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="16580-213">值為1時，會停用列印工作的用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="16580-213">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="16580-214">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="16580-214">**ForceClientSideRendering**</span></span> | <span data-ttu-id="16580-215">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="16580-215">**REG\_DWORD**</span></span> | <span data-ttu-id="16580-216">值為0，或如果此值不存在於登錄中，則會在用戶端上呈現列印工作。</span><span class="sxs-lookup"><span data-stu-id="16580-216">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="16580-217">如果無法在用戶端上呈現列印工作，則會在伺服器上轉譯。</span><span class="sxs-lookup"><span data-stu-id="16580-217">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="16580-218">如果無法在伺服器上轉譯列印工作，它將會失敗。</span><span class="sxs-lookup"><span data-stu-id="16580-218">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="16580-219">值為1時，會在用戶端上呈現列印工作。</span><span class="sxs-lookup"><span data-stu-id="16580-219">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="16580-220">如果無法在用戶端上呈現列印工作，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="16580-220">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16580-221">規格需求</span><span class="sxs-lookup"><span data-stu-id="16580-221">Requirements</span></span>



| <span data-ttu-id="16580-222">需求</span><span class="sxs-lookup"><span data-stu-id="16580-222">Requirement</span></span> | <span data-ttu-id="16580-223">值</span><span class="sxs-lookup"><span data-stu-id="16580-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16580-224">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16580-224">Minimum supported client</span></span><br/> | <span data-ttu-id="16580-225">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16580-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="16580-226">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16580-226">Minimum supported server</span></span><br/> | <span data-ttu-id="16580-227">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16580-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="16580-228">標頭</span><span class="sxs-lookup"><span data-stu-id="16580-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="16580-229"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="16580-229"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="16580-230">程式庫</span><span class="sxs-lookup"><span data-stu-id="16580-230">Library</span></span><br/>                  | <dl> <span data-ttu-id="16580-231"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16580-231"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="16580-232">DLL</span><span class="sxs-lookup"><span data-stu-id="16580-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16580-233"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="16580-233"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="16580-234">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="16580-234">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="16580-235">**GetPrinterDataW** (Unicode) 和 **GetPrinterDataA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="16580-235">**GetPrinterDataW** (Unicode) and **GetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="16580-236">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16580-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16580-237">列印</span><span class="sxs-lookup"><span data-stu-id="16580-237">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="16580-238">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="16580-238">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="16580-239">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="16580-239">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="16580-240">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="16580-240">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="16580-241">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="16580-241">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="16580-242">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="16580-242">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="16580-243">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="16580-243">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="16580-244">**PRINTPROCESSOR \_ CAPS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="16580-244">**PRINTPROCESSOR\_CAPS\_1**</span></span>](printprocessor-caps-1.md)
</dt> </dl>

 

