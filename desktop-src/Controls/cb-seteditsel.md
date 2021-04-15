---
title: 'CB_SETEDITSEL 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETEDITSEL 訊息，以選取下拉式方塊編輯控制項中的字元。
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465252"
---
# <a name="cb_seteditsel-message"></a><span data-ttu-id="02a7f-104">CB \_ SETEDITSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="02a7f-104">CB\_SETEDITSEL message</span></span>

<span data-ttu-id="02a7f-105">應用程式會傳送 **CB \_ SETEDITSEL** 訊息，以選取下拉式方塊編輯控制項中的字元。</span><span class="sxs-lookup"><span data-stu-id="02a7f-105">An application sends a **CB\_SETEDITSEL** message to select characters in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="02a7f-106">參數</span><span class="sxs-lookup"><span data-stu-id="02a7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a7f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02a7f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02a7f-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="02a7f-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="02a7f-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02a7f-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a7f-110">*LParam* 的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定開始位置。</span><span class="sxs-lookup"><span data-stu-id="02a7f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* specifies the starting position.</span></span> <span data-ttu-id="02a7f-111">如果 **LOWORD** 為-1，則會移除選取範圍（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="02a7f-111">If the **LOWORD** is -1, the selection, if any, is removed.</span></span>

<span data-ttu-id="02a7f-112">*LParam* 的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定結束位置。</span><span class="sxs-lookup"><span data-stu-id="02a7f-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of *lParam* specifies the ending position.</span></span> <span data-ttu-id="02a7f-113">如果 **HIWORD** 為-1，則會選取從開始位置到編輯控制項中最後一個字元的所有文字。</span><span class="sxs-lookup"><span data-stu-id="02a7f-113">If the **HIWORD** is -1, all text from the starting position to the last character in the edit control is selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a7f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="02a7f-114">Return value</span></span>

<span data-ttu-id="02a7f-115">如果訊息成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="02a7f-115">If the message succeeds, the return value is **TRUE**.</span></span> <span data-ttu-id="02a7f-116">如果訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) 樣式的下拉式方塊，則為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="02a7f-116">If the message is sent to a combo box with the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a7f-117">備註</span><span class="sxs-lookup"><span data-stu-id="02a7f-117">Remarks</span></span>

<span data-ttu-id="02a7f-118">這些位置以零為基底。</span><span class="sxs-lookup"><span data-stu-id="02a7f-118">The positions are zero-based.</span></span> <span data-ttu-id="02a7f-119">編輯控制項的第一個字元位於零位置。</span><span class="sxs-lookup"><span data-stu-id="02a7f-119">The first character of the edit control is in the zero position.</span></span> <span data-ttu-id="02a7f-120">最後一個選取的字元之後的第一個字元是在結束位置。</span><span class="sxs-lookup"><span data-stu-id="02a7f-120">The first character after the last selected character is in the ending position.</span></span> <span data-ttu-id="02a7f-121">例如，若要選取編輯控制項的前四個字元，請使用0和結束位置4的開始位置。</span><span class="sxs-lookup"><span data-stu-id="02a7f-121">For example, to select the first four characters of the edit control, use a starting position of 0 and an ending position of 4.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a7f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="02a7f-122">Requirements</span></span>



| <span data-ttu-id="02a7f-123">需求</span><span class="sxs-lookup"><span data-stu-id="02a7f-123">Requirement</span></span> | <span data-ttu-id="02a7f-124">值</span><span class="sxs-lookup"><span data-stu-id="02a7f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02a7f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02a7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="02a7f-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02a7f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="02a7f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02a7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="02a7f-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02a7f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="02a7f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="02a7f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="02a7f-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="02a7f-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a7f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02a7f-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="02a7f-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="02a7f-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="02a7f-133">**CB \_ GETEDITSEL**</span><span class="sxs-lookup"><span data-stu-id="02a7f-133">**CB\_GETEDITSEL**</span></span>](cb-geteditsel.md)
</dt> <dt>

<span data-ttu-id="02a7f-134">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="02a7f-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="02a7f-135">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="02a7f-135">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

