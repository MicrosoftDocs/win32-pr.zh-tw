---
title: 'TVM_SETINDENT 訊息 (Commctrl .h) '
description: 為樹狀檢視控制項設定縮排的寬度，並重新繪製控制項以反映新的寬度。 您可以使用 TreeView SetIndent 宏明確地傳送此訊息 \_ 。
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104178"
---
# <a name="tvm_setindent-message"></a><span data-ttu-id="4df11-105">TVM \_ SETINDENT 訊息</span><span class="sxs-lookup"><span data-stu-id="4df11-105">TVM\_SETINDENT message</span></span>

<span data-ttu-id="4df11-106">為樹狀檢視控制項設定縮排的寬度，並重新繪製控制項以反映新的寬度。</span><span class="sxs-lookup"><span data-stu-id="4df11-106">Sets the width of indentation for a tree-view control and redraws the control to reflect the new width.</span></span> <span data-ttu-id="4df11-107">您可以使用 [**TreeView \_ SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4df11-107">You can send this message explicitly or by using the [**TreeView\_SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4df11-108">參數</span><span class="sxs-lookup"><span data-stu-id="4df11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df11-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4df11-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4df11-110">縮排的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4df11-110">Width, in pixels, of the indentation.</span></span> <span data-ttu-id="4df11-111">如果這個參數小於系統定義的最小寬度，則新寬度會設定為系統定義的最小值。</span><span class="sxs-lookup"><span data-stu-id="4df11-111">If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum.</span></span>

</dd> <dt>

<span data-ttu-id="4df11-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4df11-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4df11-113">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4df11-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df11-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4df11-114">Return value</span></span>

<span data-ttu-id="4df11-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="4df11-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4df11-116">備註</span><span class="sxs-lookup"><span data-stu-id="4df11-116">Remarks</span></span>

<span data-ttu-id="4df11-117">系統定義的最小縮排值通常是五個圖元，但不是固定的。</span><span class="sxs-lookup"><span data-stu-id="4df11-117">The system-defined minimum indent value is typically five pixels, but it is not fixed.</span></span> <span data-ttu-id="4df11-118">若要在特定系統上取得最小縮排的確切值，請傳送 **TVM \_ SETINDENT** 訊息，其中 *wParam* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="4df11-118">To retrieve the exact value of the minimum indent on a particular system, send a **TVM\_SETINDENT** message with *wParam* set to zero.</span></span> <span data-ttu-id="4df11-119">然後傳送 [**TVM \_ setindent**](tvm-getindent.md) 訊息來取得最小縮排值。</span><span class="sxs-lookup"><span data-stu-id="4df11-119">Then send a [**TVM\_GETINDENT**](tvm-getindent.md) message to retrieve the minimum indent value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df11-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4df11-120">Requirements</span></span>



| <span data-ttu-id="4df11-121">需求</span><span class="sxs-lookup"><span data-stu-id="4df11-121">Requirement</span></span> | <span data-ttu-id="4df11-122">值</span><span class="sxs-lookup"><span data-stu-id="4df11-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4df11-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4df11-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4df11-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4df11-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4df11-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4df11-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4df11-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4df11-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4df11-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4df11-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df11-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4df11-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df11-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4df11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df11-130">**TreeView \_ SetIndent**</span><span class="sxs-lookup"><span data-stu-id="4df11-130">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





