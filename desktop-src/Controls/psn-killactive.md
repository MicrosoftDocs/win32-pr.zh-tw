---
title: 'PSN_KILLACTIVE (Prsht.idl 的通知碼) '
description: 通知頁面，因為正在啟用另一個頁面，或使用者已按下 [確定] 按鈕，所以即將遺失啟用。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934269"
---
# <a name="psn_killactive-notification-code"></a><span data-ttu-id="eb44d-105">PSN \_ KILLACTIVE 通知碼</span><span class="sxs-lookup"><span data-stu-id="eb44d-105">PSN\_KILLACTIVE notification code</span></span>

<span data-ttu-id="eb44d-106">通知頁面，因為正在啟用另一個頁面，或使用者已按下 [確定] 按鈕，所以即將遺失啟用。</span><span class="sxs-lookup"><span data-stu-id="eb44d-106">Notifies a page that it is about to lose activation either because another page is being activated or the user has clicked the OK button.</span></span> <span data-ttu-id="eb44d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="eb44d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="eb44d-108">參數</span><span class="sxs-lookup"><span data-stu-id="eb44d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb44d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb44d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb44d-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb44d-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="eb44d-111">此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb44d-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="eb44d-112">**PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。</span><span class="sxs-lookup"><span data-stu-id="eb44d-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb44d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb44d-113">Return value</span></span>

<span data-ttu-id="eb44d-114">傳回 **TRUE** 以防止頁面遺失啟用，或傳回 **FALSE** 表示允許。</span><span class="sxs-lookup"><span data-stu-id="eb44d-114">Returns **TRUE** to prevent the page from losing the activation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb44d-115">備註</span><span class="sxs-lookup"><span data-stu-id="eb44d-115">Remarks</span></span>

<span data-ttu-id="eb44d-116">應用程式會處理此通知碼，以驗證使用者輸入的資訊。</span><span class="sxs-lookup"><span data-stu-id="eb44d-116">An application handles this notification code to validate the information the user has entered.</span></span>

> [!Note]  
> <span data-ttu-id="eb44d-117">屬性工作表正在處理 \_ 傳送 PSN KILLACTIVE 通知碼時的頁面清單。</span><span class="sxs-lookup"><span data-stu-id="eb44d-117">The property sheet is in the process of manipulating the list of pages when the PSN\_KILLACTIVE notification code is sent.</span></span> <span data-ttu-id="eb44d-118">在處理此通知程式碼時，請勿嘗試加入、移除或插入頁面。</span><span class="sxs-lookup"><span data-stu-id="eb44d-118">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="eb44d-119">這樣做會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="eb44d-119">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="eb44d-120">若要設定傳回值，頁面的對話方塊程式必須呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數，並將 DWL \_ MSGRESULT 值設定為傳回值。</span><span class="sxs-lookup"><span data-stu-id="eb44d-120">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a DWL\_MSGRESULT value set to the return value.</span></span> <span data-ttu-id="eb44d-121">對話方塊程式必須傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="eb44d-121">The dialog box procedure must return **TRUE**.</span></span>

<span data-ttu-id="eb44d-122">如果對話方塊程式將 DWL MSGRESULT 設 \_ 為 **TRUE**，它應該會顯示訊息方塊，以說明使用者的問題。</span><span class="sxs-lookup"><span data-stu-id="eb44d-122">If the dialog box procedure sets DWL\_MSGRESULT to **TRUE**, it should display a message box to explain the problem to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb44d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb44d-123">Requirements</span></span>



| <span data-ttu-id="eb44d-124">需求</span><span class="sxs-lookup"><span data-stu-id="eb44d-124">Requirement</span></span> | <span data-ttu-id="eb44d-125">值</span><span class="sxs-lookup"><span data-stu-id="eb44d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb44d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb44d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eb44d-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb44d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eb44d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb44d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eb44d-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb44d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eb44d-130">標頭</span><span class="sxs-lookup"><span data-stu-id="eb44d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb44d-131"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb44d-131"><dt>Prsht.h</dt></span></span> </dl> |



 

