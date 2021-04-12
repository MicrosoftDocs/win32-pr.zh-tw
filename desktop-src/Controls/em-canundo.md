---
title: 'EM_CANUNDO 訊息 (Winuser .h) '
description: 判斷是否在編輯控制項的復原佇列中有任何動作。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO message Windows 控制項
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104502"
---
# <a name="em_canundo-message"></a><span data-ttu-id="1a07f-105">EM \_ CANUNDO 訊息</span><span class="sxs-lookup"><span data-stu-id="1a07f-105">EM\_CANUNDO message</span></span>

<span data-ttu-id="1a07f-106">判斷是否在編輯控制項的復原佇列中有任何動作。</span><span class="sxs-lookup"><span data-stu-id="1a07f-106">Determines whether there are any actions in an edit control's undo queue.</span></span> <span data-ttu-id="1a07f-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="1a07f-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a07f-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a07f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a07f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a07f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a07f-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1a07f-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a07f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a07f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a07f-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1a07f-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a07f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a07f-113">Return value</span></span>

<span data-ttu-id="1a07f-114">如果控制項的復原佇列中有動作，傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="1a07f-114">If there are actions in the control's undo queue, the return value is nonzero.</span></span>

<span data-ttu-id="1a07f-115">如果恢復佇列是空的，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="1a07f-115">If the undo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a07f-116">備註</span><span class="sxs-lookup"><span data-stu-id="1a07f-116">Remarks</span></span>

<span data-ttu-id="1a07f-117">如果復原佇列不是空的，您可以將 [**EM \_ 復原**](em-undo.md) 訊息傳送至控制項，以復原最近的作業。</span><span class="sxs-lookup"><span data-stu-id="1a07f-117">If the undo queue is not empty, you can send the [**EM\_UNDO**](em-undo.md) message to the control to undo the most recent operation.</span></span>

<span data-ttu-id="1a07f-118">**編輯控制項和 Rich edit 1.0：** 復原佇列只會包含最新的作業。</span><span class="sxs-lookup"><span data-stu-id="1a07f-118">**Edit controls and Rich Edit 1.0:** The undo queue contains only the most recent operation.</span></span>

<span data-ttu-id="1a07f-119">**Rich Edit 2.0 和更新版本：** 復原佇列可以包含多個作業。</span><span class="sxs-lookup"><span data-stu-id="1a07f-119">**Rich Edit 2.0 and later:** The undo queue can contain multiple operations.</span></span>

<span data-ttu-id="1a07f-120">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="1a07f-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1a07f-121">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="1a07f-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a07f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a07f-122">Requirements</span></span>



| <span data-ttu-id="1a07f-123">需求</span><span class="sxs-lookup"><span data-stu-id="1a07f-123">Requirement</span></span> | <span data-ttu-id="1a07f-124">值</span><span class="sxs-lookup"><span data-stu-id="1a07f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a07f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a07f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1a07f-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a07f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a07f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a07f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1a07f-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a07f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a07f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1a07f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a07f-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1a07f-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a07f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a07f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a07f-132">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="1a07f-132">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





