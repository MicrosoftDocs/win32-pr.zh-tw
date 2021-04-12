---
title: 'TVM_SETITEM 訊息 (Commctrl .h) '
description: TVM \_ SETITEM 訊息會設定部分或全部樹狀檢視專案的屬性。 您可以使用 TreeView SetItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465464"
---
# <a name="tvm_setitem-message"></a><span data-ttu-id="c49f1-105">TVM \_ SETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="c49f1-105">TVM\_SETITEM message</span></span>

<span data-ttu-id="c49f1-106">**TVM \_ SETITEM** 訊息會設定部分或全部樹狀檢視專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="c49f1-106">The **TVM\_SETITEM** message sets some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="c49f1-107">您可以使用 [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c49f1-107">You can send this message explicitly or by using the [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c49f1-108">參數</span><span class="sxs-lookup"><span data-stu-id="c49f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c49f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c49f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c49f1-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c49f1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c49f1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c49f1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c49f1-112">[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的指標，其中包含新的專案屬性。</span><span class="sxs-lookup"><span data-stu-id="c49f1-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="c49f1-113">使用 [4.71 版](common-control-versions.md) 和更新版本時，您可以改用 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) 結構。</span><span class="sxs-lookup"><span data-stu-id="c49f1-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c49f1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c49f1-114">Return value</span></span>

<span data-ttu-id="c49f1-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c49f1-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c49f1-116">備註</span><span class="sxs-lookup"><span data-stu-id="c49f1-116">Remarks</span></span>

<span data-ttu-id="c49f1-117">[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)或 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)結構的 **hItem** 成員會識別專案，而 **遮罩** 成員會指定要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="c49f1-117">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item, and the **mask** member specifies which attributes to set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c49f1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c49f1-118">Requirements</span></span>



| <span data-ttu-id="c49f1-119">需求</span><span class="sxs-lookup"><span data-stu-id="c49f1-119">Requirement</span></span> | <span data-ttu-id="c49f1-120">值</span><span class="sxs-lookup"><span data-stu-id="c49f1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c49f1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c49f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c49f1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c49f1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c49f1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c49f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c49f1-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c49f1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c49f1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c49f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c49f1-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c49f1-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c49f1-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="c49f1-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c49f1-128">**TVM \_SETITEMW** (Unicode) 和 **TVM \_ SETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="c49f1-128">**TVM\_SETITEMW** (Unicode) and **TVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





