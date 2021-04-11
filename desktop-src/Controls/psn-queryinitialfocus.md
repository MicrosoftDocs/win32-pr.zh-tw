---
title: 'PSN_QUERYINITIALFOCUS (Prsht.idl 的通知碼) '
description: 由屬性工作表傳送以提供屬性工作表頁面，有機會指定哪個對話方塊控制項應該接收初始焦點。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093923"
---
# <a name="psn_queryinitialfocus-notification-code"></a><span data-ttu-id="cddfe-105">PSN \_ QUERYINITIALFOCUS 通知碼</span><span class="sxs-lookup"><span data-stu-id="cddfe-105">PSN\_QUERYINITIALFOCUS notification code</span></span>

<span data-ttu-id="cddfe-106">由屬性工作表傳送以提供屬性工作表頁面，有機會指定哪個對話方塊控制項應該接收初始焦點。</span><span class="sxs-lookup"><span data-stu-id="cddfe-106">Sent by a property sheet to provide a property sheet page an opportunity to specify which dialog box control should receive the initial focus.</span></span> <span data-ttu-id="cddfe-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="cddfe-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cddfe-108">參數</span><span class="sxs-lookup"><span data-stu-id="cddfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cddfe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cddfe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cddfe-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cddfe-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure.</span></span> <span data-ttu-id="cddfe-111">將此結構的 **lParam** 成員轉換成 **HWND** 型別，以抓取預設將會獲得焦點的控制項控點。</span><span class="sxs-lookup"><span data-stu-id="cddfe-111">Cast the **lParam** member of this structure to an **HWND** type, to retrieve the handle of the control that will be given focus by default.</span></span> <span data-ttu-id="cddfe-112">結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cddfe-112">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cddfe-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cddfe-113">Return value</span></span>

<span data-ttu-id="cddfe-114">若要指定哪個控制項應獲得焦點，請傳回控制項的控點。</span><span class="sxs-lookup"><span data-stu-id="cddfe-114">To specify which control should receive focus, return the control's handle.</span></span> <span data-ttu-id="cddfe-115">否則，傳回零，焦點將會移至預設控制項。</span><span class="sxs-lookup"><span data-stu-id="cddfe-115">Otherwise, return zero and focus will go to the default control.</span></span> <span data-ttu-id="cddfe-116">若要設定傳回值，對話方塊程式必須使用 **DWL \_ MSGRESULT** 值來呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="cddfe-116">To set the return value, the dialog box procedure must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a **DWL\_MSGRESULT** value and return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cddfe-117">備註</span><span class="sxs-lookup"><span data-stu-id="cddfe-117">Remarks</span></span>

<span data-ttu-id="cddfe-118">處理此通知程式碼時，應用程式不能呼叫 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數。</span><span class="sxs-lookup"><span data-stu-id="cddfe-118">An application must not call the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function while handling this notification code.</span></span> <span data-ttu-id="cddfe-119">傳回應取得焦點之控制項的控制碼，而屬性工作表管理員將會處理焦點變更。</span><span class="sxs-lookup"><span data-stu-id="cddfe-119">Return the handle of the control that should receive focus, and the property sheet manager will handle the focus change.</span></span>

<span data-ttu-id="cddfe-120">\_如果屬性工作表管理員判斷頁面上沒有任何控制項應該取得焦點，則不會傳送 PSN QUERYINITIALFOCUS 通知碼。</span><span class="sxs-lookup"><span data-stu-id="cddfe-120">The PSN\_QUERYINITIALFOCUS notification code is not sent if the property sheet manager determines that no control on the page should receive focus.</span></span>

<span data-ttu-id="cddfe-121">此程式碼片段會針對 PSN QUERYINITIALFOCUS 執行簡單的處理常式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cddfe-121">This code fragment implements a simple handler for PSN\_QUERYINITIALFOCUS.</span></span> <span data-ttu-id="cddfe-122">它會要求將初始焦點提供給 (**IDC \_ 位置**) 的位置控制項。</span><span class="sxs-lookup"><span data-stu-id="cddfe-122">It requests that initial focus be given to the Location control (**IDC\_LOCATION**).</span></span>

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> <span data-ttu-id="cddfe-123">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此通知碼。</span><span class="sxs-lookup"><span data-stu-id="cddfe-123">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cddfe-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cddfe-124">Requirements</span></span>



| <span data-ttu-id="cddfe-125">需求</span><span class="sxs-lookup"><span data-stu-id="cddfe-125">Requirement</span></span> | <span data-ttu-id="cddfe-126">值</span><span class="sxs-lookup"><span data-stu-id="cddfe-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cddfe-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cddfe-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cddfe-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cddfe-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cddfe-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cddfe-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cddfe-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cddfe-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cddfe-131">標頭</span><span class="sxs-lookup"><span data-stu-id="cddfe-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cddfe-132"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cddfe-132"><dt>Prsht.h</dt></span></span> </dl> |



 

