---
description: '\_當移除裝置或媒體片段的要求遭到取消時，系統會廣播 DBT DEVICEQUERYREMOVEFAILED 裝置事件。'
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: 'DBT_DEVICEQUERYREMOVEFAILED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847287"
---
# <a name="dbt_devicequeryremovefailed-event"></a><span data-ttu-id="af29a-103">DBT \_ DEVICEQUERYREMOVEFAILED 事件</span><span class="sxs-lookup"><span data-stu-id="af29a-103">DBT\_DEVICEQUERYREMOVEFAILED event</span></span>

<span data-ttu-id="af29a-104">\_當移除裝置或媒體片段的要求遭到取消時，系統會廣播 DBT DEVICEQUERYREMOVEFAILED 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="af29a-104">The system broadcasts the DBT\_DEVICEQUERYREMOVEFAILED device event when a request to remove a device or piece of media has been canceled.</span></span>

<span data-ttu-id="af29a-105">若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICEQUERYREMOVEFAILED 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 </span><span class="sxs-lookup"><span data-stu-id="af29a-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVEFAILED and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="af29a-106">參數</span><span class="sxs-lookup"><span data-stu-id="af29a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af29a-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="af29a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="af29a-108">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="af29a-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="af29a-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="af29a-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="af29a-110">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="af29a-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="af29a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af29a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af29a-112">設定為 DBT \_ DEVICEQUERYREMOVEFAILED。</span><span class="sxs-lookup"><span data-stu-id="af29a-112">Set to DBT\_DEVICEQUERYREMOVEFAILED.</span></span>

</dd> <dt>

<span data-ttu-id="af29a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af29a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af29a-114">識別裝置之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="af29a-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="af29a-115">此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。</span><span class="sxs-lookup"><span data-stu-id="af29a-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="af29a-116">若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。</span><span class="sxs-lookup"><span data-stu-id="af29a-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af29a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="af29a-117">Return value</span></span>

<span data-ttu-id="af29a-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="af29a-118">Return **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="af29a-119">範例</span><span class="sxs-lookup"><span data-stu-id="af29a-119">Examples</span></span>

<span data-ttu-id="af29a-120">如需範例，請參閱 [處理移除裝置的要求](processing-a-request-to-remove-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="af29a-120">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af29a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="af29a-121">Requirements</span></span>



| <span data-ttu-id="af29a-122">需求</span><span class="sxs-lookup"><span data-stu-id="af29a-122">Requirement</span></span> | <span data-ttu-id="af29a-123">值</span><span class="sxs-lookup"><span data-stu-id="af29a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="af29a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af29a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af29a-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af29a-125">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="af29a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af29a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af29a-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af29a-127">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="af29a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="af29a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af29a-129"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="af29a-129"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af29a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af29a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af29a-131">裝置事件</span><span class="sxs-lookup"><span data-stu-id="af29a-131">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="af29a-132">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="af29a-132">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="af29a-133">**開發 \_ 廣播 \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="af29a-133">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="af29a-134">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="af29a-134">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




