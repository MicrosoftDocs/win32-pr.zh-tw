---
description: 系統會廣播 DBT \_ QUERYCHANGECONFIG 裝置事件，以要求 (dock 或取消停駐) 變更目前設定的許可權。 任何應用程式都可以拒絕此要求，並取消變更。
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: 'DBT_QUERYCHANGECONFIG (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510574"
---
# <a name="dbt_querychangeconfig-event"></a><span data-ttu-id="3693f-104">DBT \_ QUERYCHANGECONFIG 事件</span><span class="sxs-lookup"><span data-stu-id="3693f-104">DBT\_QUERYCHANGECONFIG event</span></span>

<span data-ttu-id="3693f-105">系統會廣播 DBT \_ QUERYCHANGECONFIG 裝置事件，以要求 (dock 或取消停駐) 變更目前設定的許可權。</span><span class="sxs-lookup"><span data-stu-id="3693f-105">The system broadcasts the DBT\_QUERYCHANGECONFIG device event to request permission to change the current configuration (dock or undock).</span></span> <span data-ttu-id="3693f-106">任何應用程式都可以拒絕此要求，並取消變更。</span><span class="sxs-lookup"><span data-stu-id="3693f-106">Any application can deny this request and cancel the change.</span></span>

<span data-ttu-id="3693f-107">若要廣播此裝置事件，系統會使用 *wParam* 設定為 DBT QUERYCHANGECONFIG 且 lParam 設定為零的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息 \_ 。 </span><span class="sxs-lookup"><span data-stu-id="3693f-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_QUERYCHANGECONFIG and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="3693f-108">參數</span><span class="sxs-lookup"><span data-stu-id="3693f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3693f-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="3693f-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="3693f-110">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="3693f-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="3693f-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="3693f-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="3693f-112">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="3693f-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3693f-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3693f-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3693f-114">設定為 DBT \_ QUERYCHANGECONFIG。</span><span class="sxs-lookup"><span data-stu-id="3693f-114">Set to DBT\_QUERYCHANGECONFIG.</span></span>

</dd> <dt>

<span data-ttu-id="3693f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3693f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3693f-116">設定為零。</span><span class="sxs-lookup"><span data-stu-id="3693f-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3693f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3693f-117">Return value</span></span>

<span data-ttu-id="3693f-118">傳回 **TRUE** 以授與變更設定的許可權。</span><span class="sxs-lookup"><span data-stu-id="3693f-118">Return **TRUE** to grant permission to change the configuration.</span></span>

<span data-ttu-id="3693f-119">傳回「廣播 \_ 查詢 \_ 拒絕」以拒絕變更設定的許可權。</span><span class="sxs-lookup"><span data-stu-id="3693f-119">Return BROADCAST\_QUERY\_DENY to deny permission to change the configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="3693f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3693f-120">Requirements</span></span>



| <span data-ttu-id="3693f-121">需求</span><span class="sxs-lookup"><span data-stu-id="3693f-121">Requirement</span></span> | <span data-ttu-id="3693f-122">值</span><span class="sxs-lookup"><span data-stu-id="3693f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3693f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3693f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3693f-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3693f-124">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="3693f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3693f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3693f-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3693f-126">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="3693f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3693f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3693f-128"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="3693f-128"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3693f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3693f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3693f-130">裝置事件</span><span class="sxs-lookup"><span data-stu-id="3693f-130">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="3693f-131">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="3693f-131">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="3693f-132">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="3693f-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




