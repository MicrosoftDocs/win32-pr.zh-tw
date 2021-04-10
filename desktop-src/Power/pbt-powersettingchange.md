---
description: 使用 WM \_ POWERBROADCAST 視窗訊息或服務的 HandlerEx 通知回呼傳送的電源設定變更事件。
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: 'PBT_POWERSETTINGCHANGE (WinUser 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849266"
---
# <a name="pbt_powersettingchange-event"></a><span data-ttu-id="92623-103">PBT \_ POWERSETTINGCHANGE 事件</span><span class="sxs-lookup"><span data-stu-id="92623-103">PBT\_POWERSETTINGCHANGE event</span></span>

<span data-ttu-id="92623-104">使用 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 視窗訊息或服務的 [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) 通知回呼傳送的電源設定變更事件。</span><span class="sxs-lookup"><span data-stu-id="92623-104">Power setting change event sent with a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) window message or in a [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) notification callback for services.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
```



## <a name="parameters"></a><span data-ttu-id="92623-105">參數</span><span class="sxs-lookup"><span data-stu-id="92623-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92623-106">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="92623-106">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="92623-107">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="92623-107">A handle to window.</span></span>

<span data-ttu-id="92623-108"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="92623-108"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="92623-109">值</span><span class="sxs-lookup"><span data-stu-id="92623-109">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="92623-110">意義</span><span class="sxs-lookup"><span data-stu-id="92623-110">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="92623-111"><dt>**[**WM \_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="92623-111"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="92623-112">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="92623-112">Message identifier.</span></span><br/> |



 

<span data-ttu-id="92623-113"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="92623-113"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="92623-114">值</span><span class="sxs-lookup"><span data-stu-id="92623-114">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="92623-115">意義</span><span class="sxs-lookup"><span data-stu-id="92623-115">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="92623-116"><dt>**PBT \_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="92623-116"><dt>**PBT\_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span></span> </dl> | <span data-ttu-id="92623-117">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="92623-117">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="92623-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92623-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92623-119">[**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="92623-119">Pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92623-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="92623-120">Return value</span></span>

<span data-ttu-id="92623-121">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="92623-121">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="92623-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="92623-122">Requirements</span></span>



| <span data-ttu-id="92623-123">需求</span><span class="sxs-lookup"><span data-stu-id="92623-123">Requirement</span></span> | <span data-ttu-id="92623-124">值</span><span class="sxs-lookup"><span data-stu-id="92623-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92623-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92623-125">Minimum supported client</span></span><br/> | <span data-ttu-id="92623-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92623-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="92623-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92623-127">Minimum supported server</span></span><br/> | <span data-ttu-id="92623-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92623-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="92623-129">標頭</span><span class="sxs-lookup"><span data-stu-id="92623-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="92623-130"><dt>WinUser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="92623-130"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92623-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92623-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92623-132">電源管理事件</span><span class="sxs-lookup"><span data-stu-id="92623-132">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="92623-133">**HandlerEx**</span><span class="sxs-lookup"><span data-stu-id="92623-133">**HandlerEx**</span></span>](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[<span data-ttu-id="92623-134">**WM \_ POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="92623-134">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> <dt>

[<span data-ttu-id="92623-135">**POWERBROADCAST \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="92623-135">**POWERBROADCAST\_SETTING**</span></span>](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

