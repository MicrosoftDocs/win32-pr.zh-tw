---
title: 'LB_SETCARETINDEX 訊息 (Winuser .h) '
description: 將焦點矩形設定為多重選取清單方塊中指定索引處的專案。 如果看不到專案，則會將它滾動到視野中。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- LB_SETCARETINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844112"
---
# <a name="lb_setcaretindex-message"></a><span data-ttu-id="9b41f-105">LB \_ SETCARETINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="9b41f-105">LB\_SETCARETINDEX message</span></span>

<span data-ttu-id="9b41f-106">將焦點矩形設定為多重選取清單方塊中指定索引處的專案。</span><span class="sxs-lookup"><span data-stu-id="9b41f-106">Sets the focus rectangle to the item at the specified index in a multiple-selection list box.</span></span> <span data-ttu-id="9b41f-107">如果看不到專案，則會將它滾動到視野中。</span><span class="sxs-lookup"><span data-stu-id="9b41f-107">If the item is not visible, it is scrolled into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b41f-108">參數</span><span class="sxs-lookup"><span data-stu-id="9b41f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b41f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b41f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b41f-110">指定要接收焦點矩形之清單方塊專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="9b41f-110">Specifies the zero-based index of the list box item that is to receive the focus rectangle.</span></span>

<span data-ttu-id="9b41f-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="9b41f-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="9b41f-112">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="9b41f-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="9b41f-113">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9b41f-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="9b41f-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b41f-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b41f-115">如果這個值為 **FALSE**，則會滾動專案直到完全可見為止;若為 **TRUE**，則會滾動專案，直到至少有部分可見為止。</span><span class="sxs-lookup"><span data-stu-id="9b41f-115">If this value is **FALSE**, the item is scrolled until it is fully visible; if it is **TRUE**, the item is scrolled until it is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b41f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b41f-116">Return value</span></span>

<span data-ttu-id="9b41f-117">如果發生錯誤，傳回值會是 LB \_ ERR (-1) 。</span><span class="sxs-lookup"><span data-stu-id="9b41f-117">If an error occurs, the return value is LB\_ERR (-1).</span></span> <span data-ttu-id="9b41f-118">否則， \_ 會傳回 LB ok (0) 。</span><span class="sxs-lookup"><span data-stu-id="9b41f-118">Otherwise, LB\_OKAY (0) is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b41f-119">備註</span><span class="sxs-lookup"><span data-stu-id="9b41f-119">Remarks</span></span>

<span data-ttu-id="9b41f-120">如果將此訊息傳送至不包含選取專案的單一選取清單方塊，則會將插入號索引設定為 *wParam* 參數所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="9b41f-120">If this message is sent to a single-selection list box that does not contain a selected item, the caret index is set to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="9b41f-121">如果單一選取清單方塊包含選取的專案，清單方塊會傳回 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="9b41f-121">If the single-selection list box does contain a selected item, the list box returns LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b41f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b41f-122">Requirements</span></span>



| <span data-ttu-id="9b41f-123">需求</span><span class="sxs-lookup"><span data-stu-id="9b41f-123">Requirement</span></span> | <span data-ttu-id="9b41f-124">值</span><span class="sxs-lookup"><span data-stu-id="9b41f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b41f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b41f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9b41f-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b41f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9b41f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b41f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9b41f-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b41f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b41f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9b41f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b41f-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9b41f-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b41f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b41f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b41f-132">**LB \_ GETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="9b41f-132">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> </dl>

 

 





