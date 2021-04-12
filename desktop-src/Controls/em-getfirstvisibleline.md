---
title: 'EM_GETFIRSTVISIBLELINE 訊息 (Winuser .h) '
description: 取得多行編輯控制項中最上層可見行的索引（以零為基底）。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508924"
---
# <a name="em_getfirstvisibleline-message"></a><span data-ttu-id="b11f1-105">EM \_ GETFIRSTVISIBLELINE 訊息</span><span class="sxs-lookup"><span data-stu-id="b11f1-105">EM\_GETFIRSTVISIBLELINE message</span></span>

<span data-ttu-id="b11f1-106">取得多行編輯控制項中最上層可見行的索引（以零為基底）。</span><span class="sxs-lookup"><span data-stu-id="b11f1-106">Gets the zero-based index of the uppermost visible line in a multiline edit control.</span></span> <span data-ttu-id="b11f1-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="b11f1-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b11f1-108">參數</span><span class="sxs-lookup"><span data-stu-id="b11f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b11f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b11f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b11f1-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b11f1-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b11f1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b11f1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b11f1-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b11f1-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b11f1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b11f1-113">Return value</span></span>

<span data-ttu-id="b11f1-114">傳回值是多行編輯控制項中最上層可見行的索引（以零為基底）。</span><span class="sxs-lookup"><span data-stu-id="b11f1-114">The return value is the zero-based index of the uppermost visible line in a multiline edit control.</span></span>

<span data-ttu-id="b11f1-115">**編輯控制項：** 針對單行編輯控制項，傳回值是第一個可見字元的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="b11f1-115">**Edit controls:** For single-line edit controls, the return value is the zero-based index of the first visible character.</span></span>

<span data-ttu-id="b11f1-116">**Rich edit 控制項：** 針對單行 rich edit 控制項，傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="b11f1-116">**Rich edit controls:** For single-line rich edit controls, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b11f1-117">備註</span><span class="sxs-lookup"><span data-stu-id="b11f1-117">Remarks</span></span>

<span data-ttu-id="b11f1-118">編輯控制項中的行數和線條長度，取決於控制項的寬度和目前的 Wordwrap 設定。</span><span class="sxs-lookup"><span data-stu-id="b11f1-118">The number of lines and the length of the lines in an edit control depend on the width of the control and the current Wordwrap setting.</span></span>

<span data-ttu-id="b11f1-119">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="b11f1-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b11f1-120">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="b11f1-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b11f1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b11f1-121">Requirements</span></span>



| <span data-ttu-id="b11f1-122">需求</span><span class="sxs-lookup"><span data-stu-id="b11f1-122">Requirement</span></span> | <span data-ttu-id="b11f1-123">值</span><span class="sxs-lookup"><span data-stu-id="b11f1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b11f1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b11f1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b11f1-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b11f1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b11f1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b11f1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b11f1-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b11f1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b11f1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b11f1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b11f1-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b11f1-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





