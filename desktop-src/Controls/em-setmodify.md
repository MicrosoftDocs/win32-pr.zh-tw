---
title: 'EM_SETMODIFY 訊息 (Winuser .h) '
description: 設定或清除編輯控制項的修改旗標。 修改旗標會指出是否已修改編輯控制項內的文字。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843808"
---
# <a name="em_setmodify-message"></a><span data-ttu-id="38c5b-106">EM \_ SETMODIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="38c5b-106">EM\_SETMODIFY message</span></span>

<span data-ttu-id="38c5b-107">設定或清除編輯控制項的修改旗標。</span><span class="sxs-lookup"><span data-stu-id="38c5b-107">Sets or clears the modification flag for an edit control.</span></span> <span data-ttu-id="38c5b-108">修改旗標會指出是否已修改編輯控制項內的文字。</span><span class="sxs-lookup"><span data-stu-id="38c5b-108">The modification flag indicates whether the text within the edit control has been modified.</span></span> <span data-ttu-id="38c5b-109">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="38c5b-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="38c5b-110">參數</span><span class="sxs-lookup"><span data-stu-id="38c5b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c5b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38c5b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38c5b-112">修改旗標的新值。</span><span class="sxs-lookup"><span data-stu-id="38c5b-112">The new value for the modification flag.</span></span> <span data-ttu-id="38c5b-113">值為 **TRUE** 表示文字已經過修改，而值為 **FALSE** 表示未修改。</span><span class="sxs-lookup"><span data-stu-id="38c5b-113">A value of **TRUE** indicates the text has been modified, and a value of **FALSE** indicates it has not been modified.</span></span>

</dd> <dt>

<span data-ttu-id="38c5b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38c5b-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38c5b-115">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="38c5b-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c5b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="38c5b-116">Return value</span></span>

<span data-ttu-id="38c5b-117">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="38c5b-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c5b-118">備註</span><span class="sxs-lookup"><span data-stu-id="38c5b-118">Remarks</span></span>

<span data-ttu-id="38c5b-119">建立控制項時，系統會自動將修改旗標清除為零。</span><span class="sxs-lookup"><span data-stu-id="38c5b-119">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="38c5b-120">如果使用者變更控制項的文字，系統會將旗標設定為非零。</span><span class="sxs-lookup"><span data-stu-id="38c5b-120">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="38c5b-121">您可以將 [**EM \_ GETMODIFY**](em-getmodify.md) 訊息傳送至編輯控制項，以取得旗標的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="38c5b-121">You can send the [**EM\_GETMODIFY**](em-getmodify.md) message to the edit control to retrieve the current state of the flag.</span></span>

<span data-ttu-id="38c5b-122">**Rich Edit 1.0：** 當修改旗標設為 **FALSE** 時，不含 **REO \_ DYNAMICSIZE** 旗標的建立物件將會鎖定其範圍。</span><span class="sxs-lookup"><span data-stu-id="38c5b-122">**Rich Edit 1.0:** Objects created without the **REO\_DYNAMICSIZE** flag will lock in their extents when the modify flag is set to **FALSE**.</span></span>

<span data-ttu-id="38c5b-123">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="38c5b-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="38c5b-124">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="38c5b-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38c5b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="38c5b-125">Requirements</span></span>



| <span data-ttu-id="38c5b-126">需求</span><span class="sxs-lookup"><span data-stu-id="38c5b-126">Requirement</span></span> | <span data-ttu-id="38c5b-127">值</span><span class="sxs-lookup"><span data-stu-id="38c5b-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38c5b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38c5b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="38c5b-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38c5b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="38c5b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38c5b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="38c5b-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38c5b-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38c5b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="38c5b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="38c5b-133"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="38c5b-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38c5b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38c5b-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="38c5b-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="38c5b-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38c5b-136">**EM \_ GETMODIFY**</span><span class="sxs-lookup"><span data-stu-id="38c5b-136">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> <dt>

[<span data-ttu-id="38c5b-137">**REOBJECT**</span><span class="sxs-lookup"><span data-stu-id="38c5b-137">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





