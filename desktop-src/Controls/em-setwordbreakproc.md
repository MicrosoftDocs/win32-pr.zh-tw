---
title: 'EM_SETWORDBREAKPROC 訊息 (Winuser .h) '
description: 使用應用程式定義的 Wordwrap 函數來取代編輯控制項的預設 Wordwrap 函式。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508707"
---
# <a name="em_setwordbreakproc-message"></a><span data-ttu-id="70096-105">EM \_ SETWORDBREAKPROC 訊息</span><span class="sxs-lookup"><span data-stu-id="70096-105">EM\_SETWORDBREAKPROC message</span></span>

<span data-ttu-id="70096-106">使用應用程式定義的 Wordwrap 函數來取代編輯控制項的預設 Wordwrap 函式。</span><span class="sxs-lookup"><span data-stu-id="70096-106">Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function.</span></span> <span data-ttu-id="70096-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="70096-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="70096-108">參數</span><span class="sxs-lookup"><span data-stu-id="70096-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70096-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70096-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70096-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="70096-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70096-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70096-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70096-112">應用程式定義的 Wordwrap 函式的位址。</span><span class="sxs-lookup"><span data-stu-id="70096-112">The address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="70096-113">如需有關中斷線的詳細資訊，請參閱 [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) 回呼函式的描述。</span><span class="sxs-lookup"><span data-stu-id="70096-113">For more information about breaking lines, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70096-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="70096-114">Return value</span></span>

<span data-ttu-id="70096-115">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="70096-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70096-116">備註</span><span class="sxs-lookup"><span data-stu-id="70096-116">Remarks</span></span>

<span data-ttu-id="70096-117">Wordwrap 函式會掃描文字緩衝區，其中包含要傳送至螢幕的文字，並尋找不符合目前畫面線的第一個字組。</span><span class="sxs-lookup"><span data-stu-id="70096-117">A Wordwrap function scans a text buffer that contains text to be sent to the screen, looking for the first word that does not fit on the current screen line.</span></span> <span data-ttu-id="70096-118">Wordwrap 函式會將這個單字放在畫面上下一行的開頭。</span><span class="sxs-lookup"><span data-stu-id="70096-118">The Wordwrap function places this word at the beginning of the next line on the screen.</span></span>

<span data-ttu-id="70096-119">Wordwrap 函式會定義系統應該將多行編輯控制項的文字換行的點，通常是在分隔兩個單字的空白字元上。</span><span class="sxs-lookup"><span data-stu-id="70096-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span> <span data-ttu-id="70096-120">當使用者按下方向鍵和 CTRL 鍵，以將插入號移到下一個單字或上一個字組時，多行或單行編輯控制項可能會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="70096-120">Either a multiline or a single-line edit control might call this function when the user presses arrow keys in combination with the CTRL key to move the caret to the next word or previous word.</span></span> <span data-ttu-id="70096-121">預設的 Wordwrap 函式會在空白字元上中斷一行文字。</span><span class="sxs-lookup"><span data-stu-id="70096-121">The default Wordwrap function breaks a line of text at a space character.</span></span> <span data-ttu-id="70096-122">應用程式定義函式可能會定義要在連字號或空白字元以外的字元上發生的 Wordwrap。</span><span class="sxs-lookup"><span data-stu-id="70096-122">The application-defined function may define the Wordwrap to occur at a hyphen or a character other than the space character.</span></span>

<span data-ttu-id="70096-123">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="70096-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="70096-124">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="70096-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70096-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="70096-125">Requirements</span></span>



| <span data-ttu-id="70096-126">需求</span><span class="sxs-lookup"><span data-stu-id="70096-126">Requirement</span></span> | <span data-ttu-id="70096-127">值</span><span class="sxs-lookup"><span data-stu-id="70096-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70096-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70096-128">Minimum supported client</span></span><br/> | <span data-ttu-id="70096-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70096-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="70096-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70096-130">Minimum supported server</span></span><br/> | <span data-ttu-id="70096-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70096-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70096-132">標頭</span><span class="sxs-lookup"><span data-stu-id="70096-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="70096-133"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="70096-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70096-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70096-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="70096-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="70096-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="70096-136">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="70096-136">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="70096-137">**EM \_ FMTLINES**</span><span class="sxs-lookup"><span data-stu-id="70096-137">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="70096-138">**EM \_ GETWORDBREAKPROC**</span><span class="sxs-lookup"><span data-stu-id="70096-138">**EM\_GETWORDBREAKPROC**</span></span>](em-getwordbreakproc.md)
</dt> </dl>

 

