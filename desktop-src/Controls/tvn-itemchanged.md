---
title: 'TVN_ITEMCHANGED (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，專案屬性已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843652"
---
# <a name="tvn_itemchanged-notification-code"></a><span data-ttu-id="0a0f2-105">IZDEBSKI \_ ITEMCHANGED 通知碼</span><span class="sxs-lookup"><span data-stu-id="0a0f2-105">TVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="0a0f2-106">通知樹狀檢視控制項的父視窗，專案屬性已變更。</span><span class="sxs-lookup"><span data-stu-id="0a0f2-106">Notifies a tree-view control's parent window that item attributes have changed.</span></span> <span data-ttu-id="0a0f2-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="0a0f2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0a0f2-108">參數</span><span class="sxs-lookup"><span data-stu-id="0a0f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a0f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a0f2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a0f2-110">[**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange)結構的指標，描述已變更的專案。</span><span class="sxs-lookup"><span data-stu-id="0a0f2-110">Pointer to a [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that changed.</span></span> <span data-ttu-id="0a0f2-111">**UChanged** 成員設定為 TVIF \_ STATE。</span><span class="sxs-lookup"><span data-stu-id="0a0f2-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a0f2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a0f2-112">Return value</span></span>

<span data-ttu-id="0a0f2-113">如果接受變更，則傳回 **FALSE** ，否則會傳回 **TRUE** 以防止變更。</span><span class="sxs-lookup"><span data-stu-id="0a0f2-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a0f2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a0f2-114">Requirements</span></span>



| <span data-ttu-id="0a0f2-115">需求</span><span class="sxs-lookup"><span data-stu-id="0a0f2-115">Requirement</span></span> | <span data-ttu-id="0a0f2-116">值</span><span class="sxs-lookup"><span data-stu-id="0a0f2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a0f2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a0f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a0f2-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a0f2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a0f2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a0f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a0f2-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a0f2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a0f2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0a0f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a0f2-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a0f2-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0a0f2-123">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="0a0f2-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0a0f2-124">**Izdebski \_ITEMCHANGEDW** (Unicode) 和 **izdebski \_ ITEMCHANGEDA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="0a0f2-124">**TVN\_ITEMCHANGEDW** (Unicode) and **TVN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0a0f2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a0f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a0f2-126">IZDEBSKI \_ ITEMCHANGING</span><span class="sxs-lookup"><span data-stu-id="0a0f2-126">TVN\_ITEMCHANGING</span></span>](tvn-itemchanging.md)
</dt> </dl>

 

 





