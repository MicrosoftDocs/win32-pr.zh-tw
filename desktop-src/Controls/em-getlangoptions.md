---
title: 'EM_GETLANGOPTIONS 訊息 (Richedit .h) '
description: 取得 rich edit 控制項的 [輸入方法編輯器] 選項設定， (IME) 和亞洲語言支援。
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- EM_GETLANGOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27254ccb10093059eb9161410f4e25efdc59306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843164"
---
# <a name="em_getlangoptions-message"></a><span data-ttu-id="af9e4-104">EM \_ GETLANGOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="af9e4-104">EM\_GETLANGOPTIONS message</span></span>

<span data-ttu-id="af9e4-105">取得 rich edit 控制項的 [輸入方法編輯器] 選項設定， (IME) 和亞洲語言支援。</span><span class="sxs-lookup"><span data-stu-id="af9e4-105">Gets a rich edit control's option settings for Input Method Editor (IME) and Asian language support.</span></span>

## <a name="parameters"></a><span data-ttu-id="af9e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="af9e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af9e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af9e4-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="af9e4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="af9e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af9e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af9e4-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="af9e4-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9e4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="af9e4-111">Return value</span></span>

<span data-ttu-id="af9e4-112">傳回輸入法和亞洲語言設定，這可以是零或多個下列值。</span><span class="sxs-lookup"><span data-stu-id="af9e4-112">Returns the IME and Asian language settings, which can be zero or more of the following values.</span></span>



| <span data-ttu-id="af9e4-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="af9e4-113">Return code</span></span>                                                                                                     | <span data-ttu-id="af9e4-114">Description</span><span class="sxs-lookup"><span data-stu-id="af9e4-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af9e4-115"><dt>**IMF \_ AUTOFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-115"><dt>**IMF\_AUTOFONT**</dt></span></span> </dl>                    | <span data-ttu-id="af9e4-116">如果設定此旗標，當使用者明確變更為不同的鍵盤配置時，控制項會自動變更字型。</span><span class="sxs-lookup"><span data-stu-id="af9e4-116">If this flag is set, the control automatically changes fonts when the user explicitly changes to a different keyboard layout.</span></span> <span data-ttu-id="af9e4-117">針對通用 Unicode 字型關閉 **IMF \_ AUTOFONT** 相當有用。</span><span class="sxs-lookup"><span data-stu-id="af9e4-117">It is useful to turn off **IMF\_AUTOFONT** for universal Unicode fonts.</span></span> <span data-ttu-id="af9e4-118">預設會開啟此選項 (1) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-118">This option is turned on by default (1).</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="af9e4-119"><dt>**IMF \_ AUTOFONTSIZEADJUST**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-119"><dt>**IMF\_AUTOFONTSIZEADJUST**</dt></span></span> </dl>          | <span data-ttu-id="af9e4-120">如果設定此旗標，控制項會根據腳本，從插入點大小調整字型系結的字型大小。</span><span class="sxs-lookup"><span data-stu-id="af9e4-120">If this flag is set, the control scales font-bound font sizes from insertion point size according to script.</span></span> <span data-ttu-id="af9e4-121">例如，亞洲字型比西方字體稍微大一點。</span><span class="sxs-lookup"><span data-stu-id="af9e4-121">For example, Asian fonts are slightly larger than Western ones.</span></span> <span data-ttu-id="af9e4-122">預設會開啟此選項 (1) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-122">This option is turned on by default (1).</span></span><br/>                                                                                                                                                                                              |
| <dl> <span data-ttu-id="af9e4-123"><dt>**IMF \_ AUTOKEYBOARD**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-123"><dt>**IMF\_AUTOKEYBOARD**</dt></span></span> </dl>                | <span data-ttu-id="af9e4-124">如果設定此旗標，當使用者明確變更為不同的字型，或當使用者將插入點明確變更為文字中的新位置時，控制項會自動變更鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="af9e4-124">If this flag is set, the control automatically changes the keyboard layout when the user explicitly changes to a different font, or when the user explicitly changes the insertion point to a new location in the text.</span></span> <span data-ttu-id="af9e4-125">會自動開啟雙向控制項。</span><span class="sxs-lookup"><span data-stu-id="af9e4-125">Will be turned on automatically for bidirectional controls.</span></span> <span data-ttu-id="af9e4-126">針對其他所有控制項，預設會關閉它。</span><span class="sxs-lookup"><span data-stu-id="af9e4-126">For all other controls, it is turned off by default.</span></span> <span data-ttu-id="af9e4-127">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-127">This option is turned off by default (0).</span></span><br/>                                 |
| <dl> <span data-ttu-id="af9e4-128"><dt>**IMF \_ DISABLEAUTOBIDIAUTOKEYBOARD**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-128"><dt>**IMF\_DISABLEAUTOBIDIAUTOKEYBOARD**</dt></span></span> </dl> | <span data-ttu-id="af9e4-129">**Windows 8**：如果設定此旗標，控制項會使用語言中性邏輯來自動切換鍵盤。</span><span class="sxs-lookup"><span data-stu-id="af9e4-129">**Windows 8**: If this flag is set, the control uses language neutral logic for automatic keyboard switching.</span></span> <span data-ttu-id="af9e4-130">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-130">This option is turned off by default (0).</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="af9e4-131"><dt>**IMF \_ DUALFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-131"><dt>**IMF\_DUALFONT**</dt></span></span> </dl>                    | <span data-ttu-id="af9e4-132">如果設定此旗標，控制項會使用雙重字型模式。</span><span class="sxs-lookup"><span data-stu-id="af9e4-132">If this flag is set, the control uses dual-font mode.</span></span> <span data-ttu-id="af9e4-133">用於亞洲語言支援。</span><span class="sxs-lookup"><span data-stu-id="af9e4-133">Used for Asian language support.</span></span> <span data-ttu-id="af9e4-134">此控制項使用英文的 ASCII 文字字型，以及亞洲文字的亞洲字型。</span><span class="sxs-lookup"><span data-stu-id="af9e4-134">The control uses an English font for ASCII text and a Asian font for Asian text.</span></span> <span data-ttu-id="af9e4-135">預設會開啟此選項 (1) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-135">This option is turned on by default (1).</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="af9e4-136"><dt>**IMF \_ IMEALWAYSSENDNOTIFY**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-136"><dt>**IMF\_IMEALWAYSSENDNOTIFY**</dt></span></span> </dl>         | <span data-ttu-id="af9e4-137">此旗標會控制 rich edit 控制項在 IME 撰寫期間如何通知用戶端：</span><span class="sxs-lookup"><span data-stu-id="af9e4-137">This flag controls how the rich edit control notifies the client during IME composition:</span></span> <br/> <span data-ttu-id="af9e4-138">0：沒有任何 [en \_ 變更](en-change.md) 或在未確定狀態期間的 [en \_ SELCHANGE](en-selchange.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="af9e4-138">0: No [EN\_CHANGE](en-change.md) or [EN\_SELCHANGE](en-selchange.md) notifications during undetermined state.</span></span> <span data-ttu-id="af9e4-139">當最後一個字串進入時傳送通知。</span><span class="sxs-lookup"><span data-stu-id="af9e4-139">Send notification when the final string comes in.</span></span> <span data-ttu-id="af9e4-140">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="af9e4-140">This is the default.</span></span><br/> <span data-ttu-id="af9e4-141">1：在未定狀態期間傳送 [en \_ 變更](en-change.md) 和 [en \_ SELCHANGE](en-selchange.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="af9e4-141">1: Send [EN\_CHANGE](en-change.md) and [EN\_SELCHANGE](en-selchange.md) events during undetermined state.</span></span><br/> |
| <dl> <span data-ttu-id="af9e4-142"><dt>**IMF \_ IMECANCELCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-142"><dt>**IMF\_IMECANCELCOMPLETE**</dt></span></span> </dl>           | <span data-ttu-id="af9e4-143">此旗標會決定當使用者取消 IME 時，控制項如何使用 IME 的組合字元串。</span><span class="sxs-lookup"><span data-stu-id="af9e4-143">This flag determines how the control uses the composition string of an IME if the user cancels it.</span></span> <span data-ttu-id="af9e4-144">如果這項旗標已設定，控制項就會捨棄組字字串。</span><span class="sxs-lookup"><span data-stu-id="af9e4-144">If this flag is set, the control discards the composition string.</span></span> <span data-ttu-id="af9e4-145">如果這項旗標尚未設定，控制項就會使用組字字串做為結果字串。</span><span class="sxs-lookup"><span data-stu-id="af9e4-145">If this flag is not set, the control uses the composition string as the result string.</span></span> <span data-ttu-id="af9e4-146">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-146">This option is turned off by default (0).</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="af9e4-147"><dt>**IMF \_ NOIMPLICITLANG**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-147"><dt>**IMF\_NOIMPLICITLANG**</dt></span></span> </dl>              | <span data-ttu-id="af9e4-148">**Windows 8**：如果設定此旗標，請使用鍵盤語言停用戳記鍵盤輸入，並確保非東亞語言 ids 與字元所有產品相容。</span><span class="sxs-lookup"><span data-stu-id="af9e4-148">**Windows 8**: If this flag is set, disable stamping keyboard input with the keyboard language and ensuring that non-East Asian language IDss are compatible with the character repertoire.</span></span> <span data-ttu-id="af9e4-149">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-149">This option is turned off by default (0).</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="af9e4-150"><dt>**IMF \_ NOKBDLIDFIXUP**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-150"><dt>**IMF\_NOKBDLIDFIXUP**</dt></span></span> </dl>               | <span data-ttu-id="af9e4-151">**Windows 8**：如果設定此旗標，rich edit 控制項會在空白控制項上停用戳記鍵盤語言。</span><span class="sxs-lookup"><span data-stu-id="af9e4-151">**Windows 8**: If this flag is set, the rich edit control disables stamping keyboard language on an empty control.</span></span> <span data-ttu-id="af9e4-152">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-152">This option is turned off by default (0).</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="af9e4-153"><dt>**IMF \_ 拼寫**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-153"><dt>**IMF\_SPELLCHECKING**</dt></span></span> </dl>               | <span data-ttu-id="af9e4-154">**Windows 8**：如果設定此旗標，rich edit 控制項會開啟拼寫檢查。</span><span class="sxs-lookup"><span data-stu-id="af9e4-154">**Windows 8**: If this flag is set, the rich edit control turns on spell checking.</span></span> <span data-ttu-id="af9e4-155">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-155">This option is turned off by default (0).</span></span> <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="af9e4-156"><dt>**IMF \_ TKBAUTOCORRECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-156"><dt>**IMF\_TKBAUTOCORRECTION**</dt></span></span> </dl>           | <span data-ttu-id="af9e4-157">**Windows 8**：如果設定此旗標，請啟用觸控鍵盤自動校正。</span><span class="sxs-lookup"><span data-stu-id="af9e4-157">**Windows 8**: If this flag is set, enable touch keyboard autocorrect.</span></span> <span data-ttu-id="af9e4-158">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-158">This option is turned off by default (0).</span></span> <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="af9e4-159"><dt>**IMF \_ TKBPREDICTION**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-159"><dt>**IMF\_TKBPREDICTION**</dt></span></span> </dl>               | <span data-ttu-id="af9e4-160">**Windows 10**：已忽略。</span><span class="sxs-lookup"><span data-stu-id="af9e4-160">**Windows 10**: Ignored.</span></span><br/> <span data-ttu-id="af9e4-161">**Windows 8**：如果設定此旗標，rich edit 控制項會啟用觸控鍵盤預測。</span><span class="sxs-lookup"><span data-stu-id="af9e4-161">**Windows 8**: If this flag is set, the rich edit control enables touch keyboard prediction.</span></span> <span data-ttu-id="af9e4-162">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-162">This option is turned off by default (0).</span></span> <br/>                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="af9e4-163"><dt>**IMF \_ UIFONTS**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-163"><dt>**IMF\_UIFONTS**</dt></span></span> </dl>                     | <span data-ttu-id="af9e4-164">使用使用者介面預設字型。</span><span class="sxs-lookup"><span data-stu-id="af9e4-164">Use user-interface default fonts.</span></span> <span data-ttu-id="af9e4-165">依預設，此選項會關閉 (0) 。</span><span class="sxs-lookup"><span data-stu-id="af9e4-165">This option is turned off by default (0).</span></span><br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="af9e4-166">備註</span><span class="sxs-lookup"><span data-stu-id="af9e4-166">Remarks</span></span>

<span data-ttu-id="af9e4-167">預設會設定 **IMF \_ AUTOFONT** 旗標。</span><span class="sxs-lookup"><span data-stu-id="af9e4-167">The **IMF\_AUTOFONT** flag is set by default.</span></span> <span data-ttu-id="af9e4-168">預設會清除 **imf \_ AUTOKEYBOARD** 和 **imf \_ IMECANCELCOMPLETE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="af9e4-168">The **IMF\_AUTOKEYBOARD** and **IMF\_IMECANCELCOMPLETE** flags are cleared by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9e4-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="af9e4-169">Requirements</span></span>



| <span data-ttu-id="af9e4-170">需求</span><span class="sxs-lookup"><span data-stu-id="af9e4-170">Requirement</span></span> | <span data-ttu-id="af9e4-171">值</span><span class="sxs-lookup"><span data-stu-id="af9e4-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af9e4-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af9e4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="af9e4-173">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-173">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af9e4-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af9e4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="af9e4-175">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-175">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af9e4-176">標頭</span><span class="sxs-lookup"><span data-stu-id="af9e4-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="af9e4-177"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-177"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af9e4-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af9e4-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="af9e4-179">**參考**</span><span class="sxs-lookup"><span data-stu-id="af9e4-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="af9e4-180">**EM \_ SETLANGOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="af9e4-180">**EM\_SETLANGOPTIONS**</span></span>](em-setlangoptions.md)
</dt> <dt>

[<span data-ttu-id="af9e4-181">**EM \_ SETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="af9e4-181">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
</dt> </dl>

 

 





