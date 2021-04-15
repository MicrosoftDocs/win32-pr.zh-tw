---
title: 'EM_GETFILELINE 訊息 (CommCtrl .h) '
description: 從編輯控制項複製一行文字，與螢幕上顯示線條的方式無關，然後將它放在指定的緩衝區中。
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466109"
---
# <a name="em_getfileline-message-commctrlh"></a><span data-ttu-id="5514f-104">EM_GETFILELINE 訊息 (CommCtrl .h) </span><span class="sxs-lookup"><span data-stu-id="5514f-104">EM_GETFILELINE message (CommCtrl.h)</span></span>

<span data-ttu-id="5514f-105">從編輯控制項複製一行文字，與螢幕上顯示線條的方式無關，然後將它放在指定的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="5514f-105">Copies a line of text from an edit control, independently of how lines are displayed on the screen, and places it in a specified buffer.</span></span>

## <a name="parameters"></a><span data-ttu-id="5514f-106">參數</span><span class="sxs-lookup"><span data-stu-id="5514f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5514f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5514f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5514f-108">以零為基底的索引，這是從多行編輯控制項取出的行。</span><span class="sxs-lookup"><span data-stu-id="5514f-108">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="5514f-109">值為零會指定最頂端的行。</span><span class="sxs-lookup"><span data-stu-id="5514f-109">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="5514f-110">單行編輯控制項會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="5514f-110">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="5514f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5514f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5514f-112">接收一行複本之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="5514f-112">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="5514f-113">傳送訊息之前，請先將這個緩衝區的第一個字組設為緩衝區的大小（以 **TCHAR** s）。</span><span class="sxs-lookup"><span data-stu-id="5514f-113">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="5514f-114">若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。</span><span class="sxs-lookup"><span data-stu-id="5514f-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="5514f-115">第一個單字中的大小會被覆制的行覆寫。</span><span class="sxs-lookup"><span data-stu-id="5514f-115">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5514f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5514f-116">Return value</span></span>

<span data-ttu-id="5514f-117">傳回值是複製的 **TCHAR** 數目。</span><span class="sxs-lookup"><span data-stu-id="5514f-117">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="5514f-118">如果 *wParam* 參數指定的行號大於編輯控制項中的行數，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="5514f-118">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="5514f-119">備註</span><span class="sxs-lookup"><span data-stu-id="5514f-119">Remarks</span></span>

<span data-ttu-id="5514f-120">複製的行不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="5514f-120">The copied line does not contain a terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="5514f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5514f-121">Requirements</span></span>



| <span data-ttu-id="5514f-122">需求</span><span class="sxs-lookup"><span data-stu-id="5514f-122">Requirement</span></span> | <span data-ttu-id="5514f-123">值</span><span class="sxs-lookup"><span data-stu-id="5514f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5514f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5514f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5514f-125">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5514f-125">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5514f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5514f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5514f-127">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5514f-127">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5514f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5514f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5514f-129"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5514f-129"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5514f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5514f-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5514f-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="5514f-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5514f-132">**EM \_ FILELINELENGTH**</span><span class="sxs-lookup"><span data-stu-id="5514f-132">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="5514f-133">**編輯 \_ GetFileLine**</span><span class="sxs-lookup"><span data-stu-id="5514f-133">**Edit\_GetFileLine**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

<span data-ttu-id="5514f-134">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="5514f-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5514f-135">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="5514f-135">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

