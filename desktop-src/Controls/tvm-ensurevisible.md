---
title: 'TVM_ENSUREVISIBLE 訊息 (Commctrl .h) '
description: 確定樹狀檢視專案可見、展開父專案或滾動樹狀檢視控制項（如有必要）。 您可以使用 TreeView EnsureVisible 宏明確地傳送此訊息 \_ 。
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934189"
---
# <a name="tvm_ensurevisible-message"></a><span data-ttu-id="3ba42-105">TVM \_ ENSUREVISIBLE 訊息</span><span class="sxs-lookup"><span data-stu-id="3ba42-105">TVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="3ba42-106">確定樹狀檢視專案可見、展開父專案或滾動樹狀檢視控制項（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="3ba42-106">Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary.</span></span> <span data-ttu-id="3ba42-107">您可以使用 [**TreeView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3ba42-107">You can send this message explicitly or by using the [**TreeView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ba42-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ba42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba42-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ba42-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3ba42-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3ba42-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3ba42-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ba42-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ba42-112">專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ba42-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ba42-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ba42-113">Return value</span></span>

<span data-ttu-id="3ba42-114">如果系統滾動樹狀檢視控制項中的專案，但未展開任何專案，則傳回非零。</span><span class="sxs-lookup"><span data-stu-id="3ba42-114">Returns nonzero if the system scrolled the items in the tree-view control and no items were expanded.</span></span> <span data-ttu-id="3ba42-115">否則，訊息會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3ba42-115">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba42-116">備註</span><span class="sxs-lookup"><span data-stu-id="3ba42-116">Remarks</span></span>

<span data-ttu-id="3ba42-117">如果 TVM \_ ENSUREVISIBLE 訊息展開父項目，父視窗會接收 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="3ba42-117">If the TVM\_ENSUREVISIBLE message expands the parent item, the parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba42-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ba42-118">Requirements</span></span>



| <span data-ttu-id="3ba42-119">需求</span><span class="sxs-lookup"><span data-stu-id="3ba42-119">Requirement</span></span> | <span data-ttu-id="3ba42-120">值</span><span class="sxs-lookup"><span data-stu-id="3ba42-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba42-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ba42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba42-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ba42-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ba42-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ba42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba42-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ba42-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ba42-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3ba42-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ba42-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba42-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





