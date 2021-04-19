---
title: 'PSN_WIZNEXT (Prsht.idl 的通知碼) '
description: 通知頁面，表示使用者已按下 wizard 中的 [下一步] 按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 145591b725548ffc4175541fd37db8f285533590
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106993750"
---
# <a name="psn_wiznext-notification-code"></a><span data-ttu-id="f57c3-105">PSN \_ WIZNEXT 通知碼</span><span class="sxs-lookup"><span data-stu-id="f57c3-105">PSN\_WIZNEXT notification code</span></span>

<span data-ttu-id="f57c3-106">通知頁面，表示使用者已按下 wizard 中的 [ **下一步** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f57c3-106">Notifies a page that the user has clicked the **Next** button in a wizard.</span></span> <span data-ttu-id="f57c3-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f57c3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f57c3-108">參數</span><span class="sxs-lookup"><span data-stu-id="f57c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f57c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f57c3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f57c3-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f57c3-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="f57c3-111">此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f57c3-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="f57c3-112">**PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。</span><span class="sxs-lookup"><span data-stu-id="f57c3-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f57c3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f57c3-113">Return value</span></span>

<span data-ttu-id="f57c3-114">傳回0以允許 wizard 移至下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="f57c3-114">Return 0 to allow the wizard to go to the next page.</span></span> <span data-ttu-id="f57c3-115">傳回-1，以防止嚮導變更頁面。</span><span class="sxs-lookup"><span data-stu-id="f57c3-115">Return -1 to prevent the wizard from changing pages.</span></span> <span data-ttu-id="f57c3-116">若要顯示特定頁面，請傳回其對話資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f57c3-116">To display a particular page, return its dialog resource identifier.</span></span> <span data-ttu-id="f57c3-117">如果使用 [**PSP \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) 旗標來指定對話方塊，此通知會傳回對話方塊範本的指標。</span><span class="sxs-lookup"><span data-stu-id="f57c3-117">If the dialog was specified with the [**PSP\_DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) flag, this notification returns the pointer to the dialog template.</span></span>

## <a name="remarks"></a><span data-ttu-id="f57c3-118">備註</span><span class="sxs-lookup"><span data-stu-id="f57c3-118">Remarks</span></span>

<span data-ttu-id="f57c3-119">若要設定傳回值，頁面的對話方塊程式必須使用 **DWL \_ MSGRESULT** 值來呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f57c3-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the **DWL\_MSGRESULT** value and return **TRUE**.</span></span> <span data-ttu-id="f57c3-120">例如：</span><span class="sxs-lookup"><span data-stu-id="f57c3-120">For example:</span></span>

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> <span data-ttu-id="f57c3-121">屬性工作表正在處理 \_ 傳送 PSN WIZNEXT 通知碼時的頁面清單。</span><span class="sxs-lookup"><span data-stu-id="f57c3-121">The property sheet is in the process of manipulating the list of pages when the PSN\_WIZNEXT notification code is sent.</span></span> <span data-ttu-id="f57c3-122">您可以新增、插入或移除頁面以回應這些通知碼，但如果您在目前頁面之前插入或移除頁面，就必須特別小心。</span><span class="sxs-lookup"><span data-stu-id="f57c3-122">You can add, insert, or remove pages in response to these notification codes, but special care must be taken if you insert or remove pages before the current page.</span></span>

 

<span data-ttu-id="f57c3-123">如果您插入或移除目前頁面之前的頁面，您必須透過 **DWL \_ MSGRESULT** 傳回 () 非零值，以指定所需的新頁面。</span><span class="sxs-lookup"><span data-stu-id="f57c3-123">If you insert or remove pages before the current page, you must return (through **DWL\_MSGRESULT**) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="f57c3-124">但是請注意，如果您插入或移除目前頁面之前的頁面 (，其索引小於目前的頁面) ， [PSN \_ KILLACTIVE](psn-killactive.md) 可能會傳送至錯誤的頁面。</span><span class="sxs-lookup"><span data-stu-id="f57c3-124">Note, however, that if you insert or remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

<span data-ttu-id="f57c3-125">基於這個理由，建議在回應 PSN WIZNEXT 和 PSN WIZBACK 的情況下，動態新增和移除頁面的程式， \_ 只對清單結尾的頁面這麼 [ \_ ](psn-wizback.md) 做。</span><span class="sxs-lookup"><span data-stu-id="f57c3-125">For this reason, it is recommended that wizards that add and remove pages dynamically in response to PSN\_WIZNEXT and [PSN\_WIZBACK](psn-wizback.md) do so only to pages at the end of the list.</span></span> <span data-ttu-id="f57c3-126">如果您想要讓您的嚮導正確地移除頁面，請將動態頁面保留在清單結尾，然後跳回永久頁面，然後再加以刪除。</span><span class="sxs-lookup"><span data-stu-id="f57c3-126">If you want your wizard to remove pages accurately, keep the dynamic pages at the end of the list and jump back to permanent pages before deleting them.</span></span>

<span data-ttu-id="f57c3-127">例如，假設 wizard 包含一個簡介頁面、一系列的動態頁面和一個完成頁面，而且您想要在使用者到達完成頁面時刪除動態頁面。</span><span class="sxs-lookup"><span data-stu-id="f57c3-127">For example, suppose a wizard consists of an introductory page, a series of dynamic pages, and a completion page, and you want to delete the dynamic pages when the user reaches the completion page.</span></span>

1.  <span data-ttu-id="f57c3-128">Wizard 會從兩個頁面開始：「簡介」和「完成」。</span><span class="sxs-lookup"><span data-stu-id="f57c3-128">The wizard would begin with two pages, "Introduction" and "Completion."</span></span> <span data-ttu-id="f57c3-129">使用者會在 [簡介] 頁面上開始。</span><span class="sxs-lookup"><span data-stu-id="f57c3-129">The user begins on the "Introduction" page.</span></span>
    1.  <span data-ttu-id="f57c3-130"> (使用者的簡介) </span><span class="sxs-lookup"><span data-stu-id="f57c3-130">Introduction (User is here)</span></span>
    2.  <span data-ttu-id="f57c3-131">Completion</span><span class="sxs-lookup"><span data-stu-id="f57c3-131">Completion</span></span>
2.  <span data-ttu-id="f57c3-132">當使用者離開 [簡介] 時，嚮導會新增動態頁面，並將使用者放在第一個動態頁面，方法是透過 **DWL \_ MSGRESULT** 傳回 (，) [動態 1] 頁面的對話識別碼。</span><span class="sxs-lookup"><span data-stu-id="f57c3-132">When the user navigates away from "Introduction," the wizard adds the dynamic pages and places the user at the first dynamic page by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Dynamic 1."</span></span> <span data-ttu-id="f57c3-133">在此範例中，有三個動態頁面。</span><span class="sxs-lookup"><span data-stu-id="f57c3-133">In this example, there are three dynamic pages.</span></span>
    1.  <span data-ttu-id="f57c3-134">簡介</span><span class="sxs-lookup"><span data-stu-id="f57c3-134">Introduction</span></span>
    2.  <span data-ttu-id="f57c3-135">Completion</span><span class="sxs-lookup"><span data-stu-id="f57c3-135">Completion</span></span>
    3.  <span data-ttu-id="f57c3-136">動態 1 (使用者在此) </span><span class="sxs-lookup"><span data-stu-id="f57c3-136">Dynamic 1 (User is here)</span></span>
    4.  <span data-ttu-id="f57c3-137">動態2</span><span class="sxs-lookup"><span data-stu-id="f57c3-137">Dynamic 2</span></span>
    5.  <span data-ttu-id="f57c3-138">動態3</span><span class="sxs-lookup"><span data-stu-id="f57c3-138">Dynamic 3</span></span>
3.  <span data-ttu-id="f57c3-139">當使用者流覽動態頁面至「動態3」，然後流覽至下一個頁面之後，應用程式應該將使用者放在頁面「完成」。</span><span class="sxs-lookup"><span data-stu-id="f57c3-139">After the user navigates through the dynamic pages to "Dynamic 3" and then navigates to the next page, the application should place the user at the page "Completion."</span></span> <span data-ttu-id="f57c3-140">同樣地，這是透過 **DWL \_ MSGRESULT** 傳回 (，) [完成] 頁面的對話方塊識別碼來完成。</span><span class="sxs-lookup"><span data-stu-id="f57c3-140">Again, this is done by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Completion."</span></span>
    1.  <span data-ttu-id="f57c3-141">簡介</span><span class="sxs-lookup"><span data-stu-id="f57c3-141">Introduction</span></span>
    2.  <span data-ttu-id="f57c3-142"> (使用者的完成) </span><span class="sxs-lookup"><span data-stu-id="f57c3-142">Completion (User is here)</span></span>
    3.  <span data-ttu-id="f57c3-143">動態1</span><span class="sxs-lookup"><span data-stu-id="f57c3-143">Dynamic 1</span></span>
    4.  <span data-ttu-id="f57c3-144">動態2</span><span class="sxs-lookup"><span data-stu-id="f57c3-144">Dynamic 2</span></span>
    5.  <span data-ttu-id="f57c3-145">動態3</span><span class="sxs-lookup"><span data-stu-id="f57c3-145">Dynamic 3</span></span>
4.  <span data-ttu-id="f57c3-146">然後，應用程式可以將三個動態頁面 (編號的三至五) 安全地移除。</span><span class="sxs-lookup"><span data-stu-id="f57c3-146">The application can then remove the three dynamic pages (numbered three through five) safely.</span></span>
    1.  <span data-ttu-id="f57c3-147">簡介</span><span class="sxs-lookup"><span data-stu-id="f57c3-147">Introduction</span></span>
    2.  <span data-ttu-id="f57c3-148"> (使用者的完成) </span><span class="sxs-lookup"><span data-stu-id="f57c3-148">Completion (User is here)</span></span>

<span data-ttu-id="f57c3-149">請注意，只有在您的 wizard 動態移除頁面時，才需要這項技術。</span><span class="sxs-lookup"><span data-stu-id="f57c3-149">Note that this technique is necessary only if your wizard removes pages dynamically.</span></span> <span data-ttu-id="f57c3-150">如果您的 wizard 只動態新增頁面，則不需要此程式。</span><span class="sxs-lookup"><span data-stu-id="f57c3-150">If your wizard only adds pages dynamically, this process is not necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="f57c3-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="f57c3-151">Requirements</span></span>



| <span data-ttu-id="f57c3-152">需求</span><span class="sxs-lookup"><span data-stu-id="f57c3-152">Requirement</span></span> | <span data-ttu-id="f57c3-153">值</span><span class="sxs-lookup"><span data-stu-id="f57c3-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f57c3-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f57c3-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f57c3-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f57c3-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f57c3-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f57c3-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f57c3-157">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f57c3-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f57c3-158">標頭</span><span class="sxs-lookup"><span data-stu-id="f57c3-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="f57c3-159"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f57c3-159"><dt>Prsht.h</dt></span></span> </dl> |



 

