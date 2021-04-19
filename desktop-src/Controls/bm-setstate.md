---
title: 'BM_SETSTATE 訊息 (Winuser .h) '
description: 設定按鈕的醒目提示狀態。 醒目提示狀態會指出按鈕是否反白顯示，如同使用者是否已推送按鈕。 您可以明確地傳送此訊息，或使用按鈕 \_ SetState 宏。
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969964"
---
# <a name="bm_setstate-message"></a><span data-ttu-id="5eef6-106">BM \_ SETSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="5eef6-106">BM\_SETSTATE message</span></span>

<span data-ttu-id="5eef6-107">設定按鈕的醒目提示狀態。</span><span class="sxs-lookup"><span data-stu-id="5eef6-107">Sets the highlight state of a button.</span></span> <span data-ttu-id="5eef6-108">醒目提示狀態會指出按鈕是否反白顯示，如同使用者是否已推送按鈕。</span><span class="sxs-lookup"><span data-stu-id="5eef6-108">The highlight state indicates whether the button is highlighted as if the user had pushed it.</span></span> <span data-ttu-id="5eef6-109">您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) 宏。</span><span class="sxs-lookup"><span data-stu-id="5eef6-109">You can send this message explicitly or use the [**Button\_SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5eef6-110">參數</span><span class="sxs-lookup"><span data-stu-id="5eef6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eef6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5eef6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5eef6-112">指定是否要反白顯示按鈕的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="5eef6-112">A **BOOL** that specifies whether the button is highlighted.</span></span> <span data-ttu-id="5eef6-113">值為 **TRUE** 時，會反白顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="5eef6-113">A value of **TRUE** highlights the button.</span></span> <span data-ttu-id="5eef6-114">**FALSE** 值會移除任何反白顯示。</span><span class="sxs-lookup"><span data-stu-id="5eef6-114">A value of **FALSE** removes any highlighting.</span></span>

</dd> <dt>

<span data-ttu-id="5eef6-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5eef6-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5eef6-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="5eef6-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eef6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5eef6-117">Return value</span></span>

<span data-ttu-id="5eef6-118">此訊息一律會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5eef6-118">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eef6-119">備註</span><span class="sxs-lookup"><span data-stu-id="5eef6-119">Remarks</span></span>

<span data-ttu-id="5eef6-120">醒目提示只會影響按鈕的外觀。</span><span class="sxs-lookup"><span data-stu-id="5eef6-120">Highlighting affects only the appearance of a button.</span></span> <span data-ttu-id="5eef6-121">它不會影響選項按鈕或核取方塊的核取狀態。</span><span class="sxs-lookup"><span data-stu-id="5eef6-121">It has no effect on the check state of a radio button or check box.</span></span>

<span data-ttu-id="5eef6-122">當使用者將游標放在其上方，然後按下並按住滑鼠左鍵時，按鈕就會自動反白顯示。</span><span class="sxs-lookup"><span data-stu-id="5eef6-122">A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button.</span></span> <span data-ttu-id="5eef6-123">當使用者放開滑鼠按鍵時，就會移除反白顯示。</span><span class="sxs-lookup"><span data-stu-id="5eef6-123">The highlighting is removed when the user releases the mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eef6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5eef6-124">Requirements</span></span>



| <span data-ttu-id="5eef6-125">需求</span><span class="sxs-lookup"><span data-stu-id="5eef6-125">Requirement</span></span> | <span data-ttu-id="5eef6-126">值</span><span class="sxs-lookup"><span data-stu-id="5eef6-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eef6-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5eef6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5eef6-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5eef6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5eef6-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5eef6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5eef6-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5eef6-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5eef6-131">標頭</span><span class="sxs-lookup"><span data-stu-id="5eef6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eef6-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5eef6-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eef6-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5eef6-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="5eef6-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="5eef6-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5eef6-135">**BM \_ >GETSTATE**</span><span class="sxs-lookup"><span data-stu-id="5eef6-135">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="5eef6-136">**BM \_ SETCHECK**</span><span class="sxs-lookup"><span data-stu-id="5eef6-136">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





