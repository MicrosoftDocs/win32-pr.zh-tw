---
title: 'EM_GETSEL 訊息 (Winuser .h) '
description: 取得 (在編輯控制項中目前選取範圍的 TCHARs) 中的開始和結束字元位置。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025036"
---
# <a name="em_getsel-message"></a><span data-ttu-id="39a3d-105">EM \_ GETSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="39a3d-105">EM\_GETSEL message</span></span>

<span data-ttu-id="39a3d-106">取得 **TCHAR** 的開始和結束字元位置 (在編輯控制項中目前選取範圍的) 。</span><span class="sxs-lookup"><span data-stu-id="39a3d-106">Gets the starting and ending character positions (in **TCHAR** s) of the current selection in an edit control.</span></span> <span data-ttu-id="39a3d-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="39a3d-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="39a3d-108">參數</span><span class="sxs-lookup"><span data-stu-id="39a3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a3d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39a3d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a3d-110">**DWORD** 值的指標，此值會接收選取範圍的開始位置。</span><span class="sxs-lookup"><span data-stu-id="39a3d-110">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="39a3d-111">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="39a3d-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39a3d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39a3d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a3d-113">**DWORD** 值的指標，此值會接收選取範圍結尾之後第一個未選取字元的位置。</span><span class="sxs-lookup"><span data-stu-id="39a3d-113">A pointer to a **DWORD** value that receives the position of the first unselected character after the end of the selection.</span></span> <span data-ttu-id="39a3d-114">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="39a3d-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a3d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="39a3d-115">Return value</span></span>

<span data-ttu-id="39a3d-116">傳回值是以零為起始的值，其中包含選取範圍在 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))中的開始位置，以及 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中最後一個選取的 **TCHAR** 之後的第一個 **TCHAR** 位置。</span><span class="sxs-lookup"><span data-stu-id="39a3d-116">The return value is a zero-based value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the position of the first **TCHAR** after the last selected **TCHAR** in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="39a3d-117">如果其中一個值超過65535，則傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="39a3d-117">If either of these values exceeds 65,535, the return value is -1.</span></span>

<span data-ttu-id="39a3d-118">最好使用 *wParam* 和 *lParam* 中傳回的值，因為它們是完整的32位值。</span><span class="sxs-lookup"><span data-stu-id="39a3d-118">It is better to use the values returned in *wParam* and *lParam* because they are full 32-bit values.</span></span>

## <a name="remarks"></a><span data-ttu-id="39a3d-119">備註</span><span class="sxs-lookup"><span data-stu-id="39a3d-119">Remarks</span></span>

<span data-ttu-id="39a3d-120">如果沒有選取專案，開始和結束值都是插入號的位置。</span><span class="sxs-lookup"><span data-stu-id="39a3d-120">If there is no selection, the starting and ending values are both the position of the caret.</span></span>

<span data-ttu-id="39a3d-121">**Rich edit 控制項：** 您也可以使用 [**EM \_ EXGETSEL**](em-exgetsel.md) 訊息來取得相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="39a3d-121">**Rich edit controls:** You can also use the [**EM\_EXGETSEL**](em-exgetsel.md) message to retrieve the same information.</span></span> <span data-ttu-id="39a3d-122">**EM \_EXGETSEL** 也會傳回開頭和結尾字元位置做為32位值。</span><span class="sxs-lookup"><span data-stu-id="39a3d-122">**EM\_EXGETSEL** also returns starting and ending character positions as 32-bit values.</span></span>

<span data-ttu-id="39a3d-123">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="39a3d-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="39a3d-124">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="39a3d-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39a3d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="39a3d-125">Requirements</span></span>



| <span data-ttu-id="39a3d-126">需求</span><span class="sxs-lookup"><span data-stu-id="39a3d-126">Requirement</span></span> | <span data-ttu-id="39a3d-127">值</span><span class="sxs-lookup"><span data-stu-id="39a3d-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a3d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39a3d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39a3d-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39a3d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="39a3d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39a3d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39a3d-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39a3d-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39a3d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="39a3d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a3d-133"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="39a3d-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a3d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39a3d-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="39a3d-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="39a3d-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39a3d-136">**EM \_ EXGETSEL**</span><span class="sxs-lookup"><span data-stu-id="39a3d-136">**EM\_EXGETSEL**</span></span>](em-exgetsel.md)
</dt> <dt>

[<span data-ttu-id="39a3d-137">**EM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="39a3d-137">**EM\_SETSEL**</span></span>](em-setsel.md)
</dt> </dl>

 

