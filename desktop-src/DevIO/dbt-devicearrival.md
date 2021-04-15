---
description: '\_當裝置或媒體已插入並可供使用時，系統會廣播 DBT DEVICEARRIVAL 裝置事件。'
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: 'DBT_DEVICEARRIVAL (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69c2feec996b4306c271454767ca4e75d1ff855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468225"
---
# <a name="dbt_devicearrival-event"></a><span data-ttu-id="7a61e-103">DBT \_ DEVICEARRIVAL 事件</span><span class="sxs-lookup"><span data-stu-id="7a61e-103">DBT\_DEVICEARRIVAL event</span></span>

<span data-ttu-id="7a61e-104">\_當裝置或媒體已插入並可供使用時，系統會廣播 DBT DEVICEARRIVAL 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="7a61e-104">The system broadcasts the DBT\_DEVICEARRIVAL device event when a device or piece of media has been inserted and becomes available.</span></span>

<span data-ttu-id="7a61e-105">若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICEARRIVAL 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 </span><span class="sxs-lookup"><span data-stu-id="7a61e-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEARRIVAL and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="7a61e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a61e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a61e-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="7a61e-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7a61e-108">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="7a61e-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="7a61e-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="7a61e-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="7a61e-110">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a61e-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7a61e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a61e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a61e-112">設定為 DBT \_ DEVICEARRIVAL。</span><span class="sxs-lookup"><span data-stu-id="7a61e-112">Set to DBT\_DEVICEARRIVAL.</span></span>

</dd> <dt>

<span data-ttu-id="7a61e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a61e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a61e-114">結構的指標，識別所插入的裝置。</span><span class="sxs-lookup"><span data-stu-id="7a61e-114">A pointer to a structure identifying the device inserted.</span></span> <span data-ttu-id="7a61e-115">此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。</span><span class="sxs-lookup"><span data-stu-id="7a61e-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="7a61e-116">若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。</span><span class="sxs-lookup"><span data-stu-id="7a61e-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a61e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a61e-117">Return value</span></span>

<span data-ttu-id="7a61e-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7a61e-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a61e-119">備註</span><span class="sxs-lookup"><span data-stu-id="7a61e-119">Remarks</span></span>

<span data-ttu-id="7a61e-120">如果正在插入媒體，則抵達的裝置類型為磁片區， (**dbch \_ devicetype** 成員是 DBT \_ DEVTYP \_ volume) ，而 **dbcv \_ 旗標** 成員 (媒體) 的變更效果 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7a61e-120">If media is being inserted, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="7a61e-121">範例</span><span class="sxs-lookup"><span data-stu-id="7a61e-121">Examples</span></span>

<span data-ttu-id="7a61e-122">如需範例，請參閱偵測 [媒體插入或移除](detecting-media-insertion-or-removal.md)。</span><span class="sxs-lookup"><span data-stu-id="7a61e-122">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a61e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a61e-123">Requirements</span></span>



| <span data-ttu-id="7a61e-124">需求</span><span class="sxs-lookup"><span data-stu-id="7a61e-124">Requirement</span></span> | <span data-ttu-id="7a61e-125">值</span><span class="sxs-lookup"><span data-stu-id="7a61e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7a61e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a61e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7a61e-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a61e-127">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="7a61e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a61e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7a61e-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a61e-129">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="7a61e-130">標頭</span><span class="sxs-lookup"><span data-stu-id="7a61e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a61e-131"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a61e-131"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a61e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a61e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a61e-133">裝置事件</span><span class="sxs-lookup"><span data-stu-id="7a61e-133">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="7a61e-134">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="7a61e-134">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="7a61e-135">**開發 \_ 廣播 \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="7a61e-135">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="7a61e-136">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="7a61e-136">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




