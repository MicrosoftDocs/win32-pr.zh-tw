---
title: 'EM_UNDO 訊息 (Winuser .h) '
description: 此訊息會復原控制項復原佇列中的最後一個編輯控制項作業。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO message Windows 控制項
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685927"
---
# <a name="em_undo-message"></a><span data-ttu-id="da13a-105">EM \_ 復原訊息</span><span class="sxs-lookup"><span data-stu-id="da13a-105">EM\_UNDO message</span></span>

<span data-ttu-id="da13a-106">此訊息會復原控制項復原佇列中的最後一個編輯控制項作業。</span><span class="sxs-lookup"><span data-stu-id="da13a-106">This message undoes the last edit control operation in the control's undo queue.</span></span> <span data-ttu-id="da13a-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="da13a-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="da13a-108">參數</span><span class="sxs-lookup"><span data-stu-id="da13a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da13a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da13a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da13a-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="da13a-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="da13a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da13a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da13a-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="da13a-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da13a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="da13a-113">Return value</span></span>

<span data-ttu-id="da13a-114">針對單行編輯控制項，傳回值一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="da13a-114">For a single-line edit control, the return value is always **TRUE**.</span></span>

<span data-ttu-id="da13a-115">若為多行編輯控制項，如果復原作業成功，傳回值為 **TRUE** ; 如果復原作業失敗，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="da13a-115">For a multiline edit control, the return value is **TRUE** if the undo operation is successful, or **FALSE** if the undo operation fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="da13a-116">備註</span><span class="sxs-lookup"><span data-stu-id="da13a-116">Remarks</span></span>

<span data-ttu-id="da13a-117">**編輯控制項和 Rich edit 1.0：** 復原操作也可以復原。</span><span class="sxs-lookup"><span data-stu-id="da13a-117">**Edit controls and Rich Edit 1.0:** An undo operation can also be undone.</span></span> <span data-ttu-id="da13a-118">例如，您可以使用第一次 **em \_ 復原** 訊息來還原已刪除的文字，並使用第二個 **em \_ 復原** 訊息再次移除文字，只要沒有任何中間的編輯作業。</span><span class="sxs-lookup"><span data-stu-id="da13a-118">For example, you can restore deleted text with the first **EM\_UNDO** message, and remove the text again with a second **EM\_UNDO** message as long as there is no intervening edit operation.</span></span>

<span data-ttu-id="da13a-119">**Rich Edit 2.0 和更新版本：** 復原功能是多層的，因此傳送兩個 **EM \_ 復原** 訊息將會復原復原佇列中的最後兩個作業。</span><span class="sxs-lookup"><span data-stu-id="da13a-119">**Rich Edit 2.0 and later:** The undo feature is multilevel so sending two **EM\_UNDO** messages will undo the last two operations in the undo queue.</span></span> <span data-ttu-id="da13a-120">若要重做作業，請傳送 [**EM \_ 重做**](em-redo.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="da13a-120">To redo an operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

<span data-ttu-id="da13a-121">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="da13a-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="da13a-122">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="da13a-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da13a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="da13a-123">Requirements</span></span>



| <span data-ttu-id="da13a-124">需求</span><span class="sxs-lookup"><span data-stu-id="da13a-124">Requirement</span></span> | <span data-ttu-id="da13a-125">值</span><span class="sxs-lookup"><span data-stu-id="da13a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da13a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da13a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="da13a-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da13a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da13a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da13a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="da13a-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da13a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da13a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="da13a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="da13a-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="da13a-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da13a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da13a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da13a-133">**EM \_ CANUNDO**</span><span class="sxs-lookup"><span data-stu-id="da13a-133">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> </dl>

 

 





