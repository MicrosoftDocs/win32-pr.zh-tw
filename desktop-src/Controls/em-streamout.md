---
title: 'EM_STREAMOUT 訊息 (Richedit .h) '
description: 讓 rich edit 控制項將其內容傳遞至應用程式 \ 8211; 定義的 EditStreamCallback 回呼函式。 回呼函數接著可以將資料串流寫入檔案或它所選擇的任何其他位置。
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934417"
---
# <a name="em_streamout-message"></a><span data-ttu-id="f96b0-105">EM \_ STREAMOUT 訊息</span><span class="sxs-lookup"><span data-stu-id="f96b0-105">EM\_STREAMOUT message</span></span>

<span data-ttu-id="f96b0-106">讓 rich edit 控制項將其內容傳遞至應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f96b0-106">Causes a rich edit control to pass its contents to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span> <span data-ttu-id="f96b0-107">回呼函數接著可以將資料串流寫入檔案或它所選擇的任何其他位置。</span><span class="sxs-lookup"><span data-stu-id="f96b0-107">The callback function can then write the stream of data to a file or any other location that it chooses.</span></span>

## <a name="parameters"></a><span data-ttu-id="f96b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="f96b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f96b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f96b0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f96b0-110">指定資料格式和取代選項。</span><span class="sxs-lookup"><span data-stu-id="f96b0-110">Specifies the data format and replacement options.</span></span>

<span data-ttu-id="f96b0-111">此值必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f96b0-111">This value must be one of the following values.</span></span>



| <span data-ttu-id="f96b0-112">值</span><span class="sxs-lookup"><span data-stu-id="f96b0-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="f96b0-113">意義</span><span class="sxs-lookup"><span data-stu-id="f96b0-113">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="f96b0-114"><dt>**SF \_ RTF**</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-114"><dt>**SF\_RTF**</dt></span></span> </dl>                   | <span data-ttu-id="f96b0-115">Rtf。</span><span class="sxs-lookup"><span data-stu-id="f96b0-115">RTF.</span></span><br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <span data-ttu-id="f96b0-116"><dt>**SF \_ RTFNOOBJS**</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-116"><dt>**SF\_RTFNOOBJS**</dt></span></span> </dl> | <span data-ttu-id="f96b0-117">以空格取代 COM 物件的 RTF。</span><span class="sxs-lookup"><span data-stu-id="f96b0-117">RTF with spaces in place of COM objects.</span></span><br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="f96b0-118"><dt>**SF \_ 文字**</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-118"><dt>**SF\_TEXT**</dt></span></span> </dl>                | <span data-ttu-id="f96b0-119">具有空格的文字，用來取代 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="f96b0-119">Text with spaces in place of COM objects.</span></span><br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <span data-ttu-id="f96b0-120"><dt>**SF \_ TEXTIZED**</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-120"><dt>**SF\_TEXTIZED**</dt></span></span> </dl>    | <span data-ttu-id="f96b0-121">具有 COM 物件文字表示的文字。</span><span class="sxs-lookup"><span data-stu-id="f96b0-121">Text with a text representation of COM objects.</span></span><br/> |



 

<span data-ttu-id="f96b0-122">如果應用程式儲存 COM 物件本身， **SF \_ RTFNOOBJS** 選項會很有用，因為 RTF 表示 com 物件並不太精簡。</span><span class="sxs-lookup"><span data-stu-id="f96b0-122">The **SF\_RTFNOOBJS** option is useful if an application stores COM objects itself, as RTF representation of COM objects is not very compact.</span></span> <span data-ttu-id="f96b0-123">\\Objattph，後面接著一個空格的控制字代表物件位置。</span><span class="sxs-lookup"><span data-stu-id="f96b0-123">The control word, \\objattph, followed by a space denotes the object position.</span></span>

<span data-ttu-id="f96b0-124">此外，您可以指定下列旗標。</span><span class="sxs-lookup"><span data-stu-id="f96b0-124">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="f96b0-125">值</span><span class="sxs-lookup"><span data-stu-id="f96b0-125">Value</span></span>                                                                                                                                                            | <span data-ttu-id="f96b0-126">意義</span><span class="sxs-lookup"><span data-stu-id="f96b0-126">Meaning</span></span>                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="f96b0-127"><dt>**SFF \_ PLAINRTF**</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-127"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>       | <span data-ttu-id="f96b0-128">如果有指定，rich edit 控制項會只串流所有語言通用的關鍵字，並忽略語言特定關鍵字。</span><span class="sxs-lookup"><span data-stu-id="f96b0-128">If specified, the rich edit control streams out only the keywords common to all languages, ignoring language-specific keywords.</span></span> <span data-ttu-id="f96b0-129">如果未指定，rich edit 控制項會串流所有關鍵詞。</span><span class="sxs-lookup"><span data-stu-id="f96b0-129">If not specified, the rich edit control streams out all keywords.</span></span> <span data-ttu-id="f96b0-130">您可以結合此旗標與 **sf \_ RTF** 或 **sf \_ RTFNOOBJS** 旗標。</span><span class="sxs-lookup"><span data-stu-id="f96b0-130">You can combine this flag with the **SF\_RTF** or **SF\_RTFNOOBJS** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="f96b0-131"><dt>**SFF \_ 選取專案**</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-131"><dt>**SFF\_SELECTION**</dt></span></span> </dl>    | <span data-ttu-id="f96b0-132">如果有指定，rich edit 控制項會只串流目前選取範圍的內容。</span><span class="sxs-lookup"><span data-stu-id="f96b0-132">If specified, the rich edit control streams out only the contents of the current selection.</span></span> <span data-ttu-id="f96b0-133">如果未指定，控制項會串流處理整個內容。</span><span class="sxs-lookup"><span data-stu-id="f96b0-133">If not specified, the control streams out the entire contents.</span></span> <span data-ttu-id="f96b0-134">您可以結合此旗標與任何資料格式值。</span><span class="sxs-lookup"><span data-stu-id="f96b0-134">You can combine this flag with any of data format values.</span></span><br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="f96b0-135"><dt>**SF \_ UNICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-135"><dt>**SF\_UNICODE**</dt></span></span> </dl>             | <span data-ttu-id="f96b0-136">**Microsoft Rich Edit 2.0 和更新版本：** 指出 Unicode 文字。</span><span class="sxs-lookup"><span data-stu-id="f96b0-136">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="f96b0-137">您可以結合此旗標與 **SF \_ 文字** 旗標。</span><span class="sxs-lookup"><span data-stu-id="f96b0-137">You can combine this flag with the **SF\_TEXT** flag.</span></span><br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <span data-ttu-id="f96b0-138"><dt>**SF \_ USECODEPAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-138"><dt>**SF\_USECODEPAGE**</dt></span></span> </dl> | <span data-ttu-id="f96b0-139">**Rich Edit 3.0 和更新版本：** 使用其他字碼頁產生 UTF-8 RTF 以及文字。</span><span class="sxs-lookup"><span data-stu-id="f96b0-139">**Rich Edit 3.0 and later:** Generates UTF-8 RTF as well as text using other code pages.</span></span> <span data-ttu-id="f96b0-140">字碼頁是在 *wParam* 的最高字組中設定。</span><span class="sxs-lookup"><span data-stu-id="f96b0-140">The code page is set in the high word of *wParam*.</span></span> <span data-ttu-id="f96b0-141">例如，若是 UTF-8 RTF，請將 *wParam* 設定為 (CP \_ UTF8 << 16) \| sf \_ USECODEPAGE \| sf \_ RTF。</span><span class="sxs-lookup"><span data-stu-id="f96b0-141">For example, for UTF-8 RTF, set *wParam* to (CP\_UTF8 << 16) \| SF\_USECODEPAGE \| SF\_RTF.</span></span><br/>                               |



 

</dd> <dt>

<span data-ttu-id="f96b0-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f96b0-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f96b0-143">[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f96b0-143">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="f96b0-144">在輸入時，此結構的 **pfnCallback** 成員必須指向應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 函數。</span><span class="sxs-lookup"><span data-stu-id="f96b0-144">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="f96b0-145">在輸出中，如果發生錯誤， **dwError** 成員可以包含非零的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f96b0-145">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f96b0-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="f96b0-146">Return value</span></span>

<span data-ttu-id="f96b0-147">此訊息會傳回寫入至資料流程的字元數。</span><span class="sxs-lookup"><span data-stu-id="f96b0-147">This message returns the number of characters written to the data stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="f96b0-148">備註</span><span class="sxs-lookup"><span data-stu-id="f96b0-148">Remarks</span></span>

<span data-ttu-id="f96b0-149">當您傳送 **EM \_ STREAMOUT** 訊息時，rich Edit 控制項會對 [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的 **pfnCallback** 成員所指定的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)函數進行重複呼叫。</span><span class="sxs-lookup"><span data-stu-id="f96b0-149">When you send an **EM\_STREAMOUT** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="f96b0-150">每次呼叫回呼函式時，控制項都會傳遞包含控制項內容部分的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f96b0-150">Each time it calls the callback function, the control passes a buffer containing a portion of the contents of the control.</span></span> <span data-ttu-id="f96b0-151">此程式會繼續進行，直到控制項將其所有內容都傳遞給回呼函式，或直到發生錯誤為止。</span><span class="sxs-lookup"><span data-stu-id="f96b0-151">This process continues until the control has passed all its contents to the callback function, or until an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f96b0-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="f96b0-152">Requirements</span></span>



| <span data-ttu-id="f96b0-153">需求</span><span class="sxs-lookup"><span data-stu-id="f96b0-153">Requirement</span></span> | <span data-ttu-id="f96b0-154">值</span><span class="sxs-lookup"><span data-stu-id="f96b0-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f96b0-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f96b0-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f96b0-156">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f96b0-156">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f96b0-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f96b0-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f96b0-158">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f96b0-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f96b0-159">標頭</span><span class="sxs-lookup"><span data-stu-id="f96b0-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="f96b0-160"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f96b0-160"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f96b0-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f96b0-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="f96b0-162">**參考**</span><span class="sxs-lookup"><span data-stu-id="f96b0-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f96b0-163">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="f96b0-163">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="f96b0-164">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="f96b0-164">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="f96b0-165">**EM \_ STREAMIN**</span><span class="sxs-lookup"><span data-stu-id="f96b0-165">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





