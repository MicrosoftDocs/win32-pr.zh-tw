---
title: 'TVM_GETVISIBLECOUNT 訊息 (Commctrl .h) '
description: 取得可在樹狀檢視控制項的用戶端視窗中完整顯示的專案數。 您可以使用 TreeView GetVisibleCount 宏明確地傳送此訊息 \_ 。
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934087"
---
# <a name="tvm_getvisiblecount-message"></a><span data-ttu-id="b8ab2-105">TVM \_ GETVISIBLECOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="b8ab2-105">TVM\_GETVISIBLECOUNT message</span></span>

<span data-ttu-id="b8ab2-106">取得可在樹狀檢視控制項的用戶端視窗中完整顯示的專案數。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-106">Obtains the number of items that can be fully visible in the client window of a tree-view control.</span></span> <span data-ttu-id="b8ab2-107">您可以使用 [**TreeView \_ GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-107">You can send this message explicitly or by using the [**TreeView\_GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8ab2-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8ab2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ab2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8ab2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b8ab2-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b8ab2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8ab2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b8ab2-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8ab2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8ab2-113">Return value</span></span>

<span data-ttu-id="b8ab2-114">傳回樹狀檢視控制項的用戶端視窗中可完全顯示的專案數。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-114">Returns the number of items that can be fully visible in the client window of the tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ab2-115">備註</span><span class="sxs-lookup"><span data-stu-id="b8ab2-115">Remarks</span></span>

<span data-ttu-id="b8ab2-116">可以完全可見的專案數可能會大於控制項中的專案數。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-116">The number of items that can be fully visible may be greater than the number of items in the control.</span></span> <span data-ttu-id="b8ab2-117">控制項會將用戶端視窗的高度除以專案的高度，以計算此值。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-117">The control calculates this value by dividing the height of the client window by the height of an item.</span></span>

<span data-ttu-id="b8ab2-118">請注意，傳回值是可 *完全* 可見的專案數。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-118">Note that the return value is the number of items that can be *fully* visible.</span></span> <span data-ttu-id="b8ab2-119">如果您可以看到所有的20個專案和一個以上的專案，則傳回值為20。</span><span class="sxs-lookup"><span data-stu-id="b8ab2-119">If you can see all of 20 items and part of one more item, the return value is 20.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ab2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8ab2-120">Requirements</span></span>



| <span data-ttu-id="b8ab2-121">需求</span><span class="sxs-lookup"><span data-stu-id="b8ab2-121">Requirement</span></span> | <span data-ttu-id="b8ab2-122">值</span><span class="sxs-lookup"><span data-stu-id="b8ab2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ab2-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8ab2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ab2-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8ab2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8ab2-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8ab2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ab2-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8ab2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8ab2-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b8ab2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ab2-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ab2-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





