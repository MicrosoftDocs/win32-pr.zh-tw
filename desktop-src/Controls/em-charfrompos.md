---
title: 'EM_CHARFROMPOS 訊息 (Winuser .h) '
description: 取得最接近編輯控制項工作區中指定點之字元的相關資訊。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465901"
---
# <a name="em_charfrompos-message"></a><span data-ttu-id="1d669-105">EM \_ CHARFROMPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="1d669-105">EM\_CHARFROMPOS message</span></span>

<span data-ttu-id="1d669-106">取得最接近編輯控制項工作區中指定點之字元的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1d669-106">Gets information about the character closest to a specified point in the client area of an edit control.</span></span> <span data-ttu-id="1d669-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="1d669-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d669-108">參數</span><span class="sxs-lookup"><span data-stu-id="1d669-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d669-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d669-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d669-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="1d669-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d669-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d669-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d669-112">控制項工作區中某個點的座標。</span><span class="sxs-lookup"><span data-stu-id="1d669-112">The coordinates of a point in the control's client area.</span></span> <span data-ttu-id="1d669-113">座標是在螢幕單元中，相對於控制項工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="1d669-113">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="1d669-114">**Rich edit 控制項：** 包含水準和垂直座標之 [**POINTL**](/previous-versions//dd162807(v=vs.85)) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1d669-114">**Rich edit controls:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that contains the horizontal and vertical coordinates.</span></span>

<span data-ttu-id="1d669-115">**編輯控制項：**[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含水準座標。</span><span class="sxs-lookup"><span data-stu-id="1d669-115">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate.</span></span> <span data-ttu-id="1d669-116">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含垂直座標。</span><span class="sxs-lookup"><span data-stu-id="1d669-116">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d669-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d669-117">Return value</span></span>

<span data-ttu-id="1d669-118">**Rich edit 控制項：** 傳回值會指定最接近指定點的字元之以零為基底的字元索引。</span><span class="sxs-lookup"><span data-stu-id="1d669-118">**Rich edit controls:** The return value specifies the zero-based character index of the character nearest the specified point.</span></span> <span data-ttu-id="1d669-119">如果指定的點超過控制項的最後一個字元，則傳回值會指出編輯控制項中的最後一個字元。</span><span class="sxs-lookup"><span data-stu-id="1d669-119">The return value indicates the last character in the edit control if the specified point is beyond the last character in the control.</span></span>

<span data-ttu-id="1d669-120">**編輯控制項：**[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定最接近指定點的字元之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="1d669-120">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the character nearest the specified point.</span></span> <span data-ttu-id="1d669-121">此索引是相對於控制項的開頭，而不是行的開頭。</span><span class="sxs-lookup"><span data-stu-id="1d669-121">This index is relative to the beginning of the control, not the beginning of the line.</span></span> <span data-ttu-id="1d669-122">如果指定的點超過編輯控制項中的最後一個字元，則傳回值會指出控制項中的最後一個字元。</span><span class="sxs-lookup"><span data-stu-id="1d669-122">If the specified point is beyond the last character in the edit control, the return value indicates the last character in the control.</span></span> <span data-ttu-id="1d669-123">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定包含字元之行的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="1d669-123">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the line that contains the character.</span></span> <span data-ttu-id="1d669-124">針對單行編輯控制項，此值為零。</span><span class="sxs-lookup"><span data-stu-id="1d669-124">For single-line edit controls, this value is zero.</span></span> <span data-ttu-id="1d669-125">如果指定的點超過行的最後一個可見字元，則索引會指出行分隔符號。</span><span class="sxs-lookup"><span data-stu-id="1d669-125">The index indicates the line delimiter if the specified point is beyond the last visible character in a line.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d669-126">備註</span><span class="sxs-lookup"><span data-stu-id="1d669-126">Remarks</span></span>

<span data-ttu-id="1d669-127">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="1d669-127">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1d669-128">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="1d669-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="1d669-129">如果某個點傳遞至 **EM \_ CHARFROMPOS** 做為 *lParam* ，且該點超出編輯控制項的界限，則 *lResult* 為 (65535，65535) 。</span><span class="sxs-lookup"><span data-stu-id="1d669-129">If a point is passed to **EM\_CHARFROMPOS** as the *lParam* and the point is outside the bounds of the edit control, then the *lResult* is (65535, 65535).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d669-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d669-130">Requirements</span></span>



| <span data-ttu-id="1d669-131">需求</span><span class="sxs-lookup"><span data-stu-id="1d669-131">Requirement</span></span> | <span data-ttu-id="1d669-132">值</span><span class="sxs-lookup"><span data-stu-id="1d669-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d669-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d669-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1d669-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d669-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1d669-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d669-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1d669-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d669-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d669-137">標頭</span><span class="sxs-lookup"><span data-stu-id="1d669-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d669-138"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1d669-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d669-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d669-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d669-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="1d669-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d669-141">**EM \_ POSFROMCHAR**</span><span class="sxs-lookup"><span data-stu-id="1d669-141">**EM\_POSFROMCHAR**</span></span>](em-posfromchar.md)
</dt> <dt>

<span data-ttu-id="1d669-142">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="1d669-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1d669-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="1d669-143">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

<span data-ttu-id="1d669-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d669-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

