---
title: 'TVM_GETCOUNT 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項中的專案計數。 您可以使用 TreeView GetCount 宏明確地傳送此訊息 \_ 。
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466484"
---
# <a name="tvm_getcount-message"></a><span data-ttu-id="afb97-105">TVM \_ GETCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="afb97-105">TVM\_GETCOUNT message</span></span>

<span data-ttu-id="afb97-106">抓取樹狀檢視控制項中的專案計數。</span><span class="sxs-lookup"><span data-stu-id="afb97-106">Retrieves a count of the items in a tree-view control.</span></span> <span data-ttu-id="afb97-107">您可以使用 [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="afb97-107">You can send this message explicitly or by using the [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="afb97-108">參數</span><span class="sxs-lookup"><span data-stu-id="afb97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afb97-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afb97-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="afb97-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="afb97-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="afb97-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afb97-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="afb97-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="afb97-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afb97-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="afb97-113">Return value</span></span>

<span data-ttu-id="afb97-114">傳回專案的計數。</span><span class="sxs-lookup"><span data-stu-id="afb97-114">Returns the count of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="afb97-115">備註</span><span class="sxs-lookup"><span data-stu-id="afb97-115">Remarks</span></span>

<span data-ttu-id="afb97-116">[**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)所傳回的節點計數限制為整數值。</span><span class="sxs-lookup"><span data-stu-id="afb97-116">The node count returned by [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) is limited to integer values.</span></span> <span data-ttu-id="afb97-117">如果您新增超過32767的節點，宏會傳回負數值。</span><span class="sxs-lookup"><span data-stu-id="afb97-117">If you add a node beyond 32767 the macro returns a negative value.</span></span> <span data-ttu-id="afb97-118">新增65536節點之後，計數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="afb97-118">After adding 65536 nodes the count returns to zero.</span></span> <span data-ttu-id="afb97-119">發生這種情況時，樹狀檢視控制項會顯示為空白且沒有捲軸。</span><span class="sxs-lookup"><span data-stu-id="afb97-119">When this occurs, the tree-view control appears empty with no scrollbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb97-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="afb97-120">Requirements</span></span>



| <span data-ttu-id="afb97-121">需求</span><span class="sxs-lookup"><span data-stu-id="afb97-121">Requirement</span></span> | <span data-ttu-id="afb97-122">值</span><span class="sxs-lookup"><span data-stu-id="afb97-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afb97-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afb97-123">Minimum supported client</span></span><br/> | <span data-ttu-id="afb97-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afb97-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afb97-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afb97-125">Minimum supported server</span></span><br/> | <span data-ttu-id="afb97-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afb97-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afb97-127">標頭</span><span class="sxs-lookup"><span data-stu-id="afb97-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="afb97-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="afb97-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





