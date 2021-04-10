---
title: 'TVM_GETITEM 訊息 (Commctrl .h) '
description: 抓取部分或所有樹狀檢視專案的屬性。 您可以使用 TreeView GetItem 宏明確地傳送此訊息 \_ 。
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106572"
---
# <a name="tvm_getitem-message"></a><span data-ttu-id="b241f-105">TVM \_ GETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="b241f-105">TVM\_GETITEM message</span></span>

<span data-ttu-id="b241f-106">抓取部分或所有樹狀檢視專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="b241f-106">Retrieves some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="b241f-107">您可以使用 [**TreeView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b241f-107">You can send this message explicitly or by using the [**TreeView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b241f-108">參數</span><span class="sxs-lookup"><span data-stu-id="b241f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b241f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b241f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b241f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b241f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b241f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b241f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b241f-112">[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的指標，此結構會指定要取出並接收專案相關資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="b241f-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that specifies the information to retrieve and receives information about the item.</span></span> <span data-ttu-id="b241f-113">使用 [4.71 版](common-control-versions.md) 和更新版本時，您可以改用 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) 結構。</span><span class="sxs-lookup"><span data-stu-id="b241f-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b241f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b241f-114">Return value</span></span>

<span data-ttu-id="b241f-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b241f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b241f-116">備註</span><span class="sxs-lookup"><span data-stu-id="b241f-116">Remarks</span></span>

<span data-ttu-id="b241f-117">傳送訊息時， [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)或 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)結構的 **hItem** 成員會識別要取得相關資訊的專案，而 **遮罩** 成員會指定要抓取的屬性。</span><span class="sxs-lookup"><span data-stu-id="b241f-117">When the message is sent, the **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item to retrieve information about, and the **mask** member specifies the attributes to retrieve.</span></span>

<span data-ttu-id="b241f-118">如果在 \_ [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)或 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)結構的 **mask** 成員中設定 TVIF 文字旗標， **pszText** 成員必須指向有效的緩衝區，而且 **cchTextMax** 成員必須設定為該緩衝區中的字元數。</span><span class="sxs-lookup"><span data-stu-id="b241f-118">If the TVIF\_TEXT flag is set in the **mask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b241f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b241f-119">Requirements</span></span>



| <span data-ttu-id="b241f-120">需求</span><span class="sxs-lookup"><span data-stu-id="b241f-120">Requirement</span></span> | <span data-ttu-id="b241f-121">值</span><span class="sxs-lookup"><span data-stu-id="b241f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b241f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b241f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b241f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b241f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b241f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b241f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b241f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b241f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b241f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b241f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b241f-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b241f-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b241f-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b241f-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b241f-129">**TVM \_GETITEMW** (Unicode) 和 **TVM \_ GETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b241f-129">**TVM\_GETITEMW** (Unicode) and **TVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





