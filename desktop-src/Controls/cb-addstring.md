---
title: 'CB_ADDSTRING 訊息 (Winuser .h) '
description: 將字串加入下拉式方塊的清單方塊中。 如果下拉式方塊沒有 CBS \_ 排序樣式，則會將字串加入至清單結尾。 否則，會將字串插入清單中，並排序清單。
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- CB_ADDSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934917"
---
# <a name="cb_addstring-message"></a><span data-ttu-id="3c0a6-106">CB \_ ADDSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="3c0a6-106">CB\_ADDSTRING message</span></span>

<span data-ttu-id="3c0a6-107">將字串加入下拉式方塊的清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-107">Adds a string to the list box of a combo box.</span></span> <span data-ttu-id="3c0a6-108">如果下拉式方塊沒有 [**CBS \_ 排序**](combo-box-styles.md) 樣式，則會將字串加入至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-108">If the combo box does not have the [**CBS\_SORT**](combo-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="3c0a6-109">否則，會將字串插入清單中，並排序清單。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-109">Otherwise, the string is inserted into the list, and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c0a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="3c0a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c0a6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c0a6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c0a6-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c0a6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c0a6-114">要加入之以 null 終止之字串的 **LPCTSTR** 指標。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-114">An **LPCTSTR** pointer to the null-terminated string to be added.</span></span> <span data-ttu-id="3c0a6-115">如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則 *lParam* 參數的值會儲存為專案資料，而不是另一個指向的字串。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored as item data rather than the string it would otherwise point to.</span></span> <span data-ttu-id="3c0a6-116">您可以藉由傳送 [**CB \_ GETITEMDATA**](cb-getitemdata.md) 或 [**cb \_ SETITEMDATA**](cb-setitemdata.md) 訊息來取出或修改專案資料。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-116">The item data can be retrieved or modified by sending the [**CB\_GETITEMDATA**](cb-getitemdata.md) or [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c0a6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c0a6-117">Return value</span></span>

<span data-ttu-id="3c0a6-118">傳回值是下拉式方塊清單方塊中字串的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-118">The return value is the zero-based index to the string in the list box of the combo box.</span></span> <span data-ttu-id="3c0a6-119">如果發生錯誤，傳回值會是 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-119">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="3c0a6-120">如果空間不足，無法存放新的字串，它就是 CB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-120">If insufficient space is available to store the new string, it is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c0a6-121">備註</span><span class="sxs-lookup"><span data-stu-id="3c0a6-121">Remarks</span></span>

<span data-ttu-id="3c0a6-122">如果您建立具有 [**cbs \_ 排序**](combo-box-styles.md) 樣式但沒有 [**cbs \_ HASSTRINGS**](combo-box-styles.md) 樣式的主控描繪下拉式列示方塊，則會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送一或多次至下拉式方塊的擁有者，以便將新專案正確地放在清單中。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-122">If you create an owner-drawn combo box with the [**CBS\_SORT**](combo-box-styles.md) style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the [**WM\_COMPAREITEM**](wm-compareitem.md) message is sent one or more times to the owner of the combo box so the new item can be properly placed in the list.</span></span>

<span data-ttu-id="3c0a6-123">若要將字串插入清單中的特定位置，請使用 [**CB \_ INSERTSTRING**](cb-insertstring.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-123">To insert a string at a specific location within the list, use the [**CB\_INSERTSTRING**](cb-insertstring.md) message.</span></span>

<span data-ttu-id="3c0a6-124">如果下拉式方塊具有 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式，而且您新增的字串範圍超過下拉式方塊，請傳送 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息，以確保會顯示水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-124">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the combo box, send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="3c0a6-125">**Comclt32.dll 5.0 版或更新版本：** 如果設定了 [ [**cbs \_ 小寫**](combo-box-styles.md) ] 或 [ [**cbs \_ 大寫**](combo-box-styles.md) ]，則 Unicode 版本的 **CB \_ ADDSTRING** 會改變字串。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-125">**Comclt32.dll version 5.0 or later:** If [**CBS\_LOWERCASE**](combo-box-styles.md) or [**CBS\_UPPERCASE**](combo-box-styles.md) is set, the Unicode version of **CB\_ADDSTRING** alters the string.</span></span> <span data-ttu-id="3c0a6-126">如果使用唯讀的全域記憶體，這會導致應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="3c0a6-126">If using read-only global memory, this causes the application to fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0a6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c0a6-127">Requirements</span></span>



| <span data-ttu-id="3c0a6-128">需求</span><span class="sxs-lookup"><span data-stu-id="3c0a6-128">Requirement</span></span> | <span data-ttu-id="3c0a6-129">值</span><span class="sxs-lookup"><span data-stu-id="3c0a6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0a6-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c0a6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0a6-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c0a6-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c0a6-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c0a6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0a6-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c0a6-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c0a6-134">標頭</span><span class="sxs-lookup"><span data-stu-id="3c0a6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c0a6-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3c0a6-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c0a6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c0a6-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c0a6-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="3c0a6-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c0a6-138">**CB \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="3c0a6-138">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="3c0a6-139">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="3c0a6-139">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="3c0a6-140">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="3c0a6-140">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="3c0a6-141">**WM \_ COMPAREITEM**</span><span class="sxs-lookup"><span data-stu-id="3c0a6-141">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

