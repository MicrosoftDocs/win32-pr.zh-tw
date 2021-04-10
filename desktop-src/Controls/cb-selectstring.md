---
title: 'CB_SELECTSTRING 訊息 (Winuser .h) '
description: 在下拉式方塊清單中搜尋以指定字串中的字元開頭的專案。 如果找到相符的專案，就會選取它，並將其複製到編輯控制項。
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025081"
---
# <a name="cb_selectstring-message"></a><span data-ttu-id="f9ec2-105">CB \_ SELECTSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="f9ec2-105">CB\_SELECTSTRING message</span></span>

<span data-ttu-id="f9ec2-106">在下拉式方塊清單中搜尋以指定字串中的字元開頭的專案。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-106">Searches the list of a combo box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="f9ec2-107">如果找到相符的專案，就會選取它，並將其複製到編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-107">If a matching item is found, it is selected and copied to the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9ec2-108">參數</span><span class="sxs-lookup"><span data-stu-id="f9ec2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ec2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9ec2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ec2-110">在要搜尋的第一個專案之前，專案以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-110">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="f9ec2-111">當搜尋到達清單底部時，它會從清單頂端繼續至 *wParam* 參數所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-111">When the search reaches the bottom of the list, it continues from the top of the list back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="f9ec2-112">如果 *wParam* 為-1，就會從一開始就搜尋整個清單。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-112">If *wParam* is -1, the entire list is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="f9ec2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9ec2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ec2-114">以 null 結束的字串指標，其中包含要搜尋的字元。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-114">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="f9ec2-115">搜尋不區分大小寫，因此這個字串可以包含任何大小寫字母的組合。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-115">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9ec2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9ec2-116">Return value</span></span>

<span data-ttu-id="f9ec2-117">如果找到該字串，則傳回值是所選取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-117">If the string is found, the return value is the index of the selected item.</span></span> <span data-ttu-id="f9ec2-118">如果搜尋失敗，則傳回值為 CB ERR， \_ 而且目前的選取範圍不會變更。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-118">If the search is unsuccessful, the return value is CB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ec2-119">備註</span><span class="sxs-lookup"><span data-stu-id="f9ec2-119">Remarks</span></span>

<span data-ttu-id="f9ec2-120">只有當起始點的字元符合前置詞字串中的字元時，才會選取字串。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-120">A string is selected only if the characters from the starting point match the characters in the prefix string.</span></span>

<span data-ttu-id="f9ec2-121">如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則 **CB \_ SELECTSTRING** 訊息的作用取決於您是否使用 [**cbs \_ 排序**](combo-box-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-121">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_SELECTSTRING** message does depends on whether you use the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="f9ec2-122">如果使用了 **CBS \_ 排序** 樣式，系統會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給下拉式方塊的擁有者，以判斷哪一個專案符合指定的字串。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-122">If the **CBS\_SORT** style is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="f9ec2-123">如果您未使用 **CBS \_ 排序** 樣式，則 **CB \_ SELECTSTRING** 會嘗試比對 **DWORD** 值與 *lParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="f9ec2-123">If you do not use the **CBS\_SORT** style, **CB\_SELECTSTRING** attempts to match the **DWORD** value against the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ec2-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9ec2-124">Requirements</span></span>



| <span data-ttu-id="f9ec2-125">需求</span><span class="sxs-lookup"><span data-stu-id="f9ec2-125">Requirement</span></span> | <span data-ttu-id="f9ec2-126">值</span><span class="sxs-lookup"><span data-stu-id="f9ec2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ec2-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9ec2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ec2-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9ec2-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f9ec2-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9ec2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ec2-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9ec2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f9ec2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f9ec2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9ec2-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f9ec2-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9ec2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9ec2-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9ec2-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="f9ec2-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f9ec2-135">**CB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="f9ec2-135">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="f9ec2-136">**CB \_ FINDSTRINGEXACT**</span><span class="sxs-lookup"><span data-stu-id="f9ec2-136">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="f9ec2-137">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="f9ec2-137">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="f9ec2-138">**WM \_ COMPAREITEM**</span><span class="sxs-lookup"><span data-stu-id="f9ec2-138">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





