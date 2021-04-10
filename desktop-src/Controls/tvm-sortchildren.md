---
title: 'TVM_SORTCHILDREN 訊息 (Commctrl .h) '
description: 排序樹狀檢視控制項中所指定父專案的子專案。 您可以使用 TreeView SortChildren 宏明確地傳送此訊息 \_ 。
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025429"
---
# <a name="tvm_sortchildren-message"></a><span data-ttu-id="1d226-105">TVM \_ SORTCHILDREN 訊息</span><span class="sxs-lookup"><span data-stu-id="1d226-105">TVM\_SORTCHILDREN message</span></span>

<span data-ttu-id="1d226-106">排序樹狀檢視控制項中所指定父專案的子專案。</span><span class="sxs-lookup"><span data-stu-id="1d226-106">Sorts the child items of the specified parent item in a tree-view control.</span></span> <span data-ttu-id="1d226-107">您可以使用 [**TreeView \_ SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1d226-107">You can send this message explicitly or by using the [**TreeView\_SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d226-108">參數</span><span class="sxs-lookup"><span data-stu-id="1d226-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d226-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d226-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d226-110">值，指定排序是否為遞迴。</span><span class="sxs-lookup"><span data-stu-id="1d226-110">Value that specifies whether the sorting is recursive.</span></span> <span data-ttu-id="1d226-111">將 *wParam* 設為 **TRUE** ，以排序父專案底下的所有子專案層級。</span><span class="sxs-lookup"><span data-stu-id="1d226-111">Set *wParam* to **TRUE** to sort all levels of child items below the parent item.</span></span> <span data-ttu-id="1d226-112">否則，只會排序父系的直屬子系。</span><span class="sxs-lookup"><span data-stu-id="1d226-112">Otherwise, only the parent's immediate children are sorted.</span></span>

</dd> <dt>

<span data-ttu-id="1d226-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d226-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d226-114">要排序其子專案的父專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1d226-114">Handle to the parent item whose child items are to be sorted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d226-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d226-115">Return value</span></span>

<span data-ttu-id="1d226-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1d226-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d226-117">備註</span><span class="sxs-lookup"><span data-stu-id="1d226-117">Remarks</span></span>

<span data-ttu-id="1d226-118">此訊息會在專案名稱上使用 [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) Alphabetizes 樹狀目錄專案。</span><span class="sxs-lookup"><span data-stu-id="1d226-118">This message alphabetizes the tree items using [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) on the item name.</span></span> <span data-ttu-id="1d226-119">您可以使用 [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) 訊息來自訂排序行為。</span><span class="sxs-lookup"><span data-stu-id="1d226-119">You can use the [**TVM\_SORTCHILDRENCB**](tvm-sortchildrencb.md) message to customize the ordering behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d226-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d226-120">Requirements</span></span>



| <span data-ttu-id="1d226-121">需求</span><span class="sxs-lookup"><span data-stu-id="1d226-121">Requirement</span></span> | <span data-ttu-id="1d226-122">值</span><span class="sxs-lookup"><span data-stu-id="1d226-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d226-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d226-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1d226-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d226-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d226-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d226-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1d226-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d226-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d226-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1d226-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d226-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d226-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

