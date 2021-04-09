---
title: 'EM_LINESCROLL 訊息 (Winuser .h) '
description: 滾動多行編輯控制項中的文字。
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025291"
---
# <a name="em_linescroll-message"></a><span data-ttu-id="823be-104">EM \_ LINESCROLL 訊息</span><span class="sxs-lookup"><span data-stu-id="823be-104">EM\_LINESCROLL message</span></span>

<span data-ttu-id="823be-105">滾動多行編輯控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="823be-105">Scrolls the text in a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="823be-106">參數</span><span class="sxs-lookup"><span data-stu-id="823be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="823be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="823be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="823be-108">**編輯控制項：** 要水準滾動的字元數。</span><span class="sxs-lookup"><span data-stu-id="823be-108">**Edit controls:** The number of characters to scroll horizontally.</span></span>

<span data-ttu-id="823be-109">**Rich edit 控制項：** 未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="823be-109">**Rich edit controls:** This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="823be-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="823be-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="823be-111">垂直捲動的行數。</span><span class="sxs-lookup"><span data-stu-id="823be-111">The number of lines to scroll vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="823be-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="823be-112">Return value</span></span>

<span data-ttu-id="823be-113">如果訊息傳送至多行編輯控制項，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="823be-113">If the message is sent to a multiline edit control, the return value is **TRUE**.</span></span>

<span data-ttu-id="823be-114">如果訊息傳送至單行編輯控制項，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="823be-114">If the message is sent to a single-line edit control, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="823be-115">備註</span><span class="sxs-lookup"><span data-stu-id="823be-115">Remarks</span></span>

<span data-ttu-id="823be-116">控制項不會在編輯控制項中的最後一行文字之前垂直捲動。</span><span class="sxs-lookup"><span data-stu-id="823be-116">The control does not scroll vertically past the last line of text in the edit control.</span></span> <span data-ttu-id="823be-117">如果目前的行加上 *lParam* 參數所指定的行數超過編輯控制項中的行總數，則會調整此值，以便將編輯控制項的最後一行滾動至編輯控制項視窗的頂端。</span><span class="sxs-lookup"><span data-stu-id="823be-117">If the current line plus the number of lines specified by the *lParam* parameter exceeds the total number of lines in the edit control, the value is adjusted so that the last line of the edit control is scrolled to the top of the edit-control window.</span></span>

<span data-ttu-id="823be-118">**編輯控制項：\*\*\*\*EM \_ LINESCROLL** 訊息會在多行編輯控制項中，以垂直或水準方式滾動文字。</span><span class="sxs-lookup"><span data-stu-id="823be-118">**Edit controls:** The **EM\_LINESCROLL** message scrolls the text vertically or horizontally in a multiline edit control.</span></span> <span data-ttu-id="823be-119">**EM \_ LINESCROLL** 訊息可以用來將任何一行的最後一個字元水準滾動。</span><span class="sxs-lookup"><span data-stu-id="823be-119">The **EM\_LINESCROLL** message can be used to scroll horizontally past the last character of any line.</span></span>

<span data-ttu-id="823be-120">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="823be-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="823be-121">**EM \_ LINESCROLL** 訊息會在多行編輯控制項中垂直捲動文字。</span><span class="sxs-lookup"><span data-stu-id="823be-121">The **EM\_LINESCROLL** message scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="823be-122">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="823be-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="823be-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="823be-123">Requirements</span></span>



| <span data-ttu-id="823be-124">需求</span><span class="sxs-lookup"><span data-stu-id="823be-124">Requirement</span></span> | <span data-ttu-id="823be-125">值</span><span class="sxs-lookup"><span data-stu-id="823be-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823be-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="823be-126">Minimum supported client</span></span><br/> | <span data-ttu-id="823be-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="823be-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="823be-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="823be-128">Minimum supported server</span></span><br/> | <span data-ttu-id="823be-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="823be-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="823be-130">標頭</span><span class="sxs-lookup"><span data-stu-id="823be-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="823be-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="823be-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





