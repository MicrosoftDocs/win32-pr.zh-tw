---
title: 'EM_SETREADONLY 訊息 (Winuser .h) '
description: 設定或移除編輯控制項 (ES READONLY) 的唯讀樣式 \_ 。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094503"
---
# <a name="em_setreadonly-message"></a><span data-ttu-id="8c0d5-105">EM \_ SETREADONLY 訊息</span><span class="sxs-lookup"><span data-stu-id="8c0d5-105">EM\_SETREADONLY message</span></span>

<span data-ttu-id="8c0d5-106">設定或移除編輯控制項 ([**ES \_ READONLY**](edit-control-styles.md)) 的唯讀樣式。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-106">Sets or removes the read-only style ([**ES\_READONLY**](edit-control-styles.md)) of an edit control.</span></span> <span data-ttu-id="8c0d5-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c0d5-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c0d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0d5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c0d5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0d5-110">指定是否要設定或移除 [**ES \_ READONLY**](edit-control-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-110">Specifies whether to set or remove the [**ES\_READONLY**](edit-control-styles.md) style.</span></span> <span data-ttu-id="8c0d5-111">**TRUE** 值會設定 **es \_ readonly** 樣式; **FALSE** 值會移除 **es \_ readonly** 樣式。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-111">A value of **TRUE** sets the **ES\_READONLY** style; a value of **FALSE** removes the **ES\_READONLY** style.</span></span>

</dd> <dt>

<span data-ttu-id="8c0d5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c0d5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0d5-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c0d5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c0d5-114">Return value</span></span>

<span data-ttu-id="8c0d5-115">如果作業成功，則傳回值為非零。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-115">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="8c0d5-116">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-116">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0d5-117">備註</span><span class="sxs-lookup"><span data-stu-id="8c0d5-117">Remarks</span></span>

<span data-ttu-id="8c0d5-118">當編輯控制項具有 [**ES \_ READONLY**](edit-control-styles.md) 樣式時，使用者無法變更編輯控制項內的文字。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-118">When an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, the user cannot change the text within the edit control.</span></span>

<span data-ttu-id="8c0d5-119">若要判斷編輯控制項是否有 [**ES \_ READONLY**](edit-control-styles.md) 樣式，請使用 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 函數搭配 GWL \_ 樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-119">To determine whether an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_STYLE flag.</span></span>

<span data-ttu-id="8c0d5-120">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8c0d5-121">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="8c0d5-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0d5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c0d5-122">Requirements</span></span>



| <span data-ttu-id="8c0d5-123">需求</span><span class="sxs-lookup"><span data-stu-id="8c0d5-123">Requirement</span></span> | <span data-ttu-id="8c0d5-124">值</span><span class="sxs-lookup"><span data-stu-id="8c0d5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0d5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c0d5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0d5-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c0d5-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c0d5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c0d5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0d5-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c0d5-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c0d5-129">標頭</span><span class="sxs-lookup"><span data-stu-id="8c0d5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c0d5-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8c0d5-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0d5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c0d5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0d5-132">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="8c0d5-132">**GetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

