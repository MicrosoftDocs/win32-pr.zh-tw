---
title: 'PSN_QUERYCANCEL (Prsht.idl 的通知碼) '
description: 指出使用者已取消屬性工作表。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934267"
---
# <a name="psn_querycancel-notification-code"></a><span data-ttu-id="9c46b-105">PSN \_ QUERYCANCEL 通知碼</span><span class="sxs-lookup"><span data-stu-id="9c46b-105">PSN\_QUERYCANCEL notification code</span></span>

<span data-ttu-id="9c46b-106">指出使用者已取消屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="9c46b-106">Indicates that the user has canceled the property sheet.</span></span> <span data-ttu-id="9c46b-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="9c46b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a><span data-ttu-id="9c46b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9c46b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c46b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c46b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c46b-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9c46b-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="9c46b-111">此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9c46b-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="9c46b-112">**PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。</span><span class="sxs-lookup"><span data-stu-id="9c46b-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c46b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c46b-113">Return value</span></span>

<span data-ttu-id="9c46b-114">傳回 **TRUE** 以防止取消作業，或傳回 **FALSE** 以允許。</span><span class="sxs-lookup"><span data-stu-id="9c46b-114">Returns **TRUE** to prevent the cancel operation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c46b-115">備註</span><span class="sxs-lookup"><span data-stu-id="9c46b-115">Remarks</span></span>

<span data-ttu-id="9c46b-116">當使用者按一下 [ **取消** ] 按鈕時，通常會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="9c46b-116">This notification code is typically sent when a user clicks the **Cancel** button.</span></span> <span data-ttu-id="9c46b-117">當使用者按一下屬性工作表右上角的 [ **X** ] 按鈕或按下 esc 鍵時，也會一併傳送。</span><span class="sxs-lookup"><span data-stu-id="9c46b-117">It is also sent when a user clicks the **X** button in the property sheet's upper right hand corner or presses the ESCAPE key.</span></span> <span data-ttu-id="9c46b-118">屬性工作表頁面可以處理此通知碼，要求使用者確認取消作業。</span><span class="sxs-lookup"><span data-stu-id="9c46b-118">A property sheet page can handle this notification code to ask the user to verify the cancel operation.</span></span>

<span data-ttu-id="9c46b-119">若要設定傳回值，頁面的對話方塊程式必須呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數，並 \_ 將 DWL MSGRESULT 設定為傳回值。</span><span class="sxs-lookup"><span data-stu-id="9c46b-119">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT set to the return value.</span></span> <span data-ttu-id="9c46b-120">對話方塊程式必須傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9c46b-120">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c46b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c46b-121">Requirements</span></span>



| <span data-ttu-id="9c46b-122">需求</span><span class="sxs-lookup"><span data-stu-id="9c46b-122">Requirement</span></span> | <span data-ttu-id="9c46b-123">值</span><span class="sxs-lookup"><span data-stu-id="9c46b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c46b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c46b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9c46b-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c46b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9c46b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c46b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9c46b-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c46b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c46b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9c46b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c46b-129"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c46b-129"><dt>Prsht.h</dt></span></span> </dl> |



 

