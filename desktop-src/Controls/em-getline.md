---
title: 'EM_GETLINE 訊息 (Winuser .h) '
description: 從編輯控制項複製一行文字，並將它放在指定的緩衝區中。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETLINE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933993"
---
# <a name="em_getline-message-winuserh"></a><span data-ttu-id="7437a-105">EM_GETLINE 訊息 (Winuser .h) </span><span class="sxs-lookup"><span data-stu-id="7437a-105">EM_GETLINE message (Winuser.h)</span></span>

<span data-ttu-id="7437a-106">從編輯控制項複製一行文字，並將它放在指定的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="7437a-106">Copies a line of text from an edit control and places it in a specified buffer.</span></span> <span data-ttu-id="7437a-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="7437a-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7437a-108">參數</span><span class="sxs-lookup"><span data-stu-id="7437a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7437a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7437a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7437a-110">以零為基底的索引，這是從多行編輯控制項取出的行。</span><span class="sxs-lookup"><span data-stu-id="7437a-110">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="7437a-111">值為零會指定最頂端的行。</span><span class="sxs-lookup"><span data-stu-id="7437a-111">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="7437a-112">單行編輯控制項會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="7437a-112">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="7437a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7437a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7437a-114">接收一行複本之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="7437a-114">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="7437a-115">傳送訊息之前，請先將這個緩衝區的第一個字組設為緩衝區的大小（以 **TCHAR** s）。</span><span class="sxs-lookup"><span data-stu-id="7437a-115">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="7437a-116">若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。</span><span class="sxs-lookup"><span data-stu-id="7437a-116">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="7437a-117">第一個單字中的大小會被覆制的行覆寫。</span><span class="sxs-lookup"><span data-stu-id="7437a-117">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7437a-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="7437a-118">Return value</span></span>

<span data-ttu-id="7437a-119">傳回值是複製的 **TCHAR** 數目。</span><span class="sxs-lookup"><span data-stu-id="7437a-119">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="7437a-120">如果 *wParam* 參數指定的行號大於編輯控制項中的行數，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="7437a-120">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="7437a-121">備註</span><span class="sxs-lookup"><span data-stu-id="7437a-121">Remarks</span></span>

<span data-ttu-id="7437a-122">**編輯控制項：** 複製的行不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="7437a-122">**Edit controls:** The copied line does not contain a terminating null character.</span></span>

<span data-ttu-id="7437a-123">**Rich edit 控制項：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="7437a-123">**Rich edit controls:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7437a-124">複製的行不包含結束的 null 字元，除非沒有複製任何文字。</span><span class="sxs-lookup"><span data-stu-id="7437a-124">The copied line does not contain a terminating null character, unless no text was copied.</span></span> <span data-ttu-id="7437a-125">如果未複製任何文字，訊息會在緩衝區的開頭放置一個 null 字元。</span><span class="sxs-lookup"><span data-stu-id="7437a-125">If no text was copied, the message places a null character at the beginning of the buffer.</span></span> <span data-ttu-id="7437a-126">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="7437a-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7437a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7437a-127">Requirements</span></span>



| <span data-ttu-id="7437a-128">需求</span><span class="sxs-lookup"><span data-stu-id="7437a-128">Requirement</span></span> | <span data-ttu-id="7437a-129">值</span><span class="sxs-lookup"><span data-stu-id="7437a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7437a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7437a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7437a-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7437a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7437a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7437a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7437a-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7437a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7437a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="7437a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7437a-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7437a-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7437a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7437a-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="7437a-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="7437a-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7437a-138">**EM \_ LINELENGTH**</span><span class="sxs-lookup"><span data-stu-id="7437a-138">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="7437a-139">**編輯 \_ GetLine**</span><span class="sxs-lookup"><span data-stu-id="7437a-139">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

<span data-ttu-id="7437a-140">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="7437a-140">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7437a-141">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="7437a-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

