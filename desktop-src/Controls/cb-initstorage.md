---
title: 'CB_INITSTORAGE 訊息 (Winuser .h) '
description: 應用程式會先傳送 CB \_ INITSTORAGE 訊息，然後再將大量專案新增至下拉式方塊的清單方塊部分。 這則訊息會配置記憶體來儲存清單方塊專案。
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE message Windows 控制項
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094576"
---
# <a name="cb_initstorage-message"></a><span data-ttu-id="5f77d-105">CB \_ INITSTORAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="5f77d-105">CB\_INITSTORAGE message</span></span>

<span data-ttu-id="5f77d-106">應用程式會先傳送 **CB \_ INITSTORAGE** 訊息，然後再將大量專案新增至下拉式方塊的清單方塊部分。</span><span class="sxs-lookup"><span data-stu-id="5f77d-106">An application sends the **CB\_INITSTORAGE** message before adding a large number of items to the list box portion of a combo box.</span></span> <span data-ttu-id="5f77d-107">這則訊息會配置記憶體來儲存清單方塊專案。</span><span class="sxs-lookup"><span data-stu-id="5f77d-107">This message allocates memory for storing list box items.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f77d-108">參數</span><span class="sxs-lookup"><span data-stu-id="5f77d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f77d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f77d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f77d-110">要加入的專案數目。</span><span class="sxs-lookup"><span data-stu-id="5f77d-110">The number of items to add.</span></span>

</dd> <dt>

<span data-ttu-id="5f77d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f77d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f77d-112">要配置給專案字串的記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f77d-112">The amount of memory to allocate for item strings, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f77d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f77d-113">Return value</span></span>

<span data-ttu-id="5f77d-114">如果訊息成功，傳回值就是已預先配置記憶體的專案總數，也就是所有成功的 **CB \_ INITSTORAGE** 訊息新增的專案總數。</span><span class="sxs-lookup"><span data-stu-id="5f77d-114">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **CB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="5f77d-115">如果訊息失敗，則傳回值為 CB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="5f77d-115">If the message fails, the return value is CB\_ERRSPACE.</span></span>

<span data-ttu-id="5f77d-116">此訊息會配置記憶體，並傳回上述的成功和錯誤值。</span><span class="sxs-lookup"><span data-stu-id="5f77d-116">The message allocates memory and returns the success and error values described above.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f77d-117">備註</span><span class="sxs-lookup"><span data-stu-id="5f77d-117">Remarks</span></span>

<span data-ttu-id="5f77d-118">**CB \_ INITSTORAGE** 訊息可協助加速初始化具有大量專案 (超過 100) 的下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="5f77d-118">The **CB\_INITSTORAGE** message helps speed up the initialization of combo boxes that have a large number of items (over 100).</span></span> <span data-ttu-id="5f77d-119">它會保留指定的記憶體數量，讓後續的 [**CB \_ ADDSTRING**](cb-addstring.md)、 [**cb \_ INSERTSTRING**](cb-insertstring.md)和 [**CB \_ DIR**](cb-dir.md) 訊息能以最短的時間進行。</span><span class="sxs-lookup"><span data-stu-id="5f77d-119">It reserves the specified amount of memory so that subsequent [**CB\_ADDSTRING**](cb-addstring.md), [**CB\_INSERTSTRING**](cb-insertstring.md), and [**CB\_DIR**](cb-dir.md) messages take the shortest possible time.</span></span> <span data-ttu-id="5f77d-120">您可以使用 *wParam* 和 *lParam* 參數的估計值。</span><span class="sxs-lookup"><span data-stu-id="5f77d-120">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="5f77d-121">如果您高估值，系統會配置額外的記憶體，如果低估了，則會將一般配置用於超出要求數量的專案。</span><span class="sxs-lookup"><span data-stu-id="5f77d-121">If you overestimate, the extra memory is allocated, if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f77d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f77d-122">Requirements</span></span>



| <span data-ttu-id="5f77d-123">需求</span><span class="sxs-lookup"><span data-stu-id="5f77d-123">Requirement</span></span> | <span data-ttu-id="5f77d-124">值</span><span class="sxs-lookup"><span data-stu-id="5f77d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f77d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f77d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5f77d-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f77d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f77d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f77d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5f77d-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f77d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f77d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5f77d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f77d-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5f77d-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f77d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f77d-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f77d-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="5f77d-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f77d-133">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="5f77d-133">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="5f77d-134">**CB \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="5f77d-134">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="5f77d-135">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="5f77d-135">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





