---
title: 'LB_SETITEMDATA 訊息 (Winuser .h) '
description: 在清單方塊中設定與指定之專案相關聯的值。
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- LB_SETITEMDATA message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105533"
---
# <a name="lb_setitemdata-message"></a><span data-ttu-id="5421e-104">LB \_ SETITEMDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="5421e-104">LB\_SETITEMDATA message</span></span>

<span data-ttu-id="5421e-105">在清單方塊中設定與指定之專案相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="5421e-105">Sets a value associated with the specified item in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5421e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5421e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5421e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5421e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5421e-108">指定專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="5421e-108">Specifies the zero-based index of the item.</span></span> <span data-ttu-id="5421e-109">如果這個值是-1，則 *lParam* 值會套用至清單方塊中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="5421e-109">If this value is -1, the *lParam* value applies to all items in the list box.</span></span>

<span data-ttu-id="5421e-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="5421e-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="5421e-111">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="5421e-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="5421e-112">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5421e-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="5421e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5421e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5421e-114">指定要與專案相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="5421e-114">Specifies the value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5421e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5421e-115">Return value</span></span>

<span data-ttu-id="5421e-116">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="5421e-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="5421e-117">備註</span><span class="sxs-lookup"><span data-stu-id="5421e-117">Remarks</span></span>

<span data-ttu-id="5421e-118">如果專案是在以 [**磅 \_ HASSTRINGS**](list-box-styles.md)樣式建立的主控描繪清單方塊中，則此訊息會取代將專案新增至清單方塊之 [**lb \_ ADDSTRING**](lb-addstring.md)或 [**lb \_ INSERTSTRING**](lb-insertstring.md)訊息的 *lParam* 參數中所包含的值。</span><span class="sxs-lookup"><span data-stu-id="5421e-118">If the item is in an owner-drawn list box created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this message replaces the value contained in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5421e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5421e-119">Requirements</span></span>



| <span data-ttu-id="5421e-120">需求</span><span class="sxs-lookup"><span data-stu-id="5421e-120">Requirement</span></span> | <span data-ttu-id="5421e-121">值</span><span class="sxs-lookup"><span data-stu-id="5421e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5421e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5421e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5421e-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5421e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5421e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5421e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5421e-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5421e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5421e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="5421e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5421e-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5421e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5421e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5421e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5421e-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="5421e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5421e-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="5421e-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="5421e-131">**LB \_ GETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="5421e-131">**LB\_GETITEMDATA**</span></span>](lb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="5421e-132">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="5421e-132">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





