---
title: 'LB_SELITEMRANGEEX 訊息 (Winuser .h) '
description: 選取多重選取清單方塊中的一或多個連續專案。
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934907"
---
# <a name="lb_selitemrangeex-message"></a><span data-ttu-id="42d75-104">LB \_ SELITEMRANGEEX 訊息</span><span class="sxs-lookup"><span data-stu-id="42d75-104">LB\_SELITEMRANGEEX message</span></span>

<span data-ttu-id="42d75-105">選取多重選取清單方塊中的一或多個連續專案。</span><span class="sxs-lookup"><span data-stu-id="42d75-105">Selects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="42d75-106">參數</span><span class="sxs-lookup"><span data-stu-id="42d75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d75-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42d75-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42d75-108">指定要選取之第一個專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="42d75-108">Specifies the zero-based index of the first item to select.</span></span>

<span data-ttu-id="42d75-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="42d75-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="42d75-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="42d75-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="42d75-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="42d75-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="42d75-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42d75-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42d75-113">指定要選取之最後一個專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="42d75-113">Specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d75-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="42d75-114">Return value</span></span>

<span data-ttu-id="42d75-115">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="42d75-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="42d75-116">備註</span><span class="sxs-lookup"><span data-stu-id="42d75-116">Remarks</span></span>

<span data-ttu-id="42d75-117">如果 *wParam* 參數小於 *lParam* 參數，則會選取指定的專案範圍。</span><span class="sxs-lookup"><span data-stu-id="42d75-117">If the *wParam* parameter is less than the *lParam* parameter, the specified range of items is selected.</span></span> <span data-ttu-id="42d75-118">如果 *wParam* 大於或等於 *lParam*，則範圍會從指定的專案範圍中移除。</span><span class="sxs-lookup"><span data-stu-id="42d75-118">If *wParam* is greater than or equal to *lParam*, the range is removed from the specified range of items.</span></span> <span data-ttu-id="42d75-119">若只要選取一個專案，請選取兩個專案，然後取消選取不想要的專案。</span><span class="sxs-lookup"><span data-stu-id="42d75-119">To select only one item, select two items and then deselect the unwanted item.</span></span>

<span data-ttu-id="42d75-120">此訊息只能搭配多重選取清單方塊使用。</span><span class="sxs-lookup"><span data-stu-id="42d75-120">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="42d75-121">此訊息只能選取前65536個專案內的範圍。</span><span class="sxs-lookup"><span data-stu-id="42d75-121">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d75-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="42d75-122">Requirements</span></span>



| <span data-ttu-id="42d75-123">需求</span><span class="sxs-lookup"><span data-stu-id="42d75-123">Requirement</span></span> | <span data-ttu-id="42d75-124">值</span><span class="sxs-lookup"><span data-stu-id="42d75-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d75-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42d75-125">Minimum supported client</span></span><br/> | <span data-ttu-id="42d75-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42d75-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42d75-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42d75-127">Minimum supported server</span></span><br/> | <span data-ttu-id="42d75-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42d75-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42d75-129">標頭</span><span class="sxs-lookup"><span data-stu-id="42d75-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="42d75-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="42d75-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42d75-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42d75-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="42d75-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="42d75-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="42d75-133">**LB \_ SELITEMRANGE**</span><span class="sxs-lookup"><span data-stu-id="42d75-133">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> <dt>

[<span data-ttu-id="42d75-134">**LB \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="42d75-134">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





