---
title: 'EM_LINEFROMCHAR 訊息 (Winuser .h) '
description: 取得在多行編輯控制項中包含指定之字元索引的行索引。
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_LINEFROMCHAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094323"
---
# <a name="em_linefromchar-message"></a><span data-ttu-id="e7f85-104">EM \_ LINEFROMCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="e7f85-104">EM\_LINEFROMCHAR message</span></span>

<span data-ttu-id="e7f85-105">取得在多行編輯控制項中包含指定之字元索引的行索引。</span><span class="sxs-lookup"><span data-stu-id="e7f85-105">Gets the index of the line that contains the specified character index in a multiline edit control.</span></span> <span data-ttu-id="e7f85-106">字元索引是編輯控制項開頭的字元之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="e7f85-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="e7f85-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="e7f85-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7f85-108">參數</span><span class="sxs-lookup"><span data-stu-id="e7f85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7f85-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7f85-110">要取出其數位的行中所含字元的字元索引。</span><span class="sxs-lookup"><span data-stu-id="e7f85-110">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="e7f85-111">如果此參數為-1， **EM \_ LINEFROMCHAR** 會抓取目前行的行號， (包含插入號) 的行號，或者，如果有選取範圍，則為包含選取範圍開頭之行的行號。</span><span class="sxs-lookup"><span data-stu-id="e7f85-111">If this parameter is -1, **EM\_LINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="e7f85-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7f85-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7f85-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="e7f85-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f85-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7f85-114">Return value</span></span>

<span data-ttu-id="e7f85-115">傳回值是行的以零為起始的行號，包含 *wParam* 所指定的字元索引。</span><span class="sxs-lookup"><span data-stu-id="e7f85-115">The return value is the zero-based line number of the line containing the character index specified by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f85-116">備註</span><span class="sxs-lookup"><span data-stu-id="e7f85-116">Remarks</span></span>

<span data-ttu-id="e7f85-117">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="e7f85-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e7f85-118">如果字元索引大於64000，請使用 [**EM \_ EXLINEFROMCHAR**](em-exlinefromchar.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="e7f85-118">If the character index is greater than 64,000, use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span> <span data-ttu-id="e7f85-119">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="e7f85-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f85-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7f85-120">Requirements</span></span>



| <span data-ttu-id="e7f85-121">需求</span><span class="sxs-lookup"><span data-stu-id="e7f85-121">Requirement</span></span> | <span data-ttu-id="e7f85-122">值</span><span class="sxs-lookup"><span data-stu-id="e7f85-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f85-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7f85-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7f85-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7f85-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7f85-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7f85-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7f85-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7f85-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7f85-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e7f85-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7f85-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e7f85-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f85-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7f85-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7f85-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="e7f85-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e7f85-131">**EM \_ EXLINEFROMCHAR**</span><span class="sxs-lookup"><span data-stu-id="e7f85-131">**EM\_EXLINEFROMCHAR**</span></span>](em-exlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="e7f85-132">**EM \_ LINEINDEX**</span><span class="sxs-lookup"><span data-stu-id="e7f85-132">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





