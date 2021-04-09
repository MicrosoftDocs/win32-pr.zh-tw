---
title: 'TVM_SETINSERTMARK 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項中的插入標記。 您可以使用 TreeView SetInsertMark 宏明確地傳送此訊息 \_ 。
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- TVM_SETINSERTMARK message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843780"
---
# <a name="tvm_setinsertmark-message"></a><span data-ttu-id="dd251-105">TVM \_ SETINSERTMARK 訊息</span><span class="sxs-lookup"><span data-stu-id="dd251-105">TVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="dd251-106">設定樹狀檢視控制項中的插入標記。</span><span class="sxs-lookup"><span data-stu-id="dd251-106">Sets the insertion mark in a tree-view control.</span></span> <span data-ttu-id="dd251-107">您可以使用 [**TreeView \_ SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="dd251-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd251-108">參數</span><span class="sxs-lookup"><span data-stu-id="dd251-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd251-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd251-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd251-110">**布林** 值，指定插入標記是放置在指定的專案之前或之後。</span><span class="sxs-lookup"><span data-stu-id="dd251-110">**BOOL** value that specifies if the insertion mark is placed before or after the specified item.</span></span> <span data-ttu-id="dd251-111">如果這個引數不是零，則插入標記將放置在專案之後。</span><span class="sxs-lookup"><span data-stu-id="dd251-111">If this argument is nonzero, the insertion mark will be placed after the item.</span></span> <span data-ttu-id="dd251-112">如果這個引數為零，則會在專案之前放置插入標記。</span><span class="sxs-lookup"><span data-stu-id="dd251-112">If this argument is zero, the insertion mark will be placed before the item.</span></span>

</dd> <dt>

<span data-ttu-id="dd251-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd251-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd251-114">**HTREEITEM** ，指定將放置插入標記的專案。</span><span class="sxs-lookup"><span data-stu-id="dd251-114">**HTREEITEM** that specifies at which item the insertion mark will be placed.</span></span> <span data-ttu-id="dd251-115">如果這個引數為 **Null**，則會移除插入標記。</span><span class="sxs-lookup"><span data-stu-id="dd251-115">If this argument is **NULL**, the insertion mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd251-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd251-116">Return value</span></span>

<span data-ttu-id="dd251-117">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="dd251-117">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd251-118">備註</span><span class="sxs-lookup"><span data-stu-id="dd251-118">Remarks</span></span>

<span data-ttu-id="dd251-119">在某些情況下，插入標記可以出現在節點展開之後的兩個位置中。</span><span class="sxs-lookup"><span data-stu-id="dd251-119">In some circumstances, the insert mark can appear in two places after a node is expanded.</span></span> <span data-ttu-id="dd251-120">如果您使用插入標記，建議您在展開節點之後強制重新整理控制項。</span><span class="sxs-lookup"><span data-stu-id="dd251-120">If you are using insertion marks, it is recommended that you force a refresh of the control after expanding a node.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd251-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd251-121">Requirements</span></span>



| <span data-ttu-id="dd251-122">需求</span><span class="sxs-lookup"><span data-stu-id="dd251-122">Requirement</span></span> | <span data-ttu-id="dd251-123">值</span><span class="sxs-lookup"><span data-stu-id="dd251-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd251-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd251-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dd251-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd251-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd251-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd251-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dd251-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd251-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd251-128">標頭</span><span class="sxs-lookup"><span data-stu-id="dd251-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd251-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd251-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





