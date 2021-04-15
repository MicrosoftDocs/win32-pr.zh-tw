---
title: 'LB_SELECTSTRING 訊息 (Winuser .h) '
description: 在清單方塊中搜尋以指定字串中的字元開頭的專案。 如果找到相符的專案，就會選取該專案。
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- LB_SELECTSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466529"
---
# <a name="lb_selectstring-message"></a><span data-ttu-id="f4f5e-105">LB \_ SELECTSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="f4f5e-105">LB\_SELECTSTRING message</span></span>

<span data-ttu-id="f4f5e-106">在清單方塊中搜尋以指定字串中的字元開頭的專案。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-106">Searches a list box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="f4f5e-107">如果找到相符的專案，就會選取該專案。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-107">If a matching item is found, the item is selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4f5e-108">參數</span><span class="sxs-lookup"><span data-stu-id="f4f5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4f5e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4f5e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4f5e-110">搜尋第一個項目之前，項目以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-110">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="f4f5e-111">當搜尋到達清單方塊的底部時，它會從清單方塊的頂端繼續移回 *wParam* 參數所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-111">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="f4f5e-112">如果 *wParam* 為-1，就會從一開始就搜尋整個清單方塊。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-112">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="f4f5e-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="f4f5e-114">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-114">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="f4f5e-115">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-115">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="f4f5e-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4f5e-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4f5e-117">以 null 結束的字串指標，其中包含要搜尋的前置詞。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-117">A pointer to the null-terminated string that contains the prefix for which to search.</span></span> <span data-ttu-id="f4f5e-118">搜尋不會區分大小寫，因此這個字串可以包含任何大小寫字母的組合。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-118">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4f5e-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4f5e-119">Return value</span></span>

<span data-ttu-id="f4f5e-120">如果搜尋成功，傳回值就是所選取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-120">If the search is successful, the return value is the index of the selected item.</span></span> <span data-ttu-id="f4f5e-121">如果搜尋失敗，則傳回值為 LB ERR， \_ 而且目前的選取範圍不會變更。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-121">If the search is unsuccessful, the return value is LB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f5e-122">備註</span><span class="sxs-lookup"><span data-stu-id="f4f5e-122">Remarks</span></span>

<span data-ttu-id="f4f5e-123">如有必要，會滾動清單方塊以將選取的專案帶到視野中。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-123">The list box is scrolled, if necessary, to bring the selected item into view.</span></span>

<span data-ttu-id="f4f5e-124">請勿將此訊息與具有 [**磅 \_ MULTIPLESEL**](list-box-styles.md) 或 [**磅 \_ EXTENDEDSEL**](list-box-styles.md) 樣式的清單方塊一起使用。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-124">Do not use this message with a list box that has the [**LBS\_MULTIPLESEL**](list-box-styles.md) or the [**LBS\_EXTENDEDSEL**](list-box-styles.md) styles.</span></span>

<span data-ttu-id="f4f5e-125">只有當專案的初始字元與 *lParam* 參數所指定之字串中的字元相符時，才會選取該專案。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-125">An item is selected only if its initial characters from the starting point match the characters in the string specified by the *lParam* parameter.</span></span>

<span data-ttu-id="f4f5e-126">如果清單方塊具有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則 **LB \_ SELECTSTRING** 所採取的動作取決於是否使用 [**磅 \_ 排序**](list-box-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-126">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_SELECTSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="f4f5e-127">如果使用了 **磅 \_ 排序** ，系統會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給清單方塊擁有者，以判斷哪一個專案符合指定的字串。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-127">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="f4f5e-128">否則， **LB \_ SELECTSTRING** 會嘗試尋找具有 long 值的專案， (提供為符合 *lParam* 參數的 [**lb \_ ADDSTRING**](lb-addstring.md)或 [**lb \_ INSERTSTRING**](lb-insertstring.md) message) 的 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="f4f5e-128">Otherwise, **LB\_SELECTSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f5e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4f5e-129">Requirements</span></span>



| <span data-ttu-id="f4f5e-130">需求</span><span class="sxs-lookup"><span data-stu-id="f4f5e-130">Requirement</span></span> | <span data-ttu-id="f4f5e-131">值</span><span class="sxs-lookup"><span data-stu-id="f4f5e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f5e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4f5e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f4f5e-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4f5e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f4f5e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4f5e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f4f5e-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4f5e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f4f5e-136">標頭</span><span class="sxs-lookup"><span data-stu-id="f4f5e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4f5e-137"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f4f5e-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f5e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4f5e-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4f5e-139">**參考**</span><span class="sxs-lookup"><span data-stu-id="f4f5e-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f4f5e-140">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="f4f5e-140">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="f4f5e-141">**LB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="f4f5e-141">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> <dt>

[<span data-ttu-id="f4f5e-142">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="f4f5e-142">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





