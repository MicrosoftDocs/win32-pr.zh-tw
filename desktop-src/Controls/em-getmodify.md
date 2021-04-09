---
title: 'EM_GETMODIFY 訊息 (Winuser .h) '
description: 取得編輯控制項之修改旗標的狀態。 旗標會指出編輯控制項的內容是否已修改。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843204"
---
# <a name="em_getmodify-message"></a><span data-ttu-id="5984f-106">EM \_ GETMODIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="5984f-106">EM\_GETMODIFY message</span></span>

<span data-ttu-id="5984f-107">取得編輯控制項之修改旗標的狀態。</span><span class="sxs-lookup"><span data-stu-id="5984f-107">Gets the state of an edit control's modification flag.</span></span> <span data-ttu-id="5984f-108">旗標會指出編輯控制項的內容是否已修改。</span><span class="sxs-lookup"><span data-stu-id="5984f-108">The flag indicates whether the contents of the edit control have been modified.</span></span> <span data-ttu-id="5984f-109">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="5984f-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5984f-110">參數</span><span class="sxs-lookup"><span data-stu-id="5984f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5984f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5984f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5984f-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="5984f-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5984f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5984f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5984f-114">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="5984f-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5984f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5984f-115">Return value</span></span>

<span data-ttu-id="5984f-116">如果編輯控制項的內容已修改，則傳回值為非零。否則，它是零。</span><span class="sxs-lookup"><span data-stu-id="5984f-116">If the contents of edit control have been modified, the return value is nonzero; otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5984f-117">備註</span><span class="sxs-lookup"><span data-stu-id="5984f-117">Remarks</span></span>

<span data-ttu-id="5984f-118">建立控制項時，系統會自動將修改旗標清除為零。</span><span class="sxs-lookup"><span data-stu-id="5984f-118">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="5984f-119">如果使用者變更控制項的文字，系統會將旗標設定為非零。</span><span class="sxs-lookup"><span data-stu-id="5984f-119">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="5984f-120">您可以將 [**EM \_ SETMODIFY**](em-setmodify.md) 訊息傳送至編輯控制項，以設定或清除旗標。</span><span class="sxs-lookup"><span data-stu-id="5984f-120">You can send the [**EM\_SETMODIFY**](em-setmodify.md) message to the edit control to set or clear the flag.</span></span>

<span data-ttu-id="5984f-121">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="5984f-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="5984f-122">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="5984f-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5984f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5984f-123">Requirements</span></span>



| <span data-ttu-id="5984f-124">需求</span><span class="sxs-lookup"><span data-stu-id="5984f-124">Requirement</span></span> | <span data-ttu-id="5984f-125">值</span><span class="sxs-lookup"><span data-stu-id="5984f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5984f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5984f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5984f-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5984f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5984f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5984f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5984f-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5984f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5984f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5984f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5984f-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5984f-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5984f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5984f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5984f-133">**EM \_ SETMODIFY**</span><span class="sxs-lookup"><span data-stu-id="5984f-133">**EM\_SETMODIFY**</span></span>](em-setmodify.md)
</dt> </dl>

 

 





