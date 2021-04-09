---
title: 'BM_SETCHECK 訊息 (Winuser .h) '
description: 設定選項按鈕或核取方塊的核取狀態。 您可以明確地傳送此訊息，或使用按鈕 \_ SetCheck 宏來傳送。
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- BM_SETCHECK message Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024676"
---
# <a name="bm_setcheck-message"></a><span data-ttu-id="660dd-105">BM \_ SETCHECK 訊息</span><span class="sxs-lookup"><span data-stu-id="660dd-105">BM\_SETCHECK message</span></span>

<span data-ttu-id="660dd-106">設定選項按鈕或核取方塊的核取狀態。</span><span class="sxs-lookup"><span data-stu-id="660dd-106">Sets the check state of a radio button or check box.</span></span> <span data-ttu-id="660dd-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="660dd-107">You can send this message explicitly or by using the [**Button\_SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="660dd-108">參數</span><span class="sxs-lookup"><span data-stu-id="660dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="660dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="660dd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="660dd-110">檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="660dd-110">The check state.</span></span> <span data-ttu-id="660dd-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="660dd-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="660dd-112">值</span><span class="sxs-lookup"><span data-stu-id="660dd-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="660dd-113">意義</span><span class="sxs-lookup"><span data-stu-id="660dd-113">Meaning</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <span data-ttu-id="660dd-114"><dt>**BST \_ 已核取**</dt></span><span class="sxs-lookup"><span data-stu-id="660dd-114"><dt>**BST\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="660dd-115">將按鈕狀態設定為 [已檢查]。</span><span class="sxs-lookup"><span data-stu-id="660dd-115">Sets the button state to checked.</span></span><br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <span data-ttu-id="660dd-116"><dt>**BST \_ 不定**</dt></span><span class="sxs-lookup"><span data-stu-id="660dd-116"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="660dd-117">將按鈕狀態設為灰色，表示不定的狀態。</span><span class="sxs-lookup"><span data-stu-id="660dd-117">Sets the button state to grayed, indicating an indeterminate state.</span></span> <span data-ttu-id="660dd-118">只有當按鈕具有 [**BS \_ 3STATE**](button-styles.md) 或 [**BS \_ AUTO3STATE**](button-styles.md) 樣式時，才使用此值。</span><span class="sxs-lookup"><span data-stu-id="660dd-118">Use this value only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <span data-ttu-id="660dd-119"><dt>**未核取 BST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="660dd-119"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>             | <span data-ttu-id="660dd-120">將按鈕狀態設定為 [已清除]。</span><span class="sxs-lookup"><span data-stu-id="660dd-120">Sets the button state to cleared.</span></span><br/>                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="660dd-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="660dd-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="660dd-122">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="660dd-122">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="660dd-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="660dd-123">Return value</span></span>

<span data-ttu-id="660dd-124">此訊息一律會傳回零。</span><span class="sxs-lookup"><span data-stu-id="660dd-124">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="660dd-125">備註</span><span class="sxs-lookup"><span data-stu-id="660dd-125">Remarks</span></span>

<span data-ttu-id="660dd-126">**BM \_ SETCHECK** 訊息不會影響推送按鈕。</span><span class="sxs-lookup"><span data-stu-id="660dd-126">The **BM\_SETCHECK** message has no effect on push buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="660dd-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="660dd-127">Requirements</span></span>



| <span data-ttu-id="660dd-128">需求</span><span class="sxs-lookup"><span data-stu-id="660dd-128">Requirement</span></span> | <span data-ttu-id="660dd-129">值</span><span class="sxs-lookup"><span data-stu-id="660dd-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="660dd-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="660dd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="660dd-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="660dd-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="660dd-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="660dd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="660dd-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="660dd-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="660dd-134">標頭</span><span class="sxs-lookup"><span data-stu-id="660dd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="660dd-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="660dd-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="660dd-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="660dd-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="660dd-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="660dd-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="660dd-138">**BM \_ GETCHECK**</span><span class="sxs-lookup"><span data-stu-id="660dd-138">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="660dd-139">**BM \_ >GETSTATE**</span><span class="sxs-lookup"><span data-stu-id="660dd-139">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="660dd-140">**BM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="660dd-140">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





