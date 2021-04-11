---
description: GetPrinterDataEx 函式會抓取指定印表機或列印伺服器的設定資料。
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: 'GetPrinterDataEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695083"
---
# <a name="getprinterdataex-function"></a><span data-ttu-id="8f5a1-103">GetPrinterDataEx 函式</span><span class="sxs-lookup"><span data-stu-id="8f5a1-103">GetPrinterDataEx function</span></span>

<span data-ttu-id="8f5a1-104">**GetPrinterDataEx** 函式會抓取指定印表機或列印伺服器的設定資料。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-104">The **GetPrinterDataEx** function retrieves configuration data for the specified printer or print server.</span></span> <span data-ttu-id="8f5a1-105">**GetPrinterDataEx** 可以取出 [**SetPrinterData**](setprinterdata.md) 函數所儲存的值。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-105">**GetPrinterDataEx** can retrieve values that the [**SetPrinterData**](setprinterdata.md) function stored.</span></span> <span data-ttu-id="8f5a1-106">此外， **GetPrinterDataEx** 可以取出 [**SetPrinterDataEx**](setprinterdataex.md) 函數儲存在指定索引鍵下的值。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-106">In addition, **GetPrinterDataEx** can retrieve values that the [**SetPrinterDataEx**](setprinterdataex.md) function stored under a specified key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f5a1-107">語法</span><span class="sxs-lookup"><span data-stu-id="8f5a1-107">Syntax</span></span>


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="8f5a1-108">參數</span><span class="sxs-lookup"><span data-stu-id="8f5a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f5a1-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a1-110">由函式抓取設定資料之印表機或列印伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-110">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="8f5a1-111">使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="8f5a1-112">*pKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a1-113">以 null 結束的字串指標，指定包含要抓取之值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-113">A pointer to a null-terminated string that specifies the key containing the value to be retrieved.</span></span> <span data-ttu-id="8f5a1-114">使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-114">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="8f5a1-115">如果 *hPrinter* 是印表機的控制碼，而 *pKeyName* 為 **Null** 或空字串，則 **GetPrinterDataEx** 會傳回 **錯誤 \_ 不正確 \_ 參數**。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-115">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **GetPrinterDataEx** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

<span data-ttu-id="8f5a1-116">如果 *hPrinter* 是列印伺服器的控制碼，則會忽略 *pKeyName* 。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-116">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="8f5a1-117">*pValueName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-117">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a1-118">以 null 結束的字串指標，可識別要取出的資料。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-118">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="8f5a1-119">若為印表機，此字串會在 *pKeyName* 索引鍵下指定值的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-119">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="8f5a1-120">針對列印伺服器，這個字串是下列 [備註] 區段中所列的其中一個預先定義的字串。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-120">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="8f5a1-121">*pType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-121">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a1-122">變數的指標，此變數會接收儲存在值中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-122">A pointer to a variable that receives the type of data stored in the value.</span></span> <span data-ttu-id="8f5a1-123">當儲存資料時，函數會傳回 [**SetPrinterDataEx**](setprinterdataex.md) 呼叫中指定的型別。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-123">The function returns the type specified in the [**SetPrinterDataEx**](setprinterdataex.md) call when the data was stored.</span></span> <span data-ttu-id="8f5a1-124">如果您不需要此資訊，這個參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-124">This parameter can be **NULL** if you don't need the information.</span></span> <span data-ttu-id="8f5a1-125">**GetPrinterDataEx** 會將 *pType* 當作 [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)函式呼叫的 *lpdwType* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-125">**GetPrinterDataEx** passes *pType* on as the *lpdwType* parameter of a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function call.</span></span>

</dd> <dt>

<span data-ttu-id="8f5a1-126">*.pdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-126">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a1-127">接收設定資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-127">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="8f5a1-128">*nSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-128">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a1-129">*.Pdata* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-129">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

</dd> <dt>

<span data-ttu-id="8f5a1-130">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-130">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a1-131">變數的指標，此變數會接收設定資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-131">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="8f5a1-132">如果 *nSize* 所指定的緩衝區大小太小，則函式會傳回 **錯誤的 \_ \_ 資料**，而 *pcbNeeded* 會指出所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-132">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f5a1-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f5a1-133">Return value</span></span>

<span data-ttu-id="8f5a1-134">如果函式成功，則傳回值為「 **錯誤 \_ 成功**」。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-134">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="8f5a1-135">如果函式失敗，則傳回值會是錯誤值。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-135">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f5a1-136">備註</span><span class="sxs-lookup"><span data-stu-id="8f5a1-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8f5a1-137">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8f5a1-138">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8f5a1-139">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8f5a1-140">**GetPrinterDataEx** 會抓取 [**SetPrinterDataEx**](setprinterdataex.md) 和 [**SetPrinterData**](setprinterdata.md) 函式所設定的印表機設定資料。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-140">**GetPrinterDataEx** retrieves printer-configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

<span data-ttu-id="8f5a1-141">使用設定為 "PrinterDriverData" 的 *pKeyName* 參數呼叫 **GetPrinterDataEx** 相當於呼叫 [**GetPrinterData**](getprinterdata.md)函數。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-141">Calling **GetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="8f5a1-142">如果 *hPrinter* 是列印伺服器的控制碼， *pValueName* 可以指定下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-142">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="8f5a1-143">值</span><span class="sxs-lookup"><span data-stu-id="8f5a1-143">Value</span></span>                                                               | <span data-ttu-id="8f5a1-144">註解</span><span class="sxs-lookup"><span data-stu-id="8f5a1-144">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5a1-145">**SPLREG \_ 允許 \_ 使用者 \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-145">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="8f5a1-146">Windows XP Service Pack 2 (SP2) 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-146">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="8f5a1-147">Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-147">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="8f5a1-148">**SPLREG \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-148">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-149">**SPLREG \_ 嗶聲 \_ 已啟用**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-149">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-150">**SPLREG \_ 預設多工 \_ 緩衝處理 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-150">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-151">**SPLREG \_ DNS \_ 電腦 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-151">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-152">**\_存在 SPLREG DS \_**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-152">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="8f5a1-153">在成功傳回時，如果電腦位於 DS 網域， *.pdata* 會包含0x0001，否則為0。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-153">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="8f5a1-154">**\_ \_ \_ 為 \_ 使用者提供 SPLREG DS**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-154">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="8f5a1-155">在成功傳回時，如果使用者登入 DS 網域， *.pdata* 會包含0x0001，否則為0。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-155">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="8f5a1-156">**SPLREG \_ 事件 \_ 記錄檔**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-156">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-157">**SPLREG \_ 主要 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-157">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-158">**SPLREG \_ 次要 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-158">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-159">**SPLREG \_ NET \_ 快顯視窗**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-159">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="8f5a1-160">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="8f5a1-160">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="8f5a1-161">**SPLREG \_ NET \_ POPUP \_ 至 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-161">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="8f5a1-162">在成功傳回時，如果工作通知應該傳送至用戶端電腦， *.pdata* 會包含 1; 如果要將工作通知傳送給使用者，則為0。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-162">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="8f5a1-163">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="8f5a1-163">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="8f5a1-164">**SPLREG \_ OS \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-164">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="8f5a1-165">Windows XP 及更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-165">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-166">**SPLREG \_ OS \_ VERSIONEX**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-166">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-167">**SPLREG \_ 埠 \_ 執行緒 \_ 優先順序 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-167">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-168">**SPLREG \_ 埠 \_ 執行緒 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-168">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-169">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="8f5a1-170">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8f5a1-171">**\_回收前的 SPLREG 列印 \_ 驅動程式 \_ 隔離 \_ 時間 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="8f5a1-172">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8f5a1-173">**SPLREG \_ 列印 \_ 驅動 \_ 程式 \_ \_ \_ 在回收前隔離的最大物件 \_**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="8f5a1-174">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8f5a1-175">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 空閒 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-175">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="8f5a1-176">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8f5a1-177">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 執行 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-177">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="8f5a1-178">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8f5a1-179">**SPLREG \_ 列印 \_ 驅動程式 \_ 隔離覆 \_ 寫 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-179">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="8f5a1-180">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8f5a1-181">**SPLREG \_ 遠端 \_ 傳真**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-181">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="8f5a1-182">在成功傳回時，如果傳真服務支援遠端用戶端， *.pdata* 會包含0x0001，否則為0。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-182">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="8f5a1-183">**SPLREG \_ 重試 \_ 快顯視窗**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-183">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="8f5a1-184">在成功傳回時，如果伺服器設定為所有作業的 [重試] 快顯視窗， *.pdata* 會包含 1; 如果伺服器不會針對所有作業重試快顯視窗，則為0。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-184">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="8f5a1-185">Windows Server 2003 和更新版本不支援</span><span class="sxs-lookup"><span data-stu-id="8f5a1-185">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="8f5a1-186">**SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-186">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-187">**SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-187">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8f5a1-188">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-188">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="8f5a1-189">Windows Server 2003 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8f5a1-189">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="8f5a1-190">下列 *pValueName* 值指出發生錯誤時的集區列印行為。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-190">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="8f5a1-191">值</span><span class="sxs-lookup"><span data-stu-id="8f5a1-191">Value</span></span>                                       | <span data-ttu-id="8f5a1-192">註解</span><span class="sxs-lookup"><span data-stu-id="8f5a1-192">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5a1-193">**\_集區 \_ 上的 SPLREG 重新開機作業 \_ \_ \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-193">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="8f5a1-194">*.Pdata* 的值表示在發生錯誤之後，于另一個埠上重新開機作業的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-194">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="8f5a1-195">這項設定會 **\_ \_ \_ 在 \_ \_ 已啟用集區的 SPLREG 重新開機作業** 時使用。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-195">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="8f5a1-196">**\_ \_ \_ \_ 已啟用集區上的 SPLREG 重新開機作業 \_**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-196">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="8f5a1-197">*.Pdata* 中的非零值表示已啟用 **集區 \_ \_ \_ \_ \_ 錯誤的 SPLREG 重新開機作業**。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-197">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="8f5a1-198">在 **\_ 集區 \_ \_ \_ \_ 錯誤的 SPLREG 重新開機作業** 中指定的時間是最短時間。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-198">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="8f5a1-199">實際的時間可能會比較長，取決於下列埠監視器設定，這些設定是此登錄機碼下的登錄值：</span><span class="sxs-lookup"><span data-stu-id="8f5a1-199">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="8f5a1-200">**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ monitor \\ < *MonitorName* > \\ 埠**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-200">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="8f5a1-201">呼叫 [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) 函數來查詢這些值。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-201">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="8f5a1-202">埠監視器設定</span><span class="sxs-lookup"><span data-stu-id="8f5a1-202">Port monitor setting</span></span>     | <span data-ttu-id="8f5a1-203">資料類型</span><span class="sxs-lookup"><span data-stu-id="8f5a1-203">Data type</span></span>      | <span data-ttu-id="8f5a1-204">意義</span><span class="sxs-lookup"><span data-stu-id="8f5a1-204">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5a1-205">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-205">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="8f5a1-206">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-206">**REG\_DWORD**</span></span> | <span data-ttu-id="8f5a1-207">如果非零值，可讓埠監視器以埠狀態更新多工緩衝處理器。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-207">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="8f5a1-208">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-208">**StatusUpdateInterval**</span></span> | <span data-ttu-id="8f5a1-209">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-209">**REG\_DWORD**</span></span> | <span data-ttu-id="8f5a1-210">指定埠監視器以埠狀態更新多工緩衝處理器時的間隔（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-210">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="8f5a1-211">如果 *pKeyName* 是其中一個預先定義的目錄服務 (DS) 金鑰 (請參閱 [**SetPrinter**](setprinter.md)) 和 *pValueName* 包含逗號 ( '，' ) ，則逗號之前的 *pValueName* 部分是值名稱，而逗號右邊的 *pValueName* 部分是 DS 屬性 OID。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-211">If *pKeyName* is one of the predefined Directory Service (DS) keys (see [**SetPrinter**](setprinter.md)) and *pValueName* contains a comma (','), then the portion of *pValueName* before the comma is the value name and the portion of *pValueName* to the right of the comma is the DS Property OID.</span></span> <span data-ttu-id="8f5a1-212">會建立名為 OID 的子機碼，並在 OID 索引鍵底下輸入值名稱和 OID 所組成的新值。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-212">A subkey called OID is created and a new value that consists of the value name and OID is entered under the OID key.</span></span> <span data-ttu-id="8f5a1-213">[**SetPrinterDataEx**](setprinterdataex.md) 也會在 DS 機碼下新增值名稱和資料。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-213">[**SetPrinterDataEx**](setprinterdataex.md) also adds the value name and data under the DS key.</span></span>

<span data-ttu-id="8f5a1-214">在 Windows 7 和更新版本的 Windows 中，預設會在用戶端上轉譯傳送至列印伺服器的列印工作。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-214">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="8f5a1-215">您可以將 *pKeyName* 設定為 "PrinterDriverData"，並 *pValueName* 至下表中的設定值，以讀取印表機的用戶端轉譯設定。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-215">The configuration of client-side rendering for a printer can be read by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="8f5a1-216">設定</span><span class="sxs-lookup"><span data-stu-id="8f5a1-216">Setting</span></span>                      | <span data-ttu-id="8f5a1-217">資料類型</span><span class="sxs-lookup"><span data-stu-id="8f5a1-217">Data type</span></span>      | <span data-ttu-id="8f5a1-218">描述</span><span class="sxs-lookup"><span data-stu-id="8f5a1-218">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5a1-219">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-219">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="8f5a1-220">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-220">**REG\_DWORD**</span></span> | <span data-ttu-id="8f5a1-221">值為0，或如果此值不存在於登錄中，則會啟用列印工作的預設用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-221">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="8f5a1-222">值為1時，會停用列印工作的用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-222">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="8f5a1-223">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-223">**ForceClientSideRendering**</span></span> | <span data-ttu-id="8f5a1-224">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-224">**REG\_DWORD**</span></span> | <span data-ttu-id="8f5a1-225">值為0，或如果此值不存在於登錄中，則會在用戶端上呈現列印工作。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-225">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="8f5a1-226">如果無法在用戶端上呈現列印工作，則會在伺服器上轉譯。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-226">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="8f5a1-227">如果無法在伺服器上轉譯列印工作，它將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-227">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="8f5a1-228">值為1時，會在用戶端上呈現列印工作。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-228">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="8f5a1-229">如果無法在用戶端上呈現列印工作，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="8f5a1-229">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8f5a1-230">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f5a1-230">Requirements</span></span>



| <span data-ttu-id="8f5a1-231">需求</span><span class="sxs-lookup"><span data-stu-id="8f5a1-231">Requirement</span></span> | <span data-ttu-id="8f5a1-232">值</span><span class="sxs-lookup"><span data-stu-id="8f5a1-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5a1-233">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f5a1-233">Minimum supported client</span></span><br/> | <span data-ttu-id="8f5a1-234">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8f5a1-235">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f5a1-235">Minimum supported server</span></span><br/> | <span data-ttu-id="8f5a1-236">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f5a1-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8f5a1-237">標頭</span><span class="sxs-lookup"><span data-stu-id="8f5a1-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f5a1-238"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8f5a1-238"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8f5a1-239">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f5a1-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f5a1-240"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f5a1-240"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8f5a1-241">DLL</span><span class="sxs-lookup"><span data-stu-id="8f5a1-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f5a1-242"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="8f5a1-242"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8f5a1-243">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="8f5a1-243">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8f5a1-244">**GetPrinterDataExW** (Unicode) 和 **GetPrinterDataExA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="8f5a1-244">**GetPrinterDataExW** (Unicode) and **GetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="8f5a1-245">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f5a1-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f5a1-246">列印</span><span class="sxs-lookup"><span data-stu-id="8f5a1-246">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8f5a1-247">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="8f5a1-247">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8f5a1-248">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-248">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="8f5a1-249">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="8f5a1-249">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

