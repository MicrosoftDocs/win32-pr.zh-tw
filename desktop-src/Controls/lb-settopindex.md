---
title: 'LB_SETTOPINDEX 訊息 (Winuser .h) '
description: 確定清單方塊中的指定專案可以看見。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- LB_SETTOPINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b415c2369ccc7963a5139ab001159bdba7d6326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105522"
---
# <a name="lb_settopindex-message"></a><span data-ttu-id="36102-104">LB \_ SETTOPINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="36102-104">LB\_SETTOPINDEX message</span></span>

<span data-ttu-id="36102-105">確定清單方塊中的指定專案可以看見。</span><span class="sxs-lookup"><span data-stu-id="36102-105">Ensures that the specified item in a list box is visible.</span></span>

## <a name="parameters"></a><span data-ttu-id="36102-106">參數</span><span class="sxs-lookup"><span data-stu-id="36102-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36102-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36102-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36102-108">清單方塊中專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="36102-108">The zero-based index of the item in the list box.</span></span>

<span data-ttu-id="36102-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="36102-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="36102-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="36102-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="36102-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="36102-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="36102-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36102-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36102-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="36102-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36102-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="36102-114">Return value</span></span>

<span data-ttu-id="36102-115">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="36102-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="36102-116">備註</span><span class="sxs-lookup"><span data-stu-id="36102-116">Remarks</span></span>

<span data-ttu-id="36102-117">系統會將清單方塊內容滾動，讓指定的專案出現在清單方塊的頂端，或達到最大捲軸範圍。</span><span class="sxs-lookup"><span data-stu-id="36102-117">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="36102-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="36102-118">Requirements</span></span>



| <span data-ttu-id="36102-119">需求</span><span class="sxs-lookup"><span data-stu-id="36102-119">Requirement</span></span> | <span data-ttu-id="36102-120">值</span><span class="sxs-lookup"><span data-stu-id="36102-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36102-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36102-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36102-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36102-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="36102-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36102-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36102-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36102-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36102-125">標頭</span><span class="sxs-lookup"><span data-stu-id="36102-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="36102-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="36102-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36102-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36102-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36102-128">**LB \_ GETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="36102-128">**LB\_GETTOPINDEX**</span></span>](lb-gettopindex.md)
</dt> </dl>

 

 





