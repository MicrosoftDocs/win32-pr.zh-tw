---
title: 'EM_SETSEL 訊息 (Winuser .h) '
description: 選取編輯控制項中的字元範圍。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464896"
---
# <a name="em_setsel-message"></a><span data-ttu-id="e8186-105">EM \_ SETSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="e8186-105">EM\_SETSEL message</span></span>

<span data-ttu-id="e8186-106">選取編輯控制項中的字元範圍。</span><span class="sxs-lookup"><span data-stu-id="e8186-106">Selects a range of characters in an edit control.</span></span> <span data-ttu-id="e8186-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="e8186-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8186-108">參數</span><span class="sxs-lookup"><span data-stu-id="e8186-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8186-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8186-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8186-110">選取範圍的起始字元位置。</span><span class="sxs-lookup"><span data-stu-id="e8186-110">The starting character position of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="e8186-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8186-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8186-112">選取範圍的結束字元位置。</span><span class="sxs-lookup"><span data-stu-id="e8186-112">The ending character position of the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8186-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8186-113">Return value</span></span>

<span data-ttu-id="e8186-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e8186-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8186-115">備註</span><span class="sxs-lookup"><span data-stu-id="e8186-115">Remarks</span></span>

<span data-ttu-id="e8186-116">開始值可以大於結束值。</span><span class="sxs-lookup"><span data-stu-id="e8186-116">The start value can be greater than the end value.</span></span> <span data-ttu-id="e8186-117">這兩個值的下限會指定選取範圍中第一個字元的字元位置。</span><span class="sxs-lookup"><span data-stu-id="e8186-117">The lower of the two values specifies the character position of the first character in the selection.</span></span> <span data-ttu-id="e8186-118">較高的值會指定選取範圍之外第一個字元的位置。</span><span class="sxs-lookup"><span data-stu-id="e8186-118">The higher value specifies the position of the first character beyond the selection.</span></span>

<span data-ttu-id="e8186-119">開始值是選取範圍的錨點，而結束值是使用中的端點。</span><span class="sxs-lookup"><span data-stu-id="e8186-119">The start value is the anchor point of the selection, and the end value is the active end.</span></span> <span data-ttu-id="e8186-120">如果使用者使用 SHIFT 鍵來調整選取範圍的大小，則現用端點可以移動，但錨點會維持不變。</span><span class="sxs-lookup"><span data-stu-id="e8186-120">If the user uses the SHIFT key to adjust the size of the selection, the active end can move but the anchor point remains the same.</span></span>

<span data-ttu-id="e8186-121">如果 [開始] 為0且結尾為-1，則會選取 [編輯] 控制項中的所有文字。</span><span class="sxs-lookup"><span data-stu-id="e8186-121">If the start is 0 and the end is -1, all the text in the edit control is selected.</span></span> <span data-ttu-id="e8186-122">如果啟動為-1，則會取消選取任何目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="e8186-122">If the start is -1, any current selection is deselected.</span></span>

<span data-ttu-id="e8186-123">**編輯控制項：** 不論開始和結束的相對值為何，控制項會在結束位置顯示閃爍的插入號。</span><span class="sxs-lookup"><span data-stu-id="e8186-123">**Edit controls:** The control displays a flashing caret at the end position regardless of the relative values of start and end.</span></span>

<span data-ttu-id="e8186-124">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="e8186-124">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e8186-125">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="e8186-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="e8186-126">如果編輯控制項具有 [**ES \_ NOHIDESEL**](edit-control-styles.md) 樣式，不論控制項是否有焦點，都會反白顯示選取的文字。</span><span class="sxs-lookup"><span data-stu-id="e8186-126">If the edit control has the [**ES\_NOHIDESEL**](edit-control-styles.md) style, the selected text is highlighted regardless of whether the control has focus.</span></span> <span data-ttu-id="e8186-127">如果沒有 **ES \_ NOHIDESEL** 樣式，只有在編輯控制項具有焦點時，才會反白顯示選取的文字。</span><span class="sxs-lookup"><span data-stu-id="e8186-127">Without the **ES\_NOHIDESEL** style, the selected text is highlighted only when the edit control has the focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8186-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8186-128">Requirements</span></span>



| <span data-ttu-id="e8186-129">需求</span><span class="sxs-lookup"><span data-stu-id="e8186-129">Requirement</span></span> | <span data-ttu-id="e8186-130">值</span><span class="sxs-lookup"><span data-stu-id="e8186-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8186-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8186-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e8186-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8186-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e8186-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8186-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e8186-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8186-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8186-135">標頭</span><span class="sxs-lookup"><span data-stu-id="e8186-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8186-136"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e8186-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8186-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8186-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="e8186-138">**參考**</span><span class="sxs-lookup"><span data-stu-id="e8186-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e8186-139">**EM \_ GETSEL**</span><span class="sxs-lookup"><span data-stu-id="e8186-139">**EM\_GETSEL**</span></span>](em-getsel.md)
</dt> <dt>

[<span data-ttu-id="e8186-140">**EM \_ REPLACESEL**</span><span class="sxs-lookup"><span data-stu-id="e8186-140">**EM\_REPLACESEL**</span></span>](em-replacesel.md)
</dt> <dt>

[<span data-ttu-id="e8186-141">**EM \_ SCROLLCARET**</span><span class="sxs-lookup"><span data-stu-id="e8186-141">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="e8186-142">**EM \_ EXSETSEL**</span><span class="sxs-lookup"><span data-stu-id="e8186-142">**EM\_EXSETSEL**</span></span>](em-exsetsel.md)
</dt> </dl>

 

 





