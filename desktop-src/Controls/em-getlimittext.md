---
title: 'EM_GETLIMITTEXT 訊息 (Winuser .h) '
description: 取得編輯控制項的目前文字限制。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843160"
---
# <a name="em_getlimittext-message"></a><span data-ttu-id="bb77b-105">EM \_ GETLIMITTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="bb77b-105">EM\_GETLIMITTEXT message</span></span>

<span data-ttu-id="bb77b-106">取得編輯控制項的目前文字限制。</span><span class="sxs-lookup"><span data-stu-id="bb77b-106">Gets the current text limit for an edit control.</span></span> <span data-ttu-id="bb77b-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="bb77b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb77b-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb77b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb77b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb77b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb77b-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="bb77b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bb77b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb77b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb77b-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="bb77b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb77b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb77b-113">Return value</span></span>

<span data-ttu-id="bb77b-114">傳回值是文字限制。</span><span class="sxs-lookup"><span data-stu-id="bb77b-114">The return value is the text limit.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb77b-115">備註</span><span class="sxs-lookup"><span data-stu-id="bb77b-115">Remarks</span></span>

<span data-ttu-id="bb77b-116">**編輯控制項、Rich Edit 2.0 和更新版本：** 文字限制是控制項可以包含的最大文字數量（以 **TCHAR** s 為限）。</span><span class="sxs-lookup"><span data-stu-id="bb77b-116">**Edit controls, Rich Edit 2.0 and later:** The text limit is the maximum amount of text, in **TCHAR** s, that the control can contain.</span></span> <span data-ttu-id="bb77b-117">若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。</span><span class="sxs-lookup"><span data-stu-id="bb77b-117">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="bb77b-118">兩份具有相同字元限制的檔將會產生相同的文字限制，即使其中一個是 ANSI，另一個則是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="bb77b-118">Two documents with the same character limit will yield the same text limit, even if one is ANSI and the other is Unicode.</span></span>

<span data-ttu-id="bb77b-119">**Rich Edit 1.0：** 文字限制是 rich edit 控制項可以包含的最大文字數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bb77b-119">**Rich Edit 1.0:** The text limit is the maximum amount of text, in bytes, that the rich edit control can contain.</span></span>

<span data-ttu-id="bb77b-120">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="bb77b-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="bb77b-121">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="bb77b-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb77b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb77b-122">Requirements</span></span>



| <span data-ttu-id="bb77b-123">需求</span><span class="sxs-lookup"><span data-stu-id="bb77b-123">Requirement</span></span> | <span data-ttu-id="bb77b-124">值</span><span class="sxs-lookup"><span data-stu-id="bb77b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb77b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb77b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bb77b-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb77b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb77b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb77b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bb77b-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb77b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb77b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="bb77b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb77b-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bb77b-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb77b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb77b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb77b-132">**EM \_ SETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="bb77b-132">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
</dt> </dl>

 

 





