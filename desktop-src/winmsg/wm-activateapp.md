---
description: 當屬於與使用中視窗不同的應用程式視窗即將啟動時傳送。 訊息會傳送至應用程式，該應用程式的視窗正在啟動，而應用程式的視窗則會被停用。
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: 'WM_ACTI加值稅EAPP 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985471"
---
# <a name="wm_activateapp-message"></a><span data-ttu-id="bda80-104">WM \_ ACTI加值稅EAPP 訊息</span><span class="sxs-lookup"><span data-stu-id="bda80-104">WM\_ACTIVATEAPP message</span></span>

<span data-ttu-id="bda80-105">當屬於與使用中視窗不同的應用程式視窗即將啟動時傳送。</span><span class="sxs-lookup"><span data-stu-id="bda80-105">Sent when a window belonging to a different application than the active window is about to be activated.</span></span> <span data-ttu-id="bda80-106">訊息會傳送至應用程式，該應用程式的視窗正在啟動，而應用程式的視窗則會被停用。</span><span class="sxs-lookup"><span data-stu-id="bda80-106">The message is sent to the application whose window is being activated and to the application whose window is being deactivated.</span></span>

<span data-ttu-id="bda80-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="bda80-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a><span data-ttu-id="bda80-108">參數</span><span class="sxs-lookup"><span data-stu-id="bda80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda80-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bda80-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bda80-110">指出視窗是否正在啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="bda80-110">Indicates whether the window is being activated or deactivated.</span></span> <span data-ttu-id="bda80-111">如果要啟用視窗，此參數為 **TRUE** 。如果視窗正在停用，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bda80-111">This parameter is **TRUE** if the window is being activated; it is **FALSE** if the window is being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="bda80-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bda80-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bda80-113">執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="bda80-113">The thread identifier.</span></span> <span data-ttu-id="bda80-114">如果 *wParam* 參數為 **TRUE**，則 *lParam* 是擁有停用視窗之執行緒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bda80-114">If the *wParam* parameter is **TRUE**, *lParam* is the identifier of the thread that owns the window being deactivated.</span></span> <span data-ttu-id="bda80-115">如果 *wParam* 為 **FALSE**，則 *lParam* 是擁有要啟用之視窗的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="bda80-115">If *wParam* is **FALSE**, *lParam* is the identifier of the thread that owns the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda80-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bda80-116">Return value</span></span>

<span data-ttu-id="bda80-117">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="bda80-117">Type: **LRESULT**</span></span>

<span data-ttu-id="bda80-118">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="bda80-118">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda80-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bda80-119">Requirements</span></span>



| <span data-ttu-id="bda80-120">需求</span><span class="sxs-lookup"><span data-stu-id="bda80-120">Requirement</span></span> | <span data-ttu-id="bda80-121">值</span><span class="sxs-lookup"><span data-stu-id="bda80-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda80-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bda80-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bda80-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bda80-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bda80-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bda80-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bda80-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bda80-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bda80-126">標頭</span><span class="sxs-lookup"><span data-stu-id="bda80-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda80-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bda80-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bda80-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bda80-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="bda80-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="bda80-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bda80-130">**WM \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="bda80-130">**WM\_ACTIVATE**</span></span>](../inputdev/wm-activate.md)
</dt> <dt>

<span data-ttu-id="bda80-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="bda80-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bda80-132">Windows</span><span class="sxs-lookup"><span data-stu-id="bda80-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
