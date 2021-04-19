---
title: 'CB_SETITEMHEIGHT 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETITEMHEIGHT 訊息，在下拉式方塊中設定清單專案的高度或選擇欄位。
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967756"
---
# <a name="cb_setitemheight-message"></a><span data-ttu-id="9b46d-104">CB \_ SETITEMHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="9b46d-104">CB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="9b46d-105">應用程式會傳送 **CB \_ SETITEMHEIGHT** 訊息，在下拉式方塊中設定清單專案的高度或選擇欄位。</span><span class="sxs-lookup"><span data-stu-id="9b46d-105">An application sends a **CB\_SETITEMHEIGHT** message to set the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b46d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b46d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b46d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b46d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b46d-108">指定要為其設定高度之下拉式方塊的元件。</span><span class="sxs-lookup"><span data-stu-id="9b46d-108">Specifies the component of the combo box for which to set the height.</span></span>

<span data-ttu-id="9b46d-109">此參數必須為1，才能設定選取範圍欄位的高度。</span><span class="sxs-lookup"><span data-stu-id="9b46d-109">This parameter must be  1 to set the height of the selection field.</span></span> <span data-ttu-id="9b46d-110">除非下拉式方塊具有 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式，否則它必須為零以設定清單專案的高度。</span><span class="sxs-lookup"><span data-stu-id="9b46d-110">It must be zero to set the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="9b46d-111">在此情況下， *wParam* 參數是特定清單專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="9b46d-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="9b46d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b46d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b46d-113">指定 *wParam* 所識別之下拉式方塊元件的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9b46d-113">Specifies the height, in pixels, of the combo box component identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b46d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b46d-114">Return value</span></span>

<span data-ttu-id="9b46d-115">如果索引或高度無效，則傳回值為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="9b46d-115">If the index or height is invalid, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b46d-116">備註</span><span class="sxs-lookup"><span data-stu-id="9b46d-116">Remarks</span></span>

<span data-ttu-id="9b46d-117">下拉式方塊中的選取欄位高度會與清單專案的高度分開設定。</span><span class="sxs-lookup"><span data-stu-id="9b46d-117">The selection field height in a combo box is set independently of the height of the list items.</span></span> <span data-ttu-id="9b46d-118">應用程式必須確保選取欄位的高度不會小於特定清單專案的高度。</span><span class="sxs-lookup"><span data-stu-id="9b46d-118">An application must ensure that the height of the selection field is not smaller than the height of a particular list item.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b46d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b46d-119">Requirements</span></span>



| <span data-ttu-id="9b46d-120">需求</span><span class="sxs-lookup"><span data-stu-id="9b46d-120">Requirement</span></span> | <span data-ttu-id="9b46d-121">值</span><span class="sxs-lookup"><span data-stu-id="9b46d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b46d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b46d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9b46d-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b46d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9b46d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b46d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9b46d-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b46d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b46d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9b46d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b46d-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9b46d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b46d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b46d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b46d-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="9b46d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9b46d-130">**CB \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="9b46d-130">**CB\_GETITEMHEIGHT**</span></span>](cb-getitemheight.md)
</dt> <dt>

[<span data-ttu-id="9b46d-131">**WM \_ MEASUREITEM**</span><span class="sxs-lookup"><span data-stu-id="9b46d-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





