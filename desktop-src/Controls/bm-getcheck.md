---
title: 'BM_GETCHECK 訊息 (Winuser .h) '
description: 取得選項按鈕或核取方塊的檢查狀態。 您可以明確地傳送此訊息，或使用按鈕 \_ GetCheck 宏。
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK message Windows 控制項
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105768"
---
# <a name="bm_getcheck-message"></a><span data-ttu-id="cd6e0-105">BM \_ GETCHECK 訊息</span><span class="sxs-lookup"><span data-stu-id="cd6e0-105">BM\_GETCHECK message</span></span>

<span data-ttu-id="cd6e0-106">取得選項按鈕或核取方塊的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="cd6e0-106">Gets the check state of a radio button or check box.</span></span> <span data-ttu-id="cd6e0-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) 宏。</span><span class="sxs-lookup"><span data-stu-id="cd6e0-107">You can send this message explicitly or use the [**Button\_GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd6e0-108">參數</span><span class="sxs-lookup"><span data-stu-id="cd6e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd6e0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd6e0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd6e0-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="cd6e0-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd6e0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd6e0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd6e0-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="cd6e0-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd6e0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd6e0-113">Return value</span></span>

<span data-ttu-id="cd6e0-114">使用 [**BS \_ AUTOCHECKBOX**](button-styles.md)、 [**BS \_ AUTORADIOBUTTON**](button-styles.md)、 [**BS \_ AUTO3STATE**](button-styles.md)、 [**BS \_ CHECKBOX**](button-styles.md)、 [**BS \_ 單選**](button-styles.md)按鈕或 [**BS \_ 3STATE**](button-styles.md) 樣式所建立之按鈕的傳回值可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="cd6e0-114">The return value from a button created with the [**BS\_AUTOCHECKBOX**](button-styles.md), [**BS\_AUTORADIOBUTTON**](button-styles.md), [**BS\_AUTO3STATE**](button-styles.md), [**BS\_CHECKBOX**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), or [**BS\_3STATE**](button-styles.md) style can be one of the following.</span></span>



| <span data-ttu-id="cd6e0-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cd6e0-115">Return code</span></span>                                                                                       | <span data-ttu-id="cd6e0-116">Description</span><span class="sxs-lookup"><span data-stu-id="cd6e0-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd6e0-117"><dt>**BST \_ 已核取**</dt></span><span class="sxs-lookup"><span data-stu-id="cd6e0-117"><dt>**BST\_CHECKED**</dt></span></span> </dl>       | <span data-ttu-id="cd6e0-118">按鈕已核取。</span><span class="sxs-lookup"><span data-stu-id="cd6e0-118">Button is checked.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="cd6e0-119"><dt>**BST \_ 不定**</dt></span><span class="sxs-lookup"><span data-stu-id="cd6e0-119"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="cd6e0-120">按鈕會呈現灰色，表示只有在按鈕具有 [**BS \_ 3STATE**](button-styles.md) 或 [**BS \_ AUTO3STATE**](button-styles.md) 樣式) 時，才會套用不定狀態 (。</span><span class="sxs-lookup"><span data-stu-id="cd6e0-120">Button is grayed, indicating an indeterminate state (applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style).</span></span><br/> |
| <dl> <span data-ttu-id="cd6e0-121"><dt>**未核取 BST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd6e0-121"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>     | <span data-ttu-id="cd6e0-122">已清除按鈕</span><span class="sxs-lookup"><span data-stu-id="cd6e0-122">Button is cleared</span></span><br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="cd6e0-123">備註</span><span class="sxs-lookup"><span data-stu-id="cd6e0-123">Remarks</span></span>

<span data-ttu-id="cd6e0-124">如果按鈕的樣式不是列出的，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="cd6e0-124">If the button has a style other than those listed, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6e0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd6e0-125">Requirements</span></span>



| <span data-ttu-id="cd6e0-126">需求</span><span class="sxs-lookup"><span data-stu-id="cd6e0-126">Requirement</span></span> | <span data-ttu-id="cd6e0-127">值</span><span class="sxs-lookup"><span data-stu-id="cd6e0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6e0-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd6e0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cd6e0-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd6e0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd6e0-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd6e0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cd6e0-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd6e0-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd6e0-132">標頭</span><span class="sxs-lookup"><span data-stu-id="cd6e0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd6e0-133"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cd6e0-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd6e0-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd6e0-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd6e0-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="cd6e0-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd6e0-136">**BM \_ >GETSTATE**</span><span class="sxs-lookup"><span data-stu-id="cd6e0-136">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="cd6e0-137">**BM \_ SETCHECK**</span><span class="sxs-lookup"><span data-stu-id="cd6e0-137">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





