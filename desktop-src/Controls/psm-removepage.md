---
title: 'PSM_REMOVEPAGE 訊息 (Prsht.idl .h) '
description: 從屬性工作表移除頁面。 您可以使用 PropSheet RemovePage 宏明確地傳送此訊息 \_ 。
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844024"
---
# <a name="psm_removepage-message"></a><span data-ttu-id="9ac22-105">PSM \_ REMOVEPAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="9ac22-105">PSM\_REMOVEPAGE message</span></span>

<span data-ttu-id="9ac22-106">從屬性工作表移除頁面。</span><span class="sxs-lookup"><span data-stu-id="9ac22-106">Removes a page from a property sheet.</span></span> <span data-ttu-id="9ac22-107">您可以使用 [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9ac22-107">You can send this message explicitly or by using the [**PropSheet\_RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ac22-108">參數</span><span class="sxs-lookup"><span data-stu-id="9ac22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ac22-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ac22-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ac22-110">要移除之頁面的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="9ac22-110">Zero-based index of the page to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="9ac22-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ac22-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ac22-112">要移除之頁面的 HPROPSHEETPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="9ac22-112">The HPROPSHEETPAGE handle of the page to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ac22-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ac22-113">Return value</span></span>

<span data-ttu-id="9ac22-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="9ac22-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac22-115">備註</span><span class="sxs-lookup"><span data-stu-id="9ac22-115">Remarks</span></span>

<span data-ttu-id="9ac22-116">應用程式可以指定索引或控制碼，或兩者。</span><span class="sxs-lookup"><span data-stu-id="9ac22-116">An application can specify the index or the handle, or both.</span></span> <span data-ttu-id="9ac22-117">如果同時指定這兩者， *lParam* 會優先使用。</span><span class="sxs-lookup"><span data-stu-id="9ac22-117">If both are specified, *lParam* takes precedence.</span></span>

<span data-ttu-id="9ac22-118">傳送 **PSM \_ REMOVEPAGE** 會損毀正在移除的屬性工作表頁面。</span><span class="sxs-lookup"><span data-stu-id="9ac22-118">Sending **PSM\_REMOVEPAGE** destroys the property sheet page that is being removed.</span></span>

<span data-ttu-id="9ac22-119">當屬性工作表正在動作頁面清單時，會發生一些訊息和一個函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ac22-119">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="9ac22-120">當此動作執行時，嘗試修改頁面清單將會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="9ac22-120">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="9ac22-121">因此，您不應該在 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)的執行中或在處理下列通知和 Windows 訊息時使用 **PSM \_ REMOVEPAGE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="9ac22-121">Accordingly, you should not use the **PSM\_REMOVEPAGE** message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="9ac22-122">PSN \_ APPLY</span><span class="sxs-lookup"><span data-stu-id="9ac22-122">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="9ac22-123">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="9ac22-123">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="9ac22-124">PSN \_ 重設</span><span class="sxs-lookup"><span data-stu-id="9ac22-124">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="9ac22-125">PSN \_ ADVANCED.FIELD.SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="9ac22-125">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="9ac22-126">**WM 損 \_ 毀**</span><span class="sxs-lookup"><span data-stu-id="9ac22-126">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="9ac22-127">**WM \_ INITDIALOG**</span><span class="sxs-lookup"><span data-stu-id="9ac22-127">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="9ac22-128">如果您在處理其中一個訊息時，或當 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 正在運作時需要修改屬性工作表頁面，請自行張貼私用 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="9ac22-128">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="9ac22-129">在屬性工作表管理員完成其工作之前，您的應用程式將不會收到該訊息。</span><span class="sxs-lookup"><span data-stu-id="9ac22-129">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="9ac22-130">然後您可以修改頁面清單。</span><span class="sxs-lookup"><span data-stu-id="9ac22-130">Then you can modify the list of pages.</span></span>

<span data-ttu-id="9ac22-131">下列通知也會受到屬性工作表修改的影響。</span><span class="sxs-lookup"><span data-stu-id="9ac22-131">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="9ac22-132">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="9ac22-132">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="9ac22-133">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="9ac22-133">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="9ac22-134">您可以新增或移除頁面，以回應這些通知，前提是您透過 DWL MSGRESULT 傳回 (， \_) 非零值來指定所需的新頁面。</span><span class="sxs-lookup"><span data-stu-id="9ac22-134">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="9ac22-135">但是請注意，如果您移除目前頁面之前的頁面 (，其索引小於目前頁面) 的索引， [PSN \_ KILLACTIVE](psn-killactive.md) 可能會傳送至錯誤的頁面。</span><span class="sxs-lookup"><span data-stu-id="9ac22-135">Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac22-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ac22-136">Requirements</span></span>



| <span data-ttu-id="9ac22-137">需求</span><span class="sxs-lookup"><span data-stu-id="9ac22-137">Requirement</span></span> | <span data-ttu-id="9ac22-138">值</span><span class="sxs-lookup"><span data-stu-id="9ac22-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac22-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ac22-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac22-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ac22-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9ac22-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ac22-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac22-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ac22-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9ac22-143">標頭</span><span class="sxs-lookup"><span data-stu-id="9ac22-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ac22-144"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ac22-144"><dt>Prsht.h</dt></span></span> </dl> |



 

