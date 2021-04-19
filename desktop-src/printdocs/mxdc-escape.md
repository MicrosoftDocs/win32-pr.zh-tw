---
description: MXDC \_ ESCAPE 印表機 escape 函式可讓應用程式透過 MICROSOFT XPS 檔轉換程式 (MXDC) ，以 XML 檔規格 (XPS) 格式將檔寫入檔案或印表機。
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: 'MXDC_ESCAPE 函式 (Mxdc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983621"
---
# <a name="mxdc_escape-function"></a><span data-ttu-id="71be6-103">MXDC \_ ESCAPE 函式</span><span class="sxs-lookup"><span data-stu-id="71be6-103">MXDC\_ESCAPE function</span></span>

<span data-ttu-id="71be6-104">**MXDC \_ ESCAPE** 印表機 escape 函式可讓應用程式透過 Microsoft XPS 檔轉換程式 (MXDC) ，以 XML 檔規格 (XPS) 格式將檔寫入檔案或印表機。</span><span class="sxs-lookup"><span data-stu-id="71be6-104">The **MXDC\_ESCAPE** printer escape function enables applications to write documents to a file or to a printer in XML Paper Specification (XPS) format by means of the Microsoft XPS Document Converter (MXDC).</span></span>

<span data-ttu-id="71be6-105">若要執行這項作業，請使用下列參數呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 函數。</span><span class="sxs-lookup"><span data-stu-id="71be6-105">To perform this operation, call the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function with the following parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="71be6-106">語法</span><span class="sxs-lookup"><span data-stu-id="71be6-106">Syntax</span></span>


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a><span data-ttu-id="71be6-107">參數</span><span class="sxs-lookup"><span data-stu-id="71be6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71be6-108">*hdc*</span><span class="sxs-lookup"><span data-stu-id="71be6-108">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="71be6-109">印表機裝置內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="71be6-109">A handle to the printer device context.</span></span>

</dd> <dt>

<span data-ttu-id="71be6-110">*cbInput*</span><span class="sxs-lookup"><span data-stu-id="71be6-110">*cbInput*</span></span> 
</dt> <dd>

<span data-ttu-id="71be6-111">*LpszInData* 參數所指向之資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="71be6-111">The size, in bytes, of the data pointed to by the *lpszInData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="71be6-112">*lpszInData*</span><span class="sxs-lookup"><span data-stu-id="71be6-112">*lpszInData*</span></span> 
</dt> <dd>

<span data-ttu-id="71be6-113">包含輸入資料之緩衝區的指標，一律會儲存在下列其中一個結構中。</span><span class="sxs-lookup"><span data-stu-id="71be6-113">A pointer to a buffer containing the input data, which is always stored in one of the following structures.</span></span>

<dl> <dd><span data-ttu-id="71be6-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span><span class="sxs-lookup"><span data-stu-id="71be6-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span></span></dd> <dd><span data-ttu-id="71be6-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span><span class="sxs-lookup"><span data-stu-id="71be6-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span></span></dd> <dd><span data-ttu-id="71be6-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span><span class="sxs-lookup"><span data-stu-id="71be6-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span></span></dd> <dd><span data-ttu-id="71be6-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span><span class="sxs-lookup"><span data-stu-id="71be6-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span></span></dd> </dl>

<span data-ttu-id="71be6-118">其中每個結構都有一個 opcode 成員，可指定 MXDC 的用途。</span><span class="sxs-lookup"><span data-stu-id="71be6-118">Each of these structures has an opcode member that specifies what the MXDC is supposed to do.</span></span> <span data-ttu-id="71be6-119">如需這些程式碼的詳細說明，請參閱 MxdcEscapeHeader。</span><span class="sxs-lookup"><span data-stu-id="71be6-119">See MxdcEscapeHeader for detailed remarks about these codes.</span></span>



| <span data-ttu-id="71be6-120">作業程式碼 (opcode) </span><span class="sxs-lookup"><span data-stu-id="71be6-120">Operations code (opcode)</span></span>                                                                                                                                                                                                  | <span data-ttu-id="71be6-121">動作</span><span class="sxs-lookup"><span data-stu-id="71be6-121">Action</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <span data-ttu-id="71be6-122"><dt>**MXDCOP \_ 取得 \_ 檔案名**</dt></span><span class="sxs-lookup"><span data-stu-id="71be6-122"><dt>**MXDCOP\_GET\_FILENAME**</dt></span></span> </dl>                                          | <span data-ttu-id="71be6-123">將 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszOutData* 參數設定為，將輸出檔案的完整路徑設定為以零結尾的字串或該字串的大小。</span><span class="sxs-lookup"><span data-stu-id="71be6-123">Sets the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function to, either the full path of the output file as a zero-terminated string or else the size of that string.</span></span><br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <span data-ttu-id="71be6-124"><dt>**MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ**</dt></span><span class="sxs-lookup"><span data-stu-id="71be6-124"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**</dt></span></span> </dl> | <span data-ttu-id="71be6-125">將列印票證與 XPS 固定檔順序產生關聯。</span><span class="sxs-lookup"><span data-stu-id="71be6-125">Associates a print ticket with an XPS fixed document sequence.</span></span><br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <span data-ttu-id="71be6-126"><dt>**MXDCOP \_ PRINTTICKET \_ 固定 \_ 檔**</dt></span><span class="sxs-lookup"><span data-stu-id="71be6-126"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC**</dt></span></span> </dl>              | <span data-ttu-id="71be6-127">將列印票證與 XPS 檔產生關聯。</span><span class="sxs-lookup"><span data-stu-id="71be6-127">Associates a print ticket with an XPS document.</span></span><br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <span data-ttu-id="71be6-128"><dt>**MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面**</dt></span><span class="sxs-lookup"><span data-stu-id="71be6-128"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_PAGE**</dt></span></span> </dl>           | <span data-ttu-id="71be6-129">將列印票證與 XPS 頁面產生關聯。</span><span class="sxs-lookup"><span data-stu-id="71be6-129">Associates a print ticket with an XPS page.</span></span><br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <span data-ttu-id="71be6-130"><dt>**MXDCOP \_ SET \_ S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="71be6-130"><dt>**MXDCOP\_SET\_S0PAGE**</dt></span></span> </dl>                                                | <span data-ttu-id="71be6-131">將目前頁面的 XPS 標記傳送至輸出。</span><span class="sxs-lookup"><span data-stu-id="71be6-131">Sends the XPS markup of the current page to the output.</span></span><br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <span data-ttu-id="71be6-132"><dt>**MXDCOP \_ 設定 \_ S0PAGE \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="71be6-132"><dt>**MXDCOP\_SET\_S0PAGE\_RESOURCE**</dt></span></span> </dl>                    | <span data-ttu-id="71be6-133">將頁面上的資源（例如影像或字型）傳送至輸出。</span><span class="sxs-lookup"><span data-stu-id="71be6-133">Sends a resource on the page, such as an image or font, to the output.</span></span><br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <span data-ttu-id="71be6-134"><dt>**MXDCOP \_ 設定 \_ XPSPASSTHRU \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="71be6-134"><dt>**MXDCOP\_SET\_XPSPASSTHRU\_MODE**</dt></span></span> </dl>                 | <span data-ttu-id="71be6-135">將 MXDC 放入通過狀態，讓應用程式可以直接將 XPS 寫入輸出檔，而不需要 MXDC 任何處理。</span><span class="sxs-lookup"><span data-stu-id="71be6-135">Puts the MXDC into a pass through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="71be6-136">您可以用這種方式撰寫整份檔或甚至是檔順序。</span><span class="sxs-lookup"><span data-stu-id="71be6-136">An entire document or even document sequence can be written in this way.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="71be6-137">*cbOutput*</span><span class="sxs-lookup"><span data-stu-id="71be6-137">*cbOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="71be6-138">*LpszOutData* 參數所指向之資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="71be6-138">The size, in bytes, of the data pointed to by the *lpszOutData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="71be6-139">*lpszOutData*</span><span class="sxs-lookup"><span data-stu-id="71be6-139">*lpszOutData*</span></span> 
</dt> <dd>

<span data-ttu-id="71be6-140">包含輸出資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="71be6-140">A pointer to a buffer containing the output data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71be6-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="71be6-141">Return value</span></span>

<span data-ttu-id="71be6-142">如果函式成功，則傳回值大於零。</span><span class="sxs-lookup"><span data-stu-id="71be6-142">If the function succeeds, the return value is greater than zero.</span></span> <span data-ttu-id="71be6-143">如果函數失敗或不受支援，則傳回值小於或等於零。</span><span class="sxs-lookup"><span data-stu-id="71be6-143">If the function fails or is not supported, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="71be6-144">備註</span><span class="sxs-lookup"><span data-stu-id="71be6-144">Remarks</span></span>

<span data-ttu-id="71be6-145">MXDC 和 XPSDrv 支援此 escape，但 GDI 不支援。</span><span class="sxs-lookup"><span data-stu-id="71be6-145">This escape is supported by MXDC and XPSDrv, but not by GDI.</span></span>

<span data-ttu-id="71be6-146">若要判斷印表機驅動程式是否為 MXDC，請使用 [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape 來呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 。</span><span class="sxs-lookup"><span data-stu-id="71be6-146">To determine if the printer driver is the MXDC, call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="71be6-147">如果驅動程式是 MXDC，則 **ExtEscape** 會傳回以零結尾的字串 " http://schemas.microsoft.com/xps/2005/06 "。</span><span class="sxs-lookup"><span data-stu-id="71be6-147">If the driver is the MXDC, the **ExtEscape** will return the zero-terminated string, "http://schemas.microsoft.com/xps/2005/06".</span></span> <span data-ttu-id="71be6-148">請確定 *lpszOutData* 參數所參考的緩衝區夠大，足以容納這個字串。</span><span class="sxs-lookup"><span data-stu-id="71be6-148">Be sure the buffer referenced by the *lpszOutData* parameter is large enough to hold this string.</span></span>

<span data-ttu-id="71be6-149">若要判斷印表機驅動程式是否為 Windows 內建的 Microsoft XPS 檔寫入器驅動程式，請確認印表機驅動程式是否為 MXDC，然後判斷印表機驅動程式的名稱是否為 "Microsoft XPS Document Writer"。</span><span class="sxs-lookup"><span data-stu-id="71be6-149">To determine if the printer driver is the Windows in-box Microsoft XPS Document Writer driver, confirm that the printer driver is the MXDC, and then determine whether the name of the printer driver is "Microsoft XPS Document Writer".</span></span>

<span data-ttu-id="71be6-150">若要取得印表機驅動程式名稱，請使用下列其中一種技術。</span><span class="sxs-lookup"><span data-stu-id="71be6-150">To get the printer driver name, use one of the following techniques.</span></span> <dl> <span data-ttu-id="71be6-151">將 *Level* 參數值設定為1時，呼叫 [**GetPrinterDriver**](getprinterdriver.md) 。</span><span class="sxs-lookup"><span data-stu-id="71be6-151">Call [**GetPrinterDriver**](getprinterdriver.md) with the *Level* parameter value set to 1.</span></span> <span data-ttu-id="71be6-152">[**驅動程式 \_ 資訊 \_ 1**](driver-info-1.md)結構的 **pName** 成員會傳回印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="71be6-152">The printer driver name is returned in the **pName** member of the [**DRIVER\_INFO\_1**](driver-info-1.md) structure.</span></span>  
<span data-ttu-id="71be6-153">或</span><span class="sxs-lookup"><span data-stu-id="71be6-153">or</span></span>  
<span data-ttu-id="71be6-154">將 *Level* 參數值設定為2時，呼叫 [**GetPrinter**](getprinter.md) 。</span><span class="sxs-lookup"><span data-stu-id="71be6-154">Call [**GetPrinter**](getprinter.md) with the *Level* parameter value set to 2.</span></span> <span data-ttu-id="71be6-155">印表機驅動程式名稱會傳回在 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構的 **pDriverName** 成員中。</span><span class="sxs-lookup"><span data-stu-id="71be6-155">The printer driver name is returned in the **pDriverName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>  
</dl>

<span data-ttu-id="71be6-156">下表顯示在 XPS 檔案中尋找各種物件的位置，將會在其中寫入各種類型的物件。</span><span class="sxs-lookup"><span data-stu-id="71be6-156">The following table shows where to find various objects in the XPS file various types of objects will be written.</span></span>



| <span data-ttu-id="71be6-157">Object</span><span class="sxs-lookup"><span data-stu-id="71be6-157">Object</span></span>       | <span data-ttu-id="71be6-158">輸出檔中的位置</span><span class="sxs-lookup"><span data-stu-id="71be6-158">Location in the output file</span></span>    |
|--------------|--------------------------------|
| <span data-ttu-id="71be6-159">固定頁面</span><span class="sxs-lookup"><span data-stu-id="71be6-159">Fixed Page</span></span>   | <span data-ttu-id="71be6-160">/Documents/1/Pages/Esc%d.fpage</span><span class="sxs-lookup"><span data-stu-id="71be6-160">/Documents/1/Pages/Esc%d.fpage</span></span> |
| <span data-ttu-id="71be6-161">縮圖</span><span class="sxs-lookup"><span data-stu-id="71be6-161">Thumbnail</span></span>    | <span data-ttu-id="71be6-162">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="71be6-162">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="71be6-163">列印票證</span><span class="sxs-lookup"><span data-stu-id="71be6-163">Print Ticket</span></span> | <span data-ttu-id="71be6-164">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="71be6-164">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="71be6-165">字型</span><span class="sxs-lookup"><span data-stu-id="71be6-165">Font</span></span>         | <span data-ttu-id="71be6-166">/Documents/1/Resources/Fonts</span><span class="sxs-lookup"><span data-stu-id="71be6-166">/Documents/1/Resources/Fonts</span></span>   |
| <span data-ttu-id="71be6-167">Image</span><span class="sxs-lookup"><span data-stu-id="71be6-167">Image</span></span>        | <span data-ttu-id="71be6-168">/Documents/1/Resources/Images</span><span class="sxs-lookup"><span data-stu-id="71be6-168">/Documents/1/Resources/Images</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="71be6-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="71be6-169">Requirements</span></span>



| <span data-ttu-id="71be6-170">需求</span><span class="sxs-lookup"><span data-stu-id="71be6-170">Requirement</span></span> | <span data-ttu-id="71be6-171">值</span><span class="sxs-lookup"><span data-stu-id="71be6-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71be6-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71be6-172">Minimum supported client</span></span><br/> | <span data-ttu-id="71be6-173">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71be6-173">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71be6-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71be6-174">Minimum supported server</span></span><br/> | <span data-ttu-id="71be6-175">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71be6-175">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71be6-176">標頭</span><span class="sxs-lookup"><span data-stu-id="71be6-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="71be6-177"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="71be6-177"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71be6-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71be6-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71be6-179">列印</span><span class="sxs-lookup"><span data-stu-id="71be6-179">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

<span data-ttu-id="71be6-180">[印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71be6-180">[Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="71be6-181">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="71be6-181">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

