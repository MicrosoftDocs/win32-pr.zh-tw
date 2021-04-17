---
title: 'LB_FINDSTRING 訊息 (Winuser .h) '
description: 在清單方塊中尋找以指定字串開頭的第一個字串。
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- LB_FINDSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466808"
---
# <a name="lb_findstring-message"></a><span data-ttu-id="39a30-104">LB \_ FINDSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="39a30-104">LB\_FINDSTRING message</span></span>

<span data-ttu-id="39a30-105">在清單方塊中尋找以指定字串開頭的第一個字串。</span><span class="sxs-lookup"><span data-stu-id="39a30-105">Finds the first string in a list box that begins with the specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="39a30-106">參數</span><span class="sxs-lookup"><span data-stu-id="39a30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a30-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39a30-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a30-108">搜尋第一個項目之前，項目以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="39a30-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="39a30-109">當搜尋到達清單方塊的底部時，它會繼續從清單方塊的頂端搜尋回 *wParam* 參數所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="39a30-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="39a30-110">如果 *wParam* 為-1，就會從一開始就搜尋整個清單方塊。</span><span class="sxs-lookup"><span data-stu-id="39a30-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="39a30-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="39a30-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="39a30-112">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="39a30-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="39a30-113">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="39a30-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="39a30-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39a30-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a30-115">以 null 結束的字串指標，其中包含要搜尋的字串。</span><span class="sxs-lookup"><span data-stu-id="39a30-115">A pointer to the null-terminated string that contains the string for which to search.</span></span> <span data-ttu-id="39a30-116">搜尋不會區分大小寫，因此這個字串可以包含任何大小寫字母的組合。</span><span class="sxs-lookup"><span data-stu-id="39a30-116">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a30-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="39a30-117">Return value</span></span>

<span data-ttu-id="39a30-118">傳回值是相符專案的索引，如果搜尋失敗，則為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="39a30-118">The return value is the index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="39a30-119">備註</span><span class="sxs-lookup"><span data-stu-id="39a30-119">Remarks</span></span>

<span data-ttu-id="39a30-120">如果清單方塊具有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則 **LB \_ FINDSTRING** 所採取的動作取決於是否使用 [**磅 \_ 排序**](list-box-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="39a30-120">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="39a30-121">如果使用了 **磅 \_ 排序** ，系統會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給清單方塊擁有者，以判斷哪一個專案符合指定的字串。</span><span class="sxs-lookup"><span data-stu-id="39a30-121">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="39a30-122">否則， **LB \_ FINDSTRING** 會嘗試尋找具有 long 值的專案， (提供為符合 *lParam* 參數的 [**lb \_ ADDSTRING**](lb-addstring.md)或 [**lb \_ INSERTSTRING**](lb-insertstring.md) message) 的 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="39a30-122">Otherwise, **LB\_FINDSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a30-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="39a30-123">Requirements</span></span>



| <span data-ttu-id="39a30-124">需求</span><span class="sxs-lookup"><span data-stu-id="39a30-124">Requirement</span></span> | <span data-ttu-id="39a30-125">值</span><span class="sxs-lookup"><span data-stu-id="39a30-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a30-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39a30-126">Minimum supported client</span></span><br/> | <span data-ttu-id="39a30-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39a30-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="39a30-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39a30-128">Minimum supported server</span></span><br/> | <span data-ttu-id="39a30-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39a30-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39a30-130">標頭</span><span class="sxs-lookup"><span data-stu-id="39a30-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a30-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="39a30-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a30-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39a30-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a30-133">**LB \_ FINDSTRINGEXACT**</span><span class="sxs-lookup"><span data-stu-id="39a30-133">**LB\_FINDSTRINGEXACT**</span></span>](lb-findstringexact.md)
</dt> </dl>

 

 





