---
title: 'TVN_SELCHANGING (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，選取範圍即將從某個專案變更為另一個專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024984"
---
# <a name="tvn_selchanging-notification-code"></a><span data-ttu-id="2736e-105">IZDEBSKI \_ SELCHANGING 通知碼</span><span class="sxs-lookup"><span data-stu-id="2736e-105">TVN\_SELCHANGING notification code</span></span>

<span data-ttu-id="2736e-106">通知樹狀檢視控制項的父視窗，選取範圍即將從某個專案變更為另一個專案。</span><span class="sxs-lookup"><span data-stu-id="2736e-106">Notifies a tree-view control's parent window that the selection is about to change from one item to another.</span></span> <span data-ttu-id="2736e-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="2736e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="2736e-108">參數</span><span class="sxs-lookup"><span data-stu-id="2736e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2736e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2736e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2736e-110">[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2736e-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="2736e-111">**ItemOld** 和 **itemNew** 成員包含目前所選項目和新選取專案的相關有效資訊。</span><span class="sxs-lookup"><span data-stu-id="2736e-111">The **itemOld** and **itemNew** members contain valid information about the currently selected item and the newly selected item.</span></span> <span data-ttu-id="2736e-112">**動作** 成員指出滑鼠或鍵盤動作是否會造成選取範圍變更。</span><span class="sxs-lookup"><span data-stu-id="2736e-112">The **action** member indicates whether a mouse or keyboard action is causing the selection to change.</span></span> <span data-ttu-id="2736e-113">如需可能值的清單，請參閱 [izdebski \_ SELCHANGED](tvn-selchanged.md) 通知碼的描述。</span><span class="sxs-lookup"><span data-stu-id="2736e-113">For a list of possible values, see the description of the [TVN\_SELCHANGED](tvn-selchanged.md) notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2736e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2736e-114">Return value</span></span>

<span data-ttu-id="2736e-115">傳回 **TRUE** 以防止選取範圍變更。</span><span class="sxs-lookup"><span data-stu-id="2736e-115">Returns **TRUE** to prevent the selection from changing.</span></span>

## <a name="remarks"></a><span data-ttu-id="2736e-116">備註</span><span class="sxs-lookup"><span data-stu-id="2736e-116">Remarks</span></span>

<span data-ttu-id="2736e-117">回應此通知碼時，應用程式不應該刪除取得或遺失選取專案的專案。</span><span class="sxs-lookup"><span data-stu-id="2736e-117">When responding to this notification code, applications should not delete the items that are gaining or losing the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="2736e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2736e-118">Requirements</span></span>



| <span data-ttu-id="2736e-119">需求</span><span class="sxs-lookup"><span data-stu-id="2736e-119">Requirement</span></span> | <span data-ttu-id="2736e-120">值</span><span class="sxs-lookup"><span data-stu-id="2736e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2736e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2736e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2736e-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2736e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2736e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2736e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2736e-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2736e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2736e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2736e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2736e-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2736e-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2736e-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="2736e-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2736e-128">**Izdebski \_SELCHANGINGW** (Unicode) 和 **izdebski \_ SELCHANGINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="2736e-128">**TVN\_SELCHANGINGW** (Unicode) and **TVN\_SELCHANGINGA** (ANSI)</span></span><br/>           |



 

 





