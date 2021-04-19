---
description: 系統會廣播 DBT \_ DEVICEQUERYREMOVE 裝置事件，以要求移除裝置或媒體部分的許可權。
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: 'DBT_DEVICEQUERYREMOVE (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981124"
---
# <a name="dbt_devicequeryremove-event"></a><span data-ttu-id="36cc3-103">DBT \_ DEVICEQUERYREMOVE 事件</span><span class="sxs-lookup"><span data-stu-id="36cc3-103">DBT\_DEVICEQUERYREMOVE event</span></span>

<span data-ttu-id="36cc3-104">系統會廣播 DBT \_ DEVICEQUERYREMOVE 裝置事件，以要求移除裝置或媒體部分的許可權。</span><span class="sxs-lookup"><span data-stu-id="36cc3-104">The system broadcasts the DBT\_DEVICEQUERYREMOVE device event to request permission to remove a device or piece of media.</span></span> <span data-ttu-id="36cc3-105">這則訊息是應用程式和驅動程式的最後機會，以準備進行移除。</span><span class="sxs-lookup"><span data-stu-id="36cc3-105">This message is the last chance for applications and drivers to prepare for this removal.</span></span> <span data-ttu-id="36cc3-106">不過，任何應用程式都可以拒絕此要求，並取消作業。</span><span class="sxs-lookup"><span data-stu-id="36cc3-106">However, any application can deny this request and cancel the operation.</span></span>

<span data-ttu-id="36cc3-107">若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICEQUERYREMOVE 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 </span><span class="sxs-lookup"><span data-stu-id="36cc3-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="36cc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="36cc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36cc3-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="36cc3-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="36cc3-110">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="36cc3-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="36cc3-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="36cc3-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="36cc3-112">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="36cc3-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="36cc3-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36cc3-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36cc3-114">設定為 DBT \_ DEVICEQUERYREMOVE。</span><span class="sxs-lookup"><span data-stu-id="36cc3-114">Set to DBT\_DEVICEQUERYREMOVE.</span></span>

</dd> <dt>

<span data-ttu-id="36cc3-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36cc3-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36cc3-116">結構的指標，此結構識別要移除的裝置。</span><span class="sxs-lookup"><span data-stu-id="36cc3-116">A pointer to a structure identifying the device to remove.</span></span> <span data-ttu-id="36cc3-117">此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。</span><span class="sxs-lookup"><span data-stu-id="36cc3-117">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="36cc3-118">若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。</span><span class="sxs-lookup"><span data-stu-id="36cc3-118">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36cc3-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="36cc3-119">Return value</span></span>

<span data-ttu-id="36cc3-120">傳回 **TRUE** 以授與移除裝置的許可權。</span><span class="sxs-lookup"><span data-stu-id="36cc3-120">Return **TRUE** to grant permission to remove a device.</span></span>

<span data-ttu-id="36cc3-121">傳回「廣播 \_ 查詢 \_ 拒絕」以拒絕移除裝置的許可權。</span><span class="sxs-lookup"><span data-stu-id="36cc3-121">Return BROADCAST\_QUERY\_DENY to deny permission to remove a device.</span></span>

## <a name="remarks"></a><span data-ttu-id="36cc3-122">備註</span><span class="sxs-lookup"><span data-stu-id="36cc3-122">Remarks</span></span>

<span data-ttu-id="36cc3-123">您必須關閉裝置的所有控制碼，否則裝置移除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="36cc3-123">You must close all handles to the device or the device removal will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="36cc3-124">範例</span><span class="sxs-lookup"><span data-stu-id="36cc3-124">Examples</span></span>

<span data-ttu-id="36cc3-125">如需範例，請參閱 [處理移除裝置的要求](processing-a-request-to-remove-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="36cc3-125">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36cc3-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="36cc3-126">Requirements</span></span>



| <span data-ttu-id="36cc3-127">需求</span><span class="sxs-lookup"><span data-stu-id="36cc3-127">Requirement</span></span> | <span data-ttu-id="36cc3-128">值</span><span class="sxs-lookup"><span data-stu-id="36cc3-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36cc3-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36cc3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36cc3-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="36cc3-130">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="36cc3-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36cc3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36cc3-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36cc3-132">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="36cc3-133">標頭</span><span class="sxs-lookup"><span data-stu-id="36cc3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cc3-134"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="36cc3-134"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cc3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36cc3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cc3-136">裝置事件</span><span class="sxs-lookup"><span data-stu-id="36cc3-136">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="36cc3-137">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="36cc3-137">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="36cc3-138">**開發 \_ 廣播 \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="36cc3-138">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="36cc3-139">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="36cc3-139">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




