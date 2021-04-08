---
description: EnumPrinterDrivers 函式會列舉安裝在指定印表機伺服器上的印表機驅動程式。
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: 'EnumPrinterDrivers 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692904"
---
# <a name="enumprinterdrivers-function"></a><span data-ttu-id="fda31-103">EnumPrinterDrivers 函式</span><span class="sxs-lookup"><span data-stu-id="fda31-103">EnumPrinterDrivers function</span></span>

<span data-ttu-id="fda31-104">**EnumPrinterDrivers** 函式會列舉安裝在指定印表機伺服器上的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fda31-104">The **EnumPrinterDrivers** function enumerates the printer drivers installed on a specified printer server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda31-105">語法</span><span class="sxs-lookup"><span data-stu-id="fda31-105">Syntax</span></span>


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="fda31-106">參數</span><span class="sxs-lookup"><span data-stu-id="fda31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fda31-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fda31-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda31-108">以 null 結束的字串指標，指定用來列舉印表機驅動程式之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="fda31-108">A pointer to a null-terminated string that specifies the name of the server on which the printer drivers are enumerated.</span></span>

<span data-ttu-id="fda31-109">如果 *pName* 為 **Null**，此函式會列舉本機印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fda31-109">If *pName* is **NULL**, the function enumerates the local printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="fda31-110">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fda31-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda31-111">以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64、Windows x64 或 Windows NT R4000) 。</span><span class="sxs-lookup"><span data-stu-id="fda31-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, Windows x64, or Windows NT R4000).</span></span> <span data-ttu-id="fda31-112">如果這個參數為 **Null**，則函式會使用目前的呼叫端/用戶端環境 (不是目的地/伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="fda31-112">If this parameter is **NULL**, the function uses the current environment of the caller/client (not of the destination/server).</span></span>

<span data-ttu-id="fda31-113">如果 *pEnvironment* 字串指定 "all"， **EnumPrinterDrivers** 會列舉安裝在指定伺服器上之所有平臺的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fda31-113">If the *pEnvironment* string specifies "all", **EnumPrinterDrivers** enumerates printer drivers for all platforms installed on the specified server.</span></span>

</dd> <dt>

<span data-ttu-id="fda31-114">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fda31-114">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda31-115">*PDriverInfo* 緩衝區中傳回的資訊結構類型。</span><span class="sxs-lookup"><span data-stu-id="fda31-115">The type of information structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="fda31-116">它可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="fda31-116">It can be one of the following.</span></span>



| <span data-ttu-id="fda31-117">值</span><span class="sxs-lookup"><span data-stu-id="fda31-117">Value</span></span>                                                                                                | <span data-ttu-id="fda31-118">意義</span><span class="sxs-lookup"><span data-stu-id="fda31-118">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="fda31-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-119"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="fda31-120">**驅動程式 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fda31-120">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="fda31-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="fda31-122">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fda31-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="fda31-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="fda31-124">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="fda31-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="fda31-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="fda31-126">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="fda31-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="fda31-127"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-127"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="fda31-128">**驅動程式 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="fda31-128">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="fda31-129"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-129"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="fda31-130">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="fda31-130">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="fda31-131"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-131"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="fda31-132">**驅動程式 \_ 資訊 \_ 8**</span><span class="sxs-lookup"><span data-stu-id="fda31-132">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="fda31-133">*pDriverInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fda31-133">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fda31-134">接收驅動程式資訊結構陣列的緩衝區指標 \_ \_ \* ，如同 *層級* 所指定。</span><span class="sxs-lookup"><span data-stu-id="fda31-134">A pointer to a buffer that receives an array of DRIVER\_INFO\_\* structures, as specified by *Level*.</span></span> <span data-ttu-id="fda31-135">每個結構都包含描述可用印表機驅動程式的資料。</span><span class="sxs-lookup"><span data-stu-id="fda31-135">Each structure contains data that describes an available printer driver.</span></span> <span data-ttu-id="fda31-136">緩衝區必須夠大，才能接收結構的陣列，以及結構成員指向的任何字串或其他資料。</span><span class="sxs-lookup"><span data-stu-id="fda31-136">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="fda31-137">若要判斷所需的緩衝區大小，請呼叫 **EnumPrinterDrivers** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="fda31-137">To determine the required buffer size, call **EnumPrinterDrivers** with *cbBuf* set to zero.</span></span> <span data-ttu-id="fda31-138">**EnumPrinterDrivers** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fda31-138">**EnumPrinterDrivers** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="fda31-139">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fda31-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda31-140">*PDriverInfo* 所指向的緩衝區大小（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="fda31-140">The size, in bytes, of the buffer pointed to by *pDriverInfo*</span></span>

</dd> <dt>

<span data-ttu-id="fda31-141">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fda31-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fda31-142">變數的指標，此變數會接收在函式成功時複製到 *pDriverInfo* 緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="fda31-142">A pointer to a variable that receives the number of bytes copied to the *pDriverInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="fda31-143">如果緩衝區太小，則函式會失敗，而變數會收到所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="fda31-143">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="fda31-144">*pcReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fda31-144">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fda31-145">變數的指標，此變數會接收 *pDriverInfo* 緩衝區中傳回的結構數目。</span><span class="sxs-lookup"><span data-stu-id="fda31-145">A pointer to a variable that receives the number of structures returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="fda31-146">這是安裝在指定列印伺服器上的印表機驅動程式數目。</span><span class="sxs-lookup"><span data-stu-id="fda31-146">This is the number of printer drivers installed on the specified print server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fda31-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="fda31-147">Return value</span></span>

<span data-ttu-id="fda31-148">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="fda31-148">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fda31-149">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="fda31-149">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda31-150">備註</span><span class="sxs-lookup"><span data-stu-id="fda31-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fda31-151">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="fda31-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fda31-152">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="fda31-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fda31-153">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="fda31-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fda31-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="fda31-154">Requirements</span></span>



| <span data-ttu-id="fda31-155">需求</span><span class="sxs-lookup"><span data-stu-id="fda31-155">Requirement</span></span> | <span data-ttu-id="fda31-156">值</span><span class="sxs-lookup"><span data-stu-id="fda31-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fda31-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fda31-157">Minimum supported client</span></span><br/> | <span data-ttu-id="fda31-158">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fda31-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fda31-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fda31-159">Minimum supported server</span></span><br/> | <span data-ttu-id="fda31-160">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fda31-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fda31-161">標頭</span><span class="sxs-lookup"><span data-stu-id="fda31-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="fda31-162"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fda31-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fda31-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="fda31-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="fda31-164"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fda31-165">DLL</span><span class="sxs-lookup"><span data-stu-id="fda31-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fda31-166"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="fda31-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fda31-167">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="fda31-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fda31-168">**EnumPrinterDriversW** (Unicode) 和 **EnumPrinterDriversA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="fda31-168">**EnumPrinterDriversW** (Unicode) and **EnumPrinterDriversA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="fda31-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fda31-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda31-170">列印</span><span class="sxs-lookup"><span data-stu-id="fda31-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fda31-171">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="fda31-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fda31-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="fda31-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="fda31-173">**驅動程式 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fda31-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="fda31-174">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fda31-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="fda31-175">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="fda31-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="fda31-176">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="fda31-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="fda31-177">**驅動程式 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="fda31-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="fda31-178">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="fda31-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="fda31-179">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="fda31-179">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

