---
title: 'PSN_RESET (Prsht.idl 的通知碼) '
description: 通知頁面：即將終結屬性工作表。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967954"
---
# <a name="psn_reset-notification-code"></a><span data-ttu-id="0dd84-105">PSN \_ 重設通知碼</span><span class="sxs-lookup"><span data-stu-id="0dd84-105">PSN\_RESET notification code</span></span>

<span data-ttu-id="0dd84-106">通知頁面：即將終結屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="0dd84-106">Notifies a page that the property sheet is about to be destroyed.</span></span> <span data-ttu-id="0dd84-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="0dd84-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0dd84-108">參數</span><span class="sxs-lookup"><span data-stu-id="0dd84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0dd84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0dd84-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0dd84-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd84-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0dd84-111">Return value</span></span>

<span data-ttu-id="0dd84-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="0dd84-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dd84-113">備註</span><span class="sxs-lookup"><span data-stu-id="0dd84-113">Remarks</span></span>

<span data-ttu-id="0dd84-114">自從上一個 PSN 套用通知碼之後所做的所有變更都已取消，但在 [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)的情況下則不支援該通知碼。 [ \_](psn-apply.md)</span><span class="sxs-lookup"><span data-stu-id="0dd84-114">All changes made since the last [PSN\_APPLY](psn-apply.md) notification code are canceled, except in the case of [**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), which does not support that notification code.</span></span>

<span data-ttu-id="0dd84-115">如果使用者按一下屬性工作表右上角的 [ **X** ] 按鈕， *lParam* 所指向之 [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的 **lParam** 成員將設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="0dd84-115">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* will be set to **TRUE** if the user clicked the **X** button in the upper-right corner of the property sheet.</span></span> <span data-ttu-id="0dd84-116">如果使用者按一下 [**取消**] 按鈕，就會是 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0dd84-116">It will be **FALSE** if the user clicked the **Cancel** button.</span></span> <span data-ttu-id="0dd84-117">**PSHNOTIFY** 結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0dd84-117">The **PSHNOTIFY** structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="0dd84-118">應用程式可以使用此通知碼作為執行清除作業的機會。</span><span class="sxs-lookup"><span data-stu-id="0dd84-118">An application can use this notification code as an opportunity to perform cleanup operations.</span></span>

> [!Note]  
> <span data-ttu-id="0dd84-119">在 \_ 傳送 PSN 重設通知碼時，屬性工作表正在處理頁面清單。</span><span class="sxs-lookup"><span data-stu-id="0dd84-119">The property sheet is in the process of manipulating the list of pages when the PSN\_RESET notification code is sent.</span></span> <span data-ttu-id="0dd84-120">在處理此通知程式碼時，請勿嘗試加入、移除或插入頁面。</span><span class="sxs-lookup"><span data-stu-id="0dd84-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="0dd84-121">這樣做會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="0dd84-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="0dd84-122">處理此通知碼時，請勿呼叫 [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) 函數。</span><span class="sxs-lookup"><span data-stu-id="0dd84-122">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd84-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0dd84-123">Requirements</span></span>



| <span data-ttu-id="0dd84-124">需求</span><span class="sxs-lookup"><span data-stu-id="0dd84-124">Requirement</span></span> | <span data-ttu-id="0dd84-125">值</span><span class="sxs-lookup"><span data-stu-id="0dd84-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd84-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0dd84-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0dd84-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0dd84-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0dd84-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0dd84-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0dd84-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0dd84-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0dd84-130">標頭</span><span class="sxs-lookup"><span data-stu-id="0dd84-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dd84-131"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0dd84-131"><dt>Prsht.h</dt></span></span> </dl> |



 

