---
title: 'DTN_DROPDOWN (Commctrl 的通知碼) '
description: 當使用者啟動下拉式月曆時，日期和時間選擇器會傳送 (DTP) 控制。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843936"
---
# <a name="dtn_dropdown-notification-code"></a><span data-ttu-id="31e4d-105">DTN \_ 下拉式通知碼</span><span class="sxs-lookup"><span data-stu-id="31e4d-105">DTN\_DROPDOWN notification code</span></span>

<span data-ttu-id="31e4d-106">當使用者啟動下拉式月曆時，日期和時間選擇器會傳送 (DTP) 控制。</span><span class="sxs-lookup"><span data-stu-id="31e4d-106">Sent by a date and time picker (DTP) control when the user activates the drop-down month calendar.</span></span> <span data-ttu-id="31e4d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="31e4d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="31e4d-108">參數</span><span class="sxs-lookup"><span data-stu-id="31e4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e4d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31e4d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31e4d-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31e4d-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e4d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="31e4d-111">Return value</span></span>

<span data-ttu-id="31e4d-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="31e4d-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="31e4d-113">備註</span><span class="sxs-lookup"><span data-stu-id="31e4d-113">Remarks</span></span>

<span data-ttu-id="31e4d-114">您的通知處理常式可能需要執行的一項工作，是自訂下拉式月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="31e4d-114">One task that your notification handler may need to perform is to customize the dropdown month-calendar control.</span></span> <span data-ttu-id="31e4d-115">比方說，如果您不想要「移到今天」，則必須設定控制項的 [**MCS \_ NOTODAY**](month-calendar-control-styles.md)  樣式。</span><span class="sxs-lookup"><span data-stu-id="31e4d-115">For instance, if you do not want "Go To Today," you need to set the control's [**MCS\_NOTODAY**](month-calendar-control-styles.md)  style.</span></span> <span data-ttu-id="31e4d-116">若要取出月曆控制項的控制碼，請將該 DTP [**\_ GETMONTHCAL**](dtm-getmonthcal.md) 訊息傳送給 DTP。</span><span class="sxs-lookup"><span data-stu-id="31e4d-116">To retrieve a handle to the month-calendar control, send the DTP control a [**DTM\_GETMONTHCAL**](dtm-getmonthcal.md) message.</span></span> <span data-ttu-id="31e4d-117">然後，您可以使用此控制碼和 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 來設定所需的月曆樣式。</span><span class="sxs-lookup"><span data-stu-id="31e4d-117">You can then use this handle and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) to set the desired month-calendar style.</span></span>

<span data-ttu-id="31e4d-118">DTP 控制項不會維護靜態的子月份行事曆控制項。</span><span class="sxs-lookup"><span data-stu-id="31e4d-118">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="31e4d-119">在傳送此通知碼之前，將會建立新的月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="31e4d-119">The DTP control creates a new month calendar control before sending this notification code.</span></span> <span data-ttu-id="31e4d-120">此外，當 (可見) 時，DTP 控制項會終結子控制項。</span><span class="sxs-lookup"><span data-stu-id="31e4d-120">Additionally, the DTP control destroys the child control when it is not active (visible).</span></span> <span data-ttu-id="31e4d-121">因此，您的應用程式不能依賴控制項之子月份行事曆的靜態視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="31e4d-121">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e4d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="31e4d-122">Requirements</span></span>



| <span data-ttu-id="31e4d-123">需求</span><span class="sxs-lookup"><span data-stu-id="31e4d-123">Requirement</span></span> | <span data-ttu-id="31e4d-124">值</span><span class="sxs-lookup"><span data-stu-id="31e4d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31e4d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31e4d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="31e4d-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31e4d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31e4d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31e4d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="31e4d-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31e4d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31e4d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="31e4d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e4d-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="31e4d-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e4d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31e4d-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="31e4d-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="31e4d-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="31e4d-133">DTN \_ 特寫</span><span class="sxs-lookup"><span data-stu-id="31e4d-133">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="31e4d-134">**DTM \_ GETMONTHCAL**</span><span class="sxs-lookup"><span data-stu-id="31e4d-134">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

