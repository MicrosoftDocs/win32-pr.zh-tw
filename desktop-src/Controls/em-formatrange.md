---
title: 'EM_FORMATRANGE 訊息 (Richedit .h) '
description: 針對特定裝置格式化 rich edit 控制項中的文字範圍。
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843712"
---
# <a name="em_formatrange-message"></a><span data-ttu-id="6d539-104">EM \_ FORMATRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="6d539-104">EM\_FORMATRANGE message</span></span>

<span data-ttu-id="6d539-105">針對特定裝置格式化 rich edit 控制項中的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="6d539-105">Formats a range of text in a rich edit control for a specific device.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d539-106">參數</span><span class="sxs-lookup"><span data-stu-id="6d539-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d539-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d539-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d539-108">指定是否呈現文字。</span><span class="sxs-lookup"><span data-stu-id="6d539-108">Specifies whether to render the text.</span></span> <span data-ttu-id="6d539-109">如果這個參數不是零，則會呈現文字。</span><span class="sxs-lookup"><span data-stu-id="6d539-109">If this parameter is not zero, the text is rendered.</span></span> <span data-ttu-id="6d539-110">否則，只會測量文字。</span><span class="sxs-lookup"><span data-stu-id="6d539-110">Otherwise, the text is just measured.</span></span>

</dd> <dt>

<span data-ttu-id="6d539-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d539-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d539-112">[**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange)結構，其中包含輸出裝置的相關資訊，或 **Null** 表示控制項快取的可用資訊。</span><span class="sxs-lookup"><span data-stu-id="6d539-112">A [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure containing information about the output device, or **NULL** to free information cached by the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d539-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d539-113">Return value</span></span>

<span data-ttu-id="6d539-114">此訊息會傳回符合區域的最後一個字元的索引，加上1。</span><span class="sxs-lookup"><span data-stu-id="6d539-114">This message returns the index of the last character that fits in the region, plus 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d539-115">備註</span><span class="sxs-lookup"><span data-stu-id="6d539-115">Remarks</span></span>

<span data-ttu-id="6d539-116">此訊息通常是用來格式化輸出裝置（如印表機）之 rich edit 控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="6d539-116">This message is typically used to format the content of rich edit control for an output device such as a printer.</span></span>

<span data-ttu-id="6d539-117">使用此訊息來格式化某範圍的文字之後，請務必再次傳送 **EM \_ FORMATRANGE** ，但是將 *lParam* 設為 **Null**，以釋放快取的資訊，否則會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="6d539-117">After using this message to format a range of text, it is important that you free cached information by sending **EM\_FORMATRANGE** again, but with *lParam* set to **NULL**; otherwise, a memory leak will occur.</span></span> <span data-ttu-id="6d539-118">此外，在為一部裝置使用此訊息之後，您必須先釋放快取的資訊，再針對不同的裝置再次使用它。</span><span class="sxs-lookup"><span data-stu-id="6d539-118">Also, after using this message for one device, you must free cached information before using it again for a different device.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d539-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d539-119">Requirements</span></span>



| <span data-ttu-id="6d539-120">需求</span><span class="sxs-lookup"><span data-stu-id="6d539-120">Requirement</span></span> | <span data-ttu-id="6d539-121">值</span><span class="sxs-lookup"><span data-stu-id="6d539-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d539-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d539-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6d539-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d539-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d539-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d539-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6d539-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d539-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d539-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6d539-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d539-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d539-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d539-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d539-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d539-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="6d539-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d539-130">**EM \_ DISPLAYBAND**</span><span class="sxs-lookup"><span data-stu-id="6d539-130">**EM\_DISPLAYBAND**</span></span>](em-displayband.md)
</dt> <dt>

<span data-ttu-id="6d539-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="6d539-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6d539-132">列印 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="6d539-132">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

 





