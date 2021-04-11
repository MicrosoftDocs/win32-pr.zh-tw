---
title: 'EM_SCROLLCARET 訊息 (Winuser .h) '
description: 將插入號滾動至編輯控制項中的 view。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- EM_SCROLLCARET message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106265"
---
# <a name="em_scrollcaret-message"></a><span data-ttu-id="1923e-105">EM \_ SCROLLCARET 訊息</span><span class="sxs-lookup"><span data-stu-id="1923e-105">EM\_SCROLLCARET message</span></span>

<span data-ttu-id="1923e-106">將插入號滾動至編輯控制項中的 view。</span><span class="sxs-lookup"><span data-stu-id="1923e-106">Scrolls the caret into view in an edit control.</span></span> <span data-ttu-id="1923e-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="1923e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1923e-108">參數</span><span class="sxs-lookup"><span data-stu-id="1923e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1923e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1923e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1923e-110">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="1923e-110">This parameter is reserved.</span></span> <span data-ttu-id="1923e-111">它應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="1923e-111">It should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="1923e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1923e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1923e-113">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="1923e-113">This parameter is reserved.</span></span> <span data-ttu-id="1923e-114">它應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="1923e-114">It should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1923e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1923e-115">Return value</span></span>

<span data-ttu-id="1923e-116">傳回值沒有意義。</span><span class="sxs-lookup"><span data-stu-id="1923e-116">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1923e-117">備註</span><span class="sxs-lookup"><span data-stu-id="1923e-117">Remarks</span></span>

<span data-ttu-id="1923e-118">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="1923e-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1923e-119">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="1923e-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1923e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1923e-120">Requirements</span></span>



| <span data-ttu-id="1923e-121">需求</span><span class="sxs-lookup"><span data-stu-id="1923e-121">Requirement</span></span> | <span data-ttu-id="1923e-122">值</span><span class="sxs-lookup"><span data-stu-id="1923e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1923e-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1923e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1923e-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1923e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1923e-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1923e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1923e-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1923e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1923e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1923e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1923e-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1923e-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1923e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1923e-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="1923e-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="1923e-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1923e-131">**EM \_ LINESCROLL**</span><span class="sxs-lookup"><span data-stu-id="1923e-131">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="1923e-132">**EM \_ 捲軸**</span><span class="sxs-lookup"><span data-stu-id="1923e-132">**EM\_SCROLL**</span></span>](em-scroll.md)
</dt> <dt>

[<span data-ttu-id="1923e-133">**WM \_ VSCROLL**</span><span class="sxs-lookup"><span data-stu-id="1923e-133">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

 





