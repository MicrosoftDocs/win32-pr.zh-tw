---
title: 'LB_SETANCHORINDEX 訊息 (Winuser .h) '
description: 設定錨定專案 \ 郵件，也就是從中開始多重選取的專案。 多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- LB_SETANCHORINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105539"
---
# <a name="lb_setanchorindex-message"></a><span data-ttu-id="5ac39-105">LB \_ SETANCHORINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="5ac39-105">LB\_SETANCHORINDEX message</span></span>

<span data-ttu-id="5ac39-106">設定錨定專案，也就是多個選取範圍開始的專案。</span><span class="sxs-lookup"><span data-stu-id="5ac39-106">Sets the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="5ac39-107">多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。</span><span class="sxs-lookup"><span data-stu-id="5ac39-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ac39-108">參數</span><span class="sxs-lookup"><span data-stu-id="5ac39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac39-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ac39-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac39-110">指定新錨定專案的索引。</span><span class="sxs-lookup"><span data-stu-id="5ac39-110">Specifies the index of the new anchor item.</span></span>

<span data-ttu-id="5ac39-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="5ac39-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="5ac39-112">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="5ac39-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="5ac39-113">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5ac39-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="5ac39-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ac39-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac39-115">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="5ac39-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac39-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ac39-116">Return value</span></span>

<span data-ttu-id="5ac39-117">如果訊息成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="5ac39-117">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="5ac39-118">如果訊息失敗，則傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="5ac39-118">If the message fails, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac39-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ac39-119">Requirements</span></span>



| <span data-ttu-id="5ac39-120">需求</span><span class="sxs-lookup"><span data-stu-id="5ac39-120">Requirement</span></span> | <span data-ttu-id="5ac39-121">值</span><span class="sxs-lookup"><span data-stu-id="5ac39-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac39-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ac39-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac39-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ac39-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ac39-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ac39-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac39-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ac39-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ac39-126">標頭</span><span class="sxs-lookup"><span data-stu-id="5ac39-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac39-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5ac39-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac39-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ac39-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac39-129">**LB \_ GETANCHORINDEX**</span><span class="sxs-lookup"><span data-stu-id="5ac39-129">**LB\_GETANCHORINDEX**</span></span>](lb-getanchorindex.md)
</dt> </dl>

 

 





