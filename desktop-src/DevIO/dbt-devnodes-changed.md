---
description: 系統已 \_ 新增或移除裝置時，系統會將 DBT DEVNODES \_ 變更裝置事件廣播。 維護系統中裝置清單的應用程式應該重新整理其清單。
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: 'DBT_DEVNODES_CHANGED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110693"
---
# <a name="dbt_devnodes_changed-event"></a><span data-ttu-id="3435f-104">DBT \_ DEVNODES \_ 已變更事件</span><span class="sxs-lookup"><span data-stu-id="3435f-104">DBT\_DEVNODES\_CHANGED event</span></span>

<span data-ttu-id="3435f-105">系統已 \_ 新增或移除裝置時，系統會將 DBT DEVNODES \_ 變更裝置事件廣播。</span><span class="sxs-lookup"><span data-stu-id="3435f-105">The system broadcasts the DBT\_DEVNODES\_CHANGED device event when a device has been added to or removed from the system.</span></span> <span data-ttu-id="3435f-106">維護系統中裝置清單的應用程式應該重新整理其清單。</span><span class="sxs-lookup"><span data-stu-id="3435f-106">Applications that maintain lists of devices in the system should refresh their lists.</span></span>

<span data-ttu-id="3435f-107">若要廣播此裝置事件，系統會使用 *wParam* 設定為 DBT DEVNODES [**\_**](wm-devicechange.md) \_ \_ 變更且 *lParam* 設定為零的 WM DEVICECHANGE 訊息。</span><span class="sxs-lookup"><span data-stu-id="3435f-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVNODES\_CHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="3435f-108">參數</span><span class="sxs-lookup"><span data-stu-id="3435f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3435f-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="3435f-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="3435f-110">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="3435f-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="3435f-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="3435f-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="3435f-112">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="3435f-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3435f-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3435f-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3435f-114">設定為 DBT \_ DEVNODES \_ 已變更。</span><span class="sxs-lookup"><span data-stu-id="3435f-114">Set to DBT\_DEVNODES\_CHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="3435f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3435f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3435f-116">設定為零。</span><span class="sxs-lookup"><span data-stu-id="3435f-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3435f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3435f-117">Return value</span></span>

<span data-ttu-id="3435f-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="3435f-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3435f-119">備註</span><span class="sxs-lookup"><span data-stu-id="3435f-119">Remarks</span></span>

<span data-ttu-id="3435f-120">在系統中新增或移除的裝置沒有其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3435f-120">There is no additional information about which device has been added to or removed from the system.</span></span> <span data-ttu-id="3435f-121">需要詳細資訊的應用程式應該使用 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 函式來註冊裝置通知。</span><span class="sxs-lookup"><span data-stu-id="3435f-121">Applications that require more information should register for device notification using the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3435f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3435f-122">Requirements</span></span>



| <span data-ttu-id="3435f-123">需求</span><span class="sxs-lookup"><span data-stu-id="3435f-123">Requirement</span></span> | <span data-ttu-id="3435f-124">值</span><span class="sxs-lookup"><span data-stu-id="3435f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3435f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3435f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3435f-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3435f-126">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="3435f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3435f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3435f-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3435f-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="3435f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3435f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3435f-130"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="3435f-130"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3435f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3435f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3435f-132">裝置事件</span><span class="sxs-lookup"><span data-stu-id="3435f-132">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="3435f-133">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="3435f-133">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="3435f-134">**開發 \_ 廣播 \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="3435f-134">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="3435f-135">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="3435f-135">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




