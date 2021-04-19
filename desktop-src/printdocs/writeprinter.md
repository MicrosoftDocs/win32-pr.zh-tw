---
description: WritePrinter 函數會通知列印多工緩衝處理器，資料應該寫入指定的印表機。
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: 'WritePrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975118"
---
# <a name="writeprinter-function"></a><span data-ttu-id="e153c-103">WritePrinter 函式</span><span class="sxs-lookup"><span data-stu-id="e153c-103">WritePrinter function</span></span>

<span data-ttu-id="e153c-104">**WritePrinter** 函數會通知列印多工緩衝處理器，資料應該寫入指定的印表機。</span><span class="sxs-lookup"><span data-stu-id="e153c-104">The **WritePrinter** function notifies the print spooler that data should be written to the specified printer.</span></span>

> [!Note]  
> <span data-ttu-id="e153c-105">**WritePrinter** 只支援 GDI 列印，且不能用於 XPS 列印。</span><span class="sxs-lookup"><span data-stu-id="e153c-105">**WritePrinter** only supports GDI printing and must not be used for XPS printing.</span></span> <span data-ttu-id="e153c-106">如果您的列印工作使用 XPS 或 OpenXPS 列印路徑，請使用 [Xps 列印 API](/windows/desktop/printdocs/xps-printing)。</span><span class="sxs-lookup"><span data-stu-id="e153c-106">If your print job uses the XPS or the OpenXPS print path, then use the [XPS Print API](/windows/desktop/printdocs/xps-printing).</span></span> <span data-ttu-id="e153c-107">不支援使用 **WritePrinter** 將 XPS 或 OpenXPS 列印工作傳送至多工緩衝處理器，而且可能會導致無法確定的結果。</span><span class="sxs-lookup"><span data-stu-id="e153c-107">Sending XPS or OpenXPS print jobs to the spooler using **WritePrinter** is not supported and can result in undetermined results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e153c-108">語法</span><span class="sxs-lookup"><span data-stu-id="e153c-108">Syntax</span></span>


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a><span data-ttu-id="e153c-109">參數</span><span class="sxs-lookup"><span data-stu-id="e153c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e153c-110">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e153c-110">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e153c-111">印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e153c-111">A handle to the printer.</span></span> <span data-ttu-id="e153c-112">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="e153c-112">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e153c-113">*pBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e153c-113">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e153c-114">位元組陣列的指標，其中包含應寫入印表機的資料。</span><span class="sxs-lookup"><span data-stu-id="e153c-114">A pointer to an array of bytes that contains the data that should be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="e153c-115">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e153c-115">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e153c-116">陣列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e153c-116">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="e153c-117">*pcWritten* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e153c-117">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e153c-118">值的指標，此值會接收寫入至印表機的資料位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e153c-118">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e153c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e153c-119">Return value</span></span>

<span data-ttu-id="e153c-120">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="e153c-120">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e153c-121">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e153c-121">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e153c-122">備註</span><span class="sxs-lookup"><span data-stu-id="e153c-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e153c-123">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e153c-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e153c-124">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="e153c-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e153c-125">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="e153c-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e153c-126">列印工作的順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="e153c-126">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="e153c-127">若要開始列印工作，請呼叫 [**StartDocPrinter**](startdocprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="e153c-127">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="e153c-128">若要開始每個頁面，請呼叫 [**StartPagePrinter**](startpageprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="e153c-128">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="e153c-129">若要將資料寫入頁面，請呼叫 **WritePrinter**。</span><span class="sxs-lookup"><span data-stu-id="e153c-129">To write data to a page, call **WritePrinter**.</span></span>
4.  <span data-ttu-id="e153c-130">若要結束每個頁面，請呼叫 [**EndPagePrinter**](endpageprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="e153c-130">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="e153c-131">視需要針對任意數量的頁面重複2、3和4。</span><span class="sxs-lookup"><span data-stu-id="e153c-131">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="e153c-132">若要結束列印工作，請呼叫 [**EndDocPrinter**](enddocprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="e153c-132">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="e153c-133">當高階檔 (（例如 Adobe PDF 或 Microsoft Word 檔案）) 或其他印表機資料 (這類 PCL、PS 或 HPGL) 直接傳送到印表機時，檔中定義的列印設定會優先于 Windows 列印設定。</span><span class="sxs-lookup"><span data-stu-id="e153c-133">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer, the print settings defined in the document take precedent over Windows print settings.</span></span> <span data-ttu-id="e153c-134">當在 [**StartDocPrinter**](startdocprinter.md)呼叫的 *pDocInfo* 參數中傳遞的 [**DOC \_ INFO \_ 1**](doc-info-1.md)結構之 *pDatatype* 成員的值為「未經處理」時，檔會輸出，必須完整地以硬體理解的語言描述 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)樣式的列印工作設定。</span><span class="sxs-lookup"><span data-stu-id="e153c-134">Documents output when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW" must fully describe the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="e153c-135">在 Windows XP 之前的 Windows 版本中，當多工緩衝處理檔案中的頁面超過大約 350 MB 時，可能會無法列印，且不會傳送錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e153c-135">In versions of Windows prior to Windows XP, when a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="e153c-136">例如，列印大型 EMF 檔案時可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e153c-136">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="e153c-137">Windows XP 之前的 Windows 版本中的頁面大小限制取決於許多因素，包括可用的虛擬記憶體數量、呼叫進程所配置的記憶體數量，以及進程堆積中的片段量。</span><span class="sxs-lookup"><span data-stu-id="e153c-137">The page size limit in versions of Windows prior to Windows XP depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span> <span data-ttu-id="e153c-138">在 Windows XP 和更新版本的 Windows 中，EMF 檔案的大小必須小於或等於2GB。</span><span class="sxs-lookup"><span data-stu-id="e153c-138">In Windows XP and later versions of Windows, EMF files must be 2GB or less in size.</span></span> <span data-ttu-id="e153c-139">如果使用 **WritePrinter** 來寫入非 EMF 資料（例如印表機就緒的 PDL），檔案的大小只受限於可用磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="e153c-139">If **WritePrinter** is used to write non EMF data, such as printer-ready PDL, the size of the file is limited only by the available disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="e153c-140">範例</span><span class="sxs-lookup"><span data-stu-id="e153c-140">Examples</span></span>

<span data-ttu-id="e153c-141">如需使用此函式的範例程式，請參閱 [如何：使用 GDI 列印 API 進行列印](how-to--print-using-the-gdi-print-api.md)。</span><span class="sxs-lookup"><span data-stu-id="e153c-141">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e153c-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="e153c-142">Requirements</span></span>



| <span data-ttu-id="e153c-143">需求</span><span class="sxs-lookup"><span data-stu-id="e153c-143">Requirement</span></span> | <span data-ttu-id="e153c-144">值</span><span class="sxs-lookup"><span data-stu-id="e153c-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e153c-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e153c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e153c-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e153c-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e153c-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e153c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e153c-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e153c-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e153c-149">標頭</span><span class="sxs-lookup"><span data-stu-id="e153c-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e153c-150"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e153c-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e153c-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="e153c-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="e153c-152"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e153c-152"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e153c-153">DLL</span><span class="sxs-lookup"><span data-stu-id="e153c-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e153c-154"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e153c-154"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e153c-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e153c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e153c-156">列印</span><span class="sxs-lookup"><span data-stu-id="e153c-156">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e153c-157">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="e153c-157">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e153c-158">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="e153c-158">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="e153c-159">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="e153c-159">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="e153c-160">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e153c-160">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e153c-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="e153c-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="e153c-162">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="e153c-162">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="e153c-163">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="e153c-163">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

