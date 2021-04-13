---
title: 'LB_GETITEMRECT 訊息 (Winuser .h) '
description: 取得以清單方塊專案為範圍的矩形維度，這是清單方塊專案目前顯示在清單方塊中的範圍。
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- LB_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465040"
---
# <a name="lb_getitemrect-message"></a><span data-ttu-id="94ed7-104">LB \_ GETITEMRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="94ed7-104">LB\_GETITEMRECT message</span></span>

<span data-ttu-id="94ed7-105">取得以清單方塊專案為範圍的矩形維度，這是清單方塊專案目前顯示在清單方塊中的範圍。</span><span class="sxs-lookup"><span data-stu-id="94ed7-105">Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="94ed7-106">參數</span><span class="sxs-lookup"><span data-stu-id="94ed7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94ed7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94ed7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94ed7-108">項目之以零起始的索引。</span><span class="sxs-lookup"><span data-stu-id="94ed7-108">The zero-based index of the item.</span></span>

<span data-ttu-id="94ed7-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="94ed7-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="94ed7-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="94ed7-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="94ed7-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="94ed7-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="94ed7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94ed7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94ed7-113">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收清單方塊中專案的用戶端座標。</span><span class="sxs-lookup"><span data-stu-id="94ed7-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the client coordinates for the item in the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94ed7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="94ed7-114">Return value</span></span>

<span data-ttu-id="94ed7-115">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="94ed7-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ed7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="94ed7-116">Requirements</span></span>



| <span data-ttu-id="94ed7-117">需求</span><span class="sxs-lookup"><span data-stu-id="94ed7-117">Requirement</span></span> | <span data-ttu-id="94ed7-118">值</span><span class="sxs-lookup"><span data-stu-id="94ed7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ed7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94ed7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94ed7-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94ed7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="94ed7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94ed7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94ed7-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94ed7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94ed7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="94ed7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="94ed7-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="94ed7-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ed7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94ed7-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="94ed7-126">[**矩形**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94ed7-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

