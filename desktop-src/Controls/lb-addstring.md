---
title: 'LB_ADDSTRING 訊息 (Winuser .h) '
description: 將字串加入至清單方塊。 如果清單方塊沒有磅 \_ 排序樣式，則會將字串加入至清單結尾。 否則，會將字串插入清單中，並排序清單。
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025029"
---
# <a name="lb_addstring-message"></a><span data-ttu-id="3754f-106">LB \_ ADDSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="3754f-106">LB\_ADDSTRING message</span></span>

<span data-ttu-id="3754f-107">將字串加入至清單方塊。</span><span class="sxs-lookup"><span data-stu-id="3754f-107">Adds a string to a list box.</span></span> <span data-ttu-id="3754f-108">如果清單方塊沒有 [**磅 \_ 排序**](list-box-styles.md) 樣式，則會將字串加入至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="3754f-108">If the list box does not have the [**LBS\_SORT**](list-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="3754f-109">否則，會將字串插入清單中，並排序清單。</span><span class="sxs-lookup"><span data-stu-id="3754f-109">Otherwise, the string is inserted into the list and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="3754f-110">參數</span><span class="sxs-lookup"><span data-stu-id="3754f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3754f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3754f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3754f-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="3754f-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3754f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3754f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3754f-114">要加入之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="3754f-114">A pointer to the null-terminated string that is to be added.</span></span>

<span data-ttu-id="3754f-115">如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則此參數會儲存為專案資料，而不是字串。</span><span class="sxs-lookup"><span data-stu-id="3754f-115">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="3754f-116">您可以傳送 **LB \_ GETITEMDATA** 和 **lb \_ SETITEMDATA** 訊息來取得或修改專案資料。</span><span class="sxs-lookup"><span data-stu-id="3754f-116">You can send the **LB\_GETITEMDATA** and **LB\_SETITEMDATA** messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3754f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3754f-117">Return value</span></span>

<span data-ttu-id="3754f-118">傳回值是清單方塊中字串以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="3754f-118">The return value is the zero-based index of the string in the list box.</span></span> <span data-ttu-id="3754f-119">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="3754f-119">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="3754f-120">如果空間不足，無法儲存新的字串，則傳回值為 LB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="3754f-120">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3754f-121">備註</span><span class="sxs-lookup"><span data-stu-id="3754f-121">Remarks</span></span>

<span data-ttu-id="3754f-122">如果清單方塊具有主控描繪樣式和 [**磅 \_ 排序**](list-box-styles.md) 樣式（而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式），系統會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息一次或多次傳送給清單方塊的擁有者，以便在清單方塊中正確地放置新專案。</span><span class="sxs-lookup"><span data-stu-id="3754f-122">If the list box has an owner-drawn style and the [**LBS\_SORT**](list-box-styles.md) style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends the [**WM\_COMPAREITEM**](wm-compareitem.md) message one or more times to the owner of the list box to place the new item properly in the list box.</span></span>

<span data-ttu-id="3754f-123">[**LB \_ INITSTORAGE**](lb-initstorage.md)訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="3754f-123">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="3754f-124">它會保留指定的記憶體數量，讓後續的 **LB \_ ADDSTRING** 訊息能以最短的時間進行。</span><span class="sxs-lookup"><span data-stu-id="3754f-124">It reserves the specified amount of memory so that subsequent **LB\_ADDSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="3754f-125">您可以使用 *wParam* 和 *lParam* 參數的估計值。</span><span class="sxs-lookup"><span data-stu-id="3754f-125">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="3754f-126">如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。</span><span class="sxs-lookup"><span data-stu-id="3754f-126">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="3754f-127">如果清單方塊具有 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式，而且您新增的字串範圍超出清單方塊，請傳送 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息，以確保會顯示水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="3754f-127">If the list box has the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="3754f-128">若為 ANSI 應用程式，系統會使用 CP ACP 將清單方塊中的文字轉換成 Unicode \_ 。</span><span class="sxs-lookup"><span data-stu-id="3754f-128">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="3754f-129">這可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="3754f-129">This can cause problems.</span></span> <span data-ttu-id="3754f-130">例如，在日文視窗的非 Unicode 清單方塊中，重音的羅馬字元將會出現模糊。</span><span class="sxs-lookup"><span data-stu-id="3754f-130">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="3754f-131">若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。</span><span class="sxs-lookup"><span data-stu-id="3754f-131">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="3754f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="3754f-132">Requirements</span></span>



| <span data-ttu-id="3754f-133">需求</span><span class="sxs-lookup"><span data-stu-id="3754f-133">Requirement</span></span> | <span data-ttu-id="3754f-134">值</span><span class="sxs-lookup"><span data-stu-id="3754f-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3754f-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3754f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3754f-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3754f-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3754f-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3754f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3754f-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3754f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3754f-139">標頭</span><span class="sxs-lookup"><span data-stu-id="3754f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3754f-140"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3754f-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3754f-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3754f-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="3754f-142">**參考**</span><span class="sxs-lookup"><span data-stu-id="3754f-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3754f-143">**LB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="3754f-143">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="3754f-144">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="3754f-144">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="3754f-145">**LB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="3754f-145">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="3754f-146">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="3754f-146">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="3754f-147">**WM \_ COMPAREITEM**</span><span class="sxs-lookup"><span data-stu-id="3754f-147">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

