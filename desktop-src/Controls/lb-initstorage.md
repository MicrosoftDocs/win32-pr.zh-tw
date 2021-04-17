---
title: 'LB_INITSTORAGE 訊息 (Winuser .h) '
description: 配置用來儲存清單方塊專案的記憶體。 在應用程式將大量專案加入清單方塊之前，會使用此訊息。
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465373"
---
# <a name="lb_initstorage-message"></a><span data-ttu-id="18de5-105">LB \_ INITSTORAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="18de5-105">LB\_INITSTORAGE message</span></span>

<span data-ttu-id="18de5-106">配置用來儲存清單方塊專案的記憶體。</span><span class="sxs-lookup"><span data-stu-id="18de5-106">Allocates memory for storing list box items.</span></span> <span data-ttu-id="18de5-107">在應用程式將大量專案加入清單方塊之前，會使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="18de5-107">This message is used before an application adds a large number of items to a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="18de5-108">參數</span><span class="sxs-lookup"><span data-stu-id="18de5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18de5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18de5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18de5-110">要加入的專案數目。</span><span class="sxs-lookup"><span data-stu-id="18de5-110">The number of items to add.</span></span>

<span data-ttu-id="18de5-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="18de5-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="18de5-112">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="18de5-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="18de5-113">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="18de5-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="18de5-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18de5-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18de5-115">要配置給專案字串的記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="18de5-115">The amount of memory, in bytes, to allocate for item strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18de5-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="18de5-116">Return value</span></span>

<span data-ttu-id="18de5-117">如果訊息成功，則傳回值會是已預先配置記憶體的專案總數，也就是所有成功 **LB \_ INITSTORAGE** 訊息新增的專案總數。</span><span class="sxs-lookup"><span data-stu-id="18de5-117">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **LB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="18de5-118">如果訊息失敗，則傳回值為 LB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="18de5-118">If the message fails, the return value is LB\_ERRSPACE.</span></span>

<span data-ttu-id="18de5-119">Microsoft Windows NT 4.0：此訊息不會配置指定的記憶體數量;但是，它一律會傳回在 *wParam* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="18de5-119">Microsoft Windows NT 4.0 : This message does not allocate the specified amount of memory; however, it always returns the value specified in the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="18de5-120">備註</span><span class="sxs-lookup"><span data-stu-id="18de5-120">Remarks</span></span>

<span data-ttu-id="18de5-121">**LB \_ INITSTORAGE** 訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="18de5-121">The **LB\_INITSTORAGE** message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="18de5-122">它會保留指定的記憶體數量，讓後續 [**的 \_ LB ADDSTRING**](lb-addstring.md)、 [**lb \_ INSERTSTRING**](lb-insertstring.md)、 [**lb \_ DIR**](lb-dir.md)和 [**LB \_ ADDFILE**](lb-addfile.md) 訊息都能以最短的時間進行。</span><span class="sxs-lookup"><span data-stu-id="18de5-122">It reserves the specified amount of memory so that subsequent [**LB\_ADDSTRING**](lb-addstring.md), [**LB\_INSERTSTRING**](lb-insertstring.md), [**LB\_DIR**](lb-dir.md), and [**LB\_ADDFILE**](lb-addfile.md) messages take the shortest possible time.</span></span> <span data-ttu-id="18de5-123">您可以使用 *wParam* 和 *lParam* 參數的估計值。</span><span class="sxs-lookup"><span data-stu-id="18de5-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="18de5-124">如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。</span><span class="sxs-lookup"><span data-stu-id="18de5-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="18de5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="18de5-125">Requirements</span></span>



| <span data-ttu-id="18de5-126">需求</span><span class="sxs-lookup"><span data-stu-id="18de5-126">Requirement</span></span> | <span data-ttu-id="18de5-127">值</span><span class="sxs-lookup"><span data-stu-id="18de5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18de5-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18de5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="18de5-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18de5-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="18de5-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18de5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="18de5-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18de5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="18de5-132">標頭</span><span class="sxs-lookup"><span data-stu-id="18de5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="18de5-133"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="18de5-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18de5-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18de5-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="18de5-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="18de5-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18de5-136">**LB \_ ADDFILE**</span><span class="sxs-lookup"><span data-stu-id="18de5-136">**LB\_ADDFILE**</span></span>](lb-addfile.md)
</dt> <dt>

[<span data-ttu-id="18de5-137">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="18de5-137">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="18de5-138">**LB \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="18de5-138">**LB\_DIR**</span></span>](lb-dir.md)
</dt> <dt>

[<span data-ttu-id="18de5-139">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="18de5-139">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





