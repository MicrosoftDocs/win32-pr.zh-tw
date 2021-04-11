---
title: 'EM_LINEINDEX 訊息 (Winuser .h) '
description: 取得多行編輯控制項中指定行第一個字元的字元索引。
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_LINEINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934209"
---
# <a name="em_lineindex-message-winuserh"></a><span data-ttu-id="94731-104">EM_LINEINDEX 訊息 (Winuser .h) </span><span class="sxs-lookup"><span data-stu-id="94731-104">EM_LINEINDEX message (Winuser.h)</span></span>

<span data-ttu-id="94731-105">取得多行編輯控制項中指定行第一個字元的字元索引。</span><span class="sxs-lookup"><span data-stu-id="94731-105">Gets the character index of the first character of a specified line in a multiline edit control.</span></span> <span data-ttu-id="94731-106">字元索引是編輯控制項開頭的字元之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="94731-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="94731-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="94731-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="94731-108">參數</span><span class="sxs-lookup"><span data-stu-id="94731-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94731-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94731-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94731-110">以零為基底的行號。</span><span class="sxs-lookup"><span data-stu-id="94731-110">The zero-based line number.</span></span> <span data-ttu-id="94731-111">值-1 會指定包含插入號)  (行的目前行號。</span><span class="sxs-lookup"><span data-stu-id="94731-111">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="94731-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94731-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94731-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="94731-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94731-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="94731-114">Return value</span></span>

<span data-ttu-id="94731-115">傳回值是 *wParam* 參數中指定之行的字元索引，如果指定的行號大於編輯控制項中的行數，則為-1。</span><span class="sxs-lookup"><span data-stu-id="94731-115">The return value is the character index of the line specified in the *wParam* parameter, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="94731-116">備註</span><span class="sxs-lookup"><span data-stu-id="94731-116">Remarks</span></span>

<span data-ttu-id="94731-117">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="94731-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="94731-118">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="94731-118">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94731-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="94731-119">Requirements</span></span>



| <span data-ttu-id="94731-120">需求</span><span class="sxs-lookup"><span data-stu-id="94731-120">Requirement</span></span> | <span data-ttu-id="94731-121">值</span><span class="sxs-lookup"><span data-stu-id="94731-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94731-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94731-122">Minimum supported client</span></span><br/> | <span data-ttu-id="94731-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94731-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="94731-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94731-124">Minimum supported server</span></span><br/> | <span data-ttu-id="94731-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94731-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94731-126">標頭</span><span class="sxs-lookup"><span data-stu-id="94731-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="94731-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="94731-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94731-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94731-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94731-129">**EM \_ LINEFROMCHAR**</span><span class="sxs-lookup"><span data-stu-id="94731-129">**EM\_LINEFROMCHAR**</span></span>](em-linefromchar.md)
</dt> </dl>

 

 





