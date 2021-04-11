---
title: 'LVN_ITEMCHANGING (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，指出專案正在變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- LVN_ITEMCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935168"
---
# <a name="lvn_itemchanging-notification-code"></a><span data-ttu-id="d25e4-105">LVN \_ ITEMCHANGING 通知碼</span><span class="sxs-lookup"><span data-stu-id="d25e4-105">LVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="d25e4-106">通知清單視圖控制項的父視窗，指出專案正在變更。</span><span class="sxs-lookup"><span data-stu-id="d25e4-106">Notifies a list-view control's parent window that an item is changing.</span></span> <span data-ttu-id="d25e4-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d25e4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d25e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="d25e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d25e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d25e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d25e4-110">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標，該結構會識別專案並指定其屬性的變更。</span><span class="sxs-lookup"><span data-stu-id="d25e4-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes are changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d25e4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d25e4-111">Return value</span></span>

<span data-ttu-id="d25e4-112">傳回 **TRUE** 以防止變更，或傳回 **FALSE** 以允許變更。</span><span class="sxs-lookup"><span data-stu-id="d25e4-112">Returns **TRUE** to prevent the change, or **FALSE** to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="d25e4-113">備註</span><span class="sxs-lookup"><span data-stu-id="d25e4-113">Remarks</span></span>

<span data-ttu-id="d25e4-114">如果清單視圖控制項有 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式， \_ 則不會傳送 LVN ITEMCHANGING 通知碼。</span><span class="sxs-lookup"><span data-stu-id="d25e4-114">If the list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, LVN\_ITEMCHANGING notification codes are not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d25e4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d25e4-115">Requirements</span></span>



| <span data-ttu-id="d25e4-116">需求</span><span class="sxs-lookup"><span data-stu-id="d25e4-116">Requirement</span></span> | <span data-ttu-id="d25e4-117">值</span><span class="sxs-lookup"><span data-stu-id="d25e4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d25e4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d25e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d25e4-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d25e4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d25e4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d25e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d25e4-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d25e4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d25e4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d25e4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d25e4-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d25e4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





