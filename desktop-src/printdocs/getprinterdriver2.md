---
description: GetPrinterDriver2 函式會抓取指定印表機的驅動程式資料。 如果未在本機電腦上安裝驅動程式，GetPrinterDriver2 會安裝該驅動程式，並在指定的視窗中顯示任何使用者介面。
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: 'GetPrinterDriver2 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194970"
---
# <a name="getprinterdriver2-function"></a><span data-ttu-id="1410d-104">GetPrinterDriver2 函式</span><span class="sxs-lookup"><span data-stu-id="1410d-104">GetPrinterDriver2 function</span></span>

<span data-ttu-id="1410d-105">**GetPrinterDriver2** 函式會抓取指定印表機的驅動程式資料。</span><span class="sxs-lookup"><span data-stu-id="1410d-105">The **GetPrinterDriver2** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="1410d-106">如果未在本機電腦上安裝驅動程式， **GetPrinterDriver2** 會安裝該驅動程式，並在指定的視窗中顯示任何使用者介面。</span><span class="sxs-lookup"><span data-stu-id="1410d-106">If the driver is not installed on the local computer, **GetPrinterDriver2** installs it and displays any user interface to the specified window.</span></span>

## <a name="syntax"></a><span data-ttu-id="1410d-107">語法</span><span class="sxs-lookup"><span data-stu-id="1410d-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="1410d-108">參數</span><span class="sxs-lookup"><span data-stu-id="1410d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1410d-109">*hWnd* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1410d-109">*hWnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1410d-110">視窗的控制碼，將用作驅動程式在安裝期間顯示之任何使用者介面（例如對話方塊）的父視窗。</span><span class="sxs-lookup"><span data-stu-id="1410d-110">A handle of the window that will be used as the parent window of any user interface, such as a dialog box, that the driver displays during installation.</span></span> <span data-ttu-id="1410d-111">如果此參數的值為 **Null**，則在安裝期間仍會向使用者顯示驅動程式的使用者介面，但不會有父視窗。</span><span class="sxs-lookup"><span data-stu-id="1410d-111">If the value of this parameter is **NULL**, the driver's user interface will still be displayed to the user during installation, but it will not have a parent window.</span></span>

</dd> <dt>

<span data-ttu-id="1410d-112">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1410d-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1410d-113">應抓取驅動程式資料之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1410d-113">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="1410d-114">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="1410d-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="1410d-115">*pEnvironment* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1410d-115">*pEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1410d-116">以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="1410d-116">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="1410d-117">如果此參數為 **Null**，則會使用目前的呼叫應用程式和用戶端電腦的環境 (不是目的地應用程式，而列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="1410d-117">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="1410d-118">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1410d-118">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1410d-119">*PDriverInfo* 緩衝區中傳回的印表機驅動程式結構。</span><span class="sxs-lookup"><span data-stu-id="1410d-119">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="1410d-120">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1410d-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1410d-121">值</span><span class="sxs-lookup"><span data-stu-id="1410d-121">Value</span></span>                                                                                                | <span data-ttu-id="1410d-122">意義</span><span class="sxs-lookup"><span data-stu-id="1410d-122">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="1410d-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-123"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="1410d-124">**驅動程式 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="1410d-124">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="1410d-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-125"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="1410d-126">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1410d-126">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="1410d-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-127"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="1410d-128">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="1410d-128">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="1410d-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-129"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="1410d-130">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1410d-130">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="1410d-131"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-131"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="1410d-132">**驅動程式 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="1410d-132">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="1410d-133"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-133"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="1410d-134">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="1410d-134">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="1410d-135"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-135"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="1410d-136">**驅動程式 \_ 資訊 \_ 8**</span><span class="sxs-lookup"><span data-stu-id="1410d-136">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="1410d-137">*pDriverInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1410d-137">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1410d-138">緩衝區的指標，此緩衝區會接收包含驅動程式相關資訊的結構（依 *層級* 所指定）。</span><span class="sxs-lookup"><span data-stu-id="1410d-138">A pointer to a buffer that receives a structure containing information about the driver, as specified by *Level*.</span></span> <span data-ttu-id="1410d-139">緩衝區必須夠大，才能儲存結構成員所指向的字串。</span><span class="sxs-lookup"><span data-stu-id="1410d-139">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="1410d-140">若要判斷所需的緩衝區大小，請呼叫 **GetPrinterDriver2** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="1410d-140">To determine the required buffer size, call **GetPrinterDriver2** with *cbBuf* set to zero.</span></span> <span data-ttu-id="1410d-141">**GetPrinterDriver2** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回 **錯誤 \_ 的 \_ 緩衝區**，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1410d-141">**GetPrinterDriver2** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="1410d-142">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1410d-142">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1410d-143">*PDriverInfo* 點的陣列大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1410d-143">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="1410d-144">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1410d-144">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1410d-145">值的指標，如果函式成功則為，如果 *cbBuf* 太小，則會收到所需的位元組數目，以接收復制的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="1410d-145">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1410d-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="1410d-146">Return value</span></span>

<span data-ttu-id="1410d-147">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="1410d-147">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1410d-148">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="1410d-148">If the function fails, the return value is zero.</span></span> <span data-ttu-id="1410d-149">若要取得傳回狀態，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="1410d-149">To get the return status, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="1410d-150">備註</span><span class="sxs-lookup"><span data-stu-id="1410d-150">Remarks</span></span>

<span data-ttu-id="1410d-151">[**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md)、[**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md)、[**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md)、[**驅動程式 \_ 資訊 \_ 5**](driver-info-5.md)、[**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)和 [**驅動程式 \_ 資訊 \_ 8**](driver-info-8.md)結構包含 **pDriverPath** 成員中印表機驅動程式的檔案名或完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="1410d-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), [**DRIVER\_INFO\_6**](driver-info-6.md), and [**DRIVER\_INFO\_8**](driver-info-8.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="1410d-152">應用程式可以藉由呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式並提供路徑和檔案名作為單一引數，來使用路徑和檔案名來載入印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="1410d-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

<span data-ttu-id="1410d-153">此函數的 ANSI 版本，不支援 **GetPrinterDriver2A** ，而且會傳回 **\_ 不 \_ 支援的錯誤**。</span><span class="sxs-lookup"><span data-stu-id="1410d-153">The ANSI version of this function, **GetPrinterDriver2A** is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1410d-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="1410d-154">Requirements</span></span>



| <span data-ttu-id="1410d-155">需求</span><span class="sxs-lookup"><span data-stu-id="1410d-155">Requirement</span></span> | <span data-ttu-id="1410d-156">值</span><span class="sxs-lookup"><span data-stu-id="1410d-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1410d-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1410d-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1410d-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1410d-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1410d-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1410d-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1410d-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1410d-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1410d-161">標頭</span><span class="sxs-lookup"><span data-stu-id="1410d-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="1410d-162"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1410d-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1410d-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="1410d-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="1410d-164"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1410d-165">DLL</span><span class="sxs-lookup"><span data-stu-id="1410d-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1410d-166"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="1410d-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1410d-167">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1410d-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1410d-168">**GetPrinterDriver2W** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="1410d-168">**GetPrinterDriver2W** (Unicode)</span></span><br/>                                                               |



## <a name="see-also"></a><span data-ttu-id="1410d-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1410d-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1410d-170">列印</span><span class="sxs-lookup"><span data-stu-id="1410d-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1410d-171">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="1410d-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1410d-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1410d-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="1410d-173">**驅動程式 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="1410d-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="1410d-174">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1410d-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="1410d-175">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="1410d-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="1410d-176">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1410d-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="1410d-177">**驅動程式 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="1410d-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="1410d-178">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="1410d-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="1410d-179">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="1410d-179">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="1410d-180">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1410d-180">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="1410d-181">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="1410d-181">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

