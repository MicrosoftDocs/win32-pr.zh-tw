---
title: 'PSN_WIZFINISH (Prsht.idl 的通知碼) '
description: 通知頁面，表示使用者已按一下嚮導中的 [完成] 按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466092"
---
# <a name="psn_wizfinish-notification-code"></a><span data-ttu-id="7bf17-105">PSN \_ WIZFINISH 通知碼</span><span class="sxs-lookup"><span data-stu-id="7bf17-105">PSN\_WIZFINISH notification code</span></span>

<span data-ttu-id="7bf17-106">通知頁面，表示使用者已按一下嚮導中的 [ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="7bf17-106">Notifies a page that the user has clicked the **Finish** button in a wizard.</span></span> <span data-ttu-id="7bf17-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="7bf17-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7bf17-108">參數</span><span class="sxs-lookup"><span data-stu-id="7bf17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bf17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7bf17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7bf17-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7bf17-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="7bf17-111">此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7bf17-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="7bf17-112">**PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。</span><span class="sxs-lookup"><span data-stu-id="7bf17-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bf17-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7bf17-113">Return value</span></span>

-   <span data-ttu-id="7bf17-114">傳回 **TRUE** 以防止嚮導完成。</span><span class="sxs-lookup"><span data-stu-id="7bf17-114">Returns **TRUE** to prevent the wizard from finishing.</span></span>
-   [<span data-ttu-id="7bf17-115">版本5.80。</span><span class="sxs-lookup"><span data-stu-id="7bf17-115">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="7bf17-116">及更新版本。</span><span class="sxs-lookup"><span data-stu-id="7bf17-116">and later.</span></span> <span data-ttu-id="7bf17-117">傳回視窗控制碼，以防止嚮導完成。</span><span class="sxs-lookup"><span data-stu-id="7bf17-117">Returns a window handle to prevent the wizard from finishing.</span></span> <span data-ttu-id="7bf17-118">Wizard 會將焦點設為該視窗。</span><span class="sxs-lookup"><span data-stu-id="7bf17-118">The wizard will set the focus to that window.</span></span> <span data-ttu-id="7bf17-119">視窗必須由 wizard 頁面擁有。</span><span class="sxs-lookup"><span data-stu-id="7bf17-119">The window must be owned by the wizard page.</span></span>
-   <span data-ttu-id="7bf17-120">傳回 **FALSE** 以允許嚮導完成。</span><span class="sxs-lookup"><span data-stu-id="7bf17-120">Returns **FALSE** to allow the wizard to finish.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf17-121">備註</span><span class="sxs-lookup"><span data-stu-id="7bf17-121">Remarks</span></span>

<span data-ttu-id="7bf17-122">若要設定傳回值，頁面的對話方塊程式必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 值，而且對話方塊程式必須傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7bf17-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

[<span data-ttu-id="7bf17-123">版本5.80。</span><span class="sxs-lookup"><span data-stu-id="7bf17-123">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="7bf17-124">如果您的應用程式傳回 **TRUE** 以防止嚮導完成，則無法控制頁面上的哪個視窗會獲得焦點。</span><span class="sxs-lookup"><span data-stu-id="7bf17-124">If your application returns **TRUE** to prevent a wizard from finishing, it has no control over which window on the page receives focus.</span></span> <span data-ttu-id="7bf17-125">需要停止完成嚮導的應用程式通常應該會在取得焦點的 wizard 頁面上傳回視窗控制碼來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="7bf17-125">Applications that need to stop a wizard from finishing should normally do so by returning the handle of the window on the wizard page that is to receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf17-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bf17-126">Requirements</span></span>



| <span data-ttu-id="7bf17-127">需求</span><span class="sxs-lookup"><span data-stu-id="7bf17-127">Requirement</span></span> | <span data-ttu-id="7bf17-128">值</span><span class="sxs-lookup"><span data-stu-id="7bf17-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf17-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7bf17-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf17-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bf17-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7bf17-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7bf17-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf17-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bf17-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7bf17-133">標頭</span><span class="sxs-lookup"><span data-stu-id="7bf17-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf17-134"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf17-134"><dt>Prsht.h</dt></span></span> </dl> |



 

