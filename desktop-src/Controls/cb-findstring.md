---
title: 'CB_FINDSTRING 訊息 (Winuser .h) '
description: 在下拉式方塊的清單方塊中，搜尋以指定字串中的字元開頭的專案。
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- CB_FINDSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094580"
---
# <a name="cb_findstring-message"></a><span data-ttu-id="3dedd-104">CB \_ FINDSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="3dedd-104">CB\_FINDSTRING message</span></span>

<span data-ttu-id="3dedd-105">在下拉式方塊的清單方塊中，搜尋以指定字串中的字元開頭的專案。</span><span class="sxs-lookup"><span data-stu-id="3dedd-105">Searches the list box of a combo box for an item beginning with the characters in a specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="3dedd-106">參數</span><span class="sxs-lookup"><span data-stu-id="3dedd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dedd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3dedd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3dedd-108">在要搜尋的第一個專案之前，專案以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="3dedd-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="3dedd-109">當搜尋到達清單方塊的底部時，它會從清單方塊的頂端繼續移回 *wParam* 參數所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="3dedd-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="3dedd-110">如果 *wParam* 為-1，就會從一開始就搜尋整個清單方塊。</span><span class="sxs-lookup"><span data-stu-id="3dedd-110">If *wParam* is  -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="3dedd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3dedd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3dedd-112">以 null 結束的字串指標，其中包含要搜尋的字元。</span><span class="sxs-lookup"><span data-stu-id="3dedd-112">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="3dedd-113">搜尋不區分大小寫，因此這個字串可以包含任何大小寫字母的組合。</span><span class="sxs-lookup"><span data-stu-id="3dedd-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dedd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dedd-114">Return value</span></span>

<span data-ttu-id="3dedd-115">傳回值是相符專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="3dedd-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="3dedd-116">如果搜尋失敗，則為 CB \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="3dedd-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dedd-117">備註</span><span class="sxs-lookup"><span data-stu-id="3dedd-117">Remarks</span></span>

<span data-ttu-id="3dedd-118">如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則 **CB \_ FINDSTRING** 訊息的作用取決於您的應用程式是否使用 [**cbs \_ 排序**](combo-box-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="3dedd-118">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_FINDSTRING** message does depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="3dedd-119">如果您使用 **CBS \_ 排序** 樣式，則會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給下拉式方塊的擁有者，以判斷哪一個專案符合指定的字串。</span><span class="sxs-lookup"><span data-stu-id="3dedd-119">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="3dedd-120">如果您未使用 **CBS \_ 排序** 樣式， **CB \_ FINDSTRING** 訊息會搜尋符合 *lParam* 參數值的清單專案。</span><span class="sxs-lookup"><span data-stu-id="3dedd-120">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRING** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dedd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dedd-121">Requirements</span></span>



| <span data-ttu-id="3dedd-122">需求</span><span class="sxs-lookup"><span data-stu-id="3dedd-122">Requirement</span></span> | <span data-ttu-id="3dedd-123">值</span><span class="sxs-lookup"><span data-stu-id="3dedd-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dedd-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3dedd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3dedd-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dedd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3dedd-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3dedd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3dedd-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dedd-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3dedd-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3dedd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dedd-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3dedd-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dedd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dedd-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3dedd-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="3dedd-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3dedd-132">**CB \_ FINDSTRINGEXACT**</span><span class="sxs-lookup"><span data-stu-id="3dedd-132">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="3dedd-133">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="3dedd-133">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="3dedd-134">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="3dedd-134">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="3dedd-135">**WM \_ COMPAREITEM**</span><span class="sxs-lookup"><span data-stu-id="3dedd-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





