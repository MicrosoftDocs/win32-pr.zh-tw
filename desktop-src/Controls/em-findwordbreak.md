---
title: 'EM_FINDWORDBREAK 訊息 (Richedit .h) '
description: 尋找指定字元位置之前或之後的下一個字組，或抓取位於該位置之字元的相關資訊。
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465577"
---
# <a name="em_findwordbreak-message"></a><span data-ttu-id="716c1-104">EM \_ FINDWORDBREAK 訊息</span><span class="sxs-lookup"><span data-stu-id="716c1-104">EM\_FINDWORDBREAK message</span></span>

<span data-ttu-id="716c1-105">尋找指定字元位置之前或之後的下一個字組，或抓取位於該位置之字元的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="716c1-105">Finds the next word break before or after the specified character position or retrieves information about the character at that position.</span></span>

## <a name="parameters"></a><span data-ttu-id="716c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="716c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="716c1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="716c1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="716c1-108">指定尋找作業。</span><span class="sxs-lookup"><span data-stu-id="716c1-108">Specifies the find operation.</span></span> <span data-ttu-id="716c1-109">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="716c1-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="716c1-110">值</span><span class="sxs-lookup"><span data-stu-id="716c1-110">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="716c1-111">意義</span><span class="sxs-lookup"><span data-stu-id="716c1-111">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <span data-ttu-id="716c1-112"><dt>**WB \_ 分類**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-112"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>                | <span data-ttu-id="716c1-113">傳回字元類別和字元在指定位置的斷詞旗標。</span><span class="sxs-lookup"><span data-stu-id="716c1-113">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <span data-ttu-id="716c1-114"><dt>**WB \_ ISDELIMITER**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-114"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl>       | <span data-ttu-id="716c1-115">如果指定位置的字元是分隔符號，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="716c1-115">Returns **TRUE** if the character at the specified position is a delimiter, or **FALSE** otherwise.</span></span><br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <span data-ttu-id="716c1-116"><dt>**\_左 WB**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-116"><dt>**WB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="716c1-117">尋找開頭為單字的指定位置之前的最接近字元。</span><span class="sxs-lookup"><span data-stu-id="716c1-117">Finds the nearest character before the specified position that begins a word.</span></span><br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <span data-ttu-id="716c1-118"><dt>**WB \_ LEFTBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-118"><dt>**WB\_LEFTBREAK**</dt></span></span> </dl>             | <span data-ttu-id="716c1-119">尋找指定位置之前的下一個單字結尾。</span><span class="sxs-lookup"><span data-stu-id="716c1-119">Finds the next word end before the specified position.</span></span> <span data-ttu-id="716c1-120">此值與 WB \_ PREVBREAK 相同。</span><span class="sxs-lookup"><span data-stu-id="716c1-120">This value is the same as WB\_PREVBREAK.</span></span><br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <span data-ttu-id="716c1-121"><dt>**WB \_ MOVEWORDLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-121"><dt>**WB\_MOVEWORDLEFT**</dt></span></span> </dl>    | <span data-ttu-id="716c1-122">尋找在指定位置之前的單字開頭的下一個字元。</span><span class="sxs-lookup"><span data-stu-id="716c1-122">Finds the next character that begins a word before the specified position.</span></span> <span data-ttu-id="716c1-123">CTRL + 向左鍵處理期間會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="716c1-123">This value is used during CTRL+LEFT ARROW key processing.</span></span> <span data-ttu-id="716c1-124">此值類似于 WB \_ MOVEWORDPREV。</span><span class="sxs-lookup"><span data-stu-id="716c1-124">This value is the similar to WB\_MOVEWORDPREV.</span></span> <span data-ttu-id="716c1-125">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="716c1-125">See Remarks for more information.</span></span><br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <span data-ttu-id="716c1-126"><dt>**WB \_ MOVEWORDRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-126"><dt>**WB\_MOVEWORDRIGHT**</dt></span></span> </dl> | <span data-ttu-id="716c1-127">尋找在指定位置之後開始單字的下一個字元。</span><span class="sxs-lookup"><span data-stu-id="716c1-127">Finds the next character that begins a word after the specified position.</span></span> <span data-ttu-id="716c1-128">此值會在 CTRL + 右按鍵處理期間使用。</span><span class="sxs-lookup"><span data-stu-id="716c1-128">This value is used during CTRL+right key processing.</span></span> <span data-ttu-id="716c1-129">此值類似于 WB \_ MOVEWORDNEXT。</span><span class="sxs-lookup"><span data-stu-id="716c1-129">This value is similar to WB\_MOVEWORDNEXT.</span></span> <span data-ttu-id="716c1-130">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="716c1-130">See Remarks for more information.</span></span><br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <span data-ttu-id="716c1-131"><dt>**WB \_ RIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-131"><dt>**WB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="716c1-132">尋找在指定位置之後開始單字的下一個字元。</span><span class="sxs-lookup"><span data-stu-id="716c1-132">Finds the next character that begins a word after the specified position.</span></span><br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <span data-ttu-id="716c1-133"><dt>**WB \_ RIGHTBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-133"><dt>**WB\_RIGHTBREAK**</dt></span></span> </dl>          | <span data-ttu-id="716c1-134">尋找指定位置之後的下一個字組結尾分隔符號。</span><span class="sxs-lookup"><span data-stu-id="716c1-134">Finds the next end-of-word delimiter after the specified position.</span></span> <span data-ttu-id="716c1-135">此值與 WB \_ NEXTBREAK 相同。</span><span class="sxs-lookup"><span data-stu-id="716c1-135">This value is the same as WB\_NEXTBREAK.</span></span><br/>                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="716c1-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="716c1-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="716c1-137">以零起始的字元開始位置。</span><span class="sxs-lookup"><span data-stu-id="716c1-137">Zero-based character starting position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="716c1-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="716c1-138">Return value</span></span>

<span data-ttu-id="716c1-139">訊息會根據 *wParam* 參數傳回值。</span><span class="sxs-lookup"><span data-stu-id="716c1-139">The message returns a value based on the *wParam* parameter.</span></span>



| <span data-ttu-id="716c1-140">傳回碼</span><span class="sxs-lookup"><span data-stu-id="716c1-140">Return code</span></span>                                                                                    | <span data-ttu-id="716c1-141">Description</span><span class="sxs-lookup"><span data-stu-id="716c1-141">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="716c1-142"><dt>**wParam**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-142"><dt>**wParam**</dt></span></span> </dl>          | <span data-ttu-id="716c1-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="716c1-143">Return Value</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="716c1-144"><dt>**WB \_ 分類**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-144"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>    | <span data-ttu-id="716c1-145">傳回字元類別和字元在指定位置的斷詞旗標。</span><span class="sxs-lookup"><span data-stu-id="716c1-145">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                |
| <dl> <span data-ttu-id="716c1-146"><dt>**WB \_ ISDELIMITER**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-146"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl> | <span data-ttu-id="716c1-147">如果指定位置的字元是分隔符號，則傳回 **TRUE** ;否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="716c1-147">Returns **TRUE** if the character at the specified position is a delimiter; otherwise it returns **FALSE**.</span></span><br/> |
| <dl> <span data-ttu-id="716c1-148"><dt>**其他**</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-148"><dt>**Others**</dt></span></span> </dl>          | <span data-ttu-id="716c1-149">傳回斷字的字元索引。</span><span class="sxs-lookup"><span data-stu-id="716c1-149">Returns the character index of the word break.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="716c1-150">備註</span><span class="sxs-lookup"><span data-stu-id="716c1-150">Remarks</span></span>

<span data-ttu-id="716c1-151">如果 *wParam* 是 WB \_ LEFT 和 WB \_ RIGHT，則斷詞程式只會在分隔符號之後尋找斷詞。</span><span class="sxs-lookup"><span data-stu-id="716c1-151">If *wParam* is WB\_LEFT and WB\_RIGHT, the word-break procedure finds word breaks only after delimiters.</span></span> <span data-ttu-id="716c1-152">這符合編輯控制項的功能。</span><span class="sxs-lookup"><span data-stu-id="716c1-152">This matches the functionality of an edit control.</span></span> <span data-ttu-id="716c1-153">如果 *wParam* 是 WB \_ MOVEWORDLEFT 或 WB \_ MOVEWORDRIGHT，則斷詞程式也會比較字元類別和斷詞旗標。</span><span class="sxs-lookup"><span data-stu-id="716c1-153">If *wParam* is WB\_MOVEWORDLEFT or WB\_MOVEWORDRIGHT, the word-break procedure also compares character classes and word-break flags.</span></span>

<span data-ttu-id="716c1-154">如需有關字元類別和斷詞字元旗標的詳細資訊，請參閱 [單字和分行符號](using-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="716c1-154">For information about character classes and word-break flags, see [Word and Line Breaks](using-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="716c1-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="716c1-155">Requirements</span></span>



| <span data-ttu-id="716c1-156">需求</span><span class="sxs-lookup"><span data-stu-id="716c1-156">Requirement</span></span> | <span data-ttu-id="716c1-157">值</span><span class="sxs-lookup"><span data-stu-id="716c1-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="716c1-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="716c1-158">Minimum supported client</span></span><br/> | <span data-ttu-id="716c1-159">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="716c1-159">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="716c1-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="716c1-160">Minimum supported server</span></span><br/> | <span data-ttu-id="716c1-161">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="716c1-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="716c1-162">標頭</span><span class="sxs-lookup"><span data-stu-id="716c1-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="716c1-163"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-163"><dt>Richedit.h</dt></span></span> </dl> |



 

 





