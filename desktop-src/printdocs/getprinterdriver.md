---
description: GetPrinterDriver 函式會抓取指定印表機的驅動程式資料。 如果未在本機電腦上安裝驅動程式，GetPrinterDriver 會安裝該驅動程式。
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: 'GetPrinterDriver 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975497"
---
# <a name="getprinterdriver-function"></a><span data-ttu-id="6810b-104">GetPrinterDriver 函式</span><span class="sxs-lookup"><span data-stu-id="6810b-104">GetPrinterDriver function</span></span>

<span data-ttu-id="6810b-105">**GetPrinterDriver** 函式會抓取指定印表機的驅動程式資料。</span><span class="sxs-lookup"><span data-stu-id="6810b-105">The **GetPrinterDriver** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="6810b-106">如果未在本機電腦上安裝驅動程式， **GetPrinterDriver** 會安裝該驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6810b-106">If the driver is not installed on the local computer, **GetPrinterDriver** installs it.</span></span>

## <a name="syntax"></a><span data-ttu-id="6810b-107">語法</span><span class="sxs-lookup"><span data-stu-id="6810b-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="6810b-108">參數</span><span class="sxs-lookup"><span data-stu-id="6810b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6810b-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6810b-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6810b-110">應抓取驅動程式資料之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6810b-110">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="6810b-111">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="6810b-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="6810b-112">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6810b-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6810b-113">以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="6810b-113">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="6810b-114">如果此參數為 **Null**，則會使用目前的呼叫應用程式和用戶端電腦的環境 (不是目的地應用程式，而列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="6810b-114">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="6810b-115">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6810b-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6810b-116">*PDriverInfo* 緩衝區中傳回的印表機驅動程式結構。</span><span class="sxs-lookup"><span data-stu-id="6810b-116">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="6810b-117">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6810b-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6810b-118">值</span><span class="sxs-lookup"><span data-stu-id="6810b-118">Value</span></span>                                                                                                | <span data-ttu-id="6810b-119">意義</span><span class="sxs-lookup"><span data-stu-id="6810b-119">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="6810b-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-120"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="6810b-121">**驅動程式 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6810b-121">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="6810b-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-122"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="6810b-123">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6810b-123">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="6810b-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-124"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="6810b-125">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6810b-125">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="6810b-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-126"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="6810b-127">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="6810b-127">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="6810b-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-128"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="6810b-129">**驅動程式 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="6810b-129">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="6810b-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-130"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="6810b-131">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="6810b-131">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="6810b-132"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-132"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="6810b-133">**驅動程式 \_ 資訊 \_ 8**</span><span class="sxs-lookup"><span data-stu-id="6810b-133">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="6810b-134">*pDriverInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6810b-134">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6810b-135">緩衝區的指標，此緩衝區會接收包含驅動程式相關資訊的結構（依層級所指定）。</span><span class="sxs-lookup"><span data-stu-id="6810b-135">A pointer to a buffer that receives a structure containing information about the driver, as specified by Level.</span></span> <span data-ttu-id="6810b-136">緩衝區必須夠大，才能儲存結構成員所指向的字串。</span><span class="sxs-lookup"><span data-stu-id="6810b-136">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="6810b-137">若要判斷所需的緩衝區大小，請呼叫 **GetPrinterDriver** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="6810b-137">To determine the required buffer size, call **GetPrinterDriver** with *cbBuf* set to zero.</span></span> <span data-ttu-id="6810b-138">**GetPrinterDriver** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6810b-138">**GetPrinterDriver** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="6810b-139">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6810b-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6810b-140">*PDriverInfo* 點的陣列大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6810b-140">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="6810b-141">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6810b-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6810b-142">值的指標，如果函式成功則為，如果 *cbBuf* 太小，則會收到所需的位元組數目，以接收復制的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6810b-142">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6810b-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="6810b-143">Return value</span></span>

<span data-ttu-id="6810b-144">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="6810b-144">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6810b-145">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="6810b-145">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="6810b-146">針對不存在的驅動程式，此函數會傳回錯誤的 \_ \_ 印表機 \_ 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6810b-146">For a non-existent driver, the function returns ERROR\_UNKNOWN\_PRINTER\_DRIVER.</span></span>

## <a name="remarks"></a><span data-ttu-id="6810b-147">備註</span><span class="sxs-lookup"><span data-stu-id="6810b-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6810b-148">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="6810b-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6810b-149">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="6810b-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6810b-150">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="6810b-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6810b-151">[**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md)、[**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md)、[**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md)、[**驅動程式 \_ 資訊 \_ 5**](driver-info-5.md)和 [**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)結構包含 **pDriverPath** 成員中的印表機驅動程式的檔案名或完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="6810b-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), and [**DRIVER\_INFO\_6**](driver-info-6.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="6810b-152">應用程式可以藉由呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式並提供路徑和檔案名作為單一引數，來使用路徑和檔案名來載入印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6810b-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="6810b-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="6810b-153">Requirements</span></span>



| <span data-ttu-id="6810b-154">需求</span><span class="sxs-lookup"><span data-stu-id="6810b-154">Requirement</span></span> | <span data-ttu-id="6810b-155">值</span><span class="sxs-lookup"><span data-stu-id="6810b-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6810b-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6810b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="6810b-157">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6810b-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6810b-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6810b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="6810b-159">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6810b-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6810b-160">標頭</span><span class="sxs-lookup"><span data-stu-id="6810b-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="6810b-161"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6810b-161"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6810b-162">程式庫</span><span class="sxs-lookup"><span data-stu-id="6810b-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="6810b-163"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-163"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6810b-164">DLL</span><span class="sxs-lookup"><span data-stu-id="6810b-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6810b-165"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="6810b-165"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6810b-166">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="6810b-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6810b-167">**GetPrinterDriverW** (Unicode) 和 **GetPrinterDriverA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="6810b-167">**GetPrinterDriverW** (Unicode) and **GetPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="6810b-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6810b-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6810b-169">列印</span><span class="sxs-lookup"><span data-stu-id="6810b-169">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6810b-170">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="6810b-170">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6810b-171">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="6810b-171">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="6810b-172">**驅動程式 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6810b-172">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="6810b-173">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6810b-173">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="6810b-174">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6810b-174">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="6810b-175">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="6810b-175">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="6810b-176">**驅動程式 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="6810b-176">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="6810b-177">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="6810b-177">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="6810b-178">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="6810b-178">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="6810b-179">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6810b-179">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

