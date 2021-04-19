---
title: 'PSN_TRANSLATEACCELERATOR (Prsht.idl 的通知碼) '
description: 通知屬性工作表已收到鍵盤訊息。 它讓頁面有機會進行私用鍵盤快速鍵轉譯。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996174"
---
# <a name="psn_translateaccelerator-notification-code"></a><span data-ttu-id="5027f-106">PSN \_ TRANSLATEACCELERATOR 通知碼</span><span class="sxs-lookup"><span data-stu-id="5027f-106">PSN\_TRANSLATEACCELERATOR notification code</span></span>

<span data-ttu-id="5027f-107">通知屬性工作表已收到鍵盤訊息。</span><span class="sxs-lookup"><span data-stu-id="5027f-107">Notifies a property sheet that a keyboard message has been received.</span></span> <span data-ttu-id="5027f-108">它讓頁面有機會進行私用鍵盤快速鍵轉譯。</span><span class="sxs-lookup"><span data-stu-id="5027f-108">It provides the page an opportunity to do private keyboard accelerator translation.</span></span> <span data-ttu-id="5027f-109">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="5027f-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5027f-110">參數</span><span class="sxs-lookup"><span data-stu-id="5027f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5027f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5027f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5027f-112">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5027f-112">A pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="5027f-113">此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。**NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5027f-113">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of the **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="5027f-114">**PSHNOTIFY** 結構的 **lParam** 成員是訊息 [**訊息的指標。**](/windows/win32/api/winuser/ns-winuser-msg)</span><span class="sxs-lookup"><span data-stu-id="5027f-114">The **lParam** member of the **PSHNOTIFY** structure is a pointer to the message's [**MSG**](/windows/win32/api/winuser/ns-winuser-msg).</span></span> <span data-ttu-id="5027f-115">它可以轉換成 **LPMSG** 型別，以存取要轉譯之訊息的參數。</span><span class="sxs-lookup"><span data-stu-id="5027f-115">It can be cast to an **LPMSG** type, to get access to the parameters of the message to be translated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5027f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5027f-116">Return value</span></span>

<span data-ttu-id="5027f-117">傳回 PSNRET \_ MESSAGEHANDLED，表示不需要進一步處理。</span><span class="sxs-lookup"><span data-stu-id="5027f-117">Returns PSNRET\_MESSAGEHANDLED to indicate that no further processing is necessary.</span></span> <span data-ttu-id="5027f-118">傳回 PSNRET \_ >aad-userreadusingalternativesecurityid-noerror 以要求正常處理。</span><span class="sxs-lookup"><span data-stu-id="5027f-118">Returns PSNRET\_NOERROR to request normal processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="5027f-119">備註</span><span class="sxs-lookup"><span data-stu-id="5027f-119">Remarks</span></span>

<span data-ttu-id="5027f-120">若要設定傳回值，頁面的對話方塊程式必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="5027f-120">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value.</span></span> <span data-ttu-id="5027f-121">對話方塊程式必須傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5027f-121">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5027f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5027f-122">Requirements</span></span>



| <span data-ttu-id="5027f-123">需求</span><span class="sxs-lookup"><span data-stu-id="5027f-123">Requirement</span></span> | <span data-ttu-id="5027f-124">值</span><span class="sxs-lookup"><span data-stu-id="5027f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5027f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5027f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5027f-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5027f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5027f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5027f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5027f-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5027f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5027f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5027f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5027f-130"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5027f-130"><dt>Prsht.h</dt></span></span> </dl> |



 

