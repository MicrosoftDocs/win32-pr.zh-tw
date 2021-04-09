---
title: 'EM_GETRECT 訊息 (Winuser .h) '
description: 取得編輯控制項的格式化矩形。
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843707"
---
# <a name="em_getrect-message"></a><span data-ttu-id="337a1-104">EM \_ GETRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="337a1-104">EM\_GETRECT message</span></span>

<span data-ttu-id="337a1-105">取得編輯控制項的 [格式化矩形](about-edit-controls.md) 。</span><span class="sxs-lookup"><span data-stu-id="337a1-105">Gets the [formatting rectangle](about-edit-controls.md) of an edit control.</span></span> <span data-ttu-id="337a1-106">格式化矩形是控制項用來繪製文字的限制矩形。</span><span class="sxs-lookup"><span data-stu-id="337a1-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="337a1-107">限制矩形與編輯控制項視窗的大小無關。</span><span class="sxs-lookup"><span data-stu-id="337a1-107">The limiting rectangle is independent of the size of the edit-control window.</span></span> <span data-ttu-id="337a1-108">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="337a1-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="337a1-109">參數</span><span class="sxs-lookup"><span data-stu-id="337a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="337a1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="337a1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="337a1-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="337a1-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="337a1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="337a1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="337a1-113">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收格式化矩形。</span><span class="sxs-lookup"><span data-stu-id="337a1-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the formatting rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="337a1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="337a1-114">Return value</span></span>

<span data-ttu-id="337a1-115">傳回值沒有意義。</span><span class="sxs-lookup"><span data-stu-id="337a1-115">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="337a1-116">備註</span><span class="sxs-lookup"><span data-stu-id="337a1-116">Remarks</span></span>

<span data-ttu-id="337a1-117">您可以使用 [**em \_ SETRECT**](em-setrect.md) 和 [**em \_ SETRECTNP**](em-setrectnp.md) 訊息來修改多行編輯控制項的格式化矩形。</span><span class="sxs-lookup"><span data-stu-id="337a1-117">You can modify the formatting rectangle of a multiline edit control by using the [**EM\_SETRECT**](em-setrect.md) and [**EM\_SETRECTNP**](em-setrectnp.md) messages.</span></span>

<span data-ttu-id="337a1-118">在某些情況下， **em \_ GETRECT** 可能不會傳回 [**em \_ SETRECT**](em-setrect.md) 或 [**em \_ SETRECTNP**](em-setrectnp.md) 所設定的確切值，但它可以是由幾個圖元來關閉。</span><span class="sxs-lookup"><span data-stu-id="337a1-118">Under certain conditions, **EM\_GETRECT** might not return the exact values that [**EM\_SETRECT**](em-setrect.md) or [**EM\_SETRECTNP**](em-setrectnp.md) set it will be approximately correct, but it can be off by a few pixels.</span></span>

<span data-ttu-id="337a1-119">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="337a1-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="337a1-120">格式化矩形不包含選取範圍列，也就是每個段落左方未標記的區域。</span><span class="sxs-lookup"><span data-stu-id="337a1-120">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="337a1-121">按一下時，選取列會選取該行。</span><span class="sxs-lookup"><span data-stu-id="337a1-121">When clicked, the selection bar selects the line.</span></span> <span data-ttu-id="337a1-122">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="337a1-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="337a1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="337a1-123">Requirements</span></span>



| <span data-ttu-id="337a1-124">需求</span><span class="sxs-lookup"><span data-stu-id="337a1-124">Requirement</span></span> | <span data-ttu-id="337a1-125">值</span><span class="sxs-lookup"><span data-stu-id="337a1-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="337a1-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="337a1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="337a1-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="337a1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="337a1-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="337a1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="337a1-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="337a1-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="337a1-130">標頭</span><span class="sxs-lookup"><span data-stu-id="337a1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="337a1-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="337a1-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="337a1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="337a1-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="337a1-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="337a1-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="337a1-134">**EM \_ SETRECT**</span><span class="sxs-lookup"><span data-stu-id="337a1-134">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

[<span data-ttu-id="337a1-135">**EM \_ SETRECTNP**</span><span class="sxs-lookup"><span data-stu-id="337a1-135">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="337a1-136">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="337a1-136">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="337a1-137">[**矩形**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="337a1-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

