---
description: EnumPrintProcessorDatatypes 函式會列舉指定列印處理器支援的資料類型。
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: 'EnumPrintProcessorDatatypes 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513328"
---
# <a name="enumprintprocessordatatypes-function"></a><span data-ttu-id="a128b-103">EnumPrintProcessorDatatypes 函式</span><span class="sxs-lookup"><span data-stu-id="a128b-103">EnumPrintProcessorDatatypes function</span></span>

<span data-ttu-id="a128b-104">**EnumPrintProcessorDatatypes** 函式會列舉指定列印處理器支援的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a128b-104">The **EnumPrintProcessorDatatypes** function enumerates the data types that a specified print processor supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="a128b-105">語法</span><span class="sxs-lookup"><span data-stu-id="a128b-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="a128b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a128b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a128b-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a128b-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a128b-108">以 null 結束的字串指標，指定列印處理器所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a128b-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor resides.</span></span> <span data-ttu-id="a128b-109">如果這個參數為 **Null**，則會列舉本機列印處理器的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a128b-109">If this parameter is **NULL**, the data types for the local print processor are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="a128b-110">*pPrintProcessorName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a128b-110">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a128b-111">以 null 結束的字串指標，指定列舉其資料類型的列印處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="a128b-111">A pointer to a null-terminated string that specifies the name of the print processor whose data types are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="a128b-112">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a128b-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a128b-113">*PDatatypes* 緩衝區中傳回的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="a128b-113">The type of information returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="a128b-114">此參數必須是1。</span><span class="sxs-lookup"><span data-stu-id="a128b-114">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="a128b-115">*pDatatypes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a128b-115">*pDatatypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a128b-116">緩衝區的指標，此緩衝區會接收 [**資料類型 \_ 資訊 \_ 1**](datatypes-info-1.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="a128b-116">A pointer to a buffer that receives an array of [**DATATYPES\_INFO\_1**](datatypes-info-1.md) structures.</span></span> <span data-ttu-id="a128b-117">每個結構都描述可用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a128b-117">Each structure describes an available data type.</span></span> <span data-ttu-id="a128b-118">緩衝區必須夠大，才能接收結構的陣列，以及結構成員指向的任何字串或其他資料。</span><span class="sxs-lookup"><span data-stu-id="a128b-118">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="a128b-119">若要判斷所需的緩衝區大小，請呼叫 **EnumPrintProcessorDatatypes** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="a128b-119">To determine the required buffer size, call **EnumPrintProcessorDatatypes** with *cbBuf* set to zero.</span></span> <span data-ttu-id="a128b-120">**EnumPrintProcessorDatatypes** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a128b-120">**EnumPrintProcessorDatatypes** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="a128b-121">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a128b-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a128b-122">*PDatatypes* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a128b-122">The size, in bytes, of the buffer pointed to by *pDatatypes*.</span></span>

</dd> <dt>

<span data-ttu-id="a128b-123">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a128b-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a128b-124">變數的指標，此變數會接收在函式成功時複製到 *pDatatypes* 緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a128b-124">A pointer to a variable that receives the number of bytes copied to the *pDatatypes* buffer if the function succeeds.</span></span> <span data-ttu-id="a128b-125">如果緩衝區太小，則函式會失敗，而變數會收到所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a128b-125">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="a128b-126">*pcReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a128b-126">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a128b-127">變數的指標，此變數會接收 *pDatatypes* 緩衝區中傳回的結構數目。</span><span class="sxs-lookup"><span data-stu-id="a128b-127">A pointer to a variable that receives the number of structures returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="a128b-128">這是支援的資料類型數目。</span><span class="sxs-lookup"><span data-stu-id="a128b-128">This is the number of supported data types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a128b-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="a128b-129">Return value</span></span>

<span data-ttu-id="a128b-130">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="a128b-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a128b-131">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="a128b-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a128b-132">備註</span><span class="sxs-lookup"><span data-stu-id="a128b-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a128b-133">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="a128b-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a128b-134">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="a128b-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a128b-135">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="a128b-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a128b-136">v</span><span class="sxs-lookup"><span data-stu-id="a128b-136">v</span></span>

<span data-ttu-id="a128b-137">從 Windows Vista 開始，來自遠端列印伺服器的資料類型資訊，會從本機快取中取出。</span><span class="sxs-lookup"><span data-stu-id="a128b-137">Starting with Windows Vista, the data type information from remote print servers is retrieved from a local cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="a128b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="a128b-138">Requirements</span></span>



| <span data-ttu-id="a128b-139">需求</span><span class="sxs-lookup"><span data-stu-id="a128b-139">Requirement</span></span> | <span data-ttu-id="a128b-140">值</span><span class="sxs-lookup"><span data-stu-id="a128b-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a128b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a128b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a128b-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a128b-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a128b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a128b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a128b-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a128b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a128b-145">標頭</span><span class="sxs-lookup"><span data-stu-id="a128b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a128b-146"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a128b-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a128b-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="a128b-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="a128b-148"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a128b-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a128b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="a128b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a128b-150"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="a128b-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a128b-151">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a128b-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a128b-152">**EnumPrintProcessorDatatypesW** (Unicode) 和 **EnumPrintProcessorDatatypesA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a128b-152">**EnumPrintProcessorDatatypesW** (Unicode) and **EnumPrintProcessorDatatypesA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="a128b-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a128b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a128b-154">列印</span><span class="sxs-lookup"><span data-stu-id="a128b-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a128b-155">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="a128b-155">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a128b-156">**資料類型 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a128b-156">**DATATYPES\_INFO\_1**</span></span>](datatypes-info-1.md)
</dt> <dt>

[<span data-ttu-id="a128b-157">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="a128b-157">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

