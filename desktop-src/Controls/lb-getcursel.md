---
title: 'LB_GETCURSEL 訊息 (Winuser .h) '
description: 取得單一選取清單方塊中目前選取之專案的索引（如果有的話）。
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025441"
---
# <a name="lb_getcursel-message"></a><span data-ttu-id="50884-104">LB \_ GETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="50884-104">LB\_GETCURSEL message</span></span>

<span data-ttu-id="50884-105">取得單一選取清單方塊中目前選取之專案的索引（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="50884-105">Gets the index of the currently selected item, if any, in a single-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="50884-106">參數</span><span class="sxs-lookup"><span data-stu-id="50884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50884-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50884-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50884-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="50884-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="50884-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50884-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50884-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="50884-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50884-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="50884-111">Return value</span></span>

<span data-ttu-id="50884-112">在單一選取清單方塊中，傳回值是目前選取專案之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="50884-112">In a single-selection list box, the return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="50884-113">如果沒有選取專案，則傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="50884-113">If there is no selection, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="50884-114">備註</span><span class="sxs-lookup"><span data-stu-id="50884-114">Remarks</span></span>

<span data-ttu-id="50884-115">若要在多重選取清單方塊中取出選取專案的索引，請使用 [**LB \_ GETSELITEMS**](lb-getselitems.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="50884-115">To retrieve the indexes of the selected items in a multiple-selection list box, use the [**LB\_GETSELITEMS**](lb-getselitems.md) message.</span></span> <span data-ttu-id="50884-116">若要判斷是否已選取在多重選取清單方塊中具有焦點矩形的專案，請使用 [**LB \_ GETSEL**](lb-getsel.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="50884-116">To determine whether the item that has the focus rectangle in a multiple selection list box is selected, use the [**LB\_GETSEL**](lb-getsel.md) message.</span></span>

<span data-ttu-id="50884-117">如果傳送至多重選取清單方塊， **LB \_ GETCURSEL** 會傳回具有焦點矩形之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="50884-117">If sent to a multiple-selection list box, **LB\_GETCURSEL** returns the index of the item that has the focus rectangle.</span></span> <span data-ttu-id="50884-118">如果未選取任何專案，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="50884-118">If no items are selected, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="50884-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="50884-119">Requirements</span></span>



| <span data-ttu-id="50884-120">需求</span><span class="sxs-lookup"><span data-stu-id="50884-120">Requirement</span></span> | <span data-ttu-id="50884-121">值</span><span class="sxs-lookup"><span data-stu-id="50884-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50884-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50884-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50884-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50884-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50884-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50884-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50884-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50884-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50884-126">標頭</span><span class="sxs-lookup"><span data-stu-id="50884-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="50884-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="50884-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50884-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50884-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="50884-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="50884-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="50884-130">**LB \_ GETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="50884-130">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> <dt>

[<span data-ttu-id="50884-131">**LB \_ GETSEL**</span><span class="sxs-lookup"><span data-stu-id="50884-131">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="50884-132">**LB \_ GETSELITEMS**</span><span class="sxs-lookup"><span data-stu-id="50884-132">**LB\_GETSELITEMS**</span></span>](lb-getselitems.md)
</dt> <dt>

[<span data-ttu-id="50884-133">**LB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="50884-133">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> </dl>

 

 





