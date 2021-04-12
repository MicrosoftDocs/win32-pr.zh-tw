---
title: 'EM_POSFROMCHAR 訊息 (Winuser .h) '
description: 抓取編輯控制項中所指定字元的工作區座標。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508711"
---
# <a name="em_posfromchar-message"></a><span data-ttu-id="5e691-105">EM \_ POSFROMCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="5e691-105">EM\_POSFROMCHAR message</span></span>

<span data-ttu-id="5e691-106">抓取編輯控制項中所指定字元的工作區座標。</span><span class="sxs-lookup"><span data-stu-id="5e691-106">Retrieves the client area coordinates of a specified character in an edit control.</span></span> <span data-ttu-id="5e691-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="5e691-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e691-108">參數</span><span class="sxs-lookup"><span data-stu-id="5e691-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e691-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e691-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e691-110">**Rich Edit 1.0 和3.0：**[**POINTL**](/previous-versions//dd162807(v=vs.85))結構的指標，此結構會接收字元的工作區座標。</span><span class="sxs-lookup"><span data-stu-id="5e691-110">**Rich Edit 1.0 and 3.0:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that receives the client area coordinates of the character.</span></span> <span data-ttu-id="5e691-111">座標是在螢幕單元中，相對於控制項工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="5e691-111">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="5e691-112">**編輯控制項和 Rich edit 2.0：** 以零為基底的字元索引。</span><span class="sxs-lookup"><span data-stu-id="5e691-112">**Edit controls and Rich Edit 2.0:** The zero-based index of the character.</span></span>

</dd> <dt>

<span data-ttu-id="5e691-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e691-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e691-114">**Rich Edit 1.0 和3.0：** 以零為基底的字元索引。</span><span class="sxs-lookup"><span data-stu-id="5e691-114">**Rich Edit 1.0 and 3.0:** The zero-based index of the character.</span></span>

<span data-ttu-id="5e691-115">**編輯控制項和 Rich edit 2.0：** 未使用此參數。</span><span class="sxs-lookup"><span data-stu-id="5e691-115">**Edit controls and Rich Edit 2.0:** This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e691-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e691-116">Return value</span></span>

<span data-ttu-id="5e691-117">**Rich Edit 1.0 和3.0：** 未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="5e691-117">**Rich Edit 1.0 and 3.0:** The return value is not used.</span></span>

<span data-ttu-id="5e691-118">**編輯控制項和 Rich edit 2.0：** 傳回值包含字元的工作區座標。</span><span class="sxs-lookup"><span data-stu-id="5e691-118">**Edit controls and Rich Edit 2.0:** The return value contains the client area coordinates of the character.</span></span> <span data-ttu-id="5e691-119">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含水準座標，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含垂直座標。</span><span class="sxs-lookup"><span data-stu-id="5e691-119">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e691-120">備註</span><span class="sxs-lookup"><span data-stu-id="5e691-120">Remarks</span></span>

<span data-ttu-id="5e691-121">如果指定的字元未顯示在編輯控制項的工作區中，則傳回的座標可以是負值。</span><span class="sxs-lookup"><span data-stu-id="5e691-121">A returned coordinate can be a negative value if the specified character is not displayed in the edit control's client area.</span></span> <span data-ttu-id="5e691-122">座標會截斷為整數值。</span><span class="sxs-lookup"><span data-stu-id="5e691-122">The coordinates are truncated to integer values.</span></span>

<span data-ttu-id="5e691-123">如果字元是行分隔符號，則傳回的座標表示該行中最後一個可見字元以外的某個點。</span><span class="sxs-lookup"><span data-stu-id="5e691-123">If the character is a line delimiter, the returned coordinates indicate a point just beyond the last visible character in the line.</span></span> <span data-ttu-id="5e691-124">如果指定的索引大於控制項中最後一個字元的索引，控制項會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="5e691-124">If the specified index is greater than the index of the last character in the control, the control returns -1.</span></span>

<span data-ttu-id="5e691-125">**Rich Edit 3.0 和更新版本：** 為了回溯相容性，Microsoft Rich Edit 3.0 支援 Microsoft Rich Edit 2.0 所使用的語法。</span><span class="sxs-lookup"><span data-stu-id="5e691-125">**Rich Edit 3.0 and later:** For backward compatibility, Microsoft Rich Edit 3.0 supports the syntax used by Microsoft Rich Edit 2.0.</span></span> <span data-ttu-id="5e691-126">如果 Microsoft Rich Edit 3.0 偵測到 *wParam* 不是有效的 [**POINTL**](/previous-versions//dd162807(v=vs.85)) 指標，則會假設訊息是使用 Microsoft Rich Edit 2.0 語法來傳送。</span><span class="sxs-lookup"><span data-stu-id="5e691-126">If Microsoft Rich Edit 3.0 detects that *wParam* is not a valid [**POINTL**](/previous-versions//dd162807(v=vs.85)) pointer, it assumes the message was sent using the Microsoft Rich Edit 2.0 syntax.</span></span> <span data-ttu-id="5e691-127">在此情況下，它會使用傳回值傳回座標。</span><span class="sxs-lookup"><span data-stu-id="5e691-127">In this case, it uses the return value to return the coordinates.</span></span>

<span data-ttu-id="5e691-128">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="5e691-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="5e691-129">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="5e691-129">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e691-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e691-130">Requirements</span></span>



| <span data-ttu-id="5e691-131">需求</span><span class="sxs-lookup"><span data-stu-id="5e691-131">Requirement</span></span> | <span data-ttu-id="5e691-132">值</span><span class="sxs-lookup"><span data-stu-id="5e691-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e691-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e691-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5e691-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e691-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e691-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e691-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5e691-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e691-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e691-137">標頭</span><span class="sxs-lookup"><span data-stu-id="5e691-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e691-138"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5e691-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e691-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e691-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e691-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="5e691-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5e691-141">**EM \_ CHARFROMPOS**</span><span class="sxs-lookup"><span data-stu-id="5e691-141">**EM\_CHARFROMPOS**</span></span>](em-charfrompos.md)
</dt> <dt>

<span data-ttu-id="5e691-142">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="5e691-142">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="5e691-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e691-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

