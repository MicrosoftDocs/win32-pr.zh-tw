---
title: 'TVN_ITEMEXPANDING (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，表示父專案的子專案清單即將展開或折迭。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934999"
---
# <a name="tvn_itemexpanding-notification-code"></a><span data-ttu-id="cec0e-105">IZDEBSKI \_ ITEMEXPANDING 通知碼</span><span class="sxs-lookup"><span data-stu-id="cec0e-105">TVN\_ITEMEXPANDING notification code</span></span>

<span data-ttu-id="cec0e-106">通知樹狀檢視控制項的父視窗，表示父專案的子專案清單即將展開或折迭。</span><span class="sxs-lookup"><span data-stu-id="cec0e-106">Notifies a tree-view control's parent window that a parent item's list of child items is about to expand or collapse.</span></span> <span data-ttu-id="cec0e-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="cec0e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="cec0e-108">參數</span><span class="sxs-lookup"><span data-stu-id="cec0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec0e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cec0e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cec0e-110">[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cec0e-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="cec0e-111">**ItemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含有關 **hItem**、 **state** 和 **lParam** 成員中父專案的有效資訊。</span><span class="sxs-lookup"><span data-stu-id="cec0e-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="cec0e-112">**動作** 成員表示清單是要展開還是折迭。</span><span class="sxs-lookup"><span data-stu-id="cec0e-112">The **action** member indicates whether the list is to expand or collapse.</span></span> <span data-ttu-id="cec0e-113">如需可能值的清單，請參閱 [**TVM \_ 展開**](tvm-expand.md) 訊息的描述。</span><span class="sxs-lookup"><span data-stu-id="cec0e-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cec0e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cec0e-114">Return value</span></span>

<span data-ttu-id="cec0e-115">傳回 **TRUE** 以防止清單展開或折迭。</span><span class="sxs-lookup"><span data-stu-id="cec0e-115">Returns **TRUE** to prevent the list from expanding or collapsing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec0e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cec0e-116">Requirements</span></span>



| <span data-ttu-id="cec0e-117">需求</span><span class="sxs-lookup"><span data-stu-id="cec0e-117">Requirement</span></span> | <span data-ttu-id="cec0e-118">值</span><span class="sxs-lookup"><span data-stu-id="cec0e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cec0e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cec0e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cec0e-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec0e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cec0e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cec0e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cec0e-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec0e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cec0e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cec0e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cec0e-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cec0e-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cec0e-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="cec0e-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cec0e-126">**Izdebski \_ITEMEXPANDINGW** (Unicode) 和 **izdebski \_ ITEMEXPANDINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="cec0e-126">**TVN\_ITEMEXPANDINGW** (Unicode) and **TVN\_ITEMEXPANDINGA** (ANSI)</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cec0e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cec0e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec0e-128">IZDEBSKI \_ ITEMEXPANDED</span><span class="sxs-lookup"><span data-stu-id="cec0e-128">TVN\_ITEMEXPANDED</span></span>](tvn-itemexpanded.md)
</dt> </dl>

 

 





