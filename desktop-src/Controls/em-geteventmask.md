---
title: 'EM_GETEVENTMASK 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項的事件遮罩。 事件遮罩會指定控制項傳送至其父視窗的通知碼。
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- EM_GETEVENTMASK message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934737"
---
# <a name="em_geteventmask-message"></a><span data-ttu-id="56302-105">EM \_ GETEVENTMASK 訊息</span><span class="sxs-lookup"><span data-stu-id="56302-105">EM\_GETEVENTMASK message</span></span>

<span data-ttu-id="56302-106">抓取 rich edit 控制項的事件遮罩。</span><span class="sxs-lookup"><span data-stu-id="56302-106">Retrieves the event mask for a rich edit control.</span></span> <span data-ttu-id="56302-107">事件遮罩會指定控制項傳送至其父視窗的通知碼。</span><span class="sxs-lookup"><span data-stu-id="56302-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="56302-108">參數</span><span class="sxs-lookup"><span data-stu-id="56302-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56302-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56302-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56302-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="56302-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="56302-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56302-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56302-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="56302-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56302-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="56302-113">Return value</span></span>

<span data-ttu-id="56302-114">此訊息會傳回 rich edit 控制項的事件遮罩。</span><span class="sxs-lookup"><span data-stu-id="56302-114">This message returns the event mask for the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="56302-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="56302-115">Requirements</span></span>



| <span data-ttu-id="56302-116">需求</span><span class="sxs-lookup"><span data-stu-id="56302-116">Requirement</span></span> | <span data-ttu-id="56302-117">值</span><span class="sxs-lookup"><span data-stu-id="56302-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56302-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56302-118">Minimum supported client</span></span><br/> | <span data-ttu-id="56302-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56302-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56302-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56302-120">Minimum supported server</span></span><br/> | <span data-ttu-id="56302-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56302-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56302-122">標頭</span><span class="sxs-lookup"><span data-stu-id="56302-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="56302-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="56302-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56302-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56302-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="56302-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="56302-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="56302-126">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="56302-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="56302-127">**Rich Edit 控制項事件遮罩旗標**</span><span class="sxs-lookup"><span data-stu-id="56302-127">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





