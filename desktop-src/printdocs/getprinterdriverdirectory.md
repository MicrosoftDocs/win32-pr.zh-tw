---
description: GetPrinterDriverDirectory 函式會捕獲印表機驅動程式目錄的路徑。
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: 'GetPrinterDriverDirectory 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996973"
---
# <a name="getprinterdriverdirectory-function"></a><span data-ttu-id="a3e44-103">GetPrinterDriverDirectory 函式</span><span class="sxs-lookup"><span data-stu-id="a3e44-103">GetPrinterDriverDirectory function</span></span>

<span data-ttu-id="a3e44-104">**GetPrinterDriverDirectory** 函式會捕獲印表機驅動程式目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="a3e44-104">The **GetPrinterDriverDirectory** function retrieves the path of the printer-driver directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e44-105">語法</span><span class="sxs-lookup"><span data-stu-id="a3e44-105">Syntax</span></span>


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="a3e44-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3e44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e44-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3e44-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e44-108">以 null 結束的字串指標，指定印表機驅動程式所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3e44-108">A pointer to a null-terminated string that specifies the name of the server on which the printer driver resides.</span></span> <span data-ttu-id="a3e44-109">如果此參數為 **Null**，則會抓取本機驅動程式-目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="a3e44-109">If this parameter is **NULL**, the local driver-directory path is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a3e44-110">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3e44-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e44-111">以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="a3e44-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="a3e44-112">如果此參數為 **Null**，則會使用目前的呼叫應用程式和用戶端電腦的環境 (不是目的地應用程式，而列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="a3e44-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="a3e44-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3e44-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e44-114">結構層級。</span><span class="sxs-lookup"><span data-stu-id="a3e44-114">The structure level.</span></span> <span data-ttu-id="a3e44-115">此值必須是1。</span><span class="sxs-lookup"><span data-stu-id="a3e44-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="a3e44-116">*pDriverDirectory* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3e44-116">*pDriverDirectory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e44-117">接收路徑之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="a3e44-117">A pointer to a buffer that receives the path.</span></span>

</dd> <dt>

<span data-ttu-id="a3e44-118">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3e44-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e44-119">*PDriverDirectory* 所指向的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="a3e44-119">The size of the buffer to which *pDriverDirectory* points.</span></span>

</dd> <dt>

<span data-ttu-id="a3e44-120">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3e44-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e44-121">值的指標，指定函式成功時所複製的位元組數目，或者，如果 *cbBuf* 太小，則為所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a3e44-121">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e44-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3e44-122">Return value</span></span>

<span data-ttu-id="a3e44-123">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="a3e44-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a3e44-124">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="a3e44-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3e44-125">備註</span><span class="sxs-lookup"><span data-stu-id="a3e44-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a3e44-126">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="a3e44-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a3e44-127">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="a3e44-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a3e44-128">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="a3e44-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3e44-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3e44-129">Requirements</span></span>



| <span data-ttu-id="a3e44-130">需求</span><span class="sxs-lookup"><span data-stu-id="a3e44-130">Requirement</span></span> | <span data-ttu-id="a3e44-131">值</span><span class="sxs-lookup"><span data-stu-id="a3e44-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e44-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3e44-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e44-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e44-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3e44-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3e44-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e44-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e44-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3e44-136">標頭</span><span class="sxs-lookup"><span data-stu-id="a3e44-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3e44-137"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a3e44-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a3e44-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="a3e44-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3e44-139"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3e44-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a3e44-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e44-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e44-141"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="a3e44-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a3e44-142">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a3e44-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a3e44-143">**GetPrinterDriverDirectoryW** (Unicode) 和 **GetPrinterDriverDirectoryA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a3e44-143">**GetPrinterDriverDirectoryW** (Unicode) and **GetPrinterDriverDirectoryA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a3e44-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3e44-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e44-145">列印</span><span class="sxs-lookup"><span data-stu-id="a3e44-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a3e44-146">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="a3e44-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a3e44-147">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="a3e44-147">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> </dl>

 

 




