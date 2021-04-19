---
title: 'PSM_INSERTPAGE 訊息 (Prsht.idl .h) '
description: 將新頁面插入現有的屬性工作表中。 頁面可以插入指定的索引或指定的頁面之後。 您可以使用 PropSheet InsertPage 宏明確地傳送此訊息 \_ 。
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968361"
---
# <a name="psm_insertpage-message"></a><span data-ttu-id="bd493-106">PSM \_ INSERTPAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="bd493-106">PSM\_INSERTPAGE message</span></span>

<span data-ttu-id="bd493-107">將新頁面插入現有的屬性工作表中。</span><span class="sxs-lookup"><span data-stu-id="bd493-107">Inserts a new page into an existing property sheet.</span></span> <span data-ttu-id="bd493-108">頁面可以插入指定的索引或指定的頁面之後。</span><span class="sxs-lookup"><span data-stu-id="bd493-108">The page can be inserted either at a specified index or after a specified page.</span></span> <span data-ttu-id="bd493-109">您可以使用 [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="bd493-109">You can send this message explicitly or by using the [**PropSheet\_InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd493-110">參數</span><span class="sxs-lookup"><span data-stu-id="bd493-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd493-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd493-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd493-112">要插入頁面的位置。</span><span class="sxs-lookup"><span data-stu-id="bd493-112">Where the page is to be inserted.</span></span> <span data-ttu-id="bd493-113">將此參數設定為 **Null** ，以將新頁面設為第一頁。</span><span class="sxs-lookup"><span data-stu-id="bd493-113">Set this parameter to **NULL** to make the new page the first page.</span></span> <span data-ttu-id="bd493-114">若要指定要插入新頁面的位置，您可以傳遞索引或現有頁面的 HPROPSHEETPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="bd493-114">To specify where the new page is to be inserted, you can either pass an index or an existing page's HPROPSHEETPAGE handle.</span></span>



| <span data-ttu-id="bd493-115">值</span><span class="sxs-lookup"><span data-stu-id="bd493-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="bd493-116">意義</span><span class="sxs-lookup"><span data-stu-id="bd493-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd493-117"><dt></dt><dt>索引</dt></span><span class="sxs-lookup"><span data-stu-id="bd493-117"><dt></dt> <dt>index</dt></span></span> </dl>            | <span data-ttu-id="bd493-118">如果 *wParam* 參數小於 MAXUSHORT () 最大不帶正負號的短整數，則 *wParam* 會為新頁面指定以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="bd493-118">If the *wParam* parameter is less than MAXUSHORT (the largest unsigned short integer), the *wParam* specifies the zero-based index for the new page.</span></span> <span data-ttu-id="bd493-119">例如，若要將插入的頁面設為屬性工作表上的第三頁，請將 *wParam* 設定為2。</span><span class="sxs-lookup"><span data-stu-id="bd493-119">For example, to make the inserted page the third page on the property sheet, set *wParam* to 2.</span></span> <span data-ttu-id="bd493-120">若要將它設為第一頁，請將 *wParam* 設定為0。</span><span class="sxs-lookup"><span data-stu-id="bd493-120">To make it the first page, set *wParam* to 0.</span></span> <span data-ttu-id="bd493-121">如果 *wParam* 的值大於頁面數目且小於 MAXUSHORT，則會附加該頁面。</span><span class="sxs-lookup"><span data-stu-id="bd493-121">If *wParam* has a value greater than the number of pages and less than MAXUSHORT, the page will be appended.</span></span><br/> |
| <dl> <span data-ttu-id="bd493-122"><dt></dt><dt>hpageInsertAfter</dt></span><span class="sxs-lookup"><span data-stu-id="bd493-122"><dt></dt> <dt>hpageInsertAfter</dt></span></span> </dl> | <span data-ttu-id="bd493-123">如果您將 *wParam* 參數設定為現有頁面的 HPROPSHEETPAGE 控制碼，就會在新頁面之後插入新頁面。</span><span class="sxs-lookup"><span data-stu-id="bd493-123">If you set the *wParam* parameter to an existing page's HPROPSHEETPAGE handle, the new page will be inserted after it.</span></span><br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="bd493-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd493-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd493-125">要插入之頁面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bd493-125">Handle to the page to be inserted.</span></span> <span data-ttu-id="bd493-126">頁面必須先透過呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函數來建立。</span><span class="sxs-lookup"><span data-stu-id="bd493-126">The page must first be created by a call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd493-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd493-127">Return value</span></span>

<span data-ttu-id="bd493-128">如果成功插入頁面，則會傳回非零值，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="bd493-128">Returns a nonzero value if the page was successfully inserted, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd493-129">備註</span><span class="sxs-lookup"><span data-stu-id="bd493-129">Remarks</span></span>

<span data-ttu-id="bd493-130">插入點之後的頁面會向右移動，以容納新的頁面。</span><span class="sxs-lookup"><span data-stu-id="bd493-130">The pages after the insertion point are shifted to the right to accommodate the new page.</span></span>

<span data-ttu-id="bd493-131">屬性工作表未調整大小以符合新的頁面。</span><span class="sxs-lookup"><span data-stu-id="bd493-131">The property sheet is not resized to fit the new page.</span></span> <span data-ttu-id="bd493-132">不要讓新的頁面大於屬性工作表的最大頁面。</span><span class="sxs-lookup"><span data-stu-id="bd493-132">Do not make the new page larger than the property sheet's largest page.</span></span>

<span data-ttu-id="bd493-133">當屬性工作表正在動作頁面清單時，會發生一些訊息和一個函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="bd493-133">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="bd493-134">當此動作執行時，嘗試修改頁面清單將會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="bd493-134">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="bd493-135">因此，您不應該 \_ 在 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 的執行中或在處理下列通知和 Windows 訊息時使用 PSM INSERTPAGE 訊息。</span><span class="sxs-lookup"><span data-stu-id="bd493-135">Accordingly, you should not use the PSM\_INSERTPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="bd493-136">PSN \_ APPLY</span><span class="sxs-lookup"><span data-stu-id="bd493-136">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="bd493-137">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="bd493-137">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="bd493-138">PSN \_ 重設</span><span class="sxs-lookup"><span data-stu-id="bd493-138">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="bd493-139">PSN \_ ADVANCED.FIELD.SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="bd493-139">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="bd493-140">**WM 損 \_ 毀**</span><span class="sxs-lookup"><span data-stu-id="bd493-140">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="bd493-141">**WM \_ INITDIALOG**</span><span class="sxs-lookup"><span data-stu-id="bd493-141">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="bd493-142">如果您在處理其中一個訊息時，或當 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 正在運作時需要修改屬性工作表頁面，請自行張貼私用 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="bd493-142">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="bd493-143">在屬性工作表管理員完成其工作之前，您的應用程式將不會收到該訊息。</span><span class="sxs-lookup"><span data-stu-id="bd493-143">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="bd493-144">然後您可以修改頁面清單。</span><span class="sxs-lookup"><span data-stu-id="bd493-144">Then you can modify the list of pages.</span></span>

<span data-ttu-id="bd493-145">下列通知也會受到屬性工作表修改的影響。</span><span class="sxs-lookup"><span data-stu-id="bd493-145">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="bd493-146">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="bd493-146">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="bd493-147">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="bd493-147">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="bd493-148">您可以新增或移除頁面，以回應這些通知，前提是您透過 DWL MSGRESULT 傳回 (， \_) 非零值來指定所需的新頁面。</span><span class="sxs-lookup"><span data-stu-id="bd493-148">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="bd493-149">但是請注意，如果您插入的頁面是在目前的頁面 (，其索引小於目前的頁面) ， [PSN \_ KILLACTIVE](psn-killactive.md) 可能會傳送至錯誤的頁面。</span><span class="sxs-lookup"><span data-stu-id="bd493-149">Note, however, that if you insert a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

> [!Note]  
> <span data-ttu-id="bd493-150">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="bd493-150">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd493-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd493-151">Requirements</span></span>



| <span data-ttu-id="bd493-152">需求</span><span class="sxs-lookup"><span data-stu-id="bd493-152">Requirement</span></span> | <span data-ttu-id="bd493-153">值</span><span class="sxs-lookup"><span data-stu-id="bd493-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd493-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd493-154">Minimum supported client</span></span><br/> | <span data-ttu-id="bd493-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd493-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bd493-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd493-156">Minimum supported server</span></span><br/> | <span data-ttu-id="bd493-157">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd493-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd493-158">標頭</span><span class="sxs-lookup"><span data-stu-id="bd493-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd493-159"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd493-159"><dt>Prsht.h</dt></span></span> </dl> |



 

