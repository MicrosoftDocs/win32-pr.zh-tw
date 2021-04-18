---
description: FlushPrinter 函式會將緩衝區傳送至印表機，以便從暫時性狀態中清除。
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: 'FlushPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513325"
---
# <a name="flushprinter-function"></a><span data-ttu-id="e2d26-103">FlushPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="e2d26-103">FlushPrinter function</span></span>

<span data-ttu-id="e2d26-104">**FlushPrinter** 函式會將緩衝區傳送至印表機，以便從暫時性狀態中清除。</span><span class="sxs-lookup"><span data-stu-id="e2d26-104">The **FlushPrinter** function sends a buffer to the printer in order to clear it from a transient state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d26-105">語法</span><span class="sxs-lookup"><span data-stu-id="e2d26-105">Syntax</span></span>


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a><span data-ttu-id="e2d26-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2d26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d26-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2d26-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d26-108">印表機物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e2d26-108">A handle to the printer object.</span></span> <span data-ttu-id="e2d26-109">這應該是印表機驅動程式在先前的 [**WritePrinter**](writeprinter.md) 呼叫中所使用的相同控制碼。</span><span class="sxs-lookup"><span data-stu-id="e2d26-109">This should be the same handle that was used, in a prior [**WritePrinter**](writeprinter.md) call, by the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="e2d26-110">*pBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2d26-110">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d26-111">位元組陣列的指標，其中包含要寫入至印表機的資料。</span><span class="sxs-lookup"><span data-stu-id="e2d26-111">A pointer to an array of bytes that contains the data to be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="e2d26-112">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2d26-112">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d26-113">*PBuf* 所指向的陣列大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2d26-113">The size, in bytes, of the array pointed to by *pBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="e2d26-114">*pcWritten* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e2d26-114">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d26-115">值的指標，此值會接收寫入至印表機的資料位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e2d26-115">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="e2d26-116">*cSleep* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2d26-116">*cSleep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d26-117">印表機埠的 i/o 線路應維持閒置的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2d26-117">The time, in milliseconds, for which the I/O line to the printer port should be kept idle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2d26-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2d26-118">Return value</span></span>

<span data-ttu-id="e2d26-119">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="e2d26-119">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="e2d26-120">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e2d26-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2d26-121">備註</span><span class="sxs-lookup"><span data-stu-id="e2d26-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2d26-122">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e2d26-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e2d26-123">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="e2d26-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e2d26-124">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="e2d26-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e2d26-125">只有在 [**WritePrinter**](writeprinter.md)失敗時才應該呼叫 **FlushPrinter** ，讓印表機處於暫時性狀態。</span><span class="sxs-lookup"><span data-stu-id="e2d26-125">**FlushPrinter** should be called only if [**WritePrinter**](writeprinter.md) failed, leaving the printer in a transient state.</span></span> <span data-ttu-id="e2d26-126">例如，當工作中止，且印表機驅動程式已部分傳送某些原始資料至印表機時，印表機可能會進入暫時性狀態。</span><span class="sxs-lookup"><span data-stu-id="e2d26-126">For example, the printer could get into a transient state when the job gets aborted and the printer driver has partially sent some raw data to the printer.</span></span>

<span data-ttu-id="e2d26-127">**FlushPrinter** 也可以指定列印多工緩衝處理器不會將任何工作排程到對應印表機埠的閒置期間。</span><span class="sxs-lookup"><span data-stu-id="e2d26-127">**FlushPrinter** also can specify an idle period during which the print spooler does not schedule any jobs to the corresponding printer port.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d26-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2d26-128">Requirements</span></span>



| <span data-ttu-id="e2d26-129">需求</span><span class="sxs-lookup"><span data-stu-id="e2d26-129">Requirement</span></span> | <span data-ttu-id="e2d26-130">值</span><span class="sxs-lookup"><span data-stu-id="e2d26-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d26-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2d26-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d26-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2d26-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e2d26-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2d26-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d26-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2d26-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e2d26-135">標頭</span><span class="sxs-lookup"><span data-stu-id="e2d26-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2d26-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e2d26-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e2d26-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2d26-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2d26-138"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2d26-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e2d26-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e2d26-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2d26-140"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="e2d26-140"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="e2d26-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2d26-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d26-142">列印</span><span class="sxs-lookup"><span data-stu-id="e2d26-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e2d26-143">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="e2d26-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e2d26-144">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="e2d26-144">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




