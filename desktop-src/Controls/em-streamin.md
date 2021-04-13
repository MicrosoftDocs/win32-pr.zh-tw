---
title: 'EM_STREAMIN 訊息 (Richedit .h) '
description: 以定義為 \ 8211 的應用程式所提供的資料流程，取代 rich edit 控制項的內容。EditStreamCallback 回呼函數。
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN message Windows 控制項
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466348"
---
# <a name="em_streamin-message"></a><span data-ttu-id="a057a-104">EM \_ STREAMIN 訊息</span><span class="sxs-lookup"><span data-stu-id="a057a-104">EM\_STREAMIN message</span></span>

<span data-ttu-id="a057a-105">以應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 回呼函式所提供的資料流程，取代 rich edit 控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="a057a-105">Replaces the contents of a rich edit control with a stream of data provided by an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span>

## <a name="parameters"></a><span data-ttu-id="a057a-106">參數</span><span class="sxs-lookup"><span data-stu-id="a057a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a057a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a057a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a057a-108">指定資料格式和取代選項。</span><span class="sxs-lookup"><span data-stu-id="a057a-108">Specifies the data format and replacement options.</span></span> <span data-ttu-id="a057a-109">此值必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a057a-109">This value must be one of the following values.</span></span>



| <span data-ttu-id="a057a-110">值</span><span class="sxs-lookup"><span data-stu-id="a057a-110">Value</span></span>                                                                                                                                       | <span data-ttu-id="a057a-111">意義</span><span class="sxs-lookup"><span data-stu-id="a057a-111">Meaning</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="a057a-112"><dt>**SF \_ RTF**</dt></span><span class="sxs-lookup"><span data-stu-id="a057a-112"><dt>**SF\_RTF**</dt></span></span> </dl>    | <span data-ttu-id="a057a-113">RTF</span><span class="sxs-lookup"><span data-stu-id="a057a-113">RTF</span></span><br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="a057a-114"><dt>**SF \_ 文字**</dt></span><span class="sxs-lookup"><span data-stu-id="a057a-114"><dt>**SF\_TEXT**</dt></span></span> </dl> | <span data-ttu-id="a057a-115">Text</span><span class="sxs-lookup"><span data-stu-id="a057a-115">Text</span></span><br/> |



 

<span data-ttu-id="a057a-116">此外，您可以指定下列旗標。</span><span class="sxs-lookup"><span data-stu-id="a057a-116">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="a057a-117">值</span><span class="sxs-lookup"><span data-stu-id="a057a-117">Value</span></span>                                                                                                                                                         | <span data-ttu-id="a057a-118">意義</span><span class="sxs-lookup"><span data-stu-id="a057a-118">Meaning</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="a057a-119"><dt>**SFF \_ PLAINRTF**</dt></span><span class="sxs-lookup"><span data-stu-id="a057a-119"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>    | <span data-ttu-id="a057a-120">如果指定，則只會在中串流處理所有語言通用的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="a057a-120">If specified, only keywords common to all languages are streamed in.</span></span> <span data-ttu-id="a057a-121">資料流程中的語言特定 RTF 關鍵字會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a057a-121">Language-specific RTF keywords in the stream are ignored.</span></span> <span data-ttu-id="a057a-122">如果未指定，則會在中串流處理所有關鍵詞。</span><span class="sxs-lookup"><span data-stu-id="a057a-122">If not specified, all keywords are streamed in.</span></span> <span data-ttu-id="a057a-123">您可以結合此旗標與 **SF \_ RTF** 旗標。</span><span class="sxs-lookup"><span data-stu-id="a057a-123">You can combine this flag with the **SF\_RTF** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="a057a-124"><dt>**SFF \_ 選取專案**</dt></span><span class="sxs-lookup"><span data-stu-id="a057a-124"><dt>**SFF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="a057a-125">如果有指定，資料流程會取代目前選取範圍的內容。</span><span class="sxs-lookup"><span data-stu-id="a057a-125">If specified, the data stream replaces the contents of the current selection.</span></span> <span data-ttu-id="a057a-126">如果未指定，資料流程會取代控制項的整個內容。</span><span class="sxs-lookup"><span data-stu-id="a057a-126">If not specified, the data stream replaces the entire contents of the control.</span></span> <span data-ttu-id="a057a-127">您可以結合此旗標與 **sf \_ TEXT** 或 **sf \_ rtf** 旗標。</span><span class="sxs-lookup"><span data-stu-id="a057a-127">You can combine this flag with the **SF\_TEXT** or **SF\_RTF** flags.</span></span><br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="a057a-128"><dt>**SF \_ UNICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="a057a-128"><dt>**SF\_UNICODE**</dt></span></span> </dl>          | <span data-ttu-id="a057a-129">**Microsoft Rich Edit 2.0 和更新版本：** 指出 Unicode 文字。</span><span class="sxs-lookup"><span data-stu-id="a057a-129">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="a057a-130">您可以結合此旗標與 **SF \_ 文字** 旗標。</span><span class="sxs-lookup"><span data-stu-id="a057a-130">You can combine this flag with the **SF\_TEXT** flag.</span></span> <br/>                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="a057a-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a057a-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a057a-132">[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a057a-132">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="a057a-133">在輸入時，此結構的 **pfnCallback** 成員必須指向應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 函數。</span><span class="sxs-lookup"><span data-stu-id="a057a-133">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="a057a-134">在輸出中，如果發生錯誤， **dwError** 成員可以包含非零的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a057a-134">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a057a-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="a057a-135">Return value</span></span>

<span data-ttu-id="a057a-136">此訊息會傳回讀取的字元數。</span><span class="sxs-lookup"><span data-stu-id="a057a-136">This message returns the number of characters read.</span></span>

## <a name="remarks"></a><span data-ttu-id="a057a-137">備註</span><span class="sxs-lookup"><span data-stu-id="a057a-137">Remarks</span></span>

<span data-ttu-id="a057a-138">當您傳送 **EM \_ STREAMIN** 訊息時，rich Edit 控制項會對 [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的 **pfnCallback** 成員所指定的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)函數進行重複呼叫。</span><span class="sxs-lookup"><span data-stu-id="a057a-138">When you send an **EM\_STREAMIN** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="a057a-139">每次呼叫回呼函式時，就會將資料填入緩衝區，以讀取控制項。</span><span class="sxs-lookup"><span data-stu-id="a057a-139">Each time the callback function is called, it fills a buffer with data to read into the control.</span></span> <span data-ttu-id="a057a-140">這會繼續進行，直到回呼函式指出資料流程進行中的作業已完成或發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a057a-140">This continues until the callback function indicates that the stream-in operation has been completed or an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a057a-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="a057a-141">Requirements</span></span>



| <span data-ttu-id="a057a-142">需求</span><span class="sxs-lookup"><span data-stu-id="a057a-142">Requirement</span></span> | <span data-ttu-id="a057a-143">值</span><span class="sxs-lookup"><span data-stu-id="a057a-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a057a-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a057a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a057a-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a057a-145">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a057a-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a057a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a057a-147">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a057a-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a057a-148">標頭</span><span class="sxs-lookup"><span data-stu-id="a057a-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="a057a-149"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a057a-149"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a057a-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a057a-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="a057a-151">**參考**</span><span class="sxs-lookup"><span data-stu-id="a057a-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a057a-152">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="a057a-152">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="a057a-153">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="a057a-153">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="a057a-154">**EM \_ STREAMOUT**</span><span class="sxs-lookup"><span data-stu-id="a057a-154">**EM\_STREAMOUT**</span></span>](em-streamout.md)
</dt> </dl>

 

 





