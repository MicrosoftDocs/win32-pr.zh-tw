---
title: 'LB_INSERTSTRING 訊息 (Winuser .h) '
description: 將字串或專案資料插入清單方塊中。 與 LB ADDSTRING 訊息不同的是 \_ ，lb \_ INSERTSTRING 訊息並不會造成具有磅排序樣式的清單進行 \_ 排序。
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105545"
---
# <a name="lb_insertstring-message"></a><span data-ttu-id="13eb6-105">LB \_ INSERTSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="13eb6-105">LB\_INSERTSTRING message</span></span>

<span data-ttu-id="13eb6-106">將字串或專案資料插入清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="13eb6-106">Inserts a string or item data into a list box.</span></span> <span data-ttu-id="13eb6-107">與 [**lb \_ ADDSTRING**](lb-addstring.md) 訊息不同的是， **lb \_ INSERTSTRING** 訊息並不會造成具有 [**磅 \_ 排序**](list-box-styles.md) 樣式的清單進行排序。</span><span class="sxs-lookup"><span data-stu-id="13eb6-107">Unlike the [**LB\_ADDSTRING**](lb-addstring.md) message, the **LB\_INSERTSTRING** message does not cause a list with the [**LBS\_SORT**](list-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="13eb6-108">參數</span><span class="sxs-lookup"><span data-stu-id="13eb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13eb6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13eb6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13eb6-110">以零為基底的索引，這是插入字串的位置。</span><span class="sxs-lookup"><span data-stu-id="13eb6-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="13eb6-111">如果此參數為-1，則會將字串加入至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="13eb6-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="13eb6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13eb6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13eb6-113">要插入之以 null 終止之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="13eb6-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="13eb6-114">如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則此參數會儲存為專案資料，而不是字串。</span><span class="sxs-lookup"><span data-stu-id="13eb6-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="13eb6-115">您可以傳送 [**LB \_ GETITEMDATA**](lb-getitemdata.md) 和 [**lb \_ SETITEMDATA**](lb-setitemdata.md) 訊息來取得或修改專案資料。</span><span class="sxs-lookup"><span data-stu-id="13eb6-115">You can send the [**LB\_GETITEMDATA**](lb-getitemdata.md) and [**LB\_SETITEMDATA**](lb-setitemdata.md) messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13eb6-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="13eb6-116">Return value</span></span>

<span data-ttu-id="13eb6-117">傳回值是插入字串之位置的索引。</span><span class="sxs-lookup"><span data-stu-id="13eb6-117">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="13eb6-118">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="13eb6-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="13eb6-119">如果空間不足，無法儲存新的字串，則傳回值為 LB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="13eb6-119">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="13eb6-120">備註</span><span class="sxs-lookup"><span data-stu-id="13eb6-120">Remarks</span></span>

<span data-ttu-id="13eb6-121">[**LB \_ INITSTORAGE**](lb-initstorage.md)訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="13eb6-121">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="13eb6-122">它會保留指定的記憶體數量，讓後續的 **LB \_ INSERTSTRING** 訊息能以最短的時間進行。</span><span class="sxs-lookup"><span data-stu-id="13eb6-122">It reserves the specified amount of memory so that subsequent **LB\_INSERTSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="13eb6-123">您可以使用 *wParam* 和 *lParam* 參數的估計值。</span><span class="sxs-lookup"><span data-stu-id="13eb6-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="13eb6-124">如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。</span><span class="sxs-lookup"><span data-stu-id="13eb6-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="13eb6-125">如果清單方塊具有 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式，而且您插入的字串範圍超出清單方塊，請傳送 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息以確保水準捲軸出現。</span><span class="sxs-lookup"><span data-stu-id="13eb6-125">If the list box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="13eb6-126">若為 ANSI 應用程式，系統會使用 CP ACP 將清單方塊中的文字轉換成 Unicode \_ 。</span><span class="sxs-lookup"><span data-stu-id="13eb6-126">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="13eb6-127">這可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="13eb6-127">This can cause problems.</span></span> <span data-ttu-id="13eb6-128">例如，在日文視窗的非 Unicode 清單方塊中，重音的羅馬字元將會出現模糊。</span><span class="sxs-lookup"><span data-stu-id="13eb6-128">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="13eb6-129">若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。</span><span class="sxs-lookup"><span data-stu-id="13eb6-129">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="13eb6-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="13eb6-130">Requirements</span></span>



| <span data-ttu-id="13eb6-131">需求</span><span class="sxs-lookup"><span data-stu-id="13eb6-131">Requirement</span></span> | <span data-ttu-id="13eb6-132">值</span><span class="sxs-lookup"><span data-stu-id="13eb6-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13eb6-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13eb6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="13eb6-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13eb6-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13eb6-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13eb6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="13eb6-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13eb6-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13eb6-137">標頭</span><span class="sxs-lookup"><span data-stu-id="13eb6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="13eb6-138"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="13eb6-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13eb6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13eb6-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="13eb6-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="13eb6-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="13eb6-141">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="13eb6-141">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="13eb6-142">**LB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="13eb6-142">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="13eb6-143">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="13eb6-143">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

