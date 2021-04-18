---
title: 'LB_SETITEMHEIGHT 訊息 (Winuser .h) '
description: 設定清單方塊中專案的高度（以圖元為單位）。 如果清單方塊具有磅 \_ OWNERDRAWVARIABLE 樣式，則此訊息會設定 wParam 參數所指定之專案的高度。 否則，此訊息會設定清單方塊中所有專案的高度。
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466524"
---
# <a name="lb_setitemheight-message"></a><span data-ttu-id="26e60-106">LB \_ SETITEMHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="26e60-106">LB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="26e60-107">設定清單方塊中專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="26e60-107">Sets the height, in pixels, of items in a list box.</span></span> <span data-ttu-id="26e60-108">如果清單方塊具有 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式，則此訊息會設定 *wParam* 參數所指定之專案的高度。</span><span class="sxs-lookup"><span data-stu-id="26e60-108">If the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style, this message sets the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="26e60-109">否則，此訊息會設定清單方塊中所有專案的高度。</span><span class="sxs-lookup"><span data-stu-id="26e60-109">Otherwise, this message sets the height of all items in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="26e60-110">參數</span><span class="sxs-lookup"><span data-stu-id="26e60-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e60-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26e60-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26e60-112">在清單方塊中指定專案的索引（以零為基底）。</span><span class="sxs-lookup"><span data-stu-id="26e60-112">Specifies the zero-based index of the item in the list box.</span></span> <span data-ttu-id="26e60-113">只有在清單方塊具有 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式時，才使用此參數; 否則，請將它設定為零。</span><span class="sxs-lookup"><span data-stu-id="26e60-113">Use this parameter only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, set it to zero.</span></span>

<span data-ttu-id="26e60-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="26e60-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="26e60-115">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="26e60-115">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="26e60-116">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="26e60-116">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="26e60-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26e60-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26e60-118">指定專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="26e60-118">Specifies the height, in pixels, of the item.</span></span> <span data-ttu-id="26e60-119">最大高度為255圖元。</span><span class="sxs-lookup"><span data-stu-id="26e60-119">The maximum height is 255 pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e60-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="26e60-120">Return value</span></span>

<span data-ttu-id="26e60-121">如果索引或高度無效，則傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="26e60-121">If the index or height is invalid, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e60-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="26e60-122">Requirements</span></span>



| <span data-ttu-id="26e60-123">需求</span><span class="sxs-lookup"><span data-stu-id="26e60-123">Requirement</span></span> | <span data-ttu-id="26e60-124">值</span><span class="sxs-lookup"><span data-stu-id="26e60-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26e60-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26e60-125">Minimum supported client</span></span><br/> | <span data-ttu-id="26e60-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26e60-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="26e60-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26e60-127">Minimum supported server</span></span><br/> | <span data-ttu-id="26e60-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26e60-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26e60-129">標頭</span><span class="sxs-lookup"><span data-stu-id="26e60-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e60-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="26e60-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e60-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26e60-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e60-132">**LB \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="26e60-132">**LB\_GETITEMHEIGHT**</span></span>](lb-getitemheight.md)
</dt> </dl>

 

 





