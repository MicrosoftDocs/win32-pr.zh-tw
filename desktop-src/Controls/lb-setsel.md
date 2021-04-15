---
title: 'LB_SETSEL 訊息 (Winuser .h) '
description: 在多重選取清單方塊中選取專案，並視需要將專案滾動至 [view]。
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- LB_SETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466521"
---
# <a name="lb_setsel-message"></a><span data-ttu-id="53edb-104">LB \_ SETSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="53edb-104">LB\_SETSEL message</span></span>

<span data-ttu-id="53edb-105">在多重選取清單方塊中選取專案，並視需要將專案滾動至 [view]。</span><span class="sxs-lookup"><span data-stu-id="53edb-105">Selects an item in a multiple-selection list box and, if necessary, scrolls the item into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="53edb-106">參數</span><span class="sxs-lookup"><span data-stu-id="53edb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53edb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53edb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53edb-108">指定如何設定選取專案。</span><span class="sxs-lookup"><span data-stu-id="53edb-108">Specifies how to set the selection.</span></span> <span data-ttu-id="53edb-109">如果此參數為 **TRUE**，則會選取並反白顯示專案;如果為 **FALSE**，則會移除反白顯示，且不會再選取專案。</span><span class="sxs-lookup"><span data-stu-id="53edb-109">If this parameter is **TRUE**, the item is selected and highlighted; if it is **FALSE**, the highlight is removed and the item is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="53edb-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53edb-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53edb-111">指定要設定之專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="53edb-111">Specifies the zero-based index of the item to set.</span></span> <span data-ttu-id="53edb-112">如果此參數為-1，則會根據 *wParam* 的值，在所有專案中加入或移除選取範圍，且不會發生任何滾動。</span><span class="sxs-lookup"><span data-stu-id="53edb-112">If this parameter is -1, the selection is added to or removed from all items, depending on the value of *wParam*, and no scrolling occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53edb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="53edb-113">Return value</span></span>

<span data-ttu-id="53edb-114">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="53edb-114">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="53edb-115">備註</span><span class="sxs-lookup"><span data-stu-id="53edb-115">Remarks</span></span>

<span data-ttu-id="53edb-116">此訊息只能搭配多重選取清單方塊使用。</span><span class="sxs-lookup"><span data-stu-id="53edb-116">Use this message only with multiple-selection list boxes.</span></span>

## <a name="requirements"></a><span data-ttu-id="53edb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="53edb-117">Requirements</span></span>



| <span data-ttu-id="53edb-118">需求</span><span class="sxs-lookup"><span data-stu-id="53edb-118">Requirement</span></span> | <span data-ttu-id="53edb-119">值</span><span class="sxs-lookup"><span data-stu-id="53edb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53edb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53edb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53edb-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53edb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53edb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53edb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53edb-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53edb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53edb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="53edb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="53edb-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="53edb-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53edb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53edb-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="53edb-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="53edb-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53edb-128">**LB \_ GETSEL**</span><span class="sxs-lookup"><span data-stu-id="53edb-128">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="53edb-129">**LB \_ SELITEMRANGE**</span><span class="sxs-lookup"><span data-stu-id="53edb-129">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> </dl>

 

 





