---
description: EnumPrintProcessors 函式會列舉安裝在指定伺服器上的列印處理器。
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: 'EnumPrintProcessors 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944585"
---
# <a name="enumprintprocessors-function"></a><span data-ttu-id="a120b-103">EnumPrintProcessors 函式</span><span class="sxs-lookup"><span data-stu-id="a120b-103">EnumPrintProcessors function</span></span>

<span data-ttu-id="a120b-104">**EnumPrintProcessors** 函式會列舉安裝在指定伺服器上的列印處理器。</span><span class="sxs-lookup"><span data-stu-id="a120b-104">The **EnumPrintProcessors** function enumerates the print processors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a120b-105">語法</span><span class="sxs-lookup"><span data-stu-id="a120b-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="a120b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a120b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a120b-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a120b-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a120b-108">以 null 結束的字串指標，指定列印處理器所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a120b-108">A pointer to a null-terminated string that specifies the name of the server on which the print processors reside.</span></span> <span data-ttu-id="a120b-109">如果此參數為 **Null**，則會列舉本機列印處理器。</span><span class="sxs-lookup"><span data-stu-id="a120b-109">If this parameter is **NULL**, the local print processors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="a120b-110">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a120b-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a120b-111">以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="a120b-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="a120b-112">如果此參數為 **Null**，則會使用目前的呼叫應用程式和用戶端電腦的環境 (不是目的地應用程式，而列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="a120b-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="a120b-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a120b-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a120b-114">*PPrintProcessorInfo* 緩衝區中傳回的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="a120b-114">The type of information returned in the *pPrintProcessorInfo* buffer.</span></span> <span data-ttu-id="a120b-115">此參數必須是1。</span><span class="sxs-lookup"><span data-stu-id="a120b-115">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="a120b-116">*pPrintProcessorInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a120b-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a120b-117">接收 [**PRINTPROCESSOR \_ INFO \_ 1**](printprocessor-info-1.md) 結構陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="a120b-117">A pointer to a buffer that receives an array of [**PRINTPROCESSOR\_INFO\_1**](printprocessor-info-1.md) structures.</span></span> <span data-ttu-id="a120b-118">每個結構都描述可用的列印處理器。</span><span class="sxs-lookup"><span data-stu-id="a120b-118">Each structure describes an available print processor.</span></span> <span data-ttu-id="a120b-119">緩衝區必須夠大，才能接收結構的陣列，以及結構成員指向的任何字串。</span><span class="sxs-lookup"><span data-stu-id="a120b-119">The buffer must be large enough to receive the array of structures and any strings to which the structure members point.</span></span>

<span data-ttu-id="a120b-120">若要判斷所需的緩衝區大小，請呼叫 **EnumPrintProcessors** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="a120b-120">To determine the required buffer size, call **EnumPrintProcessors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="a120b-121">**EnumPrintProcessors** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a120b-121">**EnumPrintProcessors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="a120b-122">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a120b-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a120b-123">*PPrintProcessorInfo* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a120b-123">The size, in bytes, of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="a120b-124">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a120b-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a120b-125">變數的指標，此變數會接收在函式成功時複製到 *pPrintProcessorInfo* 緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a120b-125">A pointer to a variable that receives the number of bytes copied to the *pPrintProcessorInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="a120b-126">如果緩衝區太小，則函式會失敗，而變數會收到所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a120b-126">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="a120b-127">*pcReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a120b-127">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a120b-128">變數的指標，此變數會接收 *pPrintProcessorInfo* 緩衝區中傳回的結構數目。</span><span class="sxs-lookup"><span data-stu-id="a120b-128">A pointer to a variable that receives the number of structures returned in the *pPrintProcessorInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a120b-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="a120b-129">Return value</span></span>

<span data-ttu-id="a120b-130">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="a120b-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a120b-131">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="a120b-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a120b-132">備註</span><span class="sxs-lookup"><span data-stu-id="a120b-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a120b-133">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="a120b-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a120b-134">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="a120b-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a120b-135">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="a120b-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a120b-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="a120b-136">Requirements</span></span>



| <span data-ttu-id="a120b-137">需求</span><span class="sxs-lookup"><span data-stu-id="a120b-137">Requirement</span></span> | <span data-ttu-id="a120b-138">值</span><span class="sxs-lookup"><span data-stu-id="a120b-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a120b-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a120b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a120b-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a120b-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a120b-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a120b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a120b-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a120b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a120b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="a120b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a120b-144"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a120b-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a120b-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="a120b-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="a120b-146"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a120b-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a120b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a120b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a120b-148"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="a120b-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a120b-149">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a120b-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a120b-150">**EnumPrintProcessorsW** (Unicode) 和 **EnumPrintProcessorsA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a120b-150">**EnumPrintProcessorsW** (Unicode) and **EnumPrintProcessorsA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="a120b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a120b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a120b-152">列印</span><span class="sxs-lookup"><span data-stu-id="a120b-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a120b-153">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="a120b-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a120b-154">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="a120b-154">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> <dt>

[<span data-ttu-id="a120b-155">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="a120b-155">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="a120b-156">**PRINTPROCESSOR \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a120b-156">**PRINTPROCESSOR\_INFO\_1**</span></span>](printprocessor-info-1.md)
</dt> </dl>

 

