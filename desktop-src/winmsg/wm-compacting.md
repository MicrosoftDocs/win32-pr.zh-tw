---
description: 當系統偵測到超過30到60秒間隔的系統時間超過12.5% 時，就會傳送至所有最上層視窗，以壓縮記憶體。 這表示系統記憶體不足。
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: 'WM_COMPACTING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975788"
---
# <a name="wm_compacting-message"></a><span data-ttu-id="0b449-104">WM \_ 壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="0b449-104">WM\_COMPACTING message</span></span>

<span data-ttu-id="0b449-105">當系統偵測到超過30到60秒間隔的系統時間超過12.5% 時，就會傳送至所有最上層視窗，以壓縮記憶體。</span><span class="sxs-lookup"><span data-stu-id="0b449-105">Sent to all top-level windows when the system detects more than 12.5 percent of system time over a 30- to 60-second interval is being spent compacting memory.</span></span> <span data-ttu-id="0b449-106">這表示系統記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="0b449-106">This indicates that system memory is low.</span></span>

<span data-ttu-id="0b449-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="0b449-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="0b449-108">此訊息僅提供給以16位 Windows 為基礎的應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="0b449-108">This message is provided only for compatibility with 16-bit Windows-based applications.</span></span>

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a><span data-ttu-id="0b449-109">參數</span><span class="sxs-lookup"><span data-stu-id="0b449-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b449-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b449-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b449-111">中央處理單位 (CPU) 時間的比率，目前由系統壓縮記憶體到系統執行其他作業所花費的 CPU 時間。</span><span class="sxs-lookup"><span data-stu-id="0b449-111">The ratio of central processing unit (CPU) time currently spent by the system compacting memory to CPU time currently spent by the system performing other operations.</span></span> <span data-ttu-id="0b449-112">例如，0x8000 代表花費在壓縮記憶體的 CPU 時間50%。</span><span class="sxs-lookup"><span data-stu-id="0b449-112">For example, 0x8000 represents 50 percent of CPU time spent compacting memory.</span></span>

</dd> <dt>

<span data-ttu-id="0b449-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b449-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b449-114">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="0b449-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b449-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b449-115">Return value</span></span>

<span data-ttu-id="0b449-116">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0b449-116">Type: **LRESULT**</span></span>

<span data-ttu-id="0b449-117">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0b449-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b449-118">備註</span><span class="sxs-lookup"><span data-stu-id="0b449-118">Remarks</span></span>

<span data-ttu-id="0b449-119">當應用程式收到此訊息時，應該盡可能釋放最多的記憶體，將應用程式目前的活動層級以及系統上執行的應用程式總數納入考慮。</span><span class="sxs-lookup"><span data-stu-id="0b449-119">When an application receives this message, it should free as much memory as possible, taking into account the current level of activity of the application and the total number of applications running on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b449-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b449-120">Requirements</span></span>



| <span data-ttu-id="0b449-121">需求</span><span class="sxs-lookup"><span data-stu-id="0b449-121">Requirement</span></span> | <span data-ttu-id="0b449-122">值</span><span class="sxs-lookup"><span data-stu-id="0b449-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b449-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b449-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0b449-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b449-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0b449-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b449-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0b449-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b449-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b449-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0b449-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b449-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0b449-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b449-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b449-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b449-130">Windows 總覽</span><span class="sxs-lookup"><span data-stu-id="0b449-130">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
