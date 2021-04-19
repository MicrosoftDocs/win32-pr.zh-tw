---
title: 'WM_RASDIALEVENT 訊息 (Ras) '
description: '\_當 RAS 連接程式期間發生狀態事件變更時，作業系統會將 WM RASDIALEVENT 訊息傳送至視窗程式。'
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT 訊息 RAS
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969752"
---
# <a name="wm_rasdialevent-message"></a><span data-ttu-id="b288c-104">WM \_ RASDIALEVENT 訊息</span><span class="sxs-lookup"><span data-stu-id="b288c-104">WM\_RASDIALEVENT message</span></span>

<span data-ttu-id="b288c-105">當 RAS 連接程式期間發生狀態事件變更時，作業系統會將 **WM \_ RASDIALEVENT** 訊息傳送至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="b288c-105">The operating system sends a **WM\_RASDIALEVENT** message to a window procedure when a change of state event occurs during a RAS connection process.</span></span> <span data-ttu-id="b288c-106">使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)*的通知程式參數指定* 視窗來處理這類事件的通知時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b288c-106">This happens when a window has been specified to handle notifications of such events by using the *notifier* parameter of [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="b288c-107">這兩個訊息參數相當於與 [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) 和 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) 回呼函數搭配使用之相同名稱的參數。</span><span class="sxs-lookup"><span data-stu-id="b288c-107">The two message parameters are equivalent to the parameters of the same names that are used with [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span>


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a><span data-ttu-id="b288c-108">參數</span><span class="sxs-lookup"><span data-stu-id="b288c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b288c-109">*rasconnstate*</span><span class="sxs-lookup"><span data-stu-id="b288c-109">*rasconnstate*</span></span> 
</dt> <dd>

<span data-ttu-id="b288c-110">*WParam* 的值。</span><span class="sxs-lookup"><span data-stu-id="b288c-110">Value of *wParam*.</span></span> <span data-ttu-id="b288c-111">相當於 [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)和 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)回呼函數的 *rasconnstate* 參數。</span><span class="sxs-lookup"><span data-stu-id="b288c-111">Equivalent to the *rasconnstate* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="b288c-112">指定 [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) 列舉值，這個值表示 RasDial 遠端存取連接程式即將進入的狀態。</span><span class="sxs-lookup"><span data-stu-id="b288c-112">Specifies a [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumerator value that indicates the state the RasDial remote access connection process is about to enter.</span></span>

</dd> <dt>

<span data-ttu-id="b288c-113">*dwError*</span><span class="sxs-lookup"><span data-stu-id="b288c-113">*dwError*</span></span> 
</dt> <dd>

<span data-ttu-id="b288c-114">*LParam* 的值。</span><span class="sxs-lookup"><span data-stu-id="b288c-114">Value of *lParam*.</span></span> <span data-ttu-id="b288c-115">相當於 [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)和 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)回呼函數的 *dwError* 參數。</span><span class="sxs-lookup"><span data-stu-id="b288c-115">Equivalent to the *dwError* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="b288c-116">非零值表示發生的錯誤，如果未發生錯誤，則為零。</span><span class="sxs-lookup"><span data-stu-id="b288c-116">A nonzero value indicates the error that has occurred, or zero if no error has occurred.</span></span>

<span data-ttu-id="b288c-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 會在進入每個連接狀態時，將 *dwError* 設定為零的訊息傳送。</span><span class="sxs-lookup"><span data-stu-id="b288c-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sends this message with *dwError* set to zero upon entry to each connection state.</span></span> <span data-ttu-id="b288c-118">如果狀態中發生錯誤，則會再次傳送該狀態的訊息，這次會有非零的 *dwError* 值。</span><span class="sxs-lookup"><span data-stu-id="b288c-118">If an error occurs within a state, the message is sent again for the state, this time with a nonzero *dwError* value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b288c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b288c-119">Return value</span></span>

<span data-ttu-id="b288c-120">如果應用程式處理此訊息，則應該傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="b288c-120">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b288c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b288c-121">Requirements</span></span>



| <span data-ttu-id="b288c-122">需求</span><span class="sxs-lookup"><span data-stu-id="b288c-122">Requirement</span></span> | <span data-ttu-id="b288c-123">值</span><span class="sxs-lookup"><span data-stu-id="b288c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b288c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b288c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b288c-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b288c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b288c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b288c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b288c-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b288c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b288c-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b288c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b288c-129"><dt>Ras。h</dt></span><span class="sxs-lookup"><span data-stu-id="b288c-129"><dt>Ras.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b288c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b288c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b288c-131">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="b288c-131">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b288c-132">遠端存取服務訊息</span><span class="sxs-lookup"><span data-stu-id="b288c-132">Remote Access Service Messages</span></span>](remote-access-service-messages.md)
</dt> <dt>

[<span data-ttu-id="b288c-133">**RasDial**</span><span class="sxs-lookup"><span data-stu-id="b288c-133">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[<span data-ttu-id="b288c-134">**RasDialFunc**</span><span class="sxs-lookup"><span data-stu-id="b288c-134">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[<span data-ttu-id="b288c-135">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="b288c-135">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

<span data-ttu-id="b288c-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b288c-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span></span>
</dt> </dl>

 

