---
title: 'EM_GETLINECOUNT 訊息 (Winuser .h) '
description: 取得多行編輯控制項中的行數。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464544"
---
# <a name="em_getlinecount-message-winuserh"></a><span data-ttu-id="8eed1-105">EM_GETLINECOUNT 訊息 (Winuser .h) </span><span class="sxs-lookup"><span data-stu-id="8eed1-105">EM_GETLINECOUNT message (Winuser.h)</span></span>

<span data-ttu-id="8eed1-106">取得多行編輯控制項中的行數。</span><span class="sxs-lookup"><span data-stu-id="8eed1-106">Gets the number of lines in a multiline edit control.</span></span> <span data-ttu-id="8eed1-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="8eed1-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8eed1-108">參數</span><span class="sxs-lookup"><span data-stu-id="8eed1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eed1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8eed1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8eed1-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="8eed1-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8eed1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8eed1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8eed1-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="8eed1-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eed1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8eed1-113">Return value</span></span>

<span data-ttu-id="8eed1-114">傳回值是指定多行編輯控制項或 rich edit 控制項中的文字行總數的整數。</span><span class="sxs-lookup"><span data-stu-id="8eed1-114">The return value is an integer specifying the total number of text lines in the multiline edit control or rich edit control.</span></span> <span data-ttu-id="8eed1-115">如果控制項沒有任何文字，則傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="8eed1-115">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="8eed1-116">傳回值永遠不會小於1。</span><span class="sxs-lookup"><span data-stu-id="8eed1-116">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eed1-117">備註</span><span class="sxs-lookup"><span data-stu-id="8eed1-117">Remarks</span></span>

<span data-ttu-id="8eed1-118">**EM \_ GETLINECOUNT** 訊息會抓取文字行總數，而不只是目前可見的行數。</span><span class="sxs-lookup"><span data-stu-id="8eed1-118">The **EM\_GETLINECOUNT** message retrieves the total number of text lines, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="8eed1-119">如果已啟用 Wordwrap 功能，則在編輯視窗的維度變更時，可以變更行數。</span><span class="sxs-lookup"><span data-stu-id="8eed1-119">If the Wordwrap feature is enabled, the number of lines can change when the dimensions of the editing window change.</span></span>

<span data-ttu-id="8eed1-120">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="8eed1-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8eed1-121">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="8eed1-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eed1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8eed1-122">Requirements</span></span>



| <span data-ttu-id="8eed1-123">需求</span><span class="sxs-lookup"><span data-stu-id="8eed1-123">Requirement</span></span> | <span data-ttu-id="8eed1-124">值</span><span class="sxs-lookup"><span data-stu-id="8eed1-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eed1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8eed1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8eed1-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8eed1-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8eed1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8eed1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8eed1-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8eed1-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8eed1-129">標頭</span><span class="sxs-lookup"><span data-stu-id="8eed1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eed1-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8eed1-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eed1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8eed1-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="8eed1-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="8eed1-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8eed1-133">**EM \_ GETLINE**</span><span class="sxs-lookup"><span data-stu-id="8eed1-133">**EM\_GETLINE**</span></span>](em-getline.md)
</dt> <dt>

[<span data-ttu-id="8eed1-134">**EM \_ LINELENGTH**</span><span class="sxs-lookup"><span data-stu-id="8eed1-134">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="8eed1-135">**編輯 \_ GetLineCount**</span><span class="sxs-lookup"><span data-stu-id="8eed1-135">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





