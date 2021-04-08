---
description: StartDocPrinter 函式會通知列印多工緩衝處理器，檔會進行多工緩衝處理以進行列印。
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: 'StartDocPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851908"
---
# <a name="startdocprinter-function"></a><span data-ttu-id="3c233-103">StartDocPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="3c233-103">StartDocPrinter function</span></span>

<span data-ttu-id="3c233-104">**StartDocPrinter** 函式會通知列印多工緩衝處理器，檔會進行多工緩衝處理以進行列印。</span><span class="sxs-lookup"><span data-stu-id="3c233-104">The **StartDocPrinter** function notifies the print spooler that a document is to be spooled for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c233-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c233-105">Syntax</span></span>


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3c233-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c233-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c233-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c233-108">印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3c233-108">A handle to the printer.</span></span> <span data-ttu-id="3c233-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="3c233-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="3c233-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c233-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c233-111">*PDocInfo* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="3c233-111">The version of the structure to which *pDocInfo* points.</span></span> <span data-ttu-id="3c233-112">此值必須是1。</span><span class="sxs-lookup"><span data-stu-id="3c233-112">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="3c233-113">*pDocInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c233-113">*pDocInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c233-114">描述要列印之檔的 [**DOC \_ INFO \_ 1**](doc-info-1.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="3c233-114">A pointer to a [**DOC\_INFO\_1**](doc-info-1.md) structure that describes the document to print.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c233-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c233-115">Return value</span></span>

<span data-ttu-id="3c233-116">如果函式成功，則傳回值會識別列印工作。</span><span class="sxs-lookup"><span data-stu-id="3c233-116">If the function succeeds, the return value identifies the print job.</span></span>

<span data-ttu-id="3c233-117">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="3c233-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c233-118">備註</span><span class="sxs-lookup"><span data-stu-id="3c233-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c233-119">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="3c233-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3c233-120">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="3c233-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3c233-121">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="3c233-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3c233-122">列印工作的一般順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="3c233-122">The typical sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="3c233-123">若要開始列印工作，請呼叫 **StartDocPrinter**。</span><span class="sxs-lookup"><span data-stu-id="3c233-123">To begin a print job, call **StartDocPrinter**.</span></span>
2.  <span data-ttu-id="3c233-124">若要開始每個頁面，請呼叫 [**StartPagePrinter**](startpageprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="3c233-124">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="3c233-125">若要將資料寫入頁面，請呼叫 [**WritePrinter**](writeprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="3c233-125">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="3c233-126">若要結束每個頁面，請呼叫 [**EndPagePrinter**](endpageprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="3c233-126">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="3c233-127">視需要針對任意數量的頁面重複2、3和4。</span><span class="sxs-lookup"><span data-stu-id="3c233-127">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="3c233-128">若要結束列印工作，請呼叫 [**EndDocPrinter**](enddocprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="3c233-128">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="3c233-129">請注意，可能不需要呼叫 [**StartPagePrinter**](startpageprinter.md) 和 [**EndPagePrinter**](endpageprinter.md) ，例如列印資料類型是否包含頁面資訊。</span><span class="sxs-lookup"><span data-stu-id="3c233-129">Note that calling [**StartPagePrinter**](startpageprinter.md) and [**EndPagePrinter**](endpageprinter.md) may not be necessary, such as if the print data type includes the page information.</span></span>

<span data-ttu-id="3c233-130">當多工緩衝處理檔案中的頁面超過大約 350 MB 時，可能會無法列印，且不會傳送錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3c233-130">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="3c233-131">例如，列印大型 EMF 檔案時可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="3c233-131">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="3c233-132">頁面大小限制取決於許多因素，包括可用的虛擬記憶體數量、呼叫進程所配置的記憶體數量，以及進程堆積中的片段量。</span><span class="sxs-lookup"><span data-stu-id="3c233-132">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="3c233-133">範例</span><span class="sxs-lookup"><span data-stu-id="3c233-133">Examples</span></span>

<span data-ttu-id="3c233-134">如需使用此函式的範例程式，請參閱 [如何：使用 GDI 列印 API 進行列印](how-to--print-using-the-gdi-print-api.md)。</span><span class="sxs-lookup"><span data-stu-id="3c233-134">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c233-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c233-135">Requirements</span></span>



| <span data-ttu-id="3c233-136">需求</span><span class="sxs-lookup"><span data-stu-id="3c233-136">Requirement</span></span> | <span data-ttu-id="3c233-137">值</span><span class="sxs-lookup"><span data-stu-id="3c233-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c233-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c233-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3c233-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c233-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c233-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c233-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3c233-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c233-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c233-142">標頭</span><span class="sxs-lookup"><span data-stu-id="3c233-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c233-143"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3c233-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3c233-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c233-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c233-145"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c233-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3c233-146">DLL</span><span class="sxs-lookup"><span data-stu-id="3c233-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c233-147"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="3c233-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3c233-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="3c233-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3c233-149">**StartDocPrinterW** (Unicode) 和 **StartDocPrinterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="3c233-149">**StartDocPrinterW** (Unicode) and **StartDocPrinterA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="3c233-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c233-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c233-151">**System.printing.printqueue.addjob**</span><span class="sxs-lookup"><span data-stu-id="3c233-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="3c233-152">**DOC \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3c233-152">**DOC\_INFO\_1**</span></span>](doc-info-1.md)
</dt> <dt>

[<span data-ttu-id="3c233-153">**DOC \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="3c233-153">**DOC\_INFO\_2**</span></span>](doc-info-2.md)
</dt> <dt>

[<span data-ttu-id="3c233-154">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="3c233-154">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="3c233-155">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="3c233-155">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="3c233-156">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="3c233-156">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3c233-157">列印</span><span class="sxs-lookup"><span data-stu-id="3c233-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3c233-158">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="3c233-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3c233-159">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="3c233-159">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="3c233-160">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="3c233-160">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="3c233-161">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="3c233-161">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




