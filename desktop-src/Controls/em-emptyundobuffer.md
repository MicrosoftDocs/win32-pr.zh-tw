---
title: 'EM_EMPTYUNDOBUFFER 訊息 (Winuser .h) '
description: 重設編輯控制項的復原旗標。 每當編輯控制項內的作業可以復原時，就會設定 [復原] 旗標。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465900"
---
# <a name="em_emptyundobuffer-message"></a><span data-ttu-id="dc384-106">EM \_ EMPTYUNDOBUFFER 訊息</span><span class="sxs-lookup"><span data-stu-id="dc384-106">EM\_EMPTYUNDOBUFFER message</span></span>

<span data-ttu-id="dc384-107">重設編輯控制項的復原旗標。</span><span class="sxs-lookup"><span data-stu-id="dc384-107">Resets the undo flag of an edit control.</span></span> <span data-ttu-id="dc384-108">每當編輯控制項內的作業可以復原時，就會設定 [復原] 旗標。</span><span class="sxs-lookup"><span data-stu-id="dc384-108">The undo flag is set whenever an operation within the edit control can be undone.</span></span> <span data-ttu-id="dc384-109">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="dc384-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc384-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc384-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc384-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc384-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc384-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="dc384-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dc384-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc384-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc384-114">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="dc384-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc384-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc384-115">Return value</span></span>

<span data-ttu-id="dc384-116">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dc384-116">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc384-117">備註</span><span class="sxs-lookup"><span data-stu-id="dc384-117">Remarks</span></span>

<span data-ttu-id="dc384-118">每當編輯控制項收到 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 或 [**EM \_ SETHANDLE**](em-sethandle.md) 訊息時，就會自動重設復原旗標。</span><span class="sxs-lookup"><span data-stu-id="dc384-118">The undo flag is automatically reset whenever the edit control receives a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) or [**EM\_SETHANDLE**](em-sethandle.md) message.</span></span>

<span data-ttu-id="dc384-119">**編輯控制項和 Rich edit 1.0：** 控制項只能復原或重做最新的作業。</span><span class="sxs-lookup"><span data-stu-id="dc384-119">**Edit controls and Rich Edit 1.0:** The control can only undo or redo the most recent operation.</span></span>

<span data-ttu-id="dc384-120">**Rich Edit 2.0 和更新版本：\*\*\*\*EM \_ EMPTYUNDOBUFFER** 訊息會清空所有的復原和重做緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dc384-120">**Rich Edit 2.0 and later:** The **EM\_EMPTYUNDOBUFFER** message empties all undo and redo buffers.</span></span> <span data-ttu-id="dc384-121">Rich edit 控制項可讓使用者復原或重做多項作業。</span><span class="sxs-lookup"><span data-stu-id="dc384-121">Rich edit controls enable the user to undo or redo multiple operations.</span></span>

<span data-ttu-id="dc384-122">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="dc384-122">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="dc384-123">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="dc384-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc384-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc384-124">Requirements</span></span>



| <span data-ttu-id="dc384-125">需求</span><span class="sxs-lookup"><span data-stu-id="dc384-125">Requirement</span></span> | <span data-ttu-id="dc384-126">值</span><span class="sxs-lookup"><span data-stu-id="dc384-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc384-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc384-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dc384-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc384-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dc384-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc384-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dc384-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc384-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc384-131">標頭</span><span class="sxs-lookup"><span data-stu-id="dc384-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc384-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="dc384-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc384-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc384-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc384-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="dc384-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dc384-135">**EM \_ CANUNDO**</span><span class="sxs-lookup"><span data-stu-id="dc384-135">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="dc384-136">**EM \_ SETHANDLE**</span><span class="sxs-lookup"><span data-stu-id="dc384-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

[<span data-ttu-id="dc384-137">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="dc384-137">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

<span data-ttu-id="dc384-138">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="dc384-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dc384-139">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="dc384-139">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

