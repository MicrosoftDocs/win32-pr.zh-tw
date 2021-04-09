---
title: 'LVN_DELETEALLITEMS (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，表示控制項中的所有專案即將刪除。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935172"
---
# <a name="lvn_deleteallitems-notification-code"></a><span data-ttu-id="dfd60-105">LVN \_ DELETEALLITEMS 通知碼</span><span class="sxs-lookup"><span data-stu-id="dfd60-105">LVN\_DELETEALLITEMS notification code</span></span>

<span data-ttu-id="dfd60-106">通知清單視圖控制項的父視窗，表示控制項中的所有專案即將刪除。</span><span class="sxs-lookup"><span data-stu-id="dfd60-106">Notifies a list-view control's parent window that all items in the control are about to be deleted.</span></span> <span data-ttu-id="dfd60-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="dfd60-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="dfd60-108">參數</span><span class="sxs-lookup"><span data-stu-id="dfd60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd60-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dfd60-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfd60-110">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dfd60-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="dfd60-111">**IItem** 成員為-1，而其他成員為零。</span><span class="sxs-lookup"><span data-stu-id="dfd60-111">The **iItem** member is -1, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd60-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfd60-112">Return value</span></span>

<span data-ttu-id="dfd60-113">若要隱藏後續的 [LVN \_ DELETEITEM](lvn-deleteitem.md) 通知碼，請傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="dfd60-113">To suppress subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **TRUE**.</span></span>

<span data-ttu-id="dfd60-114">若要接收後續的 [LVN \_ DELETEITEM](lvn-deleteitem.md) 通知碼，請傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="dfd60-114">To receive subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfd60-115">備註</span><span class="sxs-lookup"><span data-stu-id="dfd60-115">Remarks</span></span>

<span data-ttu-id="dfd60-116">當 [**lvm \_ DELETEALLITEMS**](lvm-deleteallitems.md) 通知程式碼損毀或收到 **lvm \_ DELETEALLITEMS** 訊息時，它會傳送該控制項。</span><span class="sxs-lookup"><span data-stu-id="dfd60-116">A list-view control sends the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) notification code when it is destroyed or when it receives the **LVM\_DELETEALLITEMS** message.</span></span> <span data-ttu-id="dfd60-117">如果 **LVM \_ DELETEALLITEMS** 未傳回 **TRUE**，則此控制項也會在每個專案遭到刪除時，傳送 [LVN \_ DELETEITEM](lvn-deleteitem.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="dfd60-117">If **LVM\_DELETEALLITEMS** does not return **TRUE**, the control will also send an [LVN\_DELETEITEM](lvn-deleteitem.md) notification code as each item is deleted.</span></span>

<span data-ttu-id="dfd60-118">如果 [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) 訊息處理常式位於對話方塊程式中，請從對話方塊程式傳回 **TRUE** ，並使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 來設定訊息傳回值。</span><span class="sxs-lookup"><span data-stu-id="dfd60-118">If the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) message handler is in a dialog box procedure, return **TRUE** from the dialog box procedure, and use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set the message return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd60-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfd60-119">Requirements</span></span>



| <span data-ttu-id="dfd60-120">需求</span><span class="sxs-lookup"><span data-stu-id="dfd60-120">Requirement</span></span> | <span data-ttu-id="dfd60-121">值</span><span class="sxs-lookup"><span data-stu-id="dfd60-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd60-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfd60-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd60-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfd60-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dfd60-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfd60-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd60-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfd60-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dfd60-126">標頭</span><span class="sxs-lookup"><span data-stu-id="dfd60-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfd60-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dfd60-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

