---
title: 'LB_GETITEMHEIGHT 訊息 (Winuser .h) '
description: 取得清單方塊中專案的高度。
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843432"
---
# <a name="lb_getitemheight-message"></a><span data-ttu-id="a8d03-104">LB \_ GETITEMHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="a8d03-104">LB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="a8d03-105">取得清單方塊中專案的高度。</span><span class="sxs-lookup"><span data-stu-id="a8d03-105">Gets the height of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8d03-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8d03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d03-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8d03-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d03-108">清單方塊專案以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="a8d03-108">The zero-based index of the list box item.</span></span> <span data-ttu-id="a8d03-109">只有在清單方塊具有 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式時，才會使用此索引; 否則，它必須為零。</span><span class="sxs-lookup"><span data-stu-id="a8d03-109">This index is used only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, it must be zero.</span></span>

<span data-ttu-id="a8d03-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="a8d03-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="a8d03-111">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="a8d03-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="a8d03-112">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a8d03-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="a8d03-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8d03-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d03-114">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="a8d03-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d03-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8d03-115">Return value</span></span>

<span data-ttu-id="a8d03-116">傳回值是清單方塊中每個專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a8d03-116">The return value is the height, in pixels, of each item in the list box.</span></span> <span data-ttu-id="a8d03-117">如果清單方塊具有 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md)樣式，則傳回值為 *wParam* 參數所指定之專案的高度。</span><span class="sxs-lookup"><span data-stu-id="a8d03-117">The return value is the height of the item specified by the *wParam* parameter if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style.</span></span> <span data-ttu-id="a8d03-118">如果發生錯誤，傳回值會是 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="a8d03-118">The return value is LB\_ERR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d03-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8d03-119">Requirements</span></span>



| <span data-ttu-id="a8d03-120">需求</span><span class="sxs-lookup"><span data-stu-id="a8d03-120">Requirement</span></span> | <span data-ttu-id="a8d03-121">值</span><span class="sxs-lookup"><span data-stu-id="a8d03-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d03-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8d03-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d03-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8d03-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8d03-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8d03-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d03-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8d03-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8d03-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a8d03-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8d03-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a8d03-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8d03-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8d03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d03-129">**LB \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="a8d03-129">**LB\_SETITEMHEIGHT**</span></span>](lb-setitemheight.md)
</dt> </dl>

 

 





