---
title: 'TVM_GETITEMSTATE 訊息 (Commctrl .h) '
description: 抓取部分或所有樹狀檢視專案的狀態屬性。 您可以使用 TreeView GetItemState 宏明確地傳送此訊息 \_ 。
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025276"
---
# <a name="tvm_getitemstate-message"></a><span data-ttu-id="49b21-105">TVM \_ GETITEMSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="49b21-105">TVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="49b21-106">抓取部分或所有樹狀檢視專案的狀態屬性。</span><span class="sxs-lookup"><span data-stu-id="49b21-106">Retrieves some or all of a tree-view item's state attributes.</span></span> <span data-ttu-id="49b21-107">您可以使用 [**TreeView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="49b21-107">You can send this message explicitly or by using the [**TreeView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="49b21-108">參數</span><span class="sxs-lookup"><span data-stu-id="49b21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49b21-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49b21-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49b21-110">專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="49b21-110">Handle to the item.</span></span>

</dd> <dt>

<span data-ttu-id="49b21-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49b21-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49b21-112">用來指定要查詢之狀態的遮罩。</span><span class="sxs-lookup"><span data-stu-id="49b21-112">Mask used to specify the states to query for.</span></span> <span data-ttu-id="49b21-113">它相當於 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)的 **stateMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="49b21-113">It is equivalent to the **stateMask** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49b21-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="49b21-114">Return value</span></span>

<span data-ttu-id="49b21-115">傳回將適當的狀態位設為 **TRUE** 的 **UINT** 值。</span><span class="sxs-lookup"><span data-stu-id="49b21-115">Returns a **UINT** value with the appropriate state bits set to **TRUE**.</span></span> <span data-ttu-id="49b21-116">只有 *lParam* 指定且為 **TRUE** 的位會進行設定。</span><span class="sxs-lookup"><span data-stu-id="49b21-116">Only those bits that are specified by *lParam* and that are **TRUE** will be set.</span></span> <span data-ttu-id="49b21-117">此值相當於 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)的 **狀態** 成員。</span><span class="sxs-lookup"><span data-stu-id="49b21-117">This value is equivalent to the **state** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="49b21-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="49b21-118">Requirements</span></span>



| <span data-ttu-id="49b21-119">需求</span><span class="sxs-lookup"><span data-stu-id="49b21-119">Requirement</span></span> | <span data-ttu-id="49b21-120">值</span><span class="sxs-lookup"><span data-stu-id="49b21-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49b21-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49b21-121">Minimum supported client</span></span><br/> | <span data-ttu-id="49b21-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49b21-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49b21-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49b21-123">Minimum supported server</span></span><br/> | <span data-ttu-id="49b21-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49b21-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49b21-125">標頭</span><span class="sxs-lookup"><span data-stu-id="49b21-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="49b21-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="49b21-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





