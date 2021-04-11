---
description: 只要在 \_ 列印管理員佇列中加入或移除工作，就會從列印管理員傳送 WM SPOOLERSTATUS 訊息。
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: 'WM_SPOOLERSTATUS 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115685"
---
# <a name="wm_spoolerstatus-message"></a><span data-ttu-id="818c4-103">WM \_ SPOOLERSTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="818c4-103">WM\_SPOOLERSTATUS message</span></span>

<span data-ttu-id="818c4-104">只要在列印管理員佇列中加入或移除工作，就會從列印管理員傳送 **WM \_ SPOOLERSTATUS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="818c4-104">The **WM\_SPOOLERSTATUS** message is sent from Print Manager whenever a job is added to or removed from the Print Manager queue.</span></span>

<span data-ttu-id="818c4-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="818c4-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="818c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="818c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="818c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="818c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="818c4-108">PR \_ JOBSTATUS 旗標。</span><span class="sxs-lookup"><span data-stu-id="818c4-108">The PR\_JOBSTATUS flag.</span></span>

</dd> <dt>

<span data-ttu-id="818c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="818c4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="818c4-110">低序位字組指定列印管理員佇列中剩餘的工作數目。</span><span class="sxs-lookup"><span data-stu-id="818c4-110">The low-order word specifies the number of jobs remaining in the Print Manager queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="818c4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="818c4-111">Return value</span></span>

<span data-ttu-id="818c4-112">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="818c4-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="818c4-113">備註</span><span class="sxs-lookup"><span data-stu-id="818c4-113">Remarks</span></span>

<span data-ttu-id="818c4-114">此訊息僅供參考之用。</span><span class="sxs-lookup"><span data-stu-id="818c4-114">This message is for informational purposes only.</span></span> <span data-ttu-id="818c4-115">這則訊息是建議的訊息，並不保證傳遞的語法。</span><span class="sxs-lookup"><span data-stu-id="818c4-115">This message is advisory and does not have guaranteed delivery semantics.</span></span> <span data-ttu-id="818c4-116">應用程式不應假設它們會 \_ 在每次變更多工緩衝處理器狀態時收到 WM SPOOLERSTATUS 訊息。</span><span class="sxs-lookup"><span data-stu-id="818c4-116">Applications should not assume that they will receive a WM\_SPOOLERSTATUS message for every change in spooler status.</span></span>

<span data-ttu-id="818c4-117">在 \_ WINDOWS XP 之後，不支援 WM SPOOLERSTATUS 訊息。</span><span class="sxs-lookup"><span data-stu-id="818c4-117">The WM\_SPOOLERSTATUS message is not supported after Windows XP.</span></span> <span data-ttu-id="818c4-118">若要在列印佇列狀態變更時收到通知，您可以使用 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) 和 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)。</span><span class="sxs-lookup"><span data-stu-id="818c4-118">To be notified of changes to the print queue status, you can use [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) and [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="818c4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="818c4-119">Requirements</span></span>



| <span data-ttu-id="818c4-120">需求</span><span class="sxs-lookup"><span data-stu-id="818c4-120">Requirement</span></span> | <span data-ttu-id="818c4-121">值</span><span class="sxs-lookup"><span data-stu-id="818c4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="818c4-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="818c4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="818c4-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="818c4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="818c4-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="818c4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="818c4-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="818c4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="818c4-126">標頭</span><span class="sxs-lookup"><span data-stu-id="818c4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="818c4-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="818c4-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="818c4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="818c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="818c4-129">列印</span><span class="sxs-lookup"><span data-stu-id="818c4-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="818c4-130">列印多工緩衝處理器 API 訊息</span><span class="sxs-lookup"><span data-stu-id="818c4-130">Print Spooler API Messages</span></span>](printing-and-print-spooler-messages.md)
</dt> <dt>

[<span data-ttu-id="818c4-131">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="818c4-131">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="818c4-132">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="818c4-132">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

