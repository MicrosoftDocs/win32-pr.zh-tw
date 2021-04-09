---
description: 系統在 \_ 移除裝置或媒體時，系統會將 DBT DEVICEREMOVEPENDING 裝置事件廣播，且無法再供使用。
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: 'DBT_DEVICEREMOVEPENDING (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110696"
---
# <a name="dbt_deviceremovepending-event"></a><span data-ttu-id="0bd9e-103">DBT \_ DEVICEREMOVEPENDING 事件</span><span class="sxs-lookup"><span data-stu-id="0bd9e-103">DBT\_DEVICEREMOVEPENDING event</span></span>

<span data-ttu-id="0bd9e-104">系統在 \_ 移除裝置或媒體時，系統會將 DBT DEVICEREMOVEPENDING 裝置事件廣播，且無法再供使用。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-104">The system broadcasts the DBT\_DEVICEREMOVEPENDING device event when a device or piece of media is being removed and is no longer available for use.</span></span>

<span data-ttu-id="0bd9e-105">若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICEREMOVEPENDING 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 </span><span class="sxs-lookup"><span data-stu-id="0bd9e-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVEPENDING and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="0bd9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="0bd9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bd9e-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="0bd9e-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd9e-108">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="0bd9e-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="0bd9e-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd9e-110">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0bd9e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bd9e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd9e-112">設定為 DBT \_ DEVICEREMOVEPENDING。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-112">Set to DBT\_DEVICEREMOVEPENDING.</span></span>

</dd> <dt>

<span data-ttu-id="0bd9e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0bd9e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd9e-114">識別裝置之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="0bd9e-115">此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="0bd9e-116">若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bd9e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bd9e-117">Return value</span></span>

<span data-ttu-id="0bd9e-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd9e-119">備註</span><span class="sxs-lookup"><span data-stu-id="0bd9e-119">Remarks</span></span>

<span data-ttu-id="0bd9e-120">系統可能會廣播 DBT \_ DEVICEREMOVEPENDING 訊息，而不會傳送對應的 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-120">The system may broadcast a DBT\_DEVICEREMOVEPENDING message without sending a corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message.</span></span> <span data-ttu-id="0bd9e-121">在這種情況下，應用程式和驅動程式必須盡可能地從裝置遺失中復原。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

## <a name="examples"></a><span data-ttu-id="0bd9e-122">範例</span><span class="sxs-lookup"><span data-stu-id="0bd9e-122">Examples</span></span>

<span data-ttu-id="0bd9e-123">如需範例，請參閱 [處理移除裝置的要求](processing-a-request-to-remove-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="0bd9e-123">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd9e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bd9e-124">Requirements</span></span>



| <span data-ttu-id="0bd9e-125">需求</span><span class="sxs-lookup"><span data-stu-id="0bd9e-125">Requirement</span></span> | <span data-ttu-id="0bd9e-126">值</span><span class="sxs-lookup"><span data-stu-id="0bd9e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0bd9e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bd9e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0bd9e-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0bd9e-128">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="0bd9e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bd9e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0bd9e-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0bd9e-130">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="0bd9e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="0bd9e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bd9e-132"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="0bd9e-132"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bd9e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bd9e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd9e-134">裝置事件</span><span class="sxs-lookup"><span data-stu-id="0bd9e-134">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="0bd9e-135">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="0bd9e-135">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="0bd9e-136">**開發 \_ 廣播 \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="0bd9e-136">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="0bd9e-137">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="0bd9e-137">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




