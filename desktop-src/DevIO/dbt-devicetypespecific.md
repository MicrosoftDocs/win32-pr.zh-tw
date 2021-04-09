---
description: '\_當裝置特定事件發生時，系統會廣播 DBT DEVICETYPESPECIFIC 裝置事件。'
ms.assetid: 5d68e29d-b4d7-46f4-a35e-1db286e944ca
title: 'DBT_DEVICETYPESPECIFIC (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d7820f5769c6edd3a48b58073b55a911dae862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847286"
---
# <a name="dbt_devicetypespecific-event"></a><span data-ttu-id="f94fa-103">DBT \_ DEVICETYPESPECIFIC 事件</span><span class="sxs-lookup"><span data-stu-id="f94fa-103">DBT\_DEVICETYPESPECIFIC event</span></span>

<span data-ttu-id="f94fa-104">\_當裝置特定事件發生時，系統會廣播 DBT DEVICETYPESPECIFIC 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="f94fa-104">The system broadcasts the DBT\_DEVICETYPESPECIFIC device event when a device-specific event occurs.</span></span>

<span data-ttu-id="f94fa-105">若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICETYPESPECIFIC 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 </span><span class="sxs-lookup"><span data-stu-id="f94fa-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICETYPESPECIFIC and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="f94fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="f94fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f94fa-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="f94fa-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f94fa-108">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="f94fa-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="f94fa-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="f94fa-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f94fa-110">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="f94fa-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f94fa-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f94fa-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f94fa-112">設定為 DBT \_ DEVICETYPESPECIFIC。</span><span class="sxs-lookup"><span data-stu-id="f94fa-112">Set to DBT\_DEVICETYPESPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="f94fa-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f94fa-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f94fa-114">識別裝置之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f94fa-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="f94fa-115">此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。</span><span class="sxs-lookup"><span data-stu-id="f94fa-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="f94fa-116">若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。</span><span class="sxs-lookup"><span data-stu-id="f94fa-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f94fa-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f94fa-117">Return value</span></span>

<span data-ttu-id="f94fa-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f94fa-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f94fa-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f94fa-119">Requirements</span></span>



| <span data-ttu-id="f94fa-120">需求</span><span class="sxs-lookup"><span data-stu-id="f94fa-120">Requirement</span></span> | <span data-ttu-id="f94fa-121">值</span><span class="sxs-lookup"><span data-stu-id="f94fa-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f94fa-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f94fa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f94fa-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f94fa-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="f94fa-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f94fa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f94fa-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f94fa-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f94fa-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f94fa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f94fa-127"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="f94fa-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94fa-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f94fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94fa-129">裝置事件</span><span class="sxs-lookup"><span data-stu-id="f94fa-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="f94fa-130">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="f94fa-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="f94fa-131">**開發 \_ 廣播 \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="f94fa-131">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="f94fa-132">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="f94fa-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




