---
title: 'TVM_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項的子工具提示控制項。 您可以使用 TreeView SetToolTips 宏明確地傳送此訊息 \_ 。
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094572"
---
# <a name="tvm_settooltips-message"></a><span data-ttu-id="83ecb-105">TVM \_ SETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="83ecb-105">TVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="83ecb-106">設定樹狀檢視控制項的子工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="83ecb-106">Sets a tree-view control's child tooltip control.</span></span> <span data-ttu-id="83ecb-107">您可以使用 [**TreeView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="83ecb-107">You can send this message explicitly or by using the [**TreeView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="83ecb-108">參數</span><span class="sxs-lookup"><span data-stu-id="83ecb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83ecb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83ecb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83ecb-110">工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="83ecb-110">Handle to a tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="83ecb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83ecb-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="83ecb-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="83ecb-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83ecb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="83ecb-113">Return value</span></span>

<span data-ttu-id="83ecb-114">傳回先前針對樹狀檢視控制項設定之工具提示控制項的控制碼，如果先前未使用工具提示，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="83ecb-114">Returns the handle to tooltip control previously set for the tree-view control, or **NULL** if tooltips were not previously used.</span></span>

## <a name="remarks"></a><span data-ttu-id="83ecb-115">備註</span><span class="sxs-lookup"><span data-stu-id="83ecb-115">Remarks</span></span>

<span data-ttu-id="83ecb-116">建立時，樹狀檢視控制項會自動建立子工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="83ecb-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="83ecb-117">若要防止樹狀檢視控制項使用工具提示，請使用 [**tv \_ NOTOOLTIPS**](tree-view-control-window-styles.md) 樣式建立控制項。</span><span class="sxs-lookup"><span data-stu-id="83ecb-117">To prevent a tree-view control from using tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="83ecb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="83ecb-118">Requirements</span></span>



| <span data-ttu-id="83ecb-119">需求</span><span class="sxs-lookup"><span data-stu-id="83ecb-119">Requirement</span></span> | <span data-ttu-id="83ecb-120">值</span><span class="sxs-lookup"><span data-stu-id="83ecb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83ecb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83ecb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="83ecb-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83ecb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83ecb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83ecb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="83ecb-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83ecb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83ecb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="83ecb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="83ecb-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="83ecb-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83ecb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83ecb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ecb-128">**TVM \_ GETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="83ecb-128">**TVM\_GETTOOLTIPS**</span></span>](tvm-gettooltips.md)
</dt> </dl>

 

 





