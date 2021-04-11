---
title: 'EM_GETIMEPROPERTY 訊息 (Richedit .h) '
description: 抓取輸入方法編輯器的屬性和功能 (IME) 與目前的輸入地區設定相關聯。
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105125"
---
# <a name="em_getimeproperty-message"></a><span data-ttu-id="a40f9-104">EM \_ GETIMEPROPERTY 訊息</span><span class="sxs-lookup"><span data-stu-id="a40f9-104">EM\_GETIMEPROPERTY message</span></span>

<span data-ttu-id="a40f9-105">抓取輸入方法編輯器的屬性和功能 (IME) 與目前的輸入地區設定相關聯。</span><span class="sxs-lookup"><span data-stu-id="a40f9-105">Retrieves the property and capabilities of the Input Method Editor (IME) associated with the current input locale.</span></span>

## <a name="parameters"></a><span data-ttu-id="a40f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="a40f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a40f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a40f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a40f9-108">指定要取得之屬性資訊的類型。</span><span class="sxs-lookup"><span data-stu-id="a40f9-108">Specifies the type of property information to retrieve.</span></span> <span data-ttu-id="a40f9-109">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a40f9-110">值</span><span class="sxs-lookup"><span data-stu-id="a40f9-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="a40f9-111">意義</span><span class="sxs-lookup"><span data-stu-id="a40f9-111">Meaning</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <span data-ttu-id="a40f9-112"><dt>**IGP \_ 屬性**</dt></span><span class="sxs-lookup"><span data-stu-id="a40f9-112"><dt>**IGP\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="a40f9-113">屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="a40f9-113">Property information.</span></span><br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <span data-ttu-id="a40f9-114"><dt>**IGP \_ 轉換**</dt></span><span class="sxs-lookup"><span data-stu-id="a40f9-114"><dt>**IGP\_CONVERSION**</dt></span></span> </dl>          | <span data-ttu-id="a40f9-115">轉換功能。</span><span class="sxs-lookup"><span data-stu-id="a40f9-115">Conversion capabilities.</span></span> <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <span data-ttu-id="a40f9-116"><dt>**IGP \_ 句子**</dt></span><span class="sxs-lookup"><span data-stu-id="a40f9-116"><dt>**IGP\_SENTENCE**</dt></span></span> </dl>                | <span data-ttu-id="a40f9-117">句子模式功能。</span><span class="sxs-lookup"><span data-stu-id="a40f9-117">Sentence mode capabilities.</span></span> <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <span data-ttu-id="a40f9-118"><dt>**IGP \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="a40f9-118"><dt>**IGP\_UI**</dt></span></span> </dl>                                  | <span data-ttu-id="a40f9-119">使用者介面功能。</span><span class="sxs-lookup"><span data-stu-id="a40f9-119">User interface capabilities.</span></span> <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <span data-ttu-id="a40f9-120"><dt>**IGP \_ SETCOMPSTR**</dt></span><span class="sxs-lookup"><span data-stu-id="a40f9-120"><dt>**IGP\_SETCOMPSTR**</dt></span></span> </dl>          | <span data-ttu-id="a40f9-121">撰寫字串功能。</span><span class="sxs-lookup"><span data-stu-id="a40f9-121">Composition string capabilities.</span></span> <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <span data-ttu-id="a40f9-122"><dt>**IGP \_ SELECT**</dt></span><span class="sxs-lookup"><span data-stu-id="a40f9-122"><dt>**IGP\_SELECT**</dt></span></span> </dl>                      | <span data-ttu-id="a40f9-123">選取範圍繼承功能。</span><span class="sxs-lookup"><span data-stu-id="a40f9-123">Selection inheritance capabilities.</span></span> <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <span data-ttu-id="a40f9-124"><dt>**IGP \_ GETIMEVERSION**</dt></span><span class="sxs-lookup"><span data-stu-id="a40f9-124"><dt>**IGP\_GETIMEVERSION**</dt></span></span> </dl> | <span data-ttu-id="a40f9-125">抓取已建立指定 IME 的系統版本號碼。</span><span class="sxs-lookup"><span data-stu-id="a40f9-125">Retrieves the system version number for which the specified IME was created.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a40f9-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a40f9-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a40f9-127">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="a40f9-127">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a40f9-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="a40f9-128">Return value</span></span>

<span data-ttu-id="a40f9-129">根據 *lParam* 參數的值，傳回屬性或功能值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-129">Returns the property or capability value, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="a40f9-130">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="a40f9-130">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="a40f9-131">備註</span><span class="sxs-lookup"><span data-stu-id="a40f9-131">Remarks</span></span>

<span data-ttu-id="a40f9-132">如果 *wParam* 是 IGP \_ 屬性，它會傳回下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-132">If *wParam* is IGP\_PROPERTY, it returns one or more of the following values.</span></span>



| <span data-ttu-id="a40f9-133">需求</span><span class="sxs-lookup"><span data-stu-id="a40f9-133">Requirement</span></span> | <span data-ttu-id="a40f9-134">值</span><span class="sxs-lookup"><span data-stu-id="a40f9-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a40f9-135">\_插入號 \_ 的輸入法 \_</span><span class="sxs-lookup"><span data-stu-id="a40f9-135">IME\_PROP\_AT\_CARET</span></span>                | <span data-ttu-id="a40f9-136">如果設定，則轉換視窗位於插入號位置。</span><span class="sxs-lookup"><span data-stu-id="a40f9-136">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="a40f9-137">若為清除，則視窗接近插入號位置。</span><span class="sxs-lookup"><span data-stu-id="a40f9-137">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a40f9-138">IME \_ 特性 \_ 特殊 \_ UI</span><span class="sxs-lookup"><span data-stu-id="a40f9-138">IME\_PROP\_SPECIAL\_UI</span></span>              | <span data-ttu-id="a40f9-139">如果設定，IME 會有非標準的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="a40f9-139">If set, IME has a nonstandard user interface.</span></span> <span data-ttu-id="a40f9-140">應用程式不應該在 IME 視窗中繪製。</span><span class="sxs-lookup"><span data-stu-id="a40f9-140">The application should not draw in the IME window.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a40f9-141">IME \_ \_ 的 CANDLIST \_ \_ 從 \_ 1 開始</span><span class="sxs-lookup"><span data-stu-id="a40f9-141">IME\_PROP\_CANDLIST\_START\_FROM\_1</span></span> | <span data-ttu-id="a40f9-142">如果設定，候選清單中的字串會從1開始編號。</span><span class="sxs-lookup"><span data-stu-id="a40f9-142">If set, strings in the candidate list are numbered starting at 1.</span></span> <span data-ttu-id="a40f9-143">如果清除，字串就會從零開始。</span><span class="sxs-lookup"><span data-stu-id="a40f9-143">If clear, strings start at zero.</span></span>                                                                                                                                                                |
| <span data-ttu-id="a40f9-144">IME \_ 的 \_ UNICODE</span><span class="sxs-lookup"><span data-stu-id="a40f9-144">IME\_PROP\_UNICODE</span></span>                  | <span data-ttu-id="a40f9-145">如果設定，則會將 IME 視為 UnicodeIME。</span><span class="sxs-lookup"><span data-stu-id="a40f9-145">If set, the IME is viewed as a UnicodeIME.</span></span> <span data-ttu-id="a40f9-146">系統和 IME 會透過 UnicodeIME 介面進行通訊。</span><span class="sxs-lookup"><span data-stu-id="a40f9-146">The system and the IME will communicate through the UnicodeIME interface.</span></span> <span data-ttu-id="a40f9-147">如果清除，IME 將使用 ANSI 介面與系統通訊。</span><span class="sxs-lookup"><span data-stu-id="a40f9-147">If clear, IME will use the ANSI interface to communicate with the system.</span></span>                                                                    |
| <span data-ttu-id="a40f9-148">\_ \_ \_ 取消選取時完成的 IME \_</span><span class="sxs-lookup"><span data-stu-id="a40f9-148">IME\_PROP\_COMPLETE\_ON\_UNSELECT</span></span>   | <span data-ttu-id="a40f9-149">如果設定，則轉換視窗位於插入號位置。</span><span class="sxs-lookup"><span data-stu-id="a40f9-149">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="a40f9-150">若為清除，則視窗接近插入號位置。</span><span class="sxs-lookup"><span data-stu-id="a40f9-150">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a40f9-151">IME 的 \_ 主張 \_ 接受 \_ 寬 \_ VKEY</span><span class="sxs-lookup"><span data-stu-id="a40f9-151">IME\_PROP\_ACCEPT\_WIDE\_VKEY</span></span>       | <span data-ttu-id="a40f9-152">如果設定，IME 會使用 VK 封包來處理來自 [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) 函式的插入 Unicode \_ 。</span><span class="sxs-lookup"><span data-stu-id="a40f9-152">If set, the IME processes the injected Unicode that came from the [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) function by using VK\_PACKET.</span></span> <span data-ttu-id="a40f9-153">如果清除，IME 可能不會處理插入的 Unicode，而插入的 Unicode 可能會直接傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="a40f9-153">If clear, the IME might not process the injected Unicode, and the injected Unicode might be sent to the application directly.</span></span> |



 

<span data-ttu-id="a40f9-154">如果 *wParam* 是 IGP \_ UI，它會傳回下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-154">If *wParam* is IGP\_UI, it returns one or more of the following values.</span></span>



| <span data-ttu-id="a40f9-155">需求</span><span class="sxs-lookup"><span data-stu-id="a40f9-155">Requirement</span></span> | <span data-ttu-id="a40f9-156">值</span><span class="sxs-lookup"><span data-stu-id="a40f9-156">Value</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a40f9-157">UI \_ 上限 \_ 2700</span><span class="sxs-lookup"><span data-stu-id="a40f9-157">UI\_CAP\_2700</span></span>   | <span data-ttu-id="a40f9-158">支援0或2700的文字行距值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-158">Supports text escapement values of 0 or 2700.</span></span> <span data-ttu-id="a40f9-159">如需詳細資訊，請參閱 **lfEscapement**。</span><span class="sxs-lookup"><span data-stu-id="a40f9-159">For more information, see **lfEscapement**.</span></span>             |
| <span data-ttu-id="a40f9-160">UI \_ 端點 \_ ROT90</span><span class="sxs-lookup"><span data-stu-id="a40f9-160">UI\_CAP\_ROT90</span></span>  | <span data-ttu-id="a40f9-161">支援文字行距值0、900、1800或2700。</span><span class="sxs-lookup"><span data-stu-id="a40f9-161">Supports text escapement values of 0, 900, 1800, or 2700.</span></span> <span data-ttu-id="a40f9-162">如需詳細資訊，請參閱 **lfEscapement**。</span><span class="sxs-lookup"><span data-stu-id="a40f9-162">For more information, see **lfEscapement**.</span></span> |
| <span data-ttu-id="a40f9-163">UI \_ 端點 \_ ROTANY</span><span class="sxs-lookup"><span data-stu-id="a40f9-163">UI\_CAP\_ROTANY</span></span> | <span data-ttu-id="a40f9-164">支援任何文字行距值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-164">Supports any text escapement value.</span></span> <span data-ttu-id="a40f9-165">如需詳細資訊，請參閱 **lfEscapement**。</span><span class="sxs-lookup"><span data-stu-id="a40f9-165">For more information, see **lfEscapement**.</span></span>                       |



 

<span data-ttu-id="a40f9-166">如果 *wParam* 是 IGP \_ SETCOMPSTR，它會傳回下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-166">If *wParam* is IGP\_SETCOMPSTR, it returns one or more of the following values.</span></span>



| <span data-ttu-id="a40f9-167">需求</span><span class="sxs-lookup"><span data-stu-id="a40f9-167">Requirement</span></span> | <span data-ttu-id="a40f9-168">值</span><span class="sxs-lookup"><span data-stu-id="a40f9-168">Value</span></span> |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a40f9-169">SCS \_ 端點 \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="a40f9-169">SCS\_CAP\_COMPSTR</span></span>            | <span data-ttu-id="a40f9-170">可以透過呼叫 [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) 函式與 SCS SETSTR 值來建立組合字元串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a40f9-170">Can create the composition string by calling the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with the SCS\_SETSTR value.</span></span>                                                      |
| <span data-ttu-id="a40f9-171">SCS \_ 端點 \_ MAKEREAD</span><span class="sxs-lookup"><span data-stu-id="a40f9-171">SCS\_CAP\_MAKEREAD</span></span>           | <span data-ttu-id="a40f9-172">搭配 SCS SETSTR 使用 [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) 函式時，可以從對應的組合字元串建立讀取字串 \_ ，而不設定 *lpRead*。</span><span class="sxs-lookup"><span data-stu-id="a40f9-172">Can create the reading string from corresponding composition string when using the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with SCS\_SETSTR and without setting *lpRead*.</span></span> |
| <span data-ttu-id="a40f9-173">SCS \_ 端點 \_ SETRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="a40f9-173">SCS\_CAP\_SETRECONVERTSTRING</span></span> | <span data-ttu-id="a40f9-174">此 IME 可以支援漢字重組。</span><span class="sxs-lookup"><span data-stu-id="a40f9-174">This IME can support reconversion.</span></span> <span data-ttu-id="a40f9-175">使用 [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) 來執行 [重設]。</span><span class="sxs-lookup"><span data-stu-id="a40f9-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) to do the reconversion.</span></span>                                                                             |



 

<span data-ttu-id="a40f9-176">如果 *wParam* 為 IGP \_ SELECT，則會傳回下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-176">If *wParam* is IGP\_SELECT, it returns one or more of the following values.</span></span>



| <span data-ttu-id="a40f9-177">需求</span><span class="sxs-lookup"><span data-stu-id="a40f9-177">Requirement</span></span> | <span data-ttu-id="a40f9-178">值</span><span class="sxs-lookup"><span data-stu-id="a40f9-178">Value</span></span> |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="a40f9-179">選取 \_ 端點 \_ CONVMODE</span><span class="sxs-lookup"><span data-stu-id="a40f9-179">SELECT\_CAP\_CONVMODE</span></span> | <span data-ttu-id="a40f9-180">選取新的輸入法時繼承轉換模式。</span><span class="sxs-lookup"><span data-stu-id="a40f9-180">Inherits conversion mode when a new IME is selected.</span></span> |
| <span data-ttu-id="a40f9-181">選取 \_ 端點 \_ 句子</span><span class="sxs-lookup"><span data-stu-id="a40f9-181">SELECT\_CAP\_SENTENCE</span></span> | <span data-ttu-id="a40f9-182">選取新的 IME 時繼承句子模式。</span><span class="sxs-lookup"><span data-stu-id="a40f9-182">Inherits sentence mode when a new IME is selected.</span></span>   |



 

<span data-ttu-id="a40f9-183">如果 *wParam* 是 IGP \_ GETIMEVERSION，它會傳回下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a40f9-183">If *wParam* is IGP\_GETIMEVERSION, it returns one or more of the following values.</span></span>



| <span data-ttu-id="a40f9-184">需求</span><span class="sxs-lookup"><span data-stu-id="a40f9-184">Requirement</span></span> | <span data-ttu-id="a40f9-185">值</span><span class="sxs-lookup"><span data-stu-id="a40f9-185">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="a40f9-186">IMEVER \_ 0310</span><span class="sxs-lookup"><span data-stu-id="a40f9-186">IMEVER\_0310</span></span> | <span data-ttu-id="a40f9-187">已針對 Windows 3.1 建立 IME。</span><span class="sxs-lookup"><span data-stu-id="a40f9-187">The IME was created for Windows 3.1.</span></span>        |
| <span data-ttu-id="a40f9-188">IMEVER \_ 0400</span><span class="sxs-lookup"><span data-stu-id="a40f9-188">IMEVER\_0400</span></span> | <span data-ttu-id="a40f9-189">為 Windows 95 或更新版本建立的 IME</span><span class="sxs-lookup"><span data-stu-id="a40f9-189">The IME was created for Windows 95 or later</span></span> |



 

<span data-ttu-id="a40f9-190">這則訊息與 [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)類似，不同之處在于它會使用目前的輸入地區設定。</span><span class="sxs-lookup"><span data-stu-id="a40f9-190">This message is similar to [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), except that it uses the current input locale.</span></span> <span data-ttu-id="a40f9-191">在呼叫此函式之前，應用程式應該呼叫 [**EM \_ ISIME**](em-isime.md) 。</span><span class="sxs-lookup"><span data-stu-id="a40f9-191">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a40f9-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="a40f9-192">Requirements</span></span>



| <span data-ttu-id="a40f9-193">需求</span><span class="sxs-lookup"><span data-stu-id="a40f9-193">Requirement</span></span> | <span data-ttu-id="a40f9-194">值</span><span class="sxs-lookup"><span data-stu-id="a40f9-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a40f9-195">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a40f9-195">Minimum supported client</span></span><br/> | <span data-ttu-id="a40f9-196">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a40f9-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a40f9-197">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a40f9-197">Minimum supported server</span></span><br/> | <span data-ttu-id="a40f9-198">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a40f9-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a40f9-199">標頭</span><span class="sxs-lookup"><span data-stu-id="a40f9-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="a40f9-200"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a40f9-200"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a40f9-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a40f9-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="a40f9-202">**參考**</span><span class="sxs-lookup"><span data-stu-id="a40f9-202">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a40f9-203">**EM \_ ISIME**</span><span class="sxs-lookup"><span data-stu-id="a40f9-203">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

<span data-ttu-id="a40f9-204">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="a40f9-204">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a40f9-205">**ImmGetProperty**</span><span class="sxs-lookup"><span data-stu-id="a40f9-205">**ImmGetProperty**</span></span>](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

