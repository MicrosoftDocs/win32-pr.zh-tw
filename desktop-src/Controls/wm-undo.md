---
title: 'WM_UNDO 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 復原訊息傳送至編輯控制項，以復原最後一個作業。 將此訊息傳送至編輯控制項時，會還原先前刪除的文字，或刪除先前加入的文字。
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO message Windows 控制項
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465848"
---
# <a name="wm_undo-message"></a><span data-ttu-id="04845-105">WM \_ 復原訊息</span><span class="sxs-lookup"><span data-stu-id="04845-105">WM\_UNDO message</span></span>

<span data-ttu-id="04845-106">應用程式會將 **WM \_ 復原** 訊息傳送至編輯控制項，以復原最後一個作業。</span><span class="sxs-lookup"><span data-stu-id="04845-106">An application sends a **WM\_UNDO** message to an edit control to undo the last operation.</span></span> <span data-ttu-id="04845-107">將此訊息傳送至編輯控制項時，會還原先前刪除的文字，或刪除先前加入的文字。</span><span class="sxs-lookup"><span data-stu-id="04845-107">When this message is sent to an edit control, the previously deleted text is restored or the previously added text is deleted.</span></span>

## <a name="parameters"></a><span data-ttu-id="04845-108">參數</span><span class="sxs-lookup"><span data-stu-id="04845-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04845-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04845-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04845-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="04845-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="04845-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04845-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04845-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="04845-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04845-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="04845-113">Return value</span></span>

<span data-ttu-id="04845-114">如果訊息成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="04845-114">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="04845-115">如果訊息失敗，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="04845-115">If the message fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="04845-116">備註</span><span class="sxs-lookup"><span data-stu-id="04845-116">Remarks</span></span>

<span data-ttu-id="04845-117">**Rich Edit：** 建議使用 [**EM \_ 復原**](em-undo.md) ，而不是使用 **WM \_ 復原**。</span><span class="sxs-lookup"><span data-stu-id="04845-117">**Rich Edit:** It is recommended that [**EM\_UNDO**](em-undo.md) be used instead of **WM\_UNDO**.</span></span>

## <a name="requirements"></a><span data-ttu-id="04845-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="04845-118">Requirements</span></span>



| <span data-ttu-id="04845-119">需求</span><span class="sxs-lookup"><span data-stu-id="04845-119">Requirement</span></span> | <span data-ttu-id="04845-120">值</span><span class="sxs-lookup"><span data-stu-id="04845-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04845-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04845-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04845-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04845-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="04845-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04845-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04845-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04845-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04845-125">標頭</span><span class="sxs-lookup"><span data-stu-id="04845-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="04845-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="04845-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04845-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04845-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="04845-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="04845-128">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="04845-129">**WM \_ 清除**</span><span class="sxs-lookup"><span data-stu-id="04845-129">**WM\_CLEAR**</span></span>](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[<span data-ttu-id="04845-130">**WM \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="04845-130">**WM\_COPY**</span></span>](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[<span data-ttu-id="04845-131">**WM \_ 剪下**</span><span class="sxs-lookup"><span data-stu-id="04845-131">**WM\_CUT**</span></span>](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[<span data-ttu-id="04845-132">**WM \_ 貼上**</span><span class="sxs-lookup"><span data-stu-id="04845-132">**WM\_PASTE**</span></span>](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

