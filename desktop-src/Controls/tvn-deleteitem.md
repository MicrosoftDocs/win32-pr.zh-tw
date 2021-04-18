---
title: 'TVN_DELETEITEM (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，指出正在刪除專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465461"
---
# <a name="tvn_deleteitem-notification-code"></a><span data-ttu-id="5b623-105">IZDEBSKI \_ DELETEITEM 通知碼</span><span class="sxs-lookup"><span data-stu-id="5b623-105">TVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="5b623-106">通知樹狀檢視控制項的父視窗，指出正在刪除專案。</span><span class="sxs-lookup"><span data-stu-id="5b623-106">Notifies a tree-view control's parent window that an item is being deleted.</span></span> <span data-ttu-id="5b623-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="5b623-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="5b623-108">參數</span><span class="sxs-lookup"><span data-stu-id="5b623-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b623-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b623-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b623-110">[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5b623-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="5b623-111">**ItemOld** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其 **hItem** 和 **lParam** 成員包含有關正在刪除之專案的有效資訊。</span><span class="sxs-lookup"><span data-stu-id="5b623-111">The **itemOld** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem** and **lParam** members contain valid information about the item being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b623-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b623-112">Return value</span></span>

<span data-ttu-id="5b623-113">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="5b623-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b623-114">備註</span><span class="sxs-lookup"><span data-stu-id="5b623-114">Remarks</span></span>

<span data-ttu-id="5b623-115">如果 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **lParam** 成員指向您的應用程式所配置的記憶體，您可以在收到 izdebski \_ DELETEITEM 通知碼時釋放它。</span><span class="sxs-lookup"><span data-stu-id="5b623-115">If the **lParam** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure points to memory allocated by your application, you can free it when you receive the TVN\_DELETEITEM notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b623-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b623-116">Requirements</span></span>



| <span data-ttu-id="5b623-117">需求</span><span class="sxs-lookup"><span data-stu-id="5b623-117">Requirement</span></span> | <span data-ttu-id="5b623-118">值</span><span class="sxs-lookup"><span data-stu-id="5b623-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b623-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b623-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5b623-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b623-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b623-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b623-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5b623-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b623-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b623-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5b623-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b623-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b623-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5b623-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5b623-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5b623-126">**Izdebski \_DELETEITEMW** (Unicode) 和 **izdebski \_ DELETEITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5b623-126">**TVN\_DELETEITEMW** (Unicode) and **TVN\_DELETEITEMA** (ANSI)</span></span><br/>             |



 

 





