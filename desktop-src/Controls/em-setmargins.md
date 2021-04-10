---
title: 'EM_SETMARGINS 訊息 (Winuser .h) '
description: 設定編輯控制項的左邊界和右邊界的寬度。 訊息會重新繪製控制項，以反映新的邊界。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934549"
---
# <a name="em_setmargins-message"></a><span data-ttu-id="31a48-106">EM \_ SETMARGINS 訊息</span><span class="sxs-lookup"><span data-stu-id="31a48-106">EM\_SETMARGINS message</span></span>

<span data-ttu-id="31a48-107">設定編輯控制項的左邊界和右邊界的寬度。</span><span class="sxs-lookup"><span data-stu-id="31a48-107">Sets the widths of the left and right margins for an edit control.</span></span> <span data-ttu-id="31a48-108">訊息會重新繪製控制項，以反映新的邊界。</span><span class="sxs-lookup"><span data-stu-id="31a48-108">The message redraws the control to reflect the new margins.</span></span> <span data-ttu-id="31a48-109">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="31a48-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="31a48-110">參數</span><span class="sxs-lookup"><span data-stu-id="31a48-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a48-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31a48-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31a48-112">要設定的邊界。</span><span class="sxs-lookup"><span data-stu-id="31a48-112">The margins to set.</span></span> <span data-ttu-id="31a48-113">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="31a48-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="31a48-114">值</span><span class="sxs-lookup"><span data-stu-id="31a48-114">Value</span></span>                                                                                                                                                            | <span data-ttu-id="31a48-115">意義</span><span class="sxs-lookup"><span data-stu-id="31a48-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <span data-ttu-id="31a48-116"><dt>**EC \_ LEFTMARGIN**</dt></span><span class="sxs-lookup"><span data-stu-id="31a48-116"><dt>**EC\_LEFTMARGIN**</dt></span></span> </dl>    | <span data-ttu-id="31a48-117">設定左邊界。</span><span class="sxs-lookup"><span data-stu-id="31a48-117">Sets the left margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <span data-ttu-id="31a48-118"><dt>**EC \_ RIGHTMARGIN**</dt></span><span class="sxs-lookup"><span data-stu-id="31a48-118"><dt>**EC\_RIGHTMARGIN**</dt></span></span> </dl> | <span data-ttu-id="31a48-119">設定右邊界。</span><span class="sxs-lookup"><span data-stu-id="31a48-119">Sets the right margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <span data-ttu-id="31a48-120"><dt>**EC \_ USEFONTINFO**</dt></span><span class="sxs-lookup"><span data-stu-id="31a48-120"><dt>**EC\_USEFONTINFO**</dt></span></span> </dl> | <span data-ttu-id="31a48-121">**Rich edit 控制項：** 將左邊界和右邊界設定為使用控制項目前字型的文字度量計算的窄寬度。</span><span class="sxs-lookup"><span data-stu-id="31a48-121">**Rich edit controls:** Sets the left and right margins to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="31a48-122">如果未針對控制項設定字型，則邊界會設定為零。</span><span class="sxs-lookup"><span data-stu-id="31a48-122">If no font has been set for the control, the margins are set to zero.</span></span> <span data-ttu-id="31a48-123">*LParam* 參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="31a48-123">The *lParam* parameter is ignored.</span></span> <br/> <span data-ttu-id="31a48-124">**編輯控制項：** 在 *wParam* 參數中無法使用 **EC \_ USEFONTINFO** 值。</span><span class="sxs-lookup"><span data-stu-id="31a48-124">**Edit controls:** The **EC\_USEFONTINFO** value cannot be used in the *wParam* parameter.</span></span> <span data-ttu-id="31a48-125">它只能用在 *lParam* 參數中。</span><span class="sxs-lookup"><span data-stu-id="31a48-125">It can only be used in the *lParam* parameter.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="31a48-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31a48-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31a48-127">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定左邊界的新寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="31a48-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new width of the left margin, in pixels.</span></span> <span data-ttu-id="31a48-128">如果 *wParam* 不包含 **EC \_ LEFTMARGIN**，則會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="31a48-128">This value is ignored if *wParam* does not include **EC\_LEFTMARGIN**.</span></span>

<span data-ttu-id="31a48-129">**編輯控制項及豐富的編輯3.0 和更新版本：**[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))可以指定 **EC \_ USEFONTINFO** 值，將左邊界設定為使用控制項目前字型的文字度量來計算的窄寬度。</span><span class="sxs-lookup"><span data-stu-id="31a48-129">**Edit controls and Rich Edit 3.0 and later:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the left margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="31a48-130">如果未針對控制項設定字型，則邊界會設定為零。</span><span class="sxs-lookup"><span data-stu-id="31a48-130">If no font has been set for the control, the margin is set to zero.</span></span>

<span data-ttu-id="31a48-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定右邊界的新寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="31a48-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new width of the right margin, in pixels.</span></span> <span data-ttu-id="31a48-132">如果 *wParam* 不包含 **EC \_ RIGHTMARGIN**，則會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="31a48-132">This value is ignored if *wParam* does not include **EC\_RIGHTMARGIN**.</span></span>

<span data-ttu-id="31a48-133">**編輯控制項及豐富的編輯3.0 和更新版本：**[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))可以指定 **EC \_ USEFONTINFO** 值，將右邊界設定為使用控制項目前字型的文字度量來計算的窄寬度。</span><span class="sxs-lookup"><span data-stu-id="31a48-133">**Edit controls and Rich Edit 3.0 and later:** The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the right margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="31a48-134">如果未針對控制項設定字型，則邊界會設定為零。</span><span class="sxs-lookup"><span data-stu-id="31a48-134">If no font has been set for the control, the margin is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a48-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="31a48-135">Return value</span></span>

<span data-ttu-id="31a48-136">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="31a48-136">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31a48-137">備註</span><span class="sxs-lookup"><span data-stu-id="31a48-137">Remarks</span></span>

<span data-ttu-id="31a48-138">**編輯控制項：** 您無法在 *wParam* 參數中使用 **EC \_ USEFONTINFO** ，但可以在 *lParam* 參數中使用它。</span><span class="sxs-lookup"><span data-stu-id="31a48-138">**Edit controls:** You cannot use **EC\_USEFONTINFO** in the *wParam* parameter, but you can use it in the *lParam* parameter.</span></span>

<span data-ttu-id="31a48-139">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="31a48-139">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="31a48-140">所有 rich edit 版本都支援在 *wParam* 參數中使用 **EC \_ USEFONTINFO** 。</span><span class="sxs-lookup"><span data-stu-id="31a48-140">All rich edit versions support the use of **EC\_USEFONTINFO** in the *wParam* parameter.</span></span> <span data-ttu-id="31a48-141">不過，只有 Microsoft Rich Edit 3.0 和更新版本支援在 *lParam* 參數中使用 **EC \_ USEFONTINFO** 。</span><span class="sxs-lookup"><span data-stu-id="31a48-141">However, only Microsoft Rich Edit 3.0 and later support the use of **EC\_USEFONTINFO** in the *lParam* parameter.</span></span> <span data-ttu-id="31a48-142">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="31a48-142">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31a48-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="31a48-143">Requirements</span></span>



| <span data-ttu-id="31a48-144">需求</span><span class="sxs-lookup"><span data-stu-id="31a48-144">Requirement</span></span> | <span data-ttu-id="31a48-145">值</span><span class="sxs-lookup"><span data-stu-id="31a48-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a48-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31a48-146">Minimum supported client</span></span><br/> | <span data-ttu-id="31a48-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31a48-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="31a48-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31a48-148">Minimum supported server</span></span><br/> | <span data-ttu-id="31a48-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31a48-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="31a48-150">標頭</span><span class="sxs-lookup"><span data-stu-id="31a48-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a48-151"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="31a48-151"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31a48-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31a48-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a48-153">**EM \_ GETMARGINS**</span><span class="sxs-lookup"><span data-stu-id="31a48-153">**EM\_GETMARGINS**</span></span>](em-getmargins.md)
</dt> </dl>

 

