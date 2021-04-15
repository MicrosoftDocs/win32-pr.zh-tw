---
title: 'PSN_APPLY (Prsht.idl 的通知碼) '
description: 傳送至屬性工作表中的每個頁面，表示使用者已按下 [確定]、[關閉] 或 [套用] 按鈕，並想要讓所有變更生效。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465861"
---
# <a name="psn_apply-notification-code"></a><span data-ttu-id="4fe35-105">PSN 套用 \_ 通知碼</span><span class="sxs-lookup"><span data-stu-id="4fe35-105">PSN\_APPLY notification code</span></span>

<span data-ttu-id="4fe35-106">傳送至屬性工作表中的每個頁面，表示使用者已按下 [確定]、[關閉] 或 [套用] 按鈕，並想要讓所有變更生效。</span><span class="sxs-lookup"><span data-stu-id="4fe35-106">Sent to every page in the property sheet to indicate that the user has clicked the OK, Close, or Apply button and wants all changes to take effect.</span></span> <span data-ttu-id="4fe35-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="4fe35-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4fe35-108">參數</span><span class="sxs-lookup"><span data-stu-id="4fe35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe35-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fe35-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe35-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知程式碼的相關資訊，包括頁面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fe35-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code, including the ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe35-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fe35-111">Return value</span></span>

<span data-ttu-id="4fe35-112">設定 PSNRET \_ >aad-userreadusingalternativesecurityid-noerror，表示對此頁面所做的變更有效且已套用。</span><span class="sxs-lookup"><span data-stu-id="4fe35-112">Set PSNRET\_NOERROR to indicate that the changes made to this page are valid and have been applied.</span></span> <span data-ttu-id="4fe35-113">如果所有頁面都設定 \_ 了 PSNRET >aad-userreadusingalternativesecurityid-noerror，則可以終結屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="4fe35-113">If all pages set PSNRET\_NOERROR, the property sheet can be destroyed.</span></span> <span data-ttu-id="4fe35-114">若要指出對此頁面所做的變更無效，以及防止屬性工作表終結，請設定下列其中一個傳回值：</span><span class="sxs-lookup"><span data-stu-id="4fe35-114">To indicate that the changes made to this page are invalid and to prevent the property sheet from being destroyed, set one of the following return values:</span></span>

-   <span data-ttu-id="4fe35-115">PSNRET \_ 無效。</span><span class="sxs-lookup"><span data-stu-id="4fe35-115">PSNRET\_INVALID.</span></span> <span data-ttu-id="4fe35-116">將不會終結屬性工作表，而且焦點將會傳回此頁面。</span><span class="sxs-lookup"><span data-stu-id="4fe35-116">The property sheet will not be destroyed, and focus will be returned to this page.</span></span>
-   <span data-ttu-id="4fe35-117">PSNRET \_ 無效 \_ 的 NOCHANGEPAGE。</span><span class="sxs-lookup"><span data-stu-id="4fe35-117">PSNRET\_INVALID\_NOCHANGEPAGE.</span></span> <span data-ttu-id="4fe35-118">將不會終結屬性工作表，而且焦點會在按下按鈕時，傳回具有焦點的頁面。</span><span class="sxs-lookup"><span data-stu-id="4fe35-118">The property sheet will not be destroyed, and focus will be returned to the page that had focus when the button was pressed.</span></span>

<span data-ttu-id="4fe35-119">若要設定傳回值，頁面的對話方塊程式必須使用 DWL MSGRESULT 值來呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數 \_ ，而且對話方塊程式必須傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4fe35-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fe35-120">備註</span><span class="sxs-lookup"><span data-stu-id="4fe35-120">Remarks</span></span>

<span data-ttu-id="4fe35-121">當使用者按一下 [確定]、[套用] 或 [關閉] 按鈕時，屬性工作表會將 [PSN \_ KILLACTIVE](psn-killactive.md) 通知傳送至使用中的頁面，讓它有機會驗證使用者的變更。</span><span class="sxs-lookup"><span data-stu-id="4fe35-121">When the user clicks the OK, Apply, or Close button, the property sheet sends a [PSN\_KILLACTIVE](psn-killactive.md) notification to the active page, giving it an opportunity to validate the user's changes.</span></span> <span data-ttu-id="4fe35-122">如果變更有效，屬性工作表會將 PSN 套用通知程式 \_ 代碼傳送至每個頁面，並將其導向以將新屬性套用至對應的專案。</span><span class="sxs-lookup"><span data-stu-id="4fe35-122">If the changes are valid, the property sheet sends a PSN\_APPLY notification code to each page, directing it to apply the new properties to the corresponding item.</span></span>

> [!Note]  
> <span data-ttu-id="4fe35-123">當 \_ 傳送 PSN APPLY 通知碼時，屬性工作表正在處理頁面清單。</span><span class="sxs-lookup"><span data-stu-id="4fe35-123">The property sheet is in the process of manipulating the list of pages when the PSN\_APPLY notification code is sent.</span></span> <span data-ttu-id="4fe35-124">處理此通知時，請勿嘗試加入、移除或插入頁面。</span><span class="sxs-lookup"><span data-stu-id="4fe35-124">Do not attempt to add, remove, or insert pages while handling this notification.</span></span> <span data-ttu-id="4fe35-125">這樣做會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="4fe35-125">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="4fe35-126">如果使用者按一下 [確定] 按鈕， *lParam* 所指向之 [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的 **LParam** 成員會設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4fe35-126">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* is set to **TRUE** if the user clicks the OK button.</span></span> <span data-ttu-id="4fe35-127">如果已傳送 [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md)訊息，且使用者按一下 [關閉] 按鈕，則也會將它設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4fe35-127">It is also set to **TRUE** if the [**PSM\_CANCELTOCLOSE**](psm-canceltoclose.md) message has been sent and the user clicks the Close button.</span></span> <span data-ttu-id="4fe35-128">如果使用者按一下 [套用] 按鈕，則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4fe35-128">It is set to **FALSE** if the user clicks the Apply button.</span></span>

<span data-ttu-id="4fe35-129">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4fe35-129">The [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="4fe35-130">處理此通知碼時，請勿呼叫 [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) 函數。</span><span class="sxs-lookup"><span data-stu-id="4fe35-130">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

<span data-ttu-id="4fe35-131">如果使用者按一下 [確定] 按鈕，而且每個頁面會傳回 PSNRET \_ >aad-userreadusingalternativesecurityid-noerror 值以回應 **PSN \_ APPLY**，則會終結模式屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="4fe35-131">A modal property sheet is destroyed if the user clicks the OK button and every page returns the PSNRET\_NOERROR value in response to **PSN\_APPLY**.</span></span> <span data-ttu-id="4fe35-132">如果有任何頁面傳回 \_ 不正確 PSNRET 或 PSNRET \_ 無效 \_ 的 NOCHANGEPAGE，則會立即取消套用的進程。</span><span class="sxs-lookup"><span data-stu-id="4fe35-132">If any page returns PSNRET\_INVALID or PSNRET\_INVALID\_NOCHANGEPAGE, the Apply process is canceled immediately.</span></span> <span data-ttu-id="4fe35-133">取消頁面之後的頁面不會收到 PSN 套用 \_ 通知碼。</span><span class="sxs-lookup"><span data-stu-id="4fe35-133">Pages after the cancelling page will not receive a PSN\_APPLY notification code.</span></span>

<span data-ttu-id="4fe35-134">若要接收此通知碼，頁面必須將 DWL \_ MSGRESULT 值設定為 **FALSE** ，以回應 [PSN \_ KILLACTIVE](psn-killactive.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="4fe35-134">To receive this notification code, a page must set the DWL\_MSGRESULT value to **FALSE** in response to the [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span>

> [!Note]  
> <span data-ttu-id="4fe35-135">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此通知碼。</span><span class="sxs-lookup"><span data-stu-id="4fe35-135">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4fe35-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fe35-136">Requirements</span></span>



| <span data-ttu-id="4fe35-137">需求</span><span class="sxs-lookup"><span data-stu-id="4fe35-137">Requirement</span></span> | <span data-ttu-id="4fe35-138">值</span><span class="sxs-lookup"><span data-stu-id="4fe35-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe35-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fe35-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe35-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fe35-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4fe35-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fe35-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe35-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fe35-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4fe35-143">標頭</span><span class="sxs-lookup"><span data-stu-id="4fe35-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fe35-144"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe35-144"><dt>Prsht.h</dt></span></span> </dl> |



 

