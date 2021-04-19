---
description: EndDocPrinter 函式會結束指定之印表機的列印工作。
ms.assetid: 13c713e8-cc24-4191-8b1e-967b9e20e541
title: 'EndDocPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndDocPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 8d3e2bc110e5ee9412bb1edb89779f896edb015a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986967"
---
# <a name="enddocprinter-function"></a><span data-ttu-id="a5e8e-103">EndDocPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="a5e8e-103">EndDocPrinter function</span></span>

<span data-ttu-id="a5e8e-104">**EndDocPrinter** 函式會結束指定之印表機的列印工作。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-104">The **EndDocPrinter** function ends a print job for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e8e-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5e8e-105">Syntax</span></span>


```C++
BOOL EndDocPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="a5e8e-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5e8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e8e-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5e8e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e8e-108">列印工作應結束之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-108">Handle to a printer for which the print job should be ended.</span></span> <span data-ttu-id="a5e8e-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5e8e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5e8e-110">Return value</span></span>

<span data-ttu-id="a5e8e-111">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a5e8e-112">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e8e-113">備註</span><span class="sxs-lookup"><span data-stu-id="a5e8e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a5e8e-114">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a5e8e-115">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a5e8e-116">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a5e8e-117">如果未藉由呼叫 [**StartDocPrinter**](startdocprinter.md)函數來啟動列印工作， **EndDocPrinter** 函式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-117">The **EndDocPrinter** function returns an error if the print job was not started by calling the [**StartDocPrinter**](startdocprinter.md) function.</span></span>

<span data-ttu-id="a5e8e-118">列印工作的順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="a5e8e-118">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="a5e8e-119">若要開始列印工作，請呼叫 [**StartDocPrinter**](startdocprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-119">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="a5e8e-120">若要開始每個頁面，請呼叫 [**StartPagePrinter**](startpageprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-120">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="a5e8e-121">若要將資料寫入頁面，請呼叫 [**WritePrinter**](writeprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-121">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="a5e8e-122">若要結束每個頁面，請呼叫 [**EndPagePrinter**](endpageprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-122">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="a5e8e-123">視需要針對任意數量的頁面重複2、3和4。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-123">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="a5e8e-124">若要結束列印工作，請呼叫 **EndDocPrinter**。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-124">To end the print job, call **EndDocPrinter**.</span></span>

<span data-ttu-id="a5e8e-125">當多工緩衝處理檔案中的頁面超過大約 350 MB 時，可能會無法列印，且不會傳送錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-125">When a page in a spooled file exceeds approximately 350 MB, it may fail to print and not send an error message.</span></span> <span data-ttu-id="a5e8e-126">例如，列印大型 EMF 檔案時可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-126">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="a5e8e-127">頁面大小限制取決於許多因素，包括可用的虛擬記憶體數量、呼叫進程所配置的記憶體數量，以及進程堆積中的片段量。</span><span class="sxs-lookup"><span data-stu-id="a5e8e-127">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e8e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5e8e-128">Requirements</span></span>



| <span data-ttu-id="a5e8e-129">需求</span><span class="sxs-lookup"><span data-stu-id="a5e8e-129">Requirement</span></span> | <span data-ttu-id="a5e8e-130">值</span><span class="sxs-lookup"><span data-stu-id="a5e8e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e8e-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5e8e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e8e-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5e8e-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a5e8e-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5e8e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e8e-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5e8e-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a5e8e-135">標頭</span><span class="sxs-lookup"><span data-stu-id="a5e8e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5e8e-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a5e8e-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a5e8e-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5e8e-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5e8e-138"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5e8e-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a5e8e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a5e8e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5e8e-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5e8e-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="a5e8e-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5e8e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e8e-142">列印</span><span class="sxs-lookup"><span data-stu-id="a5e8e-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a5e8e-143">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="a5e8e-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a5e8e-144">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="a5e8e-144">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="a5e8e-145">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="a5e8e-145">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="a5e8e-146">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="a5e8e-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="a5e8e-147">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="a5e8e-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="a5e8e-148">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="a5e8e-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




