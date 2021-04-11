---
title: 'TVN_ITEMEXPANDED (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，表示父專案的子專案清單已展開或折迭。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105947"
---
# <a name="tvn_itemexpanded-notification-code"></a><span data-ttu-id="64e75-105">IZDEBSKI \_ ITEMEXPANDED 通知碼</span><span class="sxs-lookup"><span data-stu-id="64e75-105">TVN\_ITEMEXPANDED notification code</span></span>

<span data-ttu-id="64e75-106">通知樹狀檢視控制項的父視窗，表示父專案的子專案清單已展開或折迭。</span><span class="sxs-lookup"><span data-stu-id="64e75-106">Notifies a tree-view control's parent window that a parent item's list of child items has expanded or collapsed.</span></span> <span data-ttu-id="64e75-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="64e75-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="64e75-108">參數</span><span class="sxs-lookup"><span data-stu-id="64e75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64e75-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64e75-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64e75-110">[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="64e75-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="64e75-111">**ItemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含有關 **hItem**、 **state** 和 **lParam** 成員中父專案的有效資訊。</span><span class="sxs-lookup"><span data-stu-id="64e75-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="64e75-112">**動作** 成員表示清單是否展開或折迭。</span><span class="sxs-lookup"><span data-stu-id="64e75-112">The **action** member indicates whether the list expanded or collapsed.</span></span> <span data-ttu-id="64e75-113">如需可能值的清單，請參閱 [**TVM \_ 展開**](tvm-expand.md) 訊息的描述。</span><span class="sxs-lookup"><span data-stu-id="64e75-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64e75-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="64e75-114">Return value</span></span>

<span data-ttu-id="64e75-115">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="64e75-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="64e75-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="64e75-116">Requirements</span></span>



| <span data-ttu-id="64e75-117">需求</span><span class="sxs-lookup"><span data-stu-id="64e75-117">Requirement</span></span> | <span data-ttu-id="64e75-118">值</span><span class="sxs-lookup"><span data-stu-id="64e75-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64e75-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64e75-119">Minimum supported client</span></span><br/> | <span data-ttu-id="64e75-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64e75-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64e75-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64e75-121">Minimum supported server</span></span><br/> | <span data-ttu-id="64e75-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64e75-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64e75-123">標頭</span><span class="sxs-lookup"><span data-stu-id="64e75-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="64e75-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="64e75-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="64e75-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="64e75-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="64e75-126">**Izdebski \_ITEMEXPANDEDW** (Unicode) 和 **izdebski \_ ITEMEXPANDEDA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="64e75-126">**TVN\_ITEMEXPANDEDW** (Unicode) and **TVN\_ITEMEXPANDEDA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="64e75-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64e75-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e75-128">IZDEBSKI \_ ITEMEXPANDING</span><span class="sxs-lookup"><span data-stu-id="64e75-128">TVN\_ITEMEXPANDING</span></span>](tvn-itemexpanding.md)
</dt> </dl>

 

 





