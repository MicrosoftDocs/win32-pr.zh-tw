---
title: 'LB_FINDSTRINGEXACT 訊息 (Winuser .h) '
description: 尋找完全符合指定字串的第一個清單方塊字串，不同之處在于搜尋不區分大小寫。
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- LB_FINDSTRINGEXACT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025444"
---
# <a name="lb_findstringexact-message"></a><span data-ttu-id="fa285-104">LB \_ FINDSTRINGEXACT 訊息</span><span class="sxs-lookup"><span data-stu-id="fa285-104">LB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="fa285-105">尋找完全符合指定字串的第一個清單方塊字串，不同之處在于搜尋不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="fa285-105">Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa285-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa285-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa285-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa285-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa285-108">搜尋第一個項目之前，項目以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="fa285-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="fa285-109">當搜尋到達清單方塊的底部時，它會繼續從清單方塊的頂端搜尋回 *wParam* 參數所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="fa285-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="fa285-110">如果 *wParam* 為-1，就會從一開始就搜尋整個清單方塊。</span><span class="sxs-lookup"><span data-stu-id="fa285-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="fa285-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="fa285-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="fa285-112">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="fa285-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="fa285-113">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="fa285-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="fa285-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa285-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa285-115">要搜尋之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="fa285-115">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="fa285-116">搜尋不區分大小寫，因此這個字串可以包含任何大小寫字母的組合。</span><span class="sxs-lookup"><span data-stu-id="fa285-116">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa285-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa285-117">Return value</span></span>

<span data-ttu-id="fa285-118">傳回值是相符專案的以零為起始的索引，如果搜尋失敗，則為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="fa285-118">The return value is the zero-based index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa285-119">備註</span><span class="sxs-lookup"><span data-stu-id="fa285-119">Remarks</span></span>

<span data-ttu-id="fa285-120">只有當指定的字串和清單方塊專案具有相同的長度 (但在指定的) 字串結尾有 null，且具有完全相同的字元時，此函數才會成功。</span><span class="sxs-lookup"><span data-stu-id="fa285-120">This function is only successful if the specified string and a list box item have the same length (except for the null at the end of the specified string) and have exactly the same characters.</span></span>

<span data-ttu-id="fa285-121">如果清單方塊具有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則 **LB \_ FINDSTRINGEXACT** 所採取的動作取決於是否使用 [**磅 \_ 排序**](list-box-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="fa285-121">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRINGEXACT** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="fa285-122">如果使用了 **磅 \_ 排序** ，系統會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給清單方塊擁有者，以判斷哪一個專案符合指定的字串。</span><span class="sxs-lookup"><span data-stu-id="fa285-122">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="fa285-123">否則， **LB \_ FINDSTRINGEXACT** 會嘗試尋找具有 long 值的專案， (提供為符合 *lParam* 參數的 [**lb \_ ADDSTRING**](lb-addstring.md)或 [**lb \_ INSERTSTRING**](lb-insertstring.md) message) 的 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="fa285-123">Otherwise, **LB\_FINDSTRINGEXACT** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa285-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa285-124">Requirements</span></span>



| <span data-ttu-id="fa285-125">需求</span><span class="sxs-lookup"><span data-stu-id="fa285-125">Requirement</span></span> | <span data-ttu-id="fa285-126">值</span><span class="sxs-lookup"><span data-stu-id="fa285-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa285-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa285-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fa285-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa285-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa285-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa285-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fa285-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa285-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa285-131">標頭</span><span class="sxs-lookup"><span data-stu-id="fa285-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa285-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fa285-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa285-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa285-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa285-134">**LB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="fa285-134">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> </dl>

 

 





