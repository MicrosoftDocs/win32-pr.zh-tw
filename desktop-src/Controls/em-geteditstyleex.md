---
title: 'EM_GETEDITSTYLEEX 訊息 (Richedit .h) '
description: 抓取目前的擴充編輯樣式旗標。
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843684"
---
# <a name="em_geteditstyleex-message"></a><span data-ttu-id="1e66f-104">EM \_ GETEDITSTYLEEX 訊息</span><span class="sxs-lookup"><span data-stu-id="1e66f-104">EM\_GETEDITSTYLEEX message</span></span>

<span data-ttu-id="1e66f-105">抓取目前的擴充編輯樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="1e66f-105">Retrieves the current extended edit style flags.</span></span>


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a><span data-ttu-id="1e66f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1e66f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e66f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e66f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e66f-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1e66f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1e66f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e66f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e66f-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1e66f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e66f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e66f-111">Return value</span></span>

<span data-ttu-id="1e66f-112">傳回擴充編輯樣式旗標，其中可包含下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="1e66f-112">Returns the extended edit style flags, which can include one or more of the following values.</span></span>



| <span data-ttu-id="1e66f-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1e66f-113">Return code</span></span>                                                                                                | <span data-ttu-id="1e66f-114">Description</span><span class="sxs-lookup"><span data-stu-id="1e66f-114">Description</span></span>                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e66f-115"><dt>**SE \_ EX \_ HANDLEFRIENDLYURL**</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-115"><dt>**SES\_EX\_HANDLEFRIENDLYURL**</dt></span></span> </dl>  | <span data-ttu-id="1e66f-116">如果未使用暫時格式，或使用文字 autocolor (預設值： 0) ，請以相同的文字色彩和底線來顯示易記名稱連結。</span><span class="sxs-lookup"><span data-stu-id="1e66f-116">Display friendly name links with the same text color and underlining as automatic links, provided that temporary formatting isn t used or uses text autocolor (default: 0).</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="1e66f-117"><dt>**SE \_ EX 多點 \_ 觸控**</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-117"><dt>**SES\_EX\_MULTITOUCH**</dt></span></span> </dl>         | <span data-ttu-id="1e66f-118">在 Rich Edit 中啟用觸控支援。</span><span class="sxs-lookup"><span data-stu-id="1e66f-118">Enable touch support in Rich Edit.</span></span> <span data-ttu-id="1e66f-119">這包括選取專案、插入點位置和內容功能表叫用。</span><span class="sxs-lookup"><span data-stu-id="1e66f-119">This includes selection, caret placement, and context-menu invocation.</span></span> <span data-ttu-id="1e66f-120">如果未設定此旗標，則觸控是由滑鼠命令模擬，而不會將觸控模式詳細資訊納入考慮 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="1e66f-120">When this flag is not set, touch is emulated by mouse commands, which do not take touch-mode specifics into account (default: 0).</span></span> <br/>      |
| <dl> <span data-ttu-id="1e66f-121"><dt>**SE \_ EX \_ NOACETATESELECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-121"><dt>**SES\_EX\_NOACETATESELECTION**</dt></span></span> </dl> | <span data-ttu-id="1e66f-122">使用傳統的 Windows 選取文字和背景色彩來顯示選取的文字，而非背景 acetate 色彩 (預設： 0) 。</span><span class="sxs-lookup"><span data-stu-id="1e66f-122">Display selected text using classic Windows selection text and background colors instead of background acetate color (default: 0).</span></span> <br/>                                                                                                               |
| <dl> <span data-ttu-id="1e66f-123"><dt>**SE \_ EX \_ NOMATH**</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-123"><dt>**SES\_EX\_NOMATH**</dt></span></span> </dl>             | <span data-ttu-id="1e66f-124">停用插入數學區域 (預設： 1) 。</span><span class="sxs-lookup"><span data-stu-id="1e66f-124">Disable insertion of math zones (default: 1).</span></span> <span data-ttu-id="1e66f-125">若要啟用數學編輯和顯示，請將 *wParam* 設定為0的 [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md)訊息，並將 *lParam* 設定為 [ **SES \_ EX \_ NOMATH**]。</span><span class="sxs-lookup"><span data-stu-id="1e66f-125">To enable math editing and display, send the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message with *wParam* set to 0, and *lParam* set to **SES\_EX\_NOMATH**.</span></span> <br/>                              |
| <dl> <span data-ttu-id="1e66f-126"><dt>**\_ \_ 值得注意的 SES**</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-126"><dt>**SES\_EX\_NOTABLE**</dt></span></span> </dl>            | <span data-ttu-id="1e66f-127">停用資料表的插入。</span><span class="sxs-lookup"><span data-stu-id="1e66f-127">Disable insertion of tables.</span></span> <span data-ttu-id="1e66f-128">[**EM \_ INSERTTABLE**](em-inserttable.md)訊息會傳回 **E \_ 失敗**，而 RTF 資料表會略過 (預設值： 0) 。</span><span class="sxs-lookup"><span data-stu-id="1e66f-128">The [**EM\_INSERTTABLE**](em-inserttable.md) message returns **E\_FAIL** and RTF tables are skipped (default: 0).</span></span> <br/>                                                                                                  |
| <dl> <span data-ttu-id="1e66f-129"><dt>**SE \_ EX \_ USESINGLELINE**</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-129"><dt>**SES\_EX\_USESINGLELINE**</dt></span></span> </dl>      | <span data-ttu-id="1e66f-130">啟用多行控制項，其作用就像單行控制項一樣，可以在單行高度大於視窗高度 (預設值： 0) 時垂直捲動。</span><span class="sxs-lookup"><span data-stu-id="1e66f-130">Enable a multiline control to act like a single-line control with the ability to scroll vertically when the single-line height is greater than the window height (default: 0).</span></span> <br/>                                                                   |
| <dl> <span data-ttu-id="1e66f-131"><dt>**SE \_ HIDETEMPFORMAT**</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-131"><dt>**SES\_HIDETEMPFORMAT**</dt></span></span> </dl>         | <span data-ttu-id="1e66f-132">隱藏使用 **tomApplyTmp** 呼叫 [**ITextFont**](/windows/desktop/api/Tom/nf-tom-itextfont-reset)時所建立的暫時格式。</span><span class="sxs-lookup"><span data-stu-id="1e66f-132">Hide temporary formatting that is created when [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) is called with **tomApplyTmp**.</span></span> <span data-ttu-id="1e66f-133">例如，拼寫檢查程式會使用這類格式，在可能拼錯的單字底下顯示彎曲的底線。</span><span class="sxs-lookup"><span data-stu-id="1e66f-133">For example, such formatting is used by spell checkers to display a squiggly underline under possibly misspelled words.</span></span><br/> |
| <dl> <span data-ttu-id="1e66f-134"><dt>**SE \_ EX \_ USEMOUSEWPARAM**</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-134"><dt>**SES\_EX\_USEMOUSEWPARAM**</dt></span></span> </dl>     | <span data-ttu-id="1e66f-135">處理 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)訊息時，請使用 *wParam* ，而不要呼叫 [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate)。</span><span class="sxs-lookup"><span data-stu-id="1e66f-135">Use *wParam* when handling the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message and do not call [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="1e66f-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e66f-136">Requirements</span></span>



| <span data-ttu-id="1e66f-137">需求</span><span class="sxs-lookup"><span data-stu-id="1e66f-137">Requirement</span></span> | <span data-ttu-id="1e66f-138">值</span><span class="sxs-lookup"><span data-stu-id="1e66f-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e66f-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e66f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1e66f-140">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e66f-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1e66f-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e66f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1e66f-142">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e66f-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e66f-143">標頭</span><span class="sxs-lookup"><span data-stu-id="1e66f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e66f-144"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e66f-144"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e66f-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e66f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e66f-146">**EM \_ SETEDITSTYLEEX**</span><span class="sxs-lookup"><span data-stu-id="1e66f-146">**EM\_SETEDITSTYLEEX**</span></span>](em-seteditstyleex.md)
</dt> </dl>

 

