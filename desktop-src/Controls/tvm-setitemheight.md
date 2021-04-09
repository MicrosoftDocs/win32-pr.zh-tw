---
title: 'TVM_SETITEMHEIGHT 訊息 (Commctrl .h) '
description: 設定樹狀檢視專案的高度。 您可以使用 TreeView SetItemHeight 宏明確地傳送此訊息 \_ 。
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934538"
---
# <a name="tvm_setitemheight-message"></a><span data-ttu-id="19ef1-105">TVM \_ SETITEMHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="19ef1-105">TVM\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="19ef1-106">設定樹狀檢視專案的高度。</span><span class="sxs-lookup"><span data-stu-id="19ef1-106">Sets the height of the tree-view items.</span></span> <span data-ttu-id="19ef1-107">您可以使用 [**TreeView \_ SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="19ef1-107">You can send this message explicitly or by using the [**TreeView\_SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="19ef1-108">參數</span><span class="sxs-lookup"><span data-stu-id="19ef1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ef1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19ef1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19ef1-110">樹狀檢視中每個專案的新高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="19ef1-110">New height of every item in the tree view, in pixels.</span></span> <span data-ttu-id="19ef1-111">小於1的高度將設定為1。</span><span class="sxs-lookup"><span data-stu-id="19ef1-111">Heights less than 1 will be set to 1.</span></span> <span data-ttu-id="19ef1-112">如果這個引數不是偶數，而且樹狀檢視控制項沒有 [**tv \_ NONEVENHEIGHT**](tree-view-control-window-styles.md) 樣式，則這個值會向下舍入至最接近的偶數值。</span><span class="sxs-lookup"><span data-stu-id="19ef1-112">If this argument is not even and the tree-view control does not have the [**TVS\_NONEVENHEIGHT**](tree-view-control-window-styles.md) style, this value will be rounded down to the nearest even value.</span></span> <span data-ttu-id="19ef1-113">如果這個引數是-1，控制項將會還原為使用其預設專案高度。</span><span class="sxs-lookup"><span data-stu-id="19ef1-113">If this argument is -1, the control will revert to using its default item height.</span></span>

</dd> <dt>

<span data-ttu-id="19ef1-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19ef1-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="19ef1-115">必須為零。</span><span class="sxs-lookup"><span data-stu-id="19ef1-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ef1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="19ef1-116">Return value</span></span>

<span data-ttu-id="19ef1-117">傳回專案的先前高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="19ef1-117">Returns the previous height of the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="19ef1-118">備註</span><span class="sxs-lookup"><span data-stu-id="19ef1-118">Remarks</span></span>

<span data-ttu-id="19ef1-119">樹狀檢視控制項會使用此值作為所有專案的高度。</span><span class="sxs-lookup"><span data-stu-id="19ef1-119">The tree-view control uses this value for the height of all items.</span></span> <span data-ttu-id="19ef1-120">若要修改個別專案的高度，請參閱 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)結構之 **iIntegral** 成員的描述。</span><span class="sxs-lookup"><span data-stu-id="19ef1-120">To modify the height of individual items, see the description of the **iIntegral** member of the [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ef1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="19ef1-121">Requirements</span></span>



| <span data-ttu-id="19ef1-122">需求</span><span class="sxs-lookup"><span data-stu-id="19ef1-122">Requirement</span></span> | <span data-ttu-id="19ef1-123">值</span><span class="sxs-lookup"><span data-stu-id="19ef1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19ef1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19ef1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19ef1-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19ef1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19ef1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19ef1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19ef1-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19ef1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19ef1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="19ef1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="19ef1-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="19ef1-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ef1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19ef1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ef1-131">**TVM \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="19ef1-131">**TVM\_GETITEMHEIGHT**</span></span>](tvm-getitemheight.md)
</dt> </dl>

 

 





