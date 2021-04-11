---
description: 當使用者執行筆觸時傳送。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: 'WM_TABLET_FLICK 訊息 (Tpcshrd .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191296"
---
# <a name="wm_tablet_flick-message"></a><span data-ttu-id="78524-104">WM \_ TABLET \_ 筆鋒訊息</span><span class="sxs-lookup"><span data-stu-id="78524-104">WM\_TABLET\_FLICK message</span></span>

<span data-ttu-id="78524-105">當使用者執行筆觸時傳送。</span><span class="sxs-lookup"><span data-stu-id="78524-105">Sent when a user performs a pen flick.</span></span> <span data-ttu-id="78524-106">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="78524-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a><span data-ttu-id="78524-107">參數</span><span class="sxs-lookup"><span data-stu-id="78524-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78524-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78524-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78524-109">[**筆鋒 \_ 資料結構**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)，其中包含所發生之筆觸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78524-109">A [**FLICK\_DATA Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) that contains information about the pen flick that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="78524-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78524-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78524-111">指定手寫筆筆觸發生位置的 [**筆鋒 \_ 點結構**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) 。</span><span class="sxs-lookup"><span data-stu-id="78524-111">The [**FLICK\_POINT Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) that specifies where the pen flick occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78524-112">備註</span><span class="sxs-lookup"><span data-stu-id="78524-112">Remarks</span></span>

<span data-ttu-id="78524-113">筆觸是一個單向畫筆手勢，要求使用者在快速、直接撥動的動作中與數位板聯繫。</span><span class="sxs-lookup"><span data-stu-id="78524-113">A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion.</span></span> <span data-ttu-id="78524-114">筆勢的特性是高速和高度的 straightness。</span><span class="sxs-lookup"><span data-stu-id="78524-114">A flick is characterized by high speed and a high degree of straightness.</span></span> <span data-ttu-id="78524-115">筆觸是由其方向來識別。</span><span class="sxs-lookup"><span data-stu-id="78524-115">A flick is identified by its direction.</span></span> <span data-ttu-id="78524-116">您可以用對應至基線和次要羅盤方向的八個方向來進行筆觸。</span><span class="sxs-lookup"><span data-stu-id="78524-116">Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.</span></span>

<span data-ttu-id="78524-117">當筆觸出現時，Windows 會先傳送 **WM \_ TABLET \_ 筆鋒** 訊息（視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函式接收）來通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="78524-117">When a pen flick occurs, Windows first notifies an application by sending a **WM\_TABLET\_FLICK** message, which a window receives through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="78524-118">傳回「 **筆觸 \_ WM \_ 處理的 \_ 遮罩** 常數」（如 [筆觸常數](flicks-constants.md)中所述），以表示應用程式已回應 **WM \_ TABLET \_ 筆鋒** 訊息。</span><span class="sxs-lookup"><span data-stu-id="78524-118">Return the **FLICK\_WM\_HANDLED\_MASK** constant, described in [Flicks Constants](flicks-constants.md), to indicate that the application responded to the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="78524-119">如果應用程式未傳回筆觸 **\_ WM \_ 處理的 \_ 遮罩**，則 Windows 會根據與手寫筆筆觸相關聯的動作傳送後續通知（例如 [**Wm \_ APPCOMMAND**](../inputdev/wm-appcommand.md)、 [**wm \_ VSCROLL**](../controls/wm-vscroll.md)或 [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md)），來執行筆觸控制台中指定的預設動作。</span><span class="sxs-lookup"><span data-stu-id="78524-119">If the application does not return **FLICK\_WM\_HANDLED\_MASK**, Windows performs the default action specified in the flicks control panel by sending a follow-up notification, such as [**WM\_APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM\_VSCROLL**](../controls/wm-vscroll.md), or [**WM\_KEYDOWN**](../inputdev/wm-keydown.md), depending on which action is associated with the pen flick.</span></span>

<span data-ttu-id="78524-120">處理 **WM \_ TABLET 筆觸 \_** 訊息時，請特別小心。</span><span class="sxs-lookup"><span data-stu-id="78524-120">Use caution when handling the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="78524-121">**WM \_TABLET \_ 筆觸** 是經由 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) 函式傳遞。</span><span class="sxs-lookup"><span data-stu-id="78524-121">**WM\_TABLET\_FLICK** is passed via the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="78524-122">如果您呼叫 COM 介面上的方法，該物件必須在相同的進程中。</span><span class="sxs-lookup"><span data-stu-id="78524-122">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="78524-123">如果不是，COM 會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="78524-123">If not, COM throws an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="78524-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="78524-124">Requirements</span></span>



| <span data-ttu-id="78524-125">需求</span><span class="sxs-lookup"><span data-stu-id="78524-125">Requirement</span></span> | <span data-ttu-id="78524-126">值</span><span class="sxs-lookup"><span data-stu-id="78524-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="78524-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78524-127">Minimum supported client</span></span><br/> | <span data-ttu-id="78524-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78524-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="78524-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78524-129">Minimum supported server</span></span><br/> | <span data-ttu-id="78524-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78524-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="78524-131">標頭</span><span class="sxs-lookup"><span data-stu-id="78524-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="78524-132"><dt>Tpcshrd。h</dt></span><span class="sxs-lookup"><span data-stu-id="78524-132"><dt>Tpcshrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78524-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78524-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78524-134">**筆鋒 \_ 資料結構**</span><span class="sxs-lookup"><span data-stu-id="78524-134">**flick\_data structure**</span></span>](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[<span data-ttu-id="78524-135">**wm \_ tablet \_ 筆鋒訊息**</span><span class="sxs-lookup"><span data-stu-id="78524-135">**wm\_tablet\_flick message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="78524-136">筆觸手勢</span><span class="sxs-lookup"><span data-stu-id="78524-136">flicks gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="78524-137">[回應觸控筆觸](/previous-versions/windows/desktop/ms703447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78524-137">[responding to pen flicks](/previous-versions/windows/desktop/ms703447(v=vs.85))</span></span>
</dt> </dl>

 

 
