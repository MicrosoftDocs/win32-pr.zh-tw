---
title: 'EM_SETRECT 訊息 (Winuser .h) '
description: 設定多行編輯控制項的格式化矩形。
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12b171478b0cb9d47496d20d4d1b6b1e8ddd29a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025033"
---
# <a name="em_setrect-message"></a><span data-ttu-id="643de-104">EM \_ SETRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="643de-104">EM\_SETRECT message</span></span>

<span data-ttu-id="643de-105">設定多行編輯控制項的 [格式化矩形](about-edit-controls.md) 。</span><span class="sxs-lookup"><span data-stu-id="643de-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="643de-106">格式化矩形是控制項用來繪製文字的限制矩形。</span><span class="sxs-lookup"><span data-stu-id="643de-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="643de-107">限制矩形與編輯控制項視窗的大小無關。</span><span class="sxs-lookup"><span data-stu-id="643de-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="643de-108">此訊息只會由多行編輯控制項處理。</span><span class="sxs-lookup"><span data-stu-id="643de-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="643de-109">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="643de-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="643de-110">參數</span><span class="sxs-lookup"><span data-stu-id="643de-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="643de-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="643de-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="643de-112">**Rich Edit 2.0 和更新版本：** 指出 *lParam* 是否指定絕對或相對座標。</span><span class="sxs-lookup"><span data-stu-id="643de-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="643de-113">值為零表示絕對座標。</span><span class="sxs-lookup"><span data-stu-id="643de-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="643de-114">值為1時，表示相對於目前格式化矩形的位移。</span><span class="sxs-lookup"><span data-stu-id="643de-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="643de-115"> (位移可以是正數或負數。 ) </span><span class="sxs-lookup"><span data-stu-id="643de-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="643de-116">**編輯控制項和 Rich edit 1.0：** 未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="643de-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="643de-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="643de-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="643de-118">[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，指定矩形的新維度。</span><span class="sxs-lookup"><span data-stu-id="643de-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="643de-119">如果這個參數為 **Null**，則會將格式化矩形設定為其預設值。</span><span class="sxs-lookup"><span data-stu-id="643de-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="643de-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="643de-120">Return value</span></span>

<span data-ttu-id="643de-121">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="643de-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="643de-122">備註</span><span class="sxs-lookup"><span data-stu-id="643de-122">Remarks</span></span>

<span data-ttu-id="643de-123">如果已安裝觸控裝置，或從已 (安裝勾點的執行緒傳送 **EM \_ SETRECT** ，則將 *lParam* 設定為 **Null** 沒有任何作用，請參閱 [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)) 。</span><span class="sxs-lookup"><span data-stu-id="643de-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="643de-124">在這些情況下， *lParam* 應該包含 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構的有效指標。</span><span class="sxs-lookup"><span data-stu-id="643de-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="643de-125">**EM \_ SETRECT** 訊息會重新繪製編輯控制項的文字。</span><span class="sxs-lookup"><span data-stu-id="643de-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="643de-126">若要變更格式化矩形的大小而不重繪文字，請使用 [**EM \_ SETRECTNP**](em-setrectnp.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="643de-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="643de-127">當您第一次建立編輯控制項時，格式化矩形會設定為預設大小。</span><span class="sxs-lookup"><span data-stu-id="643de-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="643de-128">您可以使用 **EM \_ SETRECT** 訊息，將格式化矩形放大或小於編輯控制項視窗。</span><span class="sxs-lookup"><span data-stu-id="643de-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="643de-129">如果編輯控制項沒有水準捲軸，且格式化矩形設定為大於編輯控制項視窗，則文字行超過編輯控制項視窗的寬度 (但小於格式化矩形) 的寬度，而不是換行。</span><span class="sxs-lookup"><span data-stu-id="643de-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="643de-130">如果編輯控制項包含框線，則會以框線的大小來縮減格式化矩形。</span><span class="sxs-lookup"><span data-stu-id="643de-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="643de-131">如果您要調整 [**em \_ GETRECT**](em-getrect.md) 訊息所傳回的矩形，您必須先移除框線的大小，然後才能使用該矩形搭配 **EM \_ SETRECT** 訊息。</span><span class="sxs-lookup"><span data-stu-id="643de-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="643de-132">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="643de-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="643de-133">格式化矩形不包含選取範圍列，也就是每個段落左方未標記的區域。</span><span class="sxs-lookup"><span data-stu-id="643de-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="643de-134">當使用者按一下選取範圍時，就會選取對應的行。</span><span class="sxs-lookup"><span data-stu-id="643de-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="643de-135">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="643de-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="643de-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="643de-136">Requirements</span></span>



| <span data-ttu-id="643de-137">需求</span><span class="sxs-lookup"><span data-stu-id="643de-137">Requirement</span></span> | <span data-ttu-id="643de-138">值</span><span class="sxs-lookup"><span data-stu-id="643de-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="643de-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="643de-139">Minimum supported client</span></span><br/> | <span data-ttu-id="643de-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="643de-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="643de-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="643de-141">Minimum supported server</span></span><br/> | <span data-ttu-id="643de-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="643de-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="643de-143">標頭</span><span class="sxs-lookup"><span data-stu-id="643de-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="643de-144"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="643de-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="643de-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="643de-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="643de-146">**參考**</span><span class="sxs-lookup"><span data-stu-id="643de-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="643de-147">**EM \_ GETRECT**</span><span class="sxs-lookup"><span data-stu-id="643de-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="643de-148">**EM \_ SETRECTNP**</span><span class="sxs-lookup"><span data-stu-id="643de-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="643de-149">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="643de-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="643de-150">[**矩形**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="643de-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

