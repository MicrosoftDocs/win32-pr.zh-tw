---
description: 系統會廣播 DBT \_ CONFIGCHANGED 裝置事件，以指出目前的設定已變更，因為 dock 或取消停駐。 將資料儲存在登錄中的應用程式或驅動程式 HKEY \_ 目前的設定 \_ 金鑰應該會更新資料。
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: 'DBT_CONFIGCHANGED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187721"
---
# <a name="dbt_configchanged-event"></a><span data-ttu-id="d8408-104">DBT \_ CONFIGCHANGED 事件</span><span class="sxs-lookup"><span data-stu-id="d8408-104">DBT\_CONFIGCHANGED event</span></span>

<span data-ttu-id="d8408-105">系統會廣播 DBT \_ CONFIGCHANGED 裝置事件，以指出目前的設定已變更，因為 dock 或取消停駐。</span><span class="sxs-lookup"><span data-stu-id="d8408-105">The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock.</span></span> <span data-ttu-id="d8408-106">將資料儲存在登錄中的應用程式或驅動程式 HKEY \_ 目前的設定 \_ 金鑰應該會更新資料。</span><span class="sxs-lookup"><span data-stu-id="d8408-106">An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.</span></span>

<span data-ttu-id="d8408-107">若要廣播此裝置事件，系統會使用 *wParam* 設定為 DBT CONFIGCHANGED 且 lParam 設定為零的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息 \_ 。 </span><span class="sxs-lookup"><span data-stu-id="d8408-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="d8408-108">參數</span><span class="sxs-lookup"><span data-stu-id="d8408-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8408-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="d8408-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d8408-110">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="d8408-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="d8408-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="d8408-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="d8408-112">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8408-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d8408-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8408-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8408-114">設定為 DBT \_ CONFIGCHANGED。</span><span class="sxs-lookup"><span data-stu-id="d8408-114">Set to DBT\_CONFIGCHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="d8408-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8408-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8408-116">設定為零。</span><span class="sxs-lookup"><span data-stu-id="d8408-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8408-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8408-117">Return value</span></span>

<span data-ttu-id="d8408-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d8408-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8408-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8408-119">Requirements</span></span>



| <span data-ttu-id="d8408-120">需求</span><span class="sxs-lookup"><span data-stu-id="d8408-120">Requirement</span></span> | <span data-ttu-id="d8408-121">值</span><span class="sxs-lookup"><span data-stu-id="d8408-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8408-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8408-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d8408-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d8408-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="d8408-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8408-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d8408-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d8408-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="d8408-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d8408-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8408-127"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="d8408-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8408-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8408-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8408-129">裝置事件</span><span class="sxs-lookup"><span data-stu-id="d8408-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="d8408-130">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="d8408-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="d8408-131">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="d8408-131">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




