---
title: 'LB_SETCOUNT 訊息 (Winuser .h) '
description: 設定清單方塊中以磅 NODATA 樣式建立的專案計數 \_ ，而不是以磅 HASSTRINGS 樣式建立的專案計數 \_ 。
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025381"
---
# <a name="lb_setcount-message"></a><span data-ttu-id="699c0-104">LB \_ SETCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="699c0-104">LB\_SETCOUNT message</span></span>

<span data-ttu-id="699c0-105">設定清單方塊中以 [**磅 \_ NODATA**](list-box-styles.md) 樣式建立的專案計數，而不是以 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式建立的專案計數。</span><span class="sxs-lookup"><span data-stu-id="699c0-105">Sets the count of items in a list box created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="699c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="699c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="699c0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="699c0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="699c0-108">指定清單方塊中新的專案計數。</span><span class="sxs-lookup"><span data-stu-id="699c0-108">Specifies the new count of items in the list box.</span></span>

<span data-ttu-id="699c0-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="699c0-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="699c0-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="699c0-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="699c0-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="699c0-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="699c0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="699c0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="699c0-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="699c0-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="699c0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="699c0-114">Return value</span></span>

<span data-ttu-id="699c0-115">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="699c0-115">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="699c0-116">如果記憶體不足，無法儲存專案，則傳回值為 LB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="699c0-116">If there is insufficient memory to store the items, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="699c0-117">備註</span><span class="sxs-lookup"><span data-stu-id="699c0-117">Remarks</span></span>

<span data-ttu-id="699c0-118">只有使用 [**磅 \_ NODATA**](list-box-styles.md)樣式建立的清單方塊才支援 **LB \_ SETCOUNT** 訊息，且不會以 [**磅 \_ HASSTRINGS**](list-box-styles.md)樣式建立。</span><span class="sxs-lookup"><span data-stu-id="699c0-118">The **LB\_SETCOUNT** message is supported only by list boxes created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span> <span data-ttu-id="699c0-119">所有其他清單方塊都會傳回 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="699c0-119">All other list boxes return LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="699c0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="699c0-120">Requirements</span></span>



| <span data-ttu-id="699c0-121">需求</span><span class="sxs-lookup"><span data-stu-id="699c0-121">Requirement</span></span> | <span data-ttu-id="699c0-122">值</span><span class="sxs-lookup"><span data-stu-id="699c0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="699c0-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="699c0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="699c0-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="699c0-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="699c0-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="699c0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="699c0-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="699c0-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="699c0-127">標頭</span><span class="sxs-lookup"><span data-stu-id="699c0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="699c0-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="699c0-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="699c0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="699c0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="699c0-130">**LB \_ GETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="699c0-130">**LB\_GETCOUNT**</span></span>](lb-getcount.md)
</dt> </dl>

 

 





