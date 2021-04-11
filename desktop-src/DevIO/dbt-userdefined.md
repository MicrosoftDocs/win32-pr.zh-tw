---
description: DBT 的使用者 \_ 定義裝置事件會識別使用者定義的事件。
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: 'DBT_USERDEFINED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025919"
---
# <a name="dbt_userdefined-event"></a><span data-ttu-id="f0786-103">DBT \_ 使用者的事件</span><span class="sxs-lookup"><span data-stu-id="f0786-103">DBT\_USERDEFINED event</span></span>

<span data-ttu-id="f0786-104">DBT 的使用者 \_ 定義裝置事件會識別使用者定義的事件。</span><span class="sxs-lookup"><span data-stu-id="f0786-104">The DBT\_USERDEFINED device event identifies a user-defined event.</span></span>

<span data-ttu-id="f0786-105">若要廣播此裝置事件，請使用 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息來呼叫 [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)函數。</span><span class="sxs-lookup"><span data-stu-id="f0786-105">To broadcast this device event, call the [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) function with the [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="f0786-106">將 *wParam* 設定為 DBT 的 \_ 使用者，並設定 *lParam* ，如下所述。</span><span class="sxs-lookup"><span data-stu-id="f0786-106">Set *wParam* to DBT\_USERDEFINED and set *lParam* as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="f0786-107">參數</span><span class="sxs-lookup"><span data-stu-id="f0786-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0786-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="f0786-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f0786-109">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="f0786-109">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="f0786-110">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="f0786-110">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f0786-111">[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0786-111">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f0786-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0786-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0786-113">設定為 DBT 的 \_ 使用者。</span><span class="sxs-lookup"><span data-stu-id="f0786-113">Set to DBT\_USERDEFINED.</span></span>

</dd> <dt>

<span data-ttu-id="f0786-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0786-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0786-115">[**\_ 開發人員 \_ 廣播 \_**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)的使用者定義結構指標，描述正在進行的使用者定義廣播。</span><span class="sxs-lookup"><span data-stu-id="f0786-115">A pointer to a [**\_DEV\_BROADCAST\_USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) structure which describes the user-defined broadcast in progress.</span></span> <span data-ttu-id="f0786-116">**Dbud \_ >szname** 成員包含使用者自訂訊息的名稱，後面接著任何使用者定義的資料。</span><span class="sxs-lookup"><span data-stu-id="f0786-116">The **dbud\_szName** member contains the name of the user-defined message, followed by any user-defined data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0786-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0786-117">Return value</span></span>

<span data-ttu-id="f0786-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f0786-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0786-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0786-119">Requirements</span></span>



| <span data-ttu-id="f0786-120">需求</span><span class="sxs-lookup"><span data-stu-id="f0786-120">Requirement</span></span> | <span data-ttu-id="f0786-121">值</span><span class="sxs-lookup"><span data-stu-id="f0786-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f0786-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0786-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f0786-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0786-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="f0786-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0786-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f0786-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0786-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f0786-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f0786-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0786-127"><dt>Dbt。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0786-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0786-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0786-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0786-129">裝置事件</span><span class="sxs-lookup"><span data-stu-id="f0786-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="f0786-130">裝置管理事件</span><span class="sxs-lookup"><span data-stu-id="f0786-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="f0786-131">**\_開發人員 \_ 廣播的 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="f0786-131">**\_DEV\_BROADCAST\_USERDEFINED**</span></span>](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[<span data-ttu-id="f0786-132">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="f0786-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> <dt>

[<span data-ttu-id="f0786-133">**BroadcastSystemMessage**</span><span class="sxs-lookup"><span data-stu-id="f0786-133">**BroadcastSystemMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

