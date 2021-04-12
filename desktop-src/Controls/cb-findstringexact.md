---
title: 'CB_FINDSTRINGEXACT 訊息 (Winuser .h) '
description: 在下拉式方塊中尋找符合在 lParam 參數中指定之字串的第一個清單方塊字串。
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f70c56a5f13fffa8dfedebd13f9830c62ef941cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509498"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="c6285-104">CB \_ FINDSTRINGEXACT 訊息</span><span class="sxs-lookup"><span data-stu-id="c6285-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="c6285-105">在下拉式方塊中尋找符合在 *lParam* 參數中指定之字串的第一個清單方塊字串。</span><span class="sxs-lookup"><span data-stu-id="c6285-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6285-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6285-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6285-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6285-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6285-108">在要搜尋的第一個專案之前，專案以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="c6285-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="c6285-109">當搜尋到達清單方塊的底部時，它會從清單方塊的頂端繼續移回 *wParam* 參數所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="c6285-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="c6285-110">如果 *wParam* 是1，就會從一開始就搜尋整個清單方塊。</span><span class="sxs-lookup"><span data-stu-id="c6285-110">If *wParam* is  1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="c6285-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6285-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6285-112">要搜尋之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="c6285-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="c6285-113">搜尋不區分大小寫，因此這個字串可以包含任何大小寫字母的組合。</span><span class="sxs-lookup"><span data-stu-id="c6285-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6285-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6285-114">Return value</span></span>

<span data-ttu-id="c6285-115">傳回值是相符專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="c6285-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="c6285-116">如果搜尋失敗，則為 CB \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6285-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6285-117">備註</span><span class="sxs-lookup"><span data-stu-id="c6285-117">Remarks</span></span>

<span data-ttu-id="c6285-118">只有當指定的字串和下拉式列示方塊專案具有相同的長度 (但結尾的 null 字元) 和相同的字元時，此函式才會成功。</span><span class="sxs-lookup"><span data-stu-id="c6285-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="c6285-119">如果您建立具有主控描繪樣式但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式的下拉式方塊，則 **CB \_ FINDSTRINGEXACT** 訊息的功能取決於您的應用程式是否使用 [**cbs \_ 排序**](combo-box-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="c6285-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="c6285-120">如果您使用 **CBS \_ 排序** 樣式，則會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給下拉式方塊的擁有者，以判斷哪一個專案符合指定的字串。</span><span class="sxs-lookup"><span data-stu-id="c6285-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="c6285-121">如果您未使用 **CBS \_ 排序** 樣式， **CB \_ FINDSTRINGEXACT** 訊息會搜尋符合 *lParam* 參數值的清單專案。</span><span class="sxs-lookup"><span data-stu-id="c6285-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6285-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6285-122">Requirements</span></span>



| <span data-ttu-id="c6285-123">需求</span><span class="sxs-lookup"><span data-stu-id="c6285-123">Requirement</span></span> | <span data-ttu-id="c6285-124">值</span><span class="sxs-lookup"><span data-stu-id="c6285-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6285-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6285-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6285-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6285-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6285-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6285-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6285-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6285-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6285-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c6285-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6285-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c6285-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6285-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6285-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6285-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="c6285-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6285-133">**CB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="c6285-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="c6285-134">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="c6285-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="c6285-135">**WM \_ COMPAREITEM**</span><span class="sxs-lookup"><span data-stu-id="c6285-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





