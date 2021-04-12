---
title: 'EM_REPLACESEL 訊息 (Winuser .h) '
description: 以指定的文字取代編輯控制項中選取的文字或 rich edit 控制項。
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106271"
---
# <a name="em_replacesel-message"></a><span data-ttu-id="7083f-104">EM \_ REPLACESEL 訊息</span><span class="sxs-lookup"><span data-stu-id="7083f-104">EM\_REPLACESEL message</span></span>

<span data-ttu-id="7083f-105">以指定的文字取代編輯控制項中選取的文字或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="7083f-105">Replaces the selected text in an edit control or a rich edit control with the specified text.</span></span>

## <a name="parameters"></a><span data-ttu-id="7083f-106">參數</span><span class="sxs-lookup"><span data-stu-id="7083f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7083f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7083f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7083f-108">指定取代作業是否可以復原。</span><span class="sxs-lookup"><span data-stu-id="7083f-108">Specifies whether the replacement operation can be undone.</span></span> <span data-ttu-id="7083f-109">若為 **TRUE**，則作業可以復原。</span><span class="sxs-lookup"><span data-stu-id="7083f-109">If this is **TRUE**, the operation can be undone.</span></span> <span data-ttu-id="7083f-110">如果為 **FALSE** ，則作業無法復原。</span><span class="sxs-lookup"><span data-stu-id="7083f-110">If this is **FALSE** , the operation cannot be undone.</span></span>

</dd> <dt>

<span data-ttu-id="7083f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7083f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7083f-112">以 null 結束的字串指標，其中包含取代文字。</span><span class="sxs-lookup"><span data-stu-id="7083f-112">A pointer to a null-terminated string containing the replacement text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7083f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7083f-113">Return value</span></span>

<span data-ttu-id="7083f-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7083f-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7083f-115">備註</span><span class="sxs-lookup"><span data-stu-id="7083f-115">Remarks</span></span>

<span data-ttu-id="7083f-116">使用 **EM \_ REPLACESEL** 訊息來取代編輯控制項中的部分文字。</span><span class="sxs-lookup"><span data-stu-id="7083f-116">Use the **EM\_REPLACESEL** message to replace only a portion of the text in an edit control.</span></span> <span data-ttu-id="7083f-117">若要取代所有文字，請使用 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息。</span><span class="sxs-lookup"><span data-stu-id="7083f-117">To replace all of the text, use the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span>

<span data-ttu-id="7083f-118">如果沒有選取專案，則會在插入號插入取代文字。</span><span class="sxs-lookup"><span data-stu-id="7083f-118">If there is no selection, the replacement text is inserted at the caret.</span></span>

<span data-ttu-id="7083f-119">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="7083f-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7083f-120">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="7083f-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="7083f-121">在 rich edit 控制項中，取代文字會採用插入號的字元格式，或是選取範圍中第一個字元的選項。</span><span class="sxs-lookup"><span data-stu-id="7083f-121">In a rich edit control, the replacement text takes the formatting of the character at the caret or, if there is a selection, of the first character in the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7083f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7083f-122">Requirements</span></span>



| <span data-ttu-id="7083f-123">需求</span><span class="sxs-lookup"><span data-stu-id="7083f-123">Requirement</span></span> | <span data-ttu-id="7083f-124">值</span><span class="sxs-lookup"><span data-stu-id="7083f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7083f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7083f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7083f-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7083f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7083f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7083f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7083f-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7083f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7083f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="7083f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7083f-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7083f-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7083f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7083f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7083f-132">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="7083f-132">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

