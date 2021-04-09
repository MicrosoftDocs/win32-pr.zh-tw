---
title: 'EM_SETTEXTMODE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的文字模式或復原層級。 如果控制項包含任何文字，則訊息會失敗。
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934543"
---
# <a name="em_settextmode-message"></a><span data-ttu-id="bd2f1-105">EM \_ SETTEXTMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="bd2f1-105">EM\_SETTEXTMODE message</span></span>

<span data-ttu-id="bd2f1-106">設定 rich edit 控制項的文字模式或復原層級。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-106">Sets the text mode or undo level of a rich edit control.</span></span> <span data-ttu-id="bd2f1-107">如果控制項包含任何文字，則訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-107">The message fails if the control contains any text.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd2f1-108">參數</span><span class="sxs-lookup"><span data-stu-id="bd2f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd2f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd2f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd2f1-110">[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)列舉型別中的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-110">One or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="bd2f1-111">這些值會指定控制項的文字模式和復原層級參數的新設定。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-111">The values specify the new settings for the control's text mode and undo level parameters.</span></span>

<span data-ttu-id="bd2f1-112">指定下列其中一個值來設定文字模式參數。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-112">Specify one of the following values to set the text mode parameter.</span></span> <span data-ttu-id="bd2f1-113">如果您未指定文字模式值，文字模式會維持在其目前的設定中。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-113">If you do not specify a text mode value, the text mode remains at its current setting.</span></span> 

| <span data-ttu-id="bd2f1-114">值</span><span class="sxs-lookup"><span data-stu-id="bd2f1-114">Value</span></span>                                          | <span data-ttu-id="bd2f1-115">意義</span><span class="sxs-lookup"><span data-stu-id="bd2f1-115">Meaning</span></span>                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd2f1-116">**TM \_ 純文字**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-116">**TM\_PLAINTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="bd2f1-117">表示純文字模式，在此模式中，控制項類似于標準編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-117">Indicates plain text mode, in which the control is similar to a standard edit control.</span></span> <span data-ttu-id="bd2f1-118">如需純文字模式的詳細資訊，請參閱下列備註一節。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-118">For more information about plain text mode, see the following Remarks section.</span></span> |
| [<span data-ttu-id="bd2f1-119">**TM \_ RICHTEXT**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-119">**TM\_RICHTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="bd2f1-120">指出 rich text 模式，其中控制項具有標準的豐富編輯功能。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-120">Indicates rich text mode, in which the control has standard rich edit functionality.</span></span> <span data-ttu-id="bd2f1-121">Rich text 模式是預設設定。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-121">Rich text mode is the default setting.</span></span>                                           |



 

<span data-ttu-id="bd2f1-122">指定下列其中一個值來設定復原層級參數。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-122">Specify one of the following values to set the undo level parameter.</span></span> <span data-ttu-id="bd2f1-123">如果您沒有指定復原層級值，復原層級會維持在其目前的設定中。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-123">If you do not specify an undo level value, the undo level remains at its current setting.</span></span> 

| <span data-ttu-id="bd2f1-124">值</span><span class="sxs-lookup"><span data-stu-id="bd2f1-124">Value</span></span>                                                      | <span data-ttu-id="bd2f1-125">意義</span><span class="sxs-lookup"><span data-stu-id="bd2f1-125">Meaning</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd2f1-126">**TM \_ SINGLELEVELUNDO**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-126">**TM\_SINGLELEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="bd2f1-127">控制項可讓使用者只復原可以復原的最後一個動作。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-127">The control allows the user to undo only the last action that can be undone.</span></span>                                                                                                       |
| [<span data-ttu-id="bd2f1-128">**TM \_ MULTILEVELUNDO**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-128">**TM\_MULTILEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="bd2f1-129">控制項支援多個復原作業。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-129">The control supports multiple undo operations.</span></span> <span data-ttu-id="bd2f1-130">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-130">This is the default setting.</span></span> <span data-ttu-id="bd2f1-131">使用 [**EM \_ SETUNDOLIMIT**](em-setundolimit.md) 訊息來設定復原動作的最大數目。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-131">Use the [**EM\_SETUNDOLIMIT**](em-setundolimit.md) message to set the maximum number of undo actions.</span></span> |



 

<span data-ttu-id="bd2f1-132">指定下列其中一個值來設定字碼頁參數。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-132">Specify one of the following values to set the code page parameter.</span></span> <span data-ttu-id="bd2f1-133">如果您未指定字碼頁的值，字碼頁會維持在其目前的設定中。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-133">If you do not specify an code page value, the code page remains at its current setting.</span></span> 

| <span data-ttu-id="bd2f1-134">值</span><span class="sxs-lookup"><span data-stu-id="bd2f1-134">Value</span></span>                                                    | <span data-ttu-id="bd2f1-135">意義</span><span class="sxs-lookup"><span data-stu-id="bd2f1-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd2f1-136">**TM \_ SINGLECODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-136">**TM\_SINGLECODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="bd2f1-137">控制項只允許與預設字元集對應的英文鍵盤和鍵盤。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-137">The control only allows the English keyboard and a keyboard corresponding to the default character set.</span></span> <span data-ttu-id="bd2f1-138">例如，您可以有希臘文和英文。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-138">For example, you could have Greek and English.</span></span> <span data-ttu-id="bd2f1-139">請注意，這可防止 Unicode 文字輸入控制項。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-139">Note that this prevents Unicode text from entering the control.</span></span> <span data-ttu-id="bd2f1-140">例如，如果 Rich Edit 控制項必須限制為 ANSI 文字，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-140">For example, use this value if a Rich Edit control must be restricted to ANSI text.</span></span> |
| [<span data-ttu-id="bd2f1-141">**TM \_ MULTICODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-141">**TM\_MULTICODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="bd2f1-142">控制項允許在控制項中有多個字碼頁和 Unicode 文字。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-142">The control allows multiple code pages and Unicode text into the control.</span></span> <span data-ttu-id="bd2f1-143">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-143">This is the default setting.</span></span>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="bd2f1-144">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd2f1-144">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd2f1-145">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-145">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd2f1-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd2f1-146">Return value</span></span>

<span data-ttu-id="bd2f1-147">如果訊息成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-147">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="bd2f1-148">如果訊息失敗，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-148">If the message fails, the return value is a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd2f1-149">備註</span><span class="sxs-lookup"><span data-stu-id="bd2f1-149">Remarks</span></span>

<span data-ttu-id="bd2f1-150">在豐富的文字模式中，豐富的編輯控制項具有標準的豐富編輯功能。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-150">In rich text mode, a rich edit control has standard rich edit functionality.</span></span> <span data-ttu-id="bd2f1-151">不過，在純文字模式中，控制項類似于標準編輯控制項：</span><span class="sxs-lookup"><span data-stu-id="bd2f1-151">However, in plain text mode, the control is similar to a standard edit control:</span></span>

-   <span data-ttu-id="bd2f1-152">純文字控制項中的文字只能有一個格式 (例如粗體、10pt 的 Arial) 。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-152">The text in a plain text control can have only one format (such as Bold, 10pt Arial).</span></span>
-   <span data-ttu-id="bd2f1-153">使用者無法將 rich text (格式（例如 rtf) 或内嵌物件）貼入純文字控制項。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-153">The user cannot paste rich text formats, such as Rich Text Format (RTF) or embedded objects into a plain text control.</span></span>
-   <span data-ttu-id="bd2f1-154">Rich text 模式控制項一律會有預設的檔結束記號或換行字元，以格式化段落。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-154">Rich text mode controls always have a default end-of-document marker or carriage return, to format paragraphs.</span></span> <span data-ttu-id="bd2f1-155">另一方面，純文字控制項則不需要預設的檔結束記號，因此會省略。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-155">Plain text controls, on the other hand, do not need the default, end-of-document marker, so it is omitted.</span></span>

<span data-ttu-id="bd2f1-156">當控制項收到 **EM \_ SETTEXTMODE** 訊息時，不能包含任何文字。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-156">The control must contain no text when it receives the **EM\_SETTEXTMODE** message.</span></span> <span data-ttu-id="bd2f1-157">若要確定沒有任何文字，請將包含空字串 ( "" ) 傳送至 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息。</span><span class="sxs-lookup"><span data-stu-id="bd2f1-157">To ensure there is no text, send a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message with an empty string ("").</span></span>

## <a name="requirements"></a><span data-ttu-id="bd2f1-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd2f1-158">Requirements</span></span>



| <span data-ttu-id="bd2f1-159">需求</span><span class="sxs-lookup"><span data-stu-id="bd2f1-159">Requirement</span></span> | <span data-ttu-id="bd2f1-160">值</span><span class="sxs-lookup"><span data-stu-id="bd2f1-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2f1-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd2f1-161">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2f1-162">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd2f1-162">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd2f1-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd2f1-163">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2f1-164">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd2f1-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd2f1-165">標頭</span><span class="sxs-lookup"><span data-stu-id="bd2f1-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd2f1-166"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd2f1-166"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd2f1-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd2f1-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd2f1-168">**EM \_ GETTEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-168">**EM\_GETTEXTMODE**</span></span>](em-gettextmode.md)
</dt> <dt>

[<span data-ttu-id="bd2f1-169">**EM \_ SETUNDOLIMIT**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-169">**EM\_SETUNDOLIMIT**</span></span>](em-setundolimit.md)
</dt> <dt>

[<span data-ttu-id="bd2f1-170">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-170">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[<span data-ttu-id="bd2f1-171">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-171">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

