---
title: 'EM_GETWORDBREAKPROC 訊息 (Winuser .h) '
description: 取得目前 Wordwrap 函式的位址。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466236"
---
# <a name="em_getwordbreakproc-message"></a><span data-ttu-id="fdcc2-105">EM \_ GETWORDBREAKPROC 訊息</span><span class="sxs-lookup"><span data-stu-id="fdcc2-105">EM\_GETWORDBREAKPROC message</span></span>

<span data-ttu-id="fdcc2-106">取得目前 Wordwrap 函式的位址。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-106">Gets the address of the current Wordwrap function.</span></span> <span data-ttu-id="fdcc2-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdcc2-108">參數</span><span class="sxs-lookup"><span data-stu-id="fdcc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdcc2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdcc2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdcc2-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fdcc2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdcc2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdcc2-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdcc2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdcc2-113">Return value</span></span>

<span data-ttu-id="fdcc2-114">傳回值會指定應用程式定義的 Wordwrap 函式的位址。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-114">The return value specifies the address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="fdcc2-115">如果沒有任何 Wordwrap 函數，則傳回值為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-115">The return value is **NULL** if no Wordwrap function exists.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdcc2-116">備註</span><span class="sxs-lookup"><span data-stu-id="fdcc2-116">Remarks</span></span>

<span data-ttu-id="fdcc2-117">Wordwrap 函式會掃描包含要傳送給顯示之文字的文字緩衝區，尋找不符合目前顯示行的第一個單字。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-117">A Wordwrap function scans a text buffer that contains text to be sent to the display, looking for the first word that does not fit on the current display line.</span></span> <span data-ttu-id="fdcc2-118">Wordwrap 函式會將這個單字放在顯示器上下一行的開頭。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-118">The wordwrap function places this word at the beginning of the next line on the display.</span></span> <span data-ttu-id="fdcc2-119">Wordwrap 函式會定義系統應該將多行編輯控制項的文字換行的點，通常是在分隔兩個單字的空白字元上。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span>

<span data-ttu-id="fdcc2-120">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fdcc2-121">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="fdcc2-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdcc2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdcc2-122">Requirements</span></span>



| <span data-ttu-id="fdcc2-123">需求</span><span class="sxs-lookup"><span data-stu-id="fdcc2-123">Requirement</span></span> | <span data-ttu-id="fdcc2-124">值</span><span class="sxs-lookup"><span data-stu-id="fdcc2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdcc2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdcc2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fdcc2-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdcc2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fdcc2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdcc2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fdcc2-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdcc2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fdcc2-129">標頭</span><span class="sxs-lookup"><span data-stu-id="fdcc2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdcc2-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fdcc2-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdcc2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdcc2-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="fdcc2-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="fdcc2-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fdcc2-133">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="fdcc2-133">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="fdcc2-134">**EM \_ FMTLINES**</span><span class="sxs-lookup"><span data-stu-id="fdcc2-134">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="fdcc2-135">**EM \_ SETWORDBREAKPROC**</span><span class="sxs-lookup"><span data-stu-id="fdcc2-135">**EM\_SETWORDBREAKPROC**</span></span>](em-setwordbreakproc.md)
</dt> </dl>

 

