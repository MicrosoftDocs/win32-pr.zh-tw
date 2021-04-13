---
title: 'EM_SETEVENTMASK 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的事件遮罩。 事件遮罩會指定控制項傳送至其父視窗的通知碼。
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466541"
---
# <a name="em_seteventmask-message"></a><span data-ttu-id="29572-105">EM \_ SETEVENTMASK 訊息</span><span class="sxs-lookup"><span data-stu-id="29572-105">EM\_SETEVENTMASK message</span></span>

<span data-ttu-id="29572-106">設定 rich edit 控制項的事件遮罩。</span><span class="sxs-lookup"><span data-stu-id="29572-106">Sets the event mask for a rich edit control.</span></span> <span data-ttu-id="29572-107">事件遮罩會指定控制項傳送至其父視窗的通知碼。</span><span class="sxs-lookup"><span data-stu-id="29572-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="29572-108">參數</span><span class="sxs-lookup"><span data-stu-id="29572-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29572-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29572-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29572-110">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="29572-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="29572-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29572-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29572-112">Rich edit 控制項的新事件遮罩。</span><span class="sxs-lookup"><span data-stu-id="29572-112">New event mask for the rich edit control.</span></span> <span data-ttu-id="29572-113">如需事件遮罩的清單，請參閱 [**Rich Edit 控制項事件遮罩旗標**](rich-edit-control-event-mask-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="29572-113">For a list of event masks, see [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29572-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="29572-114">Return value</span></span>

<span data-ttu-id="29572-115">此訊息會傳回先前的事件遮罩。</span><span class="sxs-lookup"><span data-stu-id="29572-115">This message returns the previous event mask.</span></span>

## <a name="remarks"></a><span data-ttu-id="29572-116">備註</span><span class="sxs-lookup"><span data-stu-id="29572-116">Remarks</span></span>

<span data-ttu-id="29572-117">預設事件遮罩 (在設定 [任何] 之前) ENM [ \_ 無]。</span><span class="sxs-lookup"><span data-stu-id="29572-117">The default event mask (before any is set) is ENM\_NONE.</span></span>

## <a name="requirements"></a><span data-ttu-id="29572-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="29572-118">Requirements</span></span>



| <span data-ttu-id="29572-119">需求</span><span class="sxs-lookup"><span data-stu-id="29572-119">Requirement</span></span> | <span data-ttu-id="29572-120">值</span><span class="sxs-lookup"><span data-stu-id="29572-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29572-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29572-121">Minimum supported client</span></span><br/> | <span data-ttu-id="29572-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29572-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29572-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29572-123">Minimum supported server</span></span><br/> | <span data-ttu-id="29572-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29572-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29572-125">標頭</span><span class="sxs-lookup"><span data-stu-id="29572-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="29572-126"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="29572-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29572-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29572-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="29572-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="29572-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29572-129">**EM \_ GETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="29572-129">**EM\_GETEVENTMASK**</span></span>](em-geteventmask.md)
</dt> <dt>

[<span data-ttu-id="29572-130">**Rich Edit 控制項事件遮罩旗標**</span><span class="sxs-lookup"><span data-stu-id="29572-130">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





