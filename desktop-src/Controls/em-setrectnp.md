---
title: 'EM_SETRECTNP 訊息 (Winuser .h) '
description: 設定多行編輯控制項的格式化矩形。
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934909"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="39a64-104">EM \_ SETRECTNP 訊息</span><span class="sxs-lookup"><span data-stu-id="39a64-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="39a64-105">設定多行編輯控制項的 [格式化矩形](about-edit-controls.md) 。</span><span class="sxs-lookup"><span data-stu-id="39a64-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="39a64-106">**Em \_ SETRECTNP** 訊息與 [**em \_ SETRECT**](em-setrect.md)訊息相同，不同之處在于 **em \_ SETRECTNP** 不會 *重繪* 編輯控制項視窗。</span><span class="sxs-lookup"><span data-stu-id="39a64-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="39a64-107">格式化矩形是控制項用來繪製文字的限制矩形。</span><span class="sxs-lookup"><span data-stu-id="39a64-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="39a64-108">限制矩形與編輯控制項視窗的大小無關。</span><span class="sxs-lookup"><span data-stu-id="39a64-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="39a64-109">此訊息只會由多行編輯控制項處理。</span><span class="sxs-lookup"><span data-stu-id="39a64-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="39a64-110">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="39a64-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="39a64-111">參數</span><span class="sxs-lookup"><span data-stu-id="39a64-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a64-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39a64-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a64-113">**Rich Edit 3.0 和更新版本：** 指出新的矩形是否包含絕對或相對座標。</span><span class="sxs-lookup"><span data-stu-id="39a64-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="39a64-114">值為零表示絕對座標。</span><span class="sxs-lookup"><span data-stu-id="39a64-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="39a64-115">值為1時，表示相對於目前格式化矩形的位移。</span><span class="sxs-lookup"><span data-stu-id="39a64-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="39a64-116"> (位移可以是正數或負數。 ) </span><span class="sxs-lookup"><span data-stu-id="39a64-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="39a64-117">**編輯控制項：** 未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="39a64-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="39a64-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39a64-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a64-119">[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，指定矩形的新維度。</span><span class="sxs-lookup"><span data-stu-id="39a64-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="39a64-120">如果這個參數為 **Null**，則會將格式化矩形設定為其預設值。</span><span class="sxs-lookup"><span data-stu-id="39a64-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a64-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="39a64-121">Return value</span></span>

<span data-ttu-id="39a64-122">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="39a64-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39a64-123">備註</span><span class="sxs-lookup"><span data-stu-id="39a64-123">Remarks</span></span>

<span data-ttu-id="39a64-124">**Rich Edit：** Microsoft Rich Edit 3.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="39a64-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="39a64-125">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="39a64-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39a64-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="39a64-126">Requirements</span></span>



| <span data-ttu-id="39a64-127">需求</span><span class="sxs-lookup"><span data-stu-id="39a64-127">Requirement</span></span> | <span data-ttu-id="39a64-128">值</span><span class="sxs-lookup"><span data-stu-id="39a64-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a64-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39a64-129">Minimum supported client</span></span><br/> | <span data-ttu-id="39a64-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39a64-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="39a64-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39a64-131">Minimum supported server</span></span><br/> | <span data-ttu-id="39a64-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39a64-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39a64-133">標頭</span><span class="sxs-lookup"><span data-stu-id="39a64-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a64-134"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="39a64-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a64-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39a64-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="39a64-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="39a64-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39a64-137">**EM \_ SETRECT**</span><span class="sxs-lookup"><span data-stu-id="39a64-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="39a64-138">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="39a64-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="39a64-139">[**矩形**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39a64-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

