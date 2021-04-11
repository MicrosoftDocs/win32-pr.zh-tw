---
description: GetPrintProcessorDirectory 函式會在指定的伺服器上，捕獲列印處理器目錄的路徑。
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: 'GetPrintProcessorDirectory 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852420"
---
# <a name="getprintprocessordirectory-function"></a><span data-ttu-id="1c597-103">GetPrintProcessorDirectory 函式</span><span class="sxs-lookup"><span data-stu-id="1c597-103">GetPrintProcessorDirectory function</span></span>

<span data-ttu-id="1c597-104">**GetPrintProcessorDirectory** 函式會在指定的伺服器上，捕獲列印處理器目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="1c597-104">The **GetPrintProcessorDirectory** function retrieves the path to the print processor directory on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c597-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c597-105">Syntax</span></span>


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="1c597-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c597-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c597-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c597-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c597-108">指定伺服器名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="1c597-108">A pointer to a null-terminated string that specifies the name of the server.</span></span> <span data-ttu-id="1c597-109">如果此參數為 **Null**，則會傳回本機路徑。</span><span class="sxs-lookup"><span data-stu-id="1c597-109">If this parameter is **NULL**, a local path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="1c597-110">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c597-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c597-111">以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="1c597-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="1c597-112">如果此參數為 **Null**，則會使用目前的呼叫應用程式和用戶端電腦的環境 (不是目的地應用程式，而列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="1c597-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="1c597-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c597-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c597-114">結構層級。</span><span class="sxs-lookup"><span data-stu-id="1c597-114">The structure level.</span></span> <span data-ttu-id="1c597-115">此值必須是1。</span><span class="sxs-lookup"><span data-stu-id="1c597-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="1c597-116">*pPrintProcessorInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1c597-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c597-117">接收路徑之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="1c597-117">A pointer to a buffer that receives the path.</span></span> <span data-ttu-id="1c597-118">請注意，如果是 Windows Server 2003 SP 1 之前的作業系統，則路徑是伺服器的本機格式，而不是真正的遠端格式。</span><span class="sxs-lookup"><span data-stu-id="1c597-118">Note that, for operating systems prior to Windows Server 2003 SP 1, the path is in the local format for the server, not the true remote format.</span></span> <span data-ttu-id="1c597-119">例如，路徑會被指定為「% Windir% System32 多工 \\ \\ 緩衝處理 \\ Prtprocs \\ % 環境%」，而不是「 \\ \\ ServerName \\ Print $ \\ Prtprocs \\ % 環境%」，即使是針對遠端伺服器呼叫也是一樣。</span><span class="sxs-lookup"><span data-stu-id="1c597-119">For example, the path is given as "%Windir%\\System32\\Spool\\Prtprocs\\%Environment%" instead of "\\\\ServerName\\Print$\\Prtprocs\\%Environment%", even when called for a remote server.</span></span> <span data-ttu-id="1c597-120">若是 Windows Server 2003 SP 1 和更新版本的作業系統，則會傳回真正的遠端路徑。</span><span class="sxs-lookup"><span data-stu-id="1c597-120">For the operating systems Windows Server 2003 SP 1 and later, the true remote path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="1c597-121">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c597-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c597-122">*PPrintProcessorInfo* 所指向的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="1c597-122">The size of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="1c597-123">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1c597-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c597-124">值的指標，指定函式成功時所複製的位元組數目，或者，如果 *cbBuf* 太小，則為所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="1c597-124">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c597-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c597-125">Return value</span></span>

<span data-ttu-id="1c597-126">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="1c597-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1c597-127">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="1c597-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c597-128">備註</span><span class="sxs-lookup"><span data-stu-id="1c597-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c597-129">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="1c597-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1c597-130">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="1c597-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1c597-131">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="1c597-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c597-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c597-132">Requirements</span></span>



| <span data-ttu-id="1c597-133">需求</span><span class="sxs-lookup"><span data-stu-id="1c597-133">Requirement</span></span> | <span data-ttu-id="1c597-134">值</span><span class="sxs-lookup"><span data-stu-id="1c597-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c597-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c597-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1c597-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c597-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1c597-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c597-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1c597-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c597-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1c597-139">標頭</span><span class="sxs-lookup"><span data-stu-id="1c597-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c597-140"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1c597-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1c597-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="1c597-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c597-142"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c597-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1c597-143">DLL</span><span class="sxs-lookup"><span data-stu-id="1c597-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c597-144"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="1c597-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1c597-145">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1c597-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1c597-146">**GetPrintProcessorDirectoryW** (Unicode) 和 **GetPrintProcessorDirectoryA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1c597-146">**GetPrintProcessorDirectoryW** (Unicode) and **GetPrintProcessorDirectoryA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1c597-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c597-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c597-148">列印</span><span class="sxs-lookup"><span data-stu-id="1c597-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1c597-149">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="1c597-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1c597-150">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="1c597-150">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

 




