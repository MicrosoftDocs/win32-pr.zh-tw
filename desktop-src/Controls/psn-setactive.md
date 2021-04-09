---
title: 'PSN_SETACTIVE (Prsht.idl 的通知碼) '
description: 通知頁面，指出即將啟用。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934624"
---
# <a name="psn_setactive-notification-code"></a><span data-ttu-id="570aa-105">PSN \_ advanced.field.setactive 通知碼</span><span class="sxs-lookup"><span data-stu-id="570aa-105">PSN\_SETACTIVE notification code</span></span>

<span data-ttu-id="570aa-106">通知頁面，指出即將啟用。</span><span class="sxs-lookup"><span data-stu-id="570aa-106">Notifies a page that it is about to be activated.</span></span> <span data-ttu-id="570aa-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="570aa-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="570aa-108">參數</span><span class="sxs-lookup"><span data-stu-id="570aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="570aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="570aa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="570aa-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="570aa-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="570aa-111">此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="570aa-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="570aa-112">**PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。</span><span class="sxs-lookup"><span data-stu-id="570aa-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="570aa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="570aa-113">Return value</span></span>

<span data-ttu-id="570aa-114">傳回零以接受啟用，或-1 表示要啟用下一個頁面或前一頁 (，取決於使用者按一下 [ **下一步]** 或 [ **上一頁** ] 按鈕) 。</span><span class="sxs-lookup"><span data-stu-id="570aa-114">Returns zero to accept the activation, or -1 to activate the next or the previous page (depending on whether the user clicked the **Next** or **Back** button).</span></span> <span data-ttu-id="570aa-115">若要將啟用設定為特定頁面，請傳回頁面的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="570aa-115">To set the activation to a particular page, return the resource identifier of the page.</span></span>

## <a name="remarks"></a><span data-ttu-id="570aa-116">備註</span><span class="sxs-lookup"><span data-stu-id="570aa-116">Remarks</span></span>

<span data-ttu-id="570aa-117">PSN \_ advanced.field.setactive 通知碼會在頁面顯示之前傳送。</span><span class="sxs-lookup"><span data-stu-id="570aa-117">The PSN\_SETACTIVE notification code is sent before the page is visible.</span></span> <span data-ttu-id="570aa-118">應用程式可以使用此通知碼來初始化頁面中的資料。</span><span class="sxs-lookup"><span data-stu-id="570aa-118">An application can use this notification code to initialize data in the page.</span></span>

> [!Note]  
> <span data-ttu-id="570aa-119">屬性工作表正在處理 \_ 傳送 PSN advanced.field.setactive 通知碼時的頁面清單。</span><span class="sxs-lookup"><span data-stu-id="570aa-119">The property sheet is in the process of manipulating the list of pages when the PSN\_SETACTIVE notification code is sent.</span></span> <span data-ttu-id="570aa-120">在處理此通知程式碼時，請勿嘗試加入、移除或插入頁面。</span><span class="sxs-lookup"><span data-stu-id="570aa-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="570aa-121">這樣做會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="570aa-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="570aa-122">若要設定傳回值，頁面的對話方塊程式必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 值，而且對話方塊程式必須傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="570aa-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="570aa-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="570aa-123">Requirements</span></span>



| <span data-ttu-id="570aa-124">需求</span><span class="sxs-lookup"><span data-stu-id="570aa-124">Requirement</span></span> | <span data-ttu-id="570aa-125">值</span><span class="sxs-lookup"><span data-stu-id="570aa-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="570aa-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="570aa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="570aa-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="570aa-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="570aa-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="570aa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="570aa-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="570aa-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="570aa-130">標頭</span><span class="sxs-lookup"><span data-stu-id="570aa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="570aa-131"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="570aa-131"><dt>Prsht.h</dt></span></span> </dl> |



 

