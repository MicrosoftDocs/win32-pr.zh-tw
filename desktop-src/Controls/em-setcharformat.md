---
title: 'EM_SETCHARFORMAT 訊息 (Richedit .h) '
description: 設定 rich edit 控制項中的字元格式。
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105587"
---
# <a name="em_setcharformat-message"></a><span data-ttu-id="8b979-104">EM \_ SETCHARFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="8b979-104">EM\_SETCHARFORMAT message</span></span>

<span data-ttu-id="8b979-105">設定 rich edit 控制項中的字元格式。</span><span class="sxs-lookup"><span data-stu-id="8b979-105">Sets character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b979-106">參數</span><span class="sxs-lookup"><span data-stu-id="8b979-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b979-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b979-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b979-108">套用至控制項的字元格式。</span><span class="sxs-lookup"><span data-stu-id="8b979-108">Character formatting that applies to the control.</span></span> <span data-ttu-id="8b979-109">如果此參數為零，則會設定預設的字元格式。</span><span class="sxs-lookup"><span data-stu-id="8b979-109">If this parameter is zero, the default character format is set.</span></span> <span data-ttu-id="8b979-110">否則，它可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8b979-110">Otherwise, it can be one of the following values.</span></span>



| <span data-ttu-id="8b979-111">值</span><span class="sxs-lookup"><span data-stu-id="8b979-111">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="8b979-112">意義</span><span class="sxs-lookup"><span data-stu-id="8b979-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <span data-ttu-id="8b979-113"><dt>**SCF \_ 全部**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-113"><dt>**SCF\_ALL**</dt></span></span> </dl>                                     | <span data-ttu-id="8b979-114">將格式套用至控制項中的所有文字。</span><span class="sxs-lookup"><span data-stu-id="8b979-114">Applies the formatting to all text in the control.</span></span> <span data-ttu-id="8b979-115">**SCF \_ 選取範圍** 或 **SCF \_ 字** 組無效。</span><span class="sxs-lookup"><span data-stu-id="8b979-115">Not valid with **SCF\_SELECTION** or **SCF\_WORD**.</span></span><br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <span data-ttu-id="8b979-116"><dt>**SCF \_ ASSOCIATEFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-116"><dt>**SCF\_ASSOCIATEFONT**</dt></span></span> </dl>       | <span data-ttu-id="8b979-117">**RichEdit 4.1：** 將字型與指定的腳本產生關聯，從而變更該腳本的預設字型。</span><span class="sxs-lookup"><span data-stu-id="8b979-117">**RichEdit 4.1:** Associates a font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="8b979-118">若要指定字型，請使用下列 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)成員： **yHeight**、 **bCharSet**、 **bPitchAndFamily**、 **szFaceName** 和 **lcid**。</span><span class="sxs-lookup"><span data-stu-id="8b979-118">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <span data-ttu-id="8b979-119"><dt>**SCF \_ ASSOCIATEFONT2**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-119"><dt>**SCF\_ASSOCIATEFONT2**</dt></span></span> </dl>    | <span data-ttu-id="8b979-120">**RichEdit 4.1：** 將代理 (平面-2) 字型與指定的腳本產生關聯，進而變更該腳本的預設字型。</span><span class="sxs-lookup"><span data-stu-id="8b979-120">**RichEdit 4.1:** Associates a surrogate (plane-2) font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="8b979-121">若要指定字型，請使用下列 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)成員： **yHeight**、 **bCharSet**、 **bPitchAndFamily**、 **szFaceName** 和 **lcid**。</span><span class="sxs-lookup"><span data-stu-id="8b979-121">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <span data-ttu-id="8b979-122"><dt>**SCF \_ CHARREPFROMLCID**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-122"><dt>**SCF\_CHARREPFROMLCID**</dt></span></span> </dl> | <span data-ttu-id="8b979-123">取得從 LCID 所有產品的字元。</span><span class="sxs-lookup"><span data-stu-id="8b979-123">Gets the character repertoire from the LCID.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="8b979-124"><dt>**SCF \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-124"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>                         | <span data-ttu-id="8b979-125">**RichEdit 4.1：** 設定控制項的預設字型。</span><span class="sxs-lookup"><span data-stu-id="8b979-125">**RichEdit 4.1:** Sets the default font for the control.</span></span> <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <span data-ttu-id="8b979-126"><dt>**SPF \_ DONTSETDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-126"><dt>**SPF\_DONTSETDEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="8b979-127">當 rich edit 控制項為空白時，防止設定預設段落格式。</span><span class="sxs-lookup"><span data-stu-id="8b979-127">Prevents setting the default paragraph format when the rich edit control is empty.</span></span><br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <span data-ttu-id="8b979-128"><dt>**SCF \_ NOKBUPDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-128"><dt>**SCF\_NOKBUPDATE**</dt></span></span> </dl>                | <span data-ttu-id="8b979-129">**RichEdit 4.1：** 防止鍵盤切換以符合字型。</span><span class="sxs-lookup"><span data-stu-id="8b979-129">**RichEdit 4.1:** Prevents keyboard switching to match the font.</span></span> <span data-ttu-id="8b979-130">例如，如果設定了阿拉伯文字型，則雙向語言的自動鍵盤功能通常會將鍵盤變更為阿拉伯文鍵盤。</span><span class="sxs-lookup"><span data-stu-id="8b979-130">For example, if an Arabic font is set, normally the automatic keyboard feature for Bidi languages changes the keyboard to an Arabic keyboard.</span></span><br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="8b979-131"><dt>**SCF \_ 選取專案**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-131"><dt>**SCF\_SELECTION**</dt></span></span> </dl>                   | <span data-ttu-id="8b979-132">將格式套用至目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="8b979-132">Applies the formatting to the current selection.</span></span> <span data-ttu-id="8b979-133">如果選取專案是空的，則會將字元格式套用至插入點，而新的字元格式只會在插入點變更時生效。</span><span class="sxs-lookup"><span data-stu-id="8b979-133">If the selection is empty, the character formatting is applied to the insertion point, and the new character format is in effect only until the insertion point changes.</span></span><br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <span data-ttu-id="8b979-134"><dt>**SPF \_ SETDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-134"><dt>**SPF\_SETDEFAULT**</dt></span></span> </dl>                | <span data-ttu-id="8b979-135">設定預設段落格式化屬性。</span><span class="sxs-lookup"><span data-stu-id="8b979-135">Sets the default paragraph formatting attributes.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <span data-ttu-id="8b979-136"><dt>**SCF \_ SMARTFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-136"><dt>**SCF\_SMARTFONT**</dt></span></span> </dl>                   | <span data-ttu-id="8b979-137">只有在可以處理腳本時，才套用字型。</span><span class="sxs-lookup"><span data-stu-id="8b979-137">Apply the font only if it can handle script.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <span data-ttu-id="8b979-138"><dt>**SCF \_ USEUIRULES**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-138"><dt>**SCF\_USEUIRULES**</dt></span></span> </dl>                | <span data-ttu-id="8b979-139">**RichEdit 4.1：** 搭配 **SCF \_ 選項** 使用。</span><span class="sxs-lookup"><span data-stu-id="8b979-139">**RichEdit 4.1:** Used with **SCF\_SELECTION**.</span></span> <span data-ttu-id="8b979-140">表示格式來自工具列或其他 UI 工具，因此應該使用 UI 格式化規則，而不是常值格式。</span><span class="sxs-lookup"><span data-stu-id="8b979-140">Indicates that format came from a toolbar or other UI tool, so UI formatting rules should be used instead of literal formatting.</span></span><br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <span data-ttu-id="8b979-141"><dt>**SCF \_ WORD**</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-141"><dt>**SCF\_WORD**</dt></span></span> </dl>                                  | <span data-ttu-id="8b979-142">將格式套用至選取的單字或文字。</span><span class="sxs-lookup"><span data-stu-id="8b979-142">Applies the formatting to the selected word or words.</span></span> <span data-ttu-id="8b979-143">如果選取範圍是空的，但插入點位於單字內，則會將格式套用至文字。</span><span class="sxs-lookup"><span data-stu-id="8b979-143">If the selection is empty but the insertion point is inside a word, the formatting is applied to the word.</span></span> <span data-ttu-id="8b979-144">**SCF \_ 文字** 值必須與 **SCF \_ 選取** 值一起使用。</span><span class="sxs-lookup"><span data-stu-id="8b979-144">The **SCF\_WORD** value must be used in conjunction with the **SCF\_SELECTION** value.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="8b979-145">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b979-145">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b979-146">[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)結構的指標，指定要使用的字元格式。</span><span class="sxs-lookup"><span data-stu-id="8b979-146">Pointer to a [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure specifying the character formatting to use.</span></span> <span data-ttu-id="8b979-147">只有 **dwMask** 成員所指定的格式屬性會變更。</span><span class="sxs-lookup"><span data-stu-id="8b979-147">Only the formatting attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="8b979-148">Microsoft Rich Edit 2.0 和更新版本：此參數可以是 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) 結構的指標，也就是 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) 結構的延伸。</span><span class="sxs-lookup"><span data-stu-id="8b979-148">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="8b979-149">傳送 **EM \_ SETCHARFORMAT** 訊息之前，請將結構的 **cbSize** 成員設定為， `sizeof(CHARFORMAT)` 或指出所使用的 `sizeof(CHARFORMAT2)` 結構版本。</span><span class="sxs-lookup"><span data-stu-id="8b979-149">Before sending the **EM\_SETCHARFORMAT** message, set the structure's **cbSize** member to `sizeof(CHARFORMAT)` or `sizeof(CHARFORMAT2)` indicate which version of the structure is being used.</span></span>

<span data-ttu-id="8b979-150">當字元無效時， **szFaceName** 和 **bCharSet** 成員可能會被視為無效，例如：在中文字元上為 Arial。</span><span class="sxs-lookup"><span data-stu-id="8b979-150">The **szFaceName** and **bCharSet** members may be overruled when invalid for characters, for example: Arial on kanji characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b979-151">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b979-151">Return value</span></span>

<span data-ttu-id="8b979-152">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="8b979-152">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8b979-153">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="8b979-153">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b979-154">備註</span><span class="sxs-lookup"><span data-stu-id="8b979-154">Remarks</span></span>

<span data-ttu-id="8b979-155">如果使用相同的參數多次傳送此訊息，則會切換文字的效果。</span><span class="sxs-lookup"><span data-stu-id="8b979-155">If this message is sent more than once with the same parameters, the effect on the text is toggled.</span></span> <span data-ttu-id="8b979-156">也就是說，傳送訊息一次會產生效果，傳送訊息兩次會取消效果等等。</span><span class="sxs-lookup"><span data-stu-id="8b979-156">That is, sending the message once produces the effect, sending the message twice cancels the effect, and so forth.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b979-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b979-157">Requirements</span></span>



| <span data-ttu-id="8b979-158">需求</span><span class="sxs-lookup"><span data-stu-id="8b979-158">Requirement</span></span> | <span data-ttu-id="8b979-159">值</span><span class="sxs-lookup"><span data-stu-id="8b979-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b979-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b979-160">Minimum supported client</span></span><br/> | <span data-ttu-id="8b979-161">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b979-161">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b979-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b979-162">Minimum supported server</span></span><br/> | <span data-ttu-id="8b979-163">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b979-163">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b979-164">標頭</span><span class="sxs-lookup"><span data-stu-id="8b979-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b979-165"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b979-165"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b979-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b979-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b979-167">**參考**</span><span class="sxs-lookup"><span data-stu-id="8b979-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b979-168">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="8b979-168">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="8b979-169">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="8b979-169">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





