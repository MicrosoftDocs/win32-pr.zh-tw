---
title: 'TVN_ITEMCHANGING (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，專案屬性即將變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508607"
---
# <a name="tvn_itemchanging-notification-code"></a><span data-ttu-id="e1bb8-105">IZDEBSKI \_ ITEMCHANGING 通知碼</span><span class="sxs-lookup"><span data-stu-id="e1bb8-105">TVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="e1bb8-106">通知樹狀檢視控制項的父視窗，專案屬性即將變更。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-106">Notifies a tree-view control's parent window that item attributes are about to change.</span></span> <span data-ttu-id="e1bb8-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e1bb8-108">參數</span><span class="sxs-lookup"><span data-stu-id="e1bb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1bb8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1bb8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1bb8-110">描述正在變更之專案的 [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-110">Pointer to an [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that is changing.</span></span> <span data-ttu-id="e1bb8-111">**UChanged** 成員設定為 TVIF \_ STATE。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1bb8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1bb8-112">Return value</span></span>

<span data-ttu-id="e1bb8-113">如果接受變更，則傳回 **FALSE** ，否則會傳回 **TRUE** 以防止變更。</span><span class="sxs-lookup"><span data-stu-id="e1bb8-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1bb8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1bb8-114">Requirements</span></span>



| <span data-ttu-id="e1bb8-115">需求</span><span class="sxs-lookup"><span data-stu-id="e1bb8-115">Requirement</span></span> | <span data-ttu-id="e1bb8-116">值</span><span class="sxs-lookup"><span data-stu-id="e1bb8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bb8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1bb8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1bb8-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1bb8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1bb8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1bb8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1bb8-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1bb8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1bb8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e1bb8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1bb8-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1bb8-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e1bb8-123">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e1bb8-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e1bb8-124">**Izdebski \_ITEMCHANGINGW** (Unicode) 和 **izdebski \_ ITEMCHANGINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e1bb8-124">**TVN\_ITEMCHANGINGW** (Unicode) and **TVN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="e1bb8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1bb8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1bb8-126">IZDEBSKI \_ ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="e1bb8-126">TVN\_ITEMCHANGED</span></span>](tvn-itemchanged.md)
</dt> </dl>

 

 





