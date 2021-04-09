---
title: 'CB_DELETESTRING 訊息 (Winuser .h) '
description: 刪除下拉式方塊的清單方塊中的字串。
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING message Windows 控制項
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106002"
---
# <a name="cb_deletestring-message"></a><span data-ttu-id="b4d06-104">CB \_ DELETESTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="b4d06-104">CB\_DELETESTRING message</span></span>

<span data-ttu-id="b4d06-105">刪除下拉式方塊的清單方塊中的字串。</span><span class="sxs-lookup"><span data-stu-id="b4d06-105">Deletes a string in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4d06-106">參數</span><span class="sxs-lookup"><span data-stu-id="b4d06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4d06-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4d06-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4d06-108">要刪除之字串的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="b4d06-108">The zero-based index of the string to delete.</span></span>

</dd> <dt>

<span data-ttu-id="b4d06-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4d06-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4d06-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b4d06-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4d06-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4d06-111">Return value</span></span>

<span data-ttu-id="b4d06-112">傳回值是清單中剩餘字串的計數。</span><span class="sxs-lookup"><span data-stu-id="b4d06-112">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="b4d06-113">如果 *wParam* 參數指定的索引大於清單中的專案數，則傳回值為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="b4d06-113">If the *wParam* parameter specifies an index greater than the number of items in the list, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4d06-114">備註</span><span class="sxs-lookup"><span data-stu-id="b4d06-114">Remarks</span></span>

<span data-ttu-id="b4d06-115">如果您建立具有主控描繪樣式但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式的下拉式方塊，系統會將 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息傳送給下拉式方塊的擁有者，讓應用程式可以釋出與該專案相關聯的任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="b4d06-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the combo box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d06-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4d06-116">Requirements</span></span>



| <span data-ttu-id="b4d06-117">需求</span><span class="sxs-lookup"><span data-stu-id="b4d06-117">Requirement</span></span> | <span data-ttu-id="b4d06-118">值</span><span class="sxs-lookup"><span data-stu-id="b4d06-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4d06-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4d06-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d06-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4d06-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4d06-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4d06-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d06-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4d06-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4d06-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b4d06-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4d06-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b4d06-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4d06-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4d06-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b4d06-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="b4d06-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b4d06-127">**CB \_ RESETCONTENT**</span><span class="sxs-lookup"><span data-stu-id="b4d06-127">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="b4d06-128">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="b4d06-128">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





