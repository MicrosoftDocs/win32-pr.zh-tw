---
title: 'TVM_INSERTITEM 訊息 (Commctrl .h) '
description: 在樹狀檢視控制項中插入新專案。 您可以使用 TreeView InsertItem 宏明確地傳送此訊息 \_ 。
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843288"
---
# <a name="tvm_insertitem-message"></a><span data-ttu-id="d63f5-105">TVM \_ INSERTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="d63f5-105">TVM\_INSERTITEM message</span></span>

<span data-ttu-id="d63f5-106">在樹狀檢視控制項中插入新專案。</span><span class="sxs-lookup"><span data-stu-id="d63f5-106">Inserts a new item in a tree-view control.</span></span> <span data-ttu-id="d63f5-107">您可以使用 [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d63f5-107">You can send this message explicitly or by using the [**TreeView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d63f5-108">參數</span><span class="sxs-lookup"><span data-stu-id="d63f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d63f5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d63f5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d63f5-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d63f5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d63f5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d63f5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d63f5-112">[**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa)結構的指標，指定樹狀檢視專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="d63f5-112">Pointer to a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure that specifies the attributes of the tree-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d63f5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d63f5-113">Return value</span></span>

<span data-ttu-id="d63f5-114">如果成功，則傳回新專案的 **HTREEITEM** 控制碼，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d63f5-114">Returns the **HTREEITEM** handle to the new item if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63f5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d63f5-115">Requirements</span></span>



| <span data-ttu-id="d63f5-116">需求</span><span class="sxs-lookup"><span data-stu-id="d63f5-116">Requirement</span></span> | <span data-ttu-id="d63f5-117">值</span><span class="sxs-lookup"><span data-stu-id="d63f5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d63f5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d63f5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d63f5-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d63f5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d63f5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d63f5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d63f5-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d63f5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d63f5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d63f5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d63f5-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d63f5-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d63f5-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d63f5-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d63f5-125">**TVM \_INSERTITEMW** (Unicode) 和 **TVM \_ INSERTITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d63f5-125">**TVM\_INSERTITEMW** (Unicode) and **TVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d63f5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d63f5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63f5-127">IZDEBSKI \_ ENDLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="d63f5-127">TVN\_ENDLABELEDIT</span></span>](tvn-endlabeledit.md)
</dt> </dl>

 

 





