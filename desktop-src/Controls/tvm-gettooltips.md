---
title: 'TVM_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項所使用之子工具提示控制項的控制碼。 您可以使用 TreeView GetToolTips 宏明確地傳送此訊息 \_ 。
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- TVM_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464761"
---
# <a name="tvm_gettooltips-message"></a><span data-ttu-id="61e53-105">TVM \_ GETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="61e53-105">TVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="61e53-106">抓取樹狀檢視控制項所使用之子工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="61e53-106">Retrieves the handle to the child tooltip control used by a tree-view control.</span></span> <span data-ttu-id="61e53-107">您可以使用 [**TreeView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="61e53-107">You can send this message explicitly or by using the [**TreeView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61e53-108">參數</span><span class="sxs-lookup"><span data-stu-id="61e53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e53-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61e53-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="61e53-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="61e53-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="61e53-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61e53-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="61e53-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="61e53-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61e53-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="61e53-113">Return value</span></span>

<span data-ttu-id="61e53-114">傳回子工具提示控制項的控制碼，如果控制項不使用工具提示，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="61e53-114">Returns the handle to the child tooltip control, or **NULL** if the control is not using tooltips.</span></span>

## <a name="remarks"></a><span data-ttu-id="61e53-115">備註</span><span class="sxs-lookup"><span data-stu-id="61e53-115">Remarks</span></span>

<span data-ttu-id="61e53-116">建立時，樹狀檢視控制項會自動建立子工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="61e53-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="61e53-117">若要讓樹狀檢視控制項不使用工具提示，請使用 [**tv \_ NOTOOLTIPS**](tree-view-control-window-styles.md) 樣式建立控制項。</span><span class="sxs-lookup"><span data-stu-id="61e53-117">To cause a tree-view control not to use tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="61e53-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="61e53-118">Requirements</span></span>



| <span data-ttu-id="61e53-119">需求</span><span class="sxs-lookup"><span data-stu-id="61e53-119">Requirement</span></span> | <span data-ttu-id="61e53-120">值</span><span class="sxs-lookup"><span data-stu-id="61e53-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61e53-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61e53-121">Minimum supported client</span></span><br/> | <span data-ttu-id="61e53-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61e53-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61e53-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61e53-123">Minimum supported server</span></span><br/> | <span data-ttu-id="61e53-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61e53-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61e53-125">標頭</span><span class="sxs-lookup"><span data-stu-id="61e53-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="61e53-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="61e53-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61e53-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61e53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e53-128">**TVM \_ SETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="61e53-128">**TVM\_SETTOOLTIPS**</span></span>](tvm-settooltips.md)
</dt> </dl>

 

 





