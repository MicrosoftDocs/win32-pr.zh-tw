---
title: 'LB_GETSELITEMS 訊息 (Winuser .h) '
description: 填滿具有整數陣列的緩衝區，以在多重選取清單方塊中指定選取專案的專案數目。
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934450"
---
# <a name="lb_getselitems-message"></a><span data-ttu-id="e3516-104">LB \_ GETSELITEMS 訊息</span><span class="sxs-lookup"><span data-stu-id="e3516-104">LB\_GETSELITEMS message</span></span>

<span data-ttu-id="e3516-105">填滿具有整數陣列的緩衝區，以在多重選取清單方塊中指定選取專案的專案數目。</span><span class="sxs-lookup"><span data-stu-id="e3516-105">Fills a buffer with an array of integers that specify the item numbers of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3516-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3516-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3516-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3516-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3516-108">要將其專案編號放在緩衝區中的已選取專案數目上限。</span><span class="sxs-lookup"><span data-stu-id="e3516-108">The maximum number of selected items whose item numbers are to be placed in the buffer.</span></span>

<span data-ttu-id="e3516-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="e3516-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="e3516-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="e3516-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="e3516-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e3516-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="e3516-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3516-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3516-113">緩衝區的指標，足以容納 *wParam* 參數所指定的整數數目。</span><span class="sxs-lookup"><span data-stu-id="e3516-113">A pointer to a buffer large enough for the number of integers specified by the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3516-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3516-114">Return value</span></span>

<span data-ttu-id="e3516-115">傳回值是放置在緩衝區中的專案數目。</span><span class="sxs-lookup"><span data-stu-id="e3516-115">The return value is the number of items placed in the buffer.</span></span> <span data-ttu-id="e3516-116">如果清單方塊是單一選取清單方塊，則傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="e3516-116">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3516-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3516-117">Requirements</span></span>



| <span data-ttu-id="e3516-118">需求</span><span class="sxs-lookup"><span data-stu-id="e3516-118">Requirement</span></span> | <span data-ttu-id="e3516-119">值</span><span class="sxs-lookup"><span data-stu-id="e3516-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3516-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3516-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3516-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3516-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3516-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3516-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3516-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3516-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3516-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e3516-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3516-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e3516-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3516-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3516-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3516-127">**LB \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="e3516-127">**LB\_GETSELCOUNT**</span></span>](lb-getselcount.md)
</dt> </dl>

 

 





