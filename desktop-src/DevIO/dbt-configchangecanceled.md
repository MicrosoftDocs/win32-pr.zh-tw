---
description: '\_當 (停駐或取消停駐) 變更目前設定的要求時，系統會廣播 DBT CONFIGCHANGECANCELED 裝置事件。'
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: 'DBT_CONFIGCHANGECANCELED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97944daa698808c55f88bc377c9bf1c59c1217fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847289"
---
# <a name="dbt_configchangecanceled-event"></a><span data-ttu-id="92988-103">DBT \_ CONFIGCHANGECANCELED 事件</span><span class="sxs-lookup"><span data-stu-id="92988-103">DBT\_CONFIGCHANGECANCELED event</span></span>

<span data-ttu-id="92988-104">\_當 (停駐或取消停駐) 變更目前設定的要求時，系統會廣播 DBT CONFIGCHANGECANCELED 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="92988-104">The system broadcasts the DBT\_CONFIGCHANGECANCELED device event when a request to change the current configuration (dock or undock) has been canceled.</span></span>

<span data-ttu-id="92988-105">若要廣播此裝置事件，系統會使用 *wParam* 設定為 DBT CONFIGCHANGECANCELED 且 lParam 設定為零的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息 \_ 。 </span><span class="sxs-lookup"><span data-stu-id="92988-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGECANCELED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="92988-106">參數</span><span class="sxs-lookup"><span data-stu-id="92988-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92988-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="92988-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="92988-108">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="92988-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="92988-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="92988-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="92988-110">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="92988-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="92988-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92988-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92988-112">設定為 DBT \_ CONFIGCHANGECANCELED。</span><span class="sxs-lookup"><span data-stu-id="92988-112">Set to DBT\_CONFIGCHANGECANCELED.</span></span>

</dd> <dt>

<span data-ttu-id="92988-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92988-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92988-114">設定為零。</span><span class="sxs-lookup"><span data-stu-id="92988-114">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92988-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="92988-115">Return value</span></span>

<span data-ttu-id="92988-116">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="92988-116">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92988-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="92988-117">Requirements</span></span>



| <span data-ttu-id="92988-118">需求</span><span class="sxs-lookup"><span data-stu-id="92988-118">Requirement</span></span> | <span data-ttu-id="92988-119">值</span><span class="sxs-lookup"><span data-stu-id="92988-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="92988-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92988-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92988-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="92988-121">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="92988-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92988-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92988-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92988-123">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="92988-124">標頭</span><span class="sxs-lookup"><span data-stu-id="92988-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="92988-125"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="92988-125"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92988-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92988-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92988-127">裝置事件</span><span class="sxs-lookup"><span data-stu-id="92988-127">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="92988-128">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="92988-128">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="92988-129">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="92988-129">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




