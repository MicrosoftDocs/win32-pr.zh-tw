---
title: 'CB_INSERTSTRING 訊息 (Winuser .h) '
description: 將字串或專案資料插入下拉式方塊的清單中。 與 CB ADDSTRING 訊息不同的是 \_ ，cb \_ INSERTSTRING 訊息並不會讓您排序包含 CBS \_ 排序樣式的清單。
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465264"
---
# <a name="cb_insertstring-message"></a><span data-ttu-id="7f8fc-105">CB \_ INSERTSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="7f8fc-105">CB\_INSERTSTRING message</span></span>

<span data-ttu-id="7f8fc-106">將字串或專案資料插入下拉式方塊的清單中。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-106">Inserts a string or item data into the list of a combo box.</span></span> <span data-ttu-id="7f8fc-107">與 [**cb \_ ADDSTRING**](cb-addstring.md) 訊息不同的是， **cb \_ INSERTSTRING** 訊息並不會讓您排序包含 [**CBS \_ 排序**](combo-box-styles.md) 樣式的清單。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-107">Unlike the [**CB\_ADDSTRING**](cb-addstring.md) message, the **CB\_INSERTSTRING** message does not cause a list with the [**CBS\_SORT**](combo-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f8fc-108">參數</span><span class="sxs-lookup"><span data-stu-id="7f8fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f8fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f8fc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f8fc-110">以零為基底的索引，這是插入字串的位置。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="7f8fc-111">如果此參數為-1，則會將字串加入至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="7f8fc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f8fc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f8fc-113">要插入之以 null 終止之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="7f8fc-114">如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則會儲存 *lParam* 參數的值，而不是它所指向的字串。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored rather than the string to which it would otherwise point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f8fc-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f8fc-115">Return value</span></span>

<span data-ttu-id="7f8fc-116">傳回值是插入字串之位置的索引。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-116">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="7f8fc-117">如果發生錯誤，傳回值會是 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-117">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="7f8fc-118">如果沒有足夠的可用空間來儲存新的字串，則它是 CB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-118">If there is insufficient space available to store the new string, it is CB\_ERRSPACE.</span></span>

<span data-ttu-id="7f8fc-119">如果下拉式方塊具有 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式，而且您插入的字串範圍超過下拉式方塊，您應該傳送 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息，以確保會顯示水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-119">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the combo box, you should send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8fc-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f8fc-120">Requirements</span></span>



| <span data-ttu-id="7f8fc-121">需求</span><span class="sxs-lookup"><span data-stu-id="7f8fc-121">Requirement</span></span> | <span data-ttu-id="7f8fc-122">值</span><span class="sxs-lookup"><span data-stu-id="7f8fc-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8fc-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f8fc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7f8fc-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f8fc-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7f8fc-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f8fc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7f8fc-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f8fc-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f8fc-127">標頭</span><span class="sxs-lookup"><span data-stu-id="7f8fc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f8fc-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7f8fc-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f8fc-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f8fc-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7f8fc-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="7f8fc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7f8fc-131">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="7f8fc-131">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="7f8fc-132">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="7f8fc-132">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="7f8fc-133">**CB \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="7f8fc-133">**CB\_DIR**</span></span>](cb-dir.md)
</dt> </dl>

 

