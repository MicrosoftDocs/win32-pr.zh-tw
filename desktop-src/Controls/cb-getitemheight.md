---
title: 'CB_GETITEMHEIGHT 訊息 (Winuser .h) '
description: 決定下拉式方塊中清單專案的高度或選取欄位。
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843572"
---
# <a name="cb_getitemheight-message"></a><span data-ttu-id="5dab7-104">CB \_ GETITEMHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="5dab7-104">CB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="5dab7-105">決定下拉式方塊中清單專案的高度或選取欄位。</span><span class="sxs-lookup"><span data-stu-id="5dab7-105">Determines the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5dab7-106">參數</span><span class="sxs-lookup"><span data-stu-id="5dab7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dab7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dab7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dab7-108">要取出其高度的下拉式方塊元件。</span><span class="sxs-lookup"><span data-stu-id="5dab7-108">The combo box component whose height is to be retrieved.</span></span> <span data-ttu-id="5dab7-109">此參數必須是-1，才能取得選取範圍欄位的高度。</span><span class="sxs-lookup"><span data-stu-id="5dab7-109">This parameter must be -1 to retrieve the height of the selection field.</span></span> <span data-ttu-id="5dab7-110">除非下拉式方塊具有 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式，否則它必須為零才能取出清單專案的高度。</span><span class="sxs-lookup"><span data-stu-id="5dab7-110">It must be zero to retrieve the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="5dab7-111">在此情況下， *wParam* 參數是特定清單專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="5dab7-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="5dab7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5dab7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dab7-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="5dab7-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dab7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5dab7-114">Return value</span></span>

<span data-ttu-id="5dab7-115">傳回值是下拉式方塊中清單專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5dab7-115">The return value is the height, in pixels, of the list items in a combo box.</span></span> <span data-ttu-id="5dab7-116">如果下拉式方塊具有 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式，它就是 *wParam* 參數所指定之專案的高度。</span><span class="sxs-lookup"><span data-stu-id="5dab7-116">If the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, it is the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="5dab7-117">如果 *wParam* 為-1，則傳回值是 (的編輯控制項高度或下拉式方塊的靜態文字) 部分。</span><span class="sxs-lookup"><span data-stu-id="5dab7-117">If *wParam* is -1, the return value is the height of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="5dab7-118">如果發生錯誤，傳回值會是 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="5dab7-118">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dab7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dab7-119">Requirements</span></span>



| <span data-ttu-id="5dab7-120">需求</span><span class="sxs-lookup"><span data-stu-id="5dab7-120">Requirement</span></span> | <span data-ttu-id="5dab7-121">值</span><span class="sxs-lookup"><span data-stu-id="5dab7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dab7-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5dab7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5dab7-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dab7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5dab7-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5dab7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5dab7-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dab7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5dab7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="5dab7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dab7-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5dab7-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dab7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dab7-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5dab7-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="5dab7-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5dab7-130">**CB \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="5dab7-130">**CB\_SETITEMHEIGHT**</span></span>](cb-setitemheight.md)
</dt> <dt>

[<span data-ttu-id="5dab7-131">**WM \_ MEASUREITEM**</span><span class="sxs-lookup"><span data-stu-id="5dab7-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





