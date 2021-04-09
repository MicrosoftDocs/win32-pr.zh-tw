---
title: 'LB_DELETESTRING 訊息 (Winuser .h) '
description: 刪除清單方塊中的字串。
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844036"
---
# <a name="lb_deletestring-message"></a><span data-ttu-id="6648c-104">LB \_ DELETESTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="6648c-104">LB\_DELETESTRING message</span></span>

<span data-ttu-id="6648c-105">刪除清單方塊中的字串。</span><span class="sxs-lookup"><span data-stu-id="6648c-105">Deletes a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6648c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6648c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6648c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6648c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6648c-108">要刪除之字串的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="6648c-108">The zero-based index of the string to be deleted.</span></span>

<span data-ttu-id="6648c-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="6648c-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6648c-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="6648c-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6648c-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6648c-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6648c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6648c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6648c-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="6648c-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6648c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6648c-114">Return value</span></span>

<span data-ttu-id="6648c-115">傳回值是清單中剩餘字串的計數。</span><span class="sxs-lookup"><span data-stu-id="6648c-115">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="6648c-116">\_如果 *wParam* 參數指定的索引大於清單中的專案數，則傳回值為 LB ERR。</span><span class="sxs-lookup"><span data-stu-id="6648c-116">The return value is LB\_ERR if the *wParam* parameter specifies an index greater than the number of items in the list.</span></span>

## <a name="remarks"></a><span data-ttu-id="6648c-117">備註</span><span class="sxs-lookup"><span data-stu-id="6648c-117">Remarks</span></span>

<span data-ttu-id="6648c-118">如果應用程式建立具有主控描繪樣式但沒有 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式的清單方塊，系統會將 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息傳送給清單方塊的擁有者，讓應用程式可以釋出與該專案相關聯的任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="6648c-118">If an application creates the list box with an owner-drawn style but without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the list box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="6648c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6648c-119">Requirements</span></span>



| <span data-ttu-id="6648c-120">需求</span><span class="sxs-lookup"><span data-stu-id="6648c-120">Requirement</span></span> | <span data-ttu-id="6648c-121">值</span><span class="sxs-lookup"><span data-stu-id="6648c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6648c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6648c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6648c-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6648c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6648c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6648c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6648c-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6648c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6648c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6648c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6648c-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6648c-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6648c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6648c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6648c-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="6648c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6648c-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="6648c-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="6648c-131">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="6648c-131">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="6648c-132">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="6648c-132">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





