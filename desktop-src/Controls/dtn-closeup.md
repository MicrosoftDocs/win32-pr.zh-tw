---
title: 'DTN_CLOSEUP (Commctrl 的通知碼) '
description: 由日期和時間選擇器所傳送 (DTP) 控制使用者何時關閉下拉式月曆。
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686240"
---
# <a name="dtn_closeup-notification-code"></a><span data-ttu-id="e19fa-104">DTN \_ 特寫通知碼</span><span class="sxs-lookup"><span data-stu-id="e19fa-104">DTN\_CLOSEUP notification code</span></span>

<span data-ttu-id="e19fa-105">由日期和時間選擇器所傳送 (DTP) 控制使用者何時關閉下拉式月曆。</span><span class="sxs-lookup"><span data-stu-id="e19fa-105">Sent by a date and time picker (DTP) control when the user closes the drop-down month calendar.</span></span> <span data-ttu-id="e19fa-106">當使用者選擇月曆中的日期，或在行事曆開啟時按一下下拉箭號時，就會關閉月曆。</span><span class="sxs-lookup"><span data-stu-id="e19fa-106">The month calendar is closed when the user chooses a date from the month calendar or clicks the drop-down arrow while the calendar is open.</span></span> <span data-ttu-id="e19fa-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e19fa-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="e19fa-108">參數</span><span class="sxs-lookup"><span data-stu-id="e19fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e19fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e19fa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e19fa-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e19fa-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e19fa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e19fa-111">Return value</span></span>

<span data-ttu-id="e19fa-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="e19fa-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e19fa-113">備註</span><span class="sxs-lookup"><span data-stu-id="e19fa-113">Remarks</span></span>

<span data-ttu-id="e19fa-114">DTP 控制項不會維護靜態的子月份行事曆控制項。</span><span class="sxs-lookup"><span data-stu-id="e19fa-114">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="e19fa-115">在傳送此通知碼之前，DTP 控制項會終結子月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="e19fa-115">The DTP control destroys the child month calendar control prior to sending this notification code.</span></span> <span data-ttu-id="e19fa-116">因此，您的應用程式不能依賴控制項之子月份行事曆的靜態視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="e19fa-116">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="e19fa-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e19fa-117">Requirements</span></span>



| <span data-ttu-id="e19fa-118">需求</span><span class="sxs-lookup"><span data-stu-id="e19fa-118">Requirement</span></span> | <span data-ttu-id="e19fa-119">值</span><span class="sxs-lookup"><span data-stu-id="e19fa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e19fa-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e19fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e19fa-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e19fa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e19fa-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e19fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e19fa-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e19fa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e19fa-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e19fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e19fa-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e19fa-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e19fa-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e19fa-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e19fa-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="e19fa-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e19fa-128">DTN \_ 下拉式清單</span><span class="sxs-lookup"><span data-stu-id="e19fa-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="e19fa-129">**DTM \_ GETMONTHCAL**</span><span class="sxs-lookup"><span data-stu-id="e19fa-129">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

 





