---
title: 'TVN_BEGINDRAG (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，表示正在起始涉及滑鼠左鍵的拖放操作。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843655"
---
# <a name="tvn_begindrag-notification-code"></a><span data-ttu-id="ba47f-105">IZDEBSKI \_ BEGINDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="ba47f-105">TVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="ba47f-106">通知樹狀檢視控制項的父視窗，表示正在起始涉及滑鼠左鍵的拖放操作。</span><span class="sxs-lookup"><span data-stu-id="ba47f-106">Notifies a tree-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="ba47f-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="ba47f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="ba47f-108">參數</span><span class="sxs-lookup"><span data-stu-id="ba47f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba47f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba47f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba47f-110">[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ba47f-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="ba47f-111">**ItemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含在 **hItem**、 **state** 和 **lParam** 成員中拖曳之專案的相關有效資訊。</span><span class="sxs-lookup"><span data-stu-id="ba47f-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being dragged in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="ba47f-112">**PtDrag** 成員會指定滑鼠目前的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="ba47f-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba47f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba47f-113">Return value</span></span>

<span data-ttu-id="ba47f-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="ba47f-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba47f-115">備註</span><span class="sxs-lookup"><span data-stu-id="ba47f-115">Remarks</span></span>

<span data-ttu-id="ba47f-116">具有 [**電視 \_ DISABLEDRAGDROP**](tree-view-control-window-styles.md) 樣式的樹狀檢視控制項不會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="ba47f-116">A tree-view control that has the [**TVS\_DISABLEDRAGDROP**](tree-view-control-window-styles.md) style does not send this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba47f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba47f-117">Requirements</span></span>



| <span data-ttu-id="ba47f-118">需求</span><span class="sxs-lookup"><span data-stu-id="ba47f-118">Requirement</span></span> | <span data-ttu-id="ba47f-119">值</span><span class="sxs-lookup"><span data-stu-id="ba47f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba47f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba47f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ba47f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba47f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba47f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba47f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ba47f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba47f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba47f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ba47f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba47f-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba47f-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ba47f-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ba47f-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ba47f-127">**Izdebski \_BEGINDRAGW** (Unicode) 和 **izdebski \_ BEGINDRAGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="ba47f-127">**TVN\_BEGINDRAGW** (Unicode) and **TVN\_BEGINDRAGA** (ANSI)</span></span><br/>               |



 

 





