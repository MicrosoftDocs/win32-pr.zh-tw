---
description: SetPrinterDataEx 函數會設定印表機或列印伺服器的設定資料。 此函數會將設定資料儲存在印表機登錄機碼下。
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: 'SetPrinterDataEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194583"
---
# <a name="setprinterdataex-function"></a><span data-ttu-id="7b330-104">SetPrinterDataEx 函式</span><span class="sxs-lookup"><span data-stu-id="7b330-104">SetPrinterDataEx function</span></span>

<span data-ttu-id="7b330-105">**SetPrinterDataEx** 函數會設定印表機或列印伺服器的設定資料。</span><span class="sxs-lookup"><span data-stu-id="7b330-105">The **SetPrinterDataEx** function sets the configuration data for a printer or print server.</span></span> <span data-ttu-id="7b330-106">此函數會將設定資料儲存在印表機的登錄機碼下。</span><span class="sxs-lookup"><span data-stu-id="7b330-106">The function stores the configuration data under the printer's registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b330-107">語法</span><span class="sxs-lookup"><span data-stu-id="7b330-107">Syntax</span></span>


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a><span data-ttu-id="7b330-108">參數</span><span class="sxs-lookup"><span data-stu-id="7b330-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b330-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b330-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b330-110">此函式會設定設定資料之印表機或列印伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7b330-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="7b330-111">使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="7b330-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="7b330-112">*pKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b330-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b330-113">以 null 結束的字串指標，指定包含要設定之值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7b330-113">A pointer to a null-terminated string that specifies the key containing the value to set.</span></span> <span data-ttu-id="7b330-114">如果指定的機碼或子機碼不存在，則函式會建立它們。</span><span class="sxs-lookup"><span data-stu-id="7b330-114">If the specified key or subkeys do not exist, the function creates them.</span></span>

<span data-ttu-id="7b330-115">若要儲存可在目錄服務 (DS) 中發佈的設定資料，請指定下列其中一個預先定義的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="7b330-115">To store configuration data that can be published in the directory service (DS), specify one of the following predefined registry keys.</span></span>



| <span data-ttu-id="7b330-116">值</span><span class="sxs-lookup"><span data-stu-id="7b330-116">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="7b330-117">意義</span><span class="sxs-lookup"><span data-stu-id="7b330-117">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <span data-ttu-id="7b330-118"><dt>**SPLDS_DRIVER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="7b330-118"><dt>**SPLDS_DRIVER_KEY**</dt></span></span> </dl>    | <span data-ttu-id="7b330-119">印表機驅動程式會使用此金鑰來儲存驅動程式屬性。</span><span class="sxs-lookup"><span data-stu-id="7b330-119">Printer drivers use this key to store driver properties.</span></span><br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <span data-ttu-id="7b330-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="7b330-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span></span> </dl> | <span data-ttu-id="7b330-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="7b330-121">Reserved.</span></span> <span data-ttu-id="7b330-122">僅供列印多工緩衝處理器用來儲存內部多工緩衝處理器屬性。</span><span class="sxs-lookup"><span data-stu-id="7b330-122">Used only by the print spooler to store internal spooler properties.</span></span><br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <span data-ttu-id="7b330-123"><dt>**SPLDS_USER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="7b330-123"><dt>**SPLDS_USER_KEY**</dt></span></span> </dl>          | <span data-ttu-id="7b330-124">應用程式會使用此金鑰來儲存印表機內容，例如印表機資產號碼。</span><span class="sxs-lookup"><span data-stu-id="7b330-124">Applications use this key to store printer properties such as printer asset numbers.</span></span><br/> |



 

<span data-ttu-id="7b330-125">只有當架構中有對應的屬性時，儲存在 SPLDS_USER_KEY 機碼下的值才會在目錄服務中發行。</span><span class="sxs-lookup"><span data-stu-id="7b330-125">Values that are stored under the SPLDS_USER_KEY key are published in the directory service only if there is a corresponding property in the schema.</span></span> <span data-ttu-id="7b330-126">網域系統管理員必須建立屬性（如果尚未存在）。</span><span class="sxs-lookup"><span data-stu-id="7b330-126">A domain administrator must create the property if it doesn't already exist.</span></span> <span data-ttu-id="7b330-127">若要在使用 **SetPrinterDataEx** 來加入或變更值之後發行使用者定義的屬性，請呼叫 [**SetPrinter**](setprinter.md) （ *Level* = 7），並將 [**PRINTER_INFO_7**](printer-info-7.md)的 **dwAction** 成員設為 **DSPRINT_UPDATE**。</span><span class="sxs-lookup"><span data-stu-id="7b330-127">To publish a user-defined property after you use **SetPrinterDataEx** to add or change a value, call [**SetPrinter**](setprinter.md) with *Level* = 7 and with the **dwAction** member of [**PRINTER_INFO_7**](printer-info-7.md) set to **DSPRINT_UPDATE**.</span></span>

<span data-ttu-id="7b330-128">您可以指定其他金鑰來儲存非 DS 設定資料。</span><span class="sxs-lookup"><span data-stu-id="7b330-128">You can specify other keys to store non-DS configuration data.</span></span> <span data-ttu-id="7b330-129">使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。</span><span class="sxs-lookup"><span data-stu-id="7b330-129">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="7b330-130">如果 *hPrinter* 是印表機的控制碼，而 *pKeyName* 為 **Null** 或空字串，則 **SetPrinterDataEx** 會傳回 **ERROR_INVALID_PARAMETER**。</span><span class="sxs-lookup"><span data-stu-id="7b330-130">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **SetPrinterDataEx** returns **ERROR_INVALID_PARAMETER**.</span></span>

<span data-ttu-id="7b330-131">如果 *hPrinter* 是列印伺服器的控制碼，則會忽略 *pKeyName* 。</span><span class="sxs-lookup"><span data-stu-id="7b330-131">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

<span data-ttu-id="7b330-132">請勿使用 **SPLDS_SPOOLER_KEY**。</span><span class="sxs-lookup"><span data-stu-id="7b330-132">Do not use **SPLDS_SPOOLER_KEY**.</span></span> <span data-ttu-id="7b330-133">若要變更多工緩衝處理器印表機屬性，請使用 *Level* = 2 的 [**SetPrinter**](setprinter.md) 。</span><span class="sxs-lookup"><span data-stu-id="7b330-133">To change the spooler printer properties, use [**SetPrinter**](setprinter.md) with *Level* = 2.</span></span>

</dd> <dt>

<span data-ttu-id="7b330-134">*pValueName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b330-134">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b330-135">以 null 結束的字串指標，可識別要設定的資料。</span><span class="sxs-lookup"><span data-stu-id="7b330-135">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="7b330-136">若為印表機，此字串會在 *pKeyName* 索引鍵下指定值的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b330-136">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="7b330-137">針對列印伺服器，這個字串是下列 [備註] 區段中所列的其中一個預先定義的字串。</span><span class="sxs-lookup"><span data-stu-id="7b330-137">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="7b330-138">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b330-138">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b330-139">表示 *.pdata* 參數所指向之資料類型的代碼。</span><span class="sxs-lookup"><span data-stu-id="7b330-139">A code indicating the type of data pointed to by the *pData* parameter.</span></span> <span data-ttu-id="7b330-140">如需可能的類型代碼清單，請參閱登錄 [數值型別](/windows/desktop/SysInfo/registry-value-types)。</span><span class="sxs-lookup"><span data-stu-id="7b330-140">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

<span data-ttu-id="7b330-141">如果 *pKeyName* 指定其中一個預先定義的目錄服務金鑰，則 *類型* 必須是 **REG_SZ**、 **REG_MULTI_SZ**、 **REG_DWORD** 或 **REG_BINARY**。</span><span class="sxs-lookup"><span data-stu-id="7b330-141">If *pKeyName* specifies one of the predefined directory service keys, *Type* must be **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD**, or **REG_BINARY**.</span></span> <span data-ttu-id="7b330-142">如果使用 **REG_BINARY** ， *cbData* 必須等於1，而目錄服務會將資料視為布林值。</span><span class="sxs-lookup"><span data-stu-id="7b330-142">If **REG_BINARY** is used, *cbData* must be equal to 1, and the directory service treats the data as a Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="7b330-143">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b330-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b330-144">包含印表機設定資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="7b330-144">A pointer to a buffer that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="7b330-145">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b330-145">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b330-146">陣列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7b330-146">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b330-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b330-147">Return value</span></span>

<span data-ttu-id="7b330-148">如果函式成功，則傳回值為 **ERROR_SUCCESS**。</span><span class="sxs-lookup"><span data-stu-id="7b330-148">If the function succeeds, the return value is **ERROR_SUCCESS**.</span></span>

<span data-ttu-id="7b330-149">如果函式失敗，則傳回值會是錯誤值。</span><span class="sxs-lookup"><span data-stu-id="7b330-149">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b330-150">備註</span><span class="sxs-lookup"><span data-stu-id="7b330-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7b330-151">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="7b330-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7b330-152">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="7b330-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7b330-153">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="7b330-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="7b330-154">若要取出印表機的現有設定資料或列印多工緩衝處理器，請呼叫 [**GetPrinterDataEx**](getprinterdataex.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="7b330-154">To retrieve existing configuration data for a printer or print spooler, call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

<span data-ttu-id="7b330-155">使用設定為 "PrinterDriverData" 的 *pKeyName* 參數呼叫 **SetPrinterDataEx** 相當於呼叫 [**SetPrinterData**](setprinterdata.md)函數。</span><span class="sxs-lookup"><span data-stu-id="7b330-155">Calling **SetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="7b330-156">如果 *hPrinter* 是列印伺服器的控制碼， *pValueName* 可以指定下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="7b330-156">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="7b330-157">值</span><span class="sxs-lookup"><span data-stu-id="7b330-157">Value</span></span>                                                               | <span data-ttu-id="7b330-158">註解</span><span class="sxs-lookup"><span data-stu-id="7b330-158">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b330-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="7b330-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span></span>                                | <span data-ttu-id="7b330-160">Windows XP Service Pack 2 (SP2) 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-160">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="7b330-161">Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-161">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="7b330-162">**SPLREG_BEEP_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="7b330-162">**SPLREG_BEEP_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="7b330-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span><span class="sxs-lookup"><span data-stu-id="7b330-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="7b330-164">**SPLREG_EVENT_LOG**</span><span class="sxs-lookup"><span data-stu-id="7b330-164">**SPLREG_EVENT_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="7b330-165">**SPLREG_NET_POPUP**</span><span class="sxs-lookup"><span data-stu-id="7b330-165">**SPLREG_NET_POPUP**</span></span>                                              | <span data-ttu-id="7b330-166">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="7b330-166">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="7b330-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7b330-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="7b330-168">**SPLREG_PORT_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="7b330-168">**SPLREG_PORT_THREAD_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="7b330-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span><span class="sxs-lookup"><span data-stu-id="7b330-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span></span>                        | <span data-ttu-id="7b330-170">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="7b330-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="7b330-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span></span>         | <span data-ttu-id="7b330-172">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="7b330-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="7b330-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span></span> | <span data-ttu-id="7b330-174">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="7b330-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="7b330-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span></span>                 | <span data-ttu-id="7b330-176">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="7b330-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span><span class="sxs-lookup"><span data-stu-id="7b330-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span></span>             | <span data-ttu-id="7b330-178">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="7b330-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span><span class="sxs-lookup"><span data-stu-id="7b330-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span></span>              | <span data-ttu-id="7b330-180">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="7b330-181">**SPLREG_RETRY_POPUP**</span><span class="sxs-lookup"><span data-stu-id="7b330-181">**SPLREG_RETRY_POPUP**</span></span>                                            | <span data-ttu-id="7b330-182">在成功傳回時，如果伺服器設定為所有作業的 [重試] 快顯視窗， *.pdata* 會包含 1; 如果伺服器不會針對所有作業重試快顯視窗，則為0。</span><span class="sxs-lookup"><span data-stu-id="7b330-182">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="7b330-183">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="7b330-183">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="7b330-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="7b330-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="7b330-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7b330-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="7b330-186">**SPLREG_WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="7b330-186">**SPLREG_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="7b330-187">Windows Server 2003 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7b330-187">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="7b330-188">當發生錯誤時，傳遞下列其中一個預先定義的值做為 *pValueName* 會設定集區列印行為。</span><span class="sxs-lookup"><span data-stu-id="7b330-188">Passing one of the following predefined values as *pValueName* sets the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="7b330-189">值</span><span class="sxs-lookup"><span data-stu-id="7b330-189">Value</span></span>                                       | <span data-ttu-id="7b330-190">註解</span><span class="sxs-lookup"><span data-stu-id="7b330-190">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b330-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span><span class="sxs-lookup"><span data-stu-id="7b330-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span></span>   | <span data-ttu-id="7b330-192">*.Pdata* 的值表示在發生錯誤之後，于另一個埠上重新開機作業的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7b330-192">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="7b330-193">這項設定會搭配 **SPLREG_RESTART_JOB_ON_POOL_ENABLED** 使用。</span><span class="sxs-lookup"><span data-stu-id="7b330-193">This setting is used with **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span></span><br/> |
| <span data-ttu-id="7b330-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="7b330-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span></span> | <span data-ttu-id="7b330-195">*.Pdata* 中的非零值表示已啟用 **SPLREG_RESTART_JOB_ON_POOL_ERROR** 。</span><span class="sxs-lookup"><span data-stu-id="7b330-195">A nonzero value in *pData* indicates that **SPLREG_RESTART_JOB_ON_POOL_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="7b330-196">**SPLREG_RESTART_JOB_ON_POOL_ERROR** 中指定的時間是最短的時間。</span><span class="sxs-lookup"><span data-stu-id="7b330-196">The time specified in **SPLREG_RESTART_JOB_ON_POOL_ERROR** is a minimum time.</span></span> <span data-ttu-id="7b330-197">實際的時間可能會比較長，取決於下列埠監視器設定，這些設定是此登錄機碼下的登錄值：</span><span class="sxs-lookup"><span data-stu-id="7b330-197">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="7b330-198">**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ monitor \\ < *MonitorName* > \\ 埠**</span><span class="sxs-lookup"><span data-stu-id="7b330-198">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="7b330-199">呼叫 [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) 函數來設定這些值。</span><span class="sxs-lookup"><span data-stu-id="7b330-199">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="7b330-200">埠監視器設定</span><span class="sxs-lookup"><span data-stu-id="7b330-200">Port monitor setting</span></span>     | <span data-ttu-id="7b330-201">資料類型</span><span class="sxs-lookup"><span data-stu-id="7b330-201">Data type</span></span>      | <span data-ttu-id="7b330-202">意義</span><span class="sxs-lookup"><span data-stu-id="7b330-202">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b330-203">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="7b330-203">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="7b330-204">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b330-204">**REG_DWORD**</span></span> | <span data-ttu-id="7b330-205">如果非零值，可讓埠監視器以埠狀態更新多工緩衝處理器。</span><span class="sxs-lookup"><span data-stu-id="7b330-205">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="7b330-206">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="7b330-206">**StatusUpdateInterval**</span></span> | <span data-ttu-id="7b330-207">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b330-207">**REG_DWORD**</span></span> | <span data-ttu-id="7b330-208">指定埠監視器以埠狀態更新多工緩衝處理器時的間隔（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="7b330-208">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="7b330-209">為了確保多工緩衝處理程式會將工作重新導向至集區中的下一個可用印表機 (當列印工作未在設定的時間) 內列印時，埠監視器必須支援 SNMP，且集區中的網路埠必須設定為「已啟用 SNMP 狀態」。</span><span class="sxs-lookup"><span data-stu-id="7b330-209">To ensure that the spooler redirects jobs to the next available printer in the pool (when the print job is not printed within the set time), the port monitor must support SNMP and the network ports in the pool must be configured as "SNMP status enabled."</span></span> <span data-ttu-id="7b330-210">支援 SNMP 的埠監視器是標準 TCP/IP 埠監視器。</span><span class="sxs-lookup"><span data-stu-id="7b330-210">The port monitor that supports SNMP is Standard TCP/IP port monitor.</span></span>

<span data-ttu-id="7b330-211">在 Windows 7 和更新版本的 Windows 中，預設會在用戶端上轉譯傳送至列印伺服器的列印工作。</span><span class="sxs-lookup"><span data-stu-id="7b330-211">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="7b330-212">您可以將 *pKeyName* 設定為 "PrinterDriverData"，並 *pValueName* 至下表中的設定值，來設定列印工作的用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="7b330-212">Client-side rendering of print jobs can be configured by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="7b330-213">設定</span><span class="sxs-lookup"><span data-stu-id="7b330-213">Setting</span></span>                      | <span data-ttu-id="7b330-214">資料類型</span><span class="sxs-lookup"><span data-stu-id="7b330-214">Data type</span></span>      | <span data-ttu-id="7b330-215">描述</span><span class="sxs-lookup"><span data-stu-id="7b330-215">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b330-216">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="7b330-216">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="7b330-217">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b330-217">**REG_DWORD**</span></span> | <span data-ttu-id="7b330-218">值為0，或如果此值不存在於登錄中，則會啟用列印工作的預設用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="7b330-218">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="7b330-219">值為1時，會停用列印工作的用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="7b330-219">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="7b330-220">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="7b330-220">**ForceClientSideRendering**</span></span> | <span data-ttu-id="7b330-221">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b330-221">**REG_DWORD**</span></span> | <span data-ttu-id="7b330-222">值為0，或如果此值不存在於登錄中，則會在用戶端上呈現列印工作。</span><span class="sxs-lookup"><span data-stu-id="7b330-222">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="7b330-223">如果無法在用戶端上呈現列印工作，則會在伺服器上轉譯。</span><span class="sxs-lookup"><span data-stu-id="7b330-223">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="7b330-224">如果無法在伺服器上轉譯列印工作，它將會失敗。</span><span class="sxs-lookup"><span data-stu-id="7b330-224">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="7b330-225">值為1時，會在用戶端上呈現列印工作。</span><span class="sxs-lookup"><span data-stu-id="7b330-225">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="7b330-226">如果無法在用戶端上呈現列印工作，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="7b330-226">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7b330-227">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b330-227">Requirements</span></span>



| <span data-ttu-id="7b330-228">需求</span><span class="sxs-lookup"><span data-stu-id="7b330-228">Requirement</span></span> | <span data-ttu-id="7b330-229">值</span><span class="sxs-lookup"><span data-stu-id="7b330-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b330-230">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b330-230">Minimum supported client</span></span><br/> | <span data-ttu-id="7b330-231">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b330-231">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7b330-232">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b330-232">Minimum supported server</span></span><br/> | <span data-ttu-id="7b330-233">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b330-233">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7b330-234">標頭</span><span class="sxs-lookup"><span data-stu-id="7b330-234">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b330-235"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7b330-235"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7b330-236">程式庫</span><span class="sxs-lookup"><span data-stu-id="7b330-236">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b330-237"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b330-237"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7b330-238">DLL</span><span class="sxs-lookup"><span data-stu-id="7b330-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b330-239"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="7b330-239"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7b330-240">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7b330-240">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7b330-241">**SetPrinterDataExW** (Unicode) 和 **SetPrinterDataExA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7b330-241">**SetPrinterDataExW** (Unicode) and **SetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="7b330-242">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b330-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b330-243">列印</span><span class="sxs-lookup"><span data-stu-id="7b330-243">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7b330-244">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="7b330-244">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7b330-245">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="7b330-245">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="7b330-246">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="7b330-246">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="7b330-247">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="7b330-247">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="7b330-248">**PRINTER_INFO_7**</span><span class="sxs-lookup"><span data-stu-id="7b330-248">**PRINTER_INFO_7**</span></span>](printer-info-7.md)
</dt> </dl>

 

