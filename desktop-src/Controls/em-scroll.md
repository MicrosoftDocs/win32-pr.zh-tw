---
title: 'EM_SCROLL 訊息 (Winuser .h) '
description: 在多行編輯控制項中垂直捲動文字。 這則訊息相當於將 WM \_ VSCROLL 訊息傳送至編輯控制項。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- EM_SCROLL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106266"
---
# <a name="em_scroll-message"></a><span data-ttu-id="53608-106">EM \_ 捲軸訊息</span><span class="sxs-lookup"><span data-stu-id="53608-106">EM\_SCROLL message</span></span>

<span data-ttu-id="53608-107">在多行編輯控制項中垂直捲動文字。</span><span class="sxs-lookup"><span data-stu-id="53608-107">Scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="53608-108">這則訊息相當於將 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送至編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="53608-108">This message is equivalent to sending a [**WM\_VSCROLL**](wm-vscroll.md) message to the edit control.</span></span> <span data-ttu-id="53608-109">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="53608-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="53608-110">參數</span><span class="sxs-lookup"><span data-stu-id="53608-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53608-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53608-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53608-112">捲軸所要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="53608-112">The action the scroll bar is to take.</span></span> <span data-ttu-id="53608-113">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="53608-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="53608-114">值</span><span class="sxs-lookup"><span data-stu-id="53608-114">Value</span></span>                                                                                                                                                   | <span data-ttu-id="53608-115">意義</span><span class="sxs-lookup"><span data-stu-id="53608-115">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="53608-116"><dt>**SB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="53608-116"><dt>**SB\_LINEDOWN**</dt></span></span> </dl> | <span data-ttu-id="53608-117">向下捲動一行。</span><span class="sxs-lookup"><span data-stu-id="53608-117">Scrolls down one line.</span></span><br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="53608-118"><dt>**SB \_ 系列**</dt></span><span class="sxs-lookup"><span data-stu-id="53608-118"><dt>**SB\_LINEUP**</dt></span></span> </dl>       | <span data-ttu-id="53608-119">向上捲動一行。</span><span class="sxs-lookup"><span data-stu-id="53608-119">Scrolls up one line.</span></span><br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="53608-120"><dt>**SB \_ PAGEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="53608-120"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl> | <span data-ttu-id="53608-121">向下捲動一頁。</span><span class="sxs-lookup"><span data-stu-id="53608-121">Scrolls down one page.</span></span><br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="53608-122"><dt>**SB \_ PAGEUP**</dt></span><span class="sxs-lookup"><span data-stu-id="53608-122"><dt>**SB\_PAGEUP**</dt></span></span> </dl>       | <span data-ttu-id="53608-123">向上捲動一頁。</span><span class="sxs-lookup"><span data-stu-id="53608-123">Scrolls up one page.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="53608-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53608-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53608-125">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="53608-125">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53608-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="53608-126">Return value</span></span>

<span data-ttu-id="53608-127">如果訊息成功，則傳回值的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 為 **TRUE**，而 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 是命令所滾動的行數。</span><span class="sxs-lookup"><span data-stu-id="53608-127">If the message is successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the return value is **TRUE**, and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the number of lines that the command scrolls.</span></span> <span data-ttu-id="53608-128">如果捲軸移至文字的開頭或結尾，則傳回的數位可能與滾動的實際行數不同。</span><span class="sxs-lookup"><span data-stu-id="53608-128">The number returned may not be the same as the actual number of lines scrolled if the scrolling moves to the beginning or the end of the text.</span></span> <span data-ttu-id="53608-129">如果 *wParam* 參數指定的值無效，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="53608-129">If the *wParam* parameter specifies an invalid value, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="53608-130">備註</span><span class="sxs-lookup"><span data-stu-id="53608-130">Remarks</span></span>

<span data-ttu-id="53608-131">若要滾動至特定的行或字元位置，請使用 [**EM \_ LINESCROLL**](em-linescroll.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="53608-131">To scroll to a specific line or character position, use the [**EM\_LINESCROLL**](em-linescroll.md) message.</span></span> <span data-ttu-id="53608-132">若要將插入號滾動至視圖，請使用 [**EM \_ SCROLLCARET**](em-scrollcaret.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="53608-132">To scroll the caret into view, use the [**EM\_SCROLLCARET**](em-scrollcaret.md) message.</span></span>

<span data-ttu-id="53608-133">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="53608-133">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="53608-134">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="53608-134">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53608-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="53608-135">Requirements</span></span>



| <span data-ttu-id="53608-136">需求</span><span class="sxs-lookup"><span data-stu-id="53608-136">Requirement</span></span> | <span data-ttu-id="53608-137">值</span><span class="sxs-lookup"><span data-stu-id="53608-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53608-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53608-138">Minimum supported client</span></span><br/> | <span data-ttu-id="53608-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53608-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53608-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53608-140">Minimum supported server</span></span><br/> | <span data-ttu-id="53608-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53608-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53608-142">標頭</span><span class="sxs-lookup"><span data-stu-id="53608-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="53608-143"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="53608-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53608-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53608-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="53608-145">**參考**</span><span class="sxs-lookup"><span data-stu-id="53608-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53608-146">**EM \_ LINESCROLL**</span><span class="sxs-lookup"><span data-stu-id="53608-146">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="53608-147">**EM \_ SCROLLCARET**</span><span class="sxs-lookup"><span data-stu-id="53608-147">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="53608-148">**WM \_ VSCROLL**</span><span class="sxs-lookup"><span data-stu-id="53608-148">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

