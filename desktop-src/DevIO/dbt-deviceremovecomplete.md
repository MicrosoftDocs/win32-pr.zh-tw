---
description: '\_當實際移除裝置或媒體時，系統會廣播 DBT DEVICEREMOVECOMPLETE 裝置事件。'
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: 'DBT_DEVICEREMOVECOMPLETE (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973778"
---
# <a name="dbt_deviceremovecomplete-event"></a><span data-ttu-id="339e4-103">DBT \_ DEVICEREMOVECOMPLETE 事件</span><span class="sxs-lookup"><span data-stu-id="339e4-103">DBT\_DEVICEREMOVECOMPLETE event</span></span>

<span data-ttu-id="339e4-104">\_當實際移除裝置或媒體時，系統會廣播 DBT DEVICEREMOVECOMPLETE 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="339e4-104">The system broadcasts the DBT\_DEVICEREMOVECOMPLETE device event when a device or piece of media has been physically removed.</span></span>

<span data-ttu-id="339e4-105">若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICEREMOVECOMPLETE 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 </span><span class="sxs-lookup"><span data-stu-id="339e4-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVECOMPLETE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="339e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="339e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="339e4-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="339e4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="339e4-108">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="339e4-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="339e4-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="339e4-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="339e4-110">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="339e4-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="339e4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="339e4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="339e4-112">設定為 DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="339e4-112">Set to DBT\_DEVICEREMOVECOMPLETE</span></span>

</dd> <dt>

<span data-ttu-id="339e4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="339e4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="339e4-114">識別已移除裝置之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="339e4-114">A pointer to a structure identifying the device removed.</span></span> <span data-ttu-id="339e4-115">此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。</span><span class="sxs-lookup"><span data-stu-id="339e4-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="339e4-116">若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。</span><span class="sxs-lookup"><span data-stu-id="339e4-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="339e4-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="339e4-117">Return value</span></span>

<span data-ttu-id="339e4-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="339e4-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="339e4-119">備註</span><span class="sxs-lookup"><span data-stu-id="339e4-119">Remarks</span></span>

<span data-ttu-id="339e4-120">系統可能會廣播 DBT \_ DEVICEREMOVECOMPLETE 訊息，而不會傳送對應的 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 和 [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="339e4-120">The system may broadcast a DBT\_DEVICEREMOVECOMPLETE message without sending corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) messages.</span></span> <span data-ttu-id="339e4-121">在這種情況下，應用程式和驅動程式必須盡可能地從裝置遺失中復原。</span><span class="sxs-lookup"><span data-stu-id="339e4-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

<span data-ttu-id="339e4-122">如果正在移除媒體，則抵達的裝置類型為磁片區， (**dbch \_ devicetype** 成員是 DBT \_ DEVTYP \_ volume) ，而 **dbcv \_ 旗標** 成員 (媒體) 的變更效果 \_ 。</span><span class="sxs-lookup"><span data-stu-id="339e4-122">If media is being removed, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="339e4-123">範例</span><span class="sxs-lookup"><span data-stu-id="339e4-123">Examples</span></span>

<span data-ttu-id="339e4-124">如需範例，請參閱偵測 [媒體插入或移除](detecting-media-insertion-or-removal.md) 或 [處理移除裝置的要求](processing-a-request-to-remove-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="339e4-124">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="339e4-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="339e4-125">Requirements</span></span>



| <span data-ttu-id="339e4-126">需求</span><span class="sxs-lookup"><span data-stu-id="339e4-126">Requirement</span></span> | <span data-ttu-id="339e4-127">值</span><span class="sxs-lookup"><span data-stu-id="339e4-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="339e4-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="339e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="339e4-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="339e4-129">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="339e4-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="339e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="339e4-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="339e4-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="339e4-132">標頭</span><span class="sxs-lookup"><span data-stu-id="339e4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="339e4-133"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="339e4-133"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="339e4-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="339e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339e4-135">裝置事件</span><span class="sxs-lookup"><span data-stu-id="339e4-135">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="339e4-136">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="339e4-136">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="339e4-137">**開發 \_ 廣播 \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="339e4-137">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="339e4-138">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="339e4-138">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




