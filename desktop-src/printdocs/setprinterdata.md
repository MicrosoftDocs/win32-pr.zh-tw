---
description: SetPrinterData 函數會設定印表機或列印伺服器的設定資料。
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: 'SetPrinterData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849107"
---
# <a name="setprinterdata-function"></a><span data-ttu-id="4d58a-103">SetPrinterData 函式</span><span class="sxs-lookup"><span data-stu-id="4d58a-103">SetPrinterData function</span></span>

<span data-ttu-id="4d58a-104">**SetPrinterData** 函數會設定印表機或列印伺服器的設定資料。</span><span class="sxs-lookup"><span data-stu-id="4d58a-104">The **SetPrinterData** function sets the configuration data for a printer or print server.</span></span>

<span data-ttu-id="4d58a-105">若要指定用來儲存資料的登錄機碼，請呼叫 [**SetPrinterDataEx**](setprinterdataex.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="4d58a-105">To specify the registry key under which to store the data, call the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span> <span data-ttu-id="4d58a-106">呼叫 **SetPrinterData** 相當於呼叫 **SetPrinterDataEx** 函數，並將 *PKeyName* 參數設定為 "PrinterDriverData"。</span><span class="sxs-lookup"><span data-stu-id="4d58a-106">Calling **SetPrinterData** is equivalent to calling the **SetPrinterDataEx** function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="4d58a-107">語法</span><span class="sxs-lookup"><span data-stu-id="4d58a-107">Syntax</span></span>


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="4d58a-108">參數</span><span class="sxs-lookup"><span data-stu-id="4d58a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d58a-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d58a-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d58a-110">此函式會設定設定資料之印表機或列印伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4d58a-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="4d58a-111">使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="4d58a-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4d58a-112">*pValueName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d58a-112">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d58a-113">以 null 結束的字串指標，可識別要設定的資料。</span><span class="sxs-lookup"><span data-stu-id="4d58a-113">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="4d58a-114">針對印表機，此字串是登錄中印表機 "PrinterDriverData" 機碼下的登錄值名稱。</span><span class="sxs-lookup"><span data-stu-id="4d58a-114">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="4d58a-115">針對列印伺服器，這個字串是下列 [備註] 區段中所列的其中一個預先定義的字串。</span><span class="sxs-lookup"><span data-stu-id="4d58a-115">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="4d58a-116">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d58a-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d58a-117">表示 *.pdata* 參數所指向之資料類型的程式碼。</span><span class="sxs-lookup"><span data-stu-id="4d58a-117">A code that indicates the type of data that the *pData* parameter points to.</span></span> <span data-ttu-id="4d58a-118">如需可能的類型代碼清單，請參閱登錄 [數值型別](/windows/desktop/SysInfo/registry-value-types)。</span><span class="sxs-lookup"><span data-stu-id="4d58a-118">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="4d58a-119">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d58a-119">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d58a-120">包含印表機設定資料之位元組陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="4d58a-120">A pointer to an array of bytes that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="4d58a-121">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d58a-121">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d58a-122">陣列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4d58a-122">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d58a-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d58a-123">Return value</span></span>

<span data-ttu-id="4d58a-124">如果函式成功，則傳回值為「 **錯誤 \_ 成功**」。</span><span class="sxs-lookup"><span data-stu-id="4d58a-124">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="4d58a-125">如果函式失敗，則傳回值會是錯誤值。</span><span class="sxs-lookup"><span data-stu-id="4d58a-125">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d58a-126">備註</span><span class="sxs-lookup"><span data-stu-id="4d58a-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4d58a-127">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="4d58a-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4d58a-128">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="4d58a-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4d58a-129">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="4d58a-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4d58a-130">若要取出印表機的現有設定資料，請呼叫 [**GetPrinterDataEx**](getprinterdataex.md) 或 [**GetPrinterData**](getprinterdata.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="4d58a-130">To retrieve existing configuration data for a printer, call the [**GetPrinterDataEx**](getprinterdataex.md) or [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="4d58a-131">如果 *hPrinter* 是列印伺服器的控制碼， *pValueName* 可以指定下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="4d58a-131">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="4d58a-132">值</span><span class="sxs-lookup"><span data-stu-id="4d58a-132">Value</span></span>                                                               | <span data-ttu-id="4d58a-133">註解</span><span class="sxs-lookup"><span data-stu-id="4d58a-133">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d58a-134">**SPLREG \_ 允許 \_ 使用者 \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="4d58a-134">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="4d58a-135">Windows XP Service Pack 2 (SP2) 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-135">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="4d58a-136">Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-136">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="4d58a-137">**SPLREG \_ 嗶聲 \_ 已啟用**</span><span class="sxs-lookup"><span data-stu-id="4d58a-137">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d58a-138">**SPLREG \_ 預設多工 \_ 緩衝處理 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="4d58a-138">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d58a-139">**SPLREG \_ 事件 \_ 記錄檔**</span><span class="sxs-lookup"><span data-stu-id="4d58a-139">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d58a-140">**SPLREG \_ NET \_ 快顯視窗**</span><span class="sxs-lookup"><span data-stu-id="4d58a-140">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="4d58a-141">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="4d58a-141">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="4d58a-142">**SPLREG \_ 埠 \_ 執行緒 \_ 優先順序 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="4d58a-142">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d58a-143">**SPLREG \_ 埠 \_ 執行緒 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="4d58a-143">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d58a-144">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="4d58a-144">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="4d58a-145">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-145">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4d58a-146">**\_回收前的 SPLREG 列印 \_ 驅動程式 \_ 隔離 \_ 時間 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d58a-146">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="4d58a-147">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-147">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4d58a-148">**SPLREG \_ 列印 \_ 驅動 \_ 程式 \_ \_ \_ 在回收前隔離的最大物件 \_**</span><span class="sxs-lookup"><span data-stu-id="4d58a-148">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="4d58a-149">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-149">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4d58a-150">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 空閒 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="4d58a-150">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="4d58a-151">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-151">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4d58a-152">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 執行 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="4d58a-152">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="4d58a-153">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-153">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4d58a-154">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離覆 \_ 寫 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="4d58a-154">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="4d58a-155">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-155">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4d58a-156">**SPLREG \_ 重試 \_ 快顯視窗**</span><span class="sxs-lookup"><span data-stu-id="4d58a-156">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="4d58a-157">在成功傳回時，如果伺服器設定為所有作業的 [重試] 快顯視窗， *.pdata* 會包含 1; 如果伺服器不會針對所有作業重試快顯視窗，則為0。</span><span class="sxs-lookup"><span data-stu-id="4d58a-157">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="4d58a-158">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="4d58a-158">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="4d58a-159">**SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="4d58a-159">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d58a-160">**SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="4d58a-160">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d58a-161">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="4d58a-161">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="4d58a-162">Windows Server 2003 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58a-162">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="4d58a-163">下列 *pValueName* 值會決定發生錯誤時的集區列印行為。</span><span class="sxs-lookup"><span data-stu-id="4d58a-163">The following values of *pValueName* determine the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="4d58a-164">值</span><span class="sxs-lookup"><span data-stu-id="4d58a-164">Value</span></span>                                       | <span data-ttu-id="4d58a-165">註解</span><span class="sxs-lookup"><span data-stu-id="4d58a-165">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d58a-166">**\_集區 \_ 上的 SPLREG 重新開機作業 \_ \_ \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="4d58a-166">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="4d58a-167">*.Pdata* 的值表示在發生錯誤之後，于另一個埠上重新開機作業的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4d58a-167">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="4d58a-168">這項設定會 **\_ \_ \_ 在 \_ \_ 已啟用集區的 SPLREG 重新開機作業** 時使用。</span><span class="sxs-lookup"><span data-stu-id="4d58a-168">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="4d58a-169">**\_ \_ \_ \_ 已啟用集區上的 SPLREG 重新開機作業 \_**</span><span class="sxs-lookup"><span data-stu-id="4d58a-169">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="4d58a-170">*.Pdata* 中的非零值表示已啟用 **集區 \_ \_ \_ \_ \_ 錯誤的 SPLREG 重新開機作業**。</span><span class="sxs-lookup"><span data-stu-id="4d58a-170">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="4d58a-171">在 **\_ 集區 \_ \_ \_ \_ 錯誤的 SPLREG 重新開機作業** 中指定的時間是最短時間。</span><span class="sxs-lookup"><span data-stu-id="4d58a-171">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="4d58a-172">實際的時間可能會比較長，取決於下列埠監視器設定，這些設定是此登錄機碼下的登錄值：</span><span class="sxs-lookup"><span data-stu-id="4d58a-172">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="4d58a-173">**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ monitor \\ < *MonitorName* > \\ 埠**</span><span class="sxs-lookup"><span data-stu-id="4d58a-173">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="4d58a-174">呼叫 [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) 函數來設定這些值。</span><span class="sxs-lookup"><span data-stu-id="4d58a-174">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="4d58a-175">埠監視器設定</span><span class="sxs-lookup"><span data-stu-id="4d58a-175">Port monitor setting</span></span>     | <span data-ttu-id="4d58a-176">資料類型</span><span class="sxs-lookup"><span data-stu-id="4d58a-176">Data type</span></span>      | <span data-ttu-id="4d58a-177">意義</span><span class="sxs-lookup"><span data-stu-id="4d58a-177">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d58a-178">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="4d58a-178">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="4d58a-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4d58a-179">**REG\_DWORD**</span></span> | <span data-ttu-id="4d58a-180">如果非零值，可讓埠監視器以埠狀態更新多工緩衝處理器。</span><span class="sxs-lookup"><span data-stu-id="4d58a-180">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="4d58a-181">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="4d58a-181">**StatusUpdateInterval**</span></span> | <span data-ttu-id="4d58a-182">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4d58a-182">**REG\_DWORD**</span></span> | <span data-ttu-id="4d58a-183">指定埠監視器以埠狀態更新多工緩衝處理器時的間隔（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="4d58a-183">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="4d58a-184">在 Windows 7 和更新版本的 Windows 中，預設會在用戶端上轉譯傳送至列印伺服器的列印工作。</span><span class="sxs-lookup"><span data-stu-id="4d58a-184">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="4d58a-185">您可以藉由在 *pValueName* 中設定下列值，為每一部印表機設定用戶端的列印工作轉譯。</span><span class="sxs-lookup"><span data-stu-id="4d58a-185">Client-side rendering of a print jobs can be configured for each printer by setting the following values in *pValueName*.</span></span>



| <span data-ttu-id="4d58a-186">設定</span><span class="sxs-lookup"><span data-stu-id="4d58a-186">Setting</span></span>                      | <span data-ttu-id="4d58a-187">資料類型</span><span class="sxs-lookup"><span data-stu-id="4d58a-187">Data type</span></span>      | <span data-ttu-id="4d58a-188">描述</span><span class="sxs-lookup"><span data-stu-id="4d58a-188">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d58a-189">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="4d58a-189">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="4d58a-190">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4d58a-190">**REG\_DWORD**</span></span> | <span data-ttu-id="4d58a-191">值為0，或如果此值不存在於登錄中，則會啟用列印工作的預設用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="4d58a-191">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="4d58a-192">值為1時，會停用列印工作的用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="4d58a-192">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="4d58a-193">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="4d58a-193">**ForceClientSideRendering**</span></span> | <span data-ttu-id="4d58a-194">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4d58a-194">**REG\_DWORD**</span></span> | <span data-ttu-id="4d58a-195">值為0，或如果此值不存在於登錄中，則會在用戶端上呈現列印工作。</span><span class="sxs-lookup"><span data-stu-id="4d58a-195">A value of 0, or if this value is not present in the registry, causes the print jobs to be rendered on the client.</span></span> <span data-ttu-id="4d58a-196">如果無法在用戶端上呈現列印工作，則會在伺服器上轉譯。</span><span class="sxs-lookup"><span data-stu-id="4d58a-196">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="4d58a-197">如果無法在伺服器上轉譯列印工作，它將會失敗。</span><span class="sxs-lookup"><span data-stu-id="4d58a-197">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="4d58a-198">值為1時，會在用戶端上呈現列印工作。</span><span class="sxs-lookup"><span data-stu-id="4d58a-198">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="4d58a-199">如果無法在用戶端上呈現列印工作，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="4d58a-199">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4d58a-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d58a-200">Requirements</span></span>



| <span data-ttu-id="4d58a-201">需求</span><span class="sxs-lookup"><span data-stu-id="4d58a-201">Requirement</span></span> | <span data-ttu-id="4d58a-202">值</span><span class="sxs-lookup"><span data-stu-id="4d58a-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d58a-203">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d58a-203">Minimum supported client</span></span><br/> | <span data-ttu-id="4d58a-204">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d58a-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4d58a-205">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d58a-205">Minimum supported server</span></span><br/> | <span data-ttu-id="4d58a-206">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d58a-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4d58a-207">標頭</span><span class="sxs-lookup"><span data-stu-id="4d58a-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d58a-208"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4d58a-208"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4d58a-209">程式庫</span><span class="sxs-lookup"><span data-stu-id="4d58a-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d58a-210"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d58a-210"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4d58a-211">DLL</span><span class="sxs-lookup"><span data-stu-id="4d58a-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d58a-212"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="4d58a-212"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4d58a-213">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4d58a-213">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4d58a-214">**SetPrinterDataW** (Unicode) 和 **SetPrinterDataA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4d58a-214">**SetPrinterDataW** (Unicode) and **SetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="4d58a-215">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d58a-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d58a-216">列印</span><span class="sxs-lookup"><span data-stu-id="4d58a-216">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4d58a-217">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="4d58a-217">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4d58a-218">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="4d58a-218">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="4d58a-219">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="4d58a-219">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="4d58a-220">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="4d58a-220">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="4d58a-221">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4d58a-221">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="4d58a-222">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="4d58a-222">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

