---
description: EndPagePrinter 函式會通知列印多工緩衝處理器，應用程式是列印工作中頁面的結尾。
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: 'EndPagePrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 45e8ce005953e07f10ec621660ed38e68d50c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115481"
---
# <a name="endpageprinter-function"></a><span data-ttu-id="24934-103">EndPagePrinter 函式</span><span class="sxs-lookup"><span data-stu-id="24934-103">EndPagePrinter function</span></span>

<span data-ttu-id="24934-104">**EndPagePrinter** 函式會通知列印多工緩衝處理器，應用程式是列印工作中頁面的結尾。</span><span class="sxs-lookup"><span data-stu-id="24934-104">The **EndPagePrinter** function notifies the print spooler that the application is at the end of a page in a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="24934-105">語法</span><span class="sxs-lookup"><span data-stu-id="24934-105">Syntax</span></span>


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="24934-106">參數</span><span class="sxs-lookup"><span data-stu-id="24934-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24934-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24934-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24934-108">頁面將結束之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="24934-108">Handle to the printer for which the page will be concluded.</span></span> <span data-ttu-id="24934-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="24934-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24934-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="24934-110">Return value</span></span>

<span data-ttu-id="24934-111">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="24934-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="24934-112">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="24934-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24934-113">備註</span><span class="sxs-lookup"><span data-stu-id="24934-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24934-114">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="24934-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="24934-115">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="24934-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="24934-116">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="24934-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="24934-117">列印工作的順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="24934-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="24934-118">若要開始列印工作，請呼叫 [**StartDocPrinter**](startdocprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="24934-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="24934-119">若要開始每個頁面，請呼叫 [**StartPagePrinter**](startpageprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="24934-119">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="24934-120">若要將資料寫入頁面，請呼叫 [**WritePrinter**](writeprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="24934-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="24934-121">若要結束每個頁面，請呼叫 **EndPagePrinter**。</span><span class="sxs-lookup"><span data-stu-id="24934-121">To end each page, call **EndPagePrinter**.</span></span>
5.  <span data-ttu-id="24934-122">視需要針對任意數量的頁面重複2、3和4。</span><span class="sxs-lookup"><span data-stu-id="24934-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="24934-123">若要結束列印工作，請呼叫 [**EndDocPrinter**](enddocprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="24934-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="24934-124">當多工緩衝處理檔案中的頁面超過大約 350 MB 時，可能會無法列印，且不會傳送錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="24934-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="24934-125">例如，列印大型 EMF 檔案時可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="24934-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="24934-126">頁面大小限制取決於許多因素，包括可用的虛擬記憶體數量、呼叫進程所配置的記憶體數量，以及進程堆積中的片段量。</span><span class="sxs-lookup"><span data-stu-id="24934-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="24934-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="24934-127">Requirements</span></span>



| <span data-ttu-id="24934-128">需求</span><span class="sxs-lookup"><span data-stu-id="24934-128">Requirement</span></span> | <span data-ttu-id="24934-129">值</span><span class="sxs-lookup"><span data-stu-id="24934-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24934-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24934-130">Minimum supported client</span></span><br/> | <span data-ttu-id="24934-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24934-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="24934-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24934-132">Minimum supported server</span></span><br/> | <span data-ttu-id="24934-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24934-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="24934-134">標頭</span><span class="sxs-lookup"><span data-stu-id="24934-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="24934-135"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="24934-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="24934-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="24934-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="24934-137"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="24934-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="24934-138">DLL</span><span class="sxs-lookup"><span data-stu-id="24934-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24934-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24934-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="24934-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24934-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24934-141">列印</span><span class="sxs-lookup"><span data-stu-id="24934-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="24934-142">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="24934-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="24934-143">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="24934-143">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="24934-144">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="24934-144">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="24934-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="24934-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="24934-146">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="24934-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="24934-147">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="24934-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="24934-148">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="24934-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




