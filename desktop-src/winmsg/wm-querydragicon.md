---
description: 傳送至最小化的 (iconic) 視窗。
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: 'WM_QUERYDRAGICON 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319208"
---
# <a name="wm_querydragicon-message"></a><span data-ttu-id="d266b-103">WM \_ QUERYDRAGICON 訊息</span><span class="sxs-lookup"><span data-stu-id="d266b-103">WM\_QUERYDRAGICON message</span></span>

<span data-ttu-id="d266b-104">傳送至最小化的 (iconic) 視窗。</span><span class="sxs-lookup"><span data-stu-id="d266b-104">Sent to a minimized (iconic) window.</span></span> <span data-ttu-id="d266b-105">視窗即將由使用者拖曳，但沒有為其類別定義的圖示。</span><span class="sxs-lookup"><span data-stu-id="d266b-105">The window is about to be dragged by the user but does not have an icon defined for its class.</span></span> <span data-ttu-id="d266b-106">應用程式可以將控制碼傳回至圖示或游標。</span><span class="sxs-lookup"><span data-stu-id="d266b-106">An application can return a handle to an icon or cursor.</span></span> <span data-ttu-id="d266b-107">當使用者拖曳圖示時，系統會顯示此游標或圖示。</span><span class="sxs-lookup"><span data-stu-id="d266b-107">The system displays this cursor or icon while the user drags the icon.</span></span>

<span data-ttu-id="d266b-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d266b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a><span data-ttu-id="d266b-109">參數</span><span class="sxs-lookup"><span data-stu-id="d266b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d266b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d266b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d266b-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d266b-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d266b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d266b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d266b-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d266b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d266b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d266b-114">Return value</span></span>

<span data-ttu-id="d266b-115">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d266b-115">Type: **LRESULT**</span></span>

<span data-ttu-id="d266b-116">應用程式應該會將控制碼傳回給系統在使用者拖曳圖示時所要顯示的游標或圖示。</span><span class="sxs-lookup"><span data-stu-id="d266b-116">An application should return a handle to a cursor or icon that the system is to display while the user drags the icon.</span></span> <span data-ttu-id="d266b-117">游標或圖示必須與顯示驅動程式的解析度相容。</span><span class="sxs-lookup"><span data-stu-id="d266b-117">The cursor or icon must be compatible with the display driver's resolution.</span></span> <span data-ttu-id="d266b-118">如果應用程式傳回 **Null**，系統就會顯示預設資料指標。</span><span class="sxs-lookup"><span data-stu-id="d266b-118">If the application returns **NULL**, the system displays the default cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="d266b-119">備註</span><span class="sxs-lookup"><span data-stu-id="d266b-119">Remarks</span></span>

<span data-ttu-id="d266b-120">當使用者拖曳沒有類別圖示的視窗圖示時，系統會將圖示取代為預設游標。</span><span class="sxs-lookup"><span data-stu-id="d266b-120">When the user drags the icon of a window without a class icon, the system replaces the icon with a default cursor.</span></span> <span data-ttu-id="d266b-121">如果應用程式需要在拖曳期間顯示不同的資料指標，它必須傳回與顯示器驅動程式解析度相容之游標或圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d266b-121">If the application requires a different cursor to be displayed during dragging, it must return a handle to the cursor or icon compatible with the display driver's resolution.</span></span> <span data-ttu-id="d266b-122">如果應用程式將控制碼傳回至色彩游標或圖示，系統會將游標或圖示轉換成黑色和白色。</span><span class="sxs-lookup"><span data-stu-id="d266b-122">If an application returns a handle to a color cursor or icon, the system converts the cursor or icon to black and white.</span></span> <span data-ttu-id="d266b-123">應用程式可以呼叫 [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) 或 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) 函式，以從可執行檔的 ( .exe) 檔案中的資源載入資料指標或圖示，並取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="d266b-123">The application can call the [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) or [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to load a cursor or icon from the resources in its executable (.exe) file and to retrieve this handle.</span></span>

<span data-ttu-id="d266b-124">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **布林** 值，並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="d266b-124">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="d266b-125">[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)函數所設定的 **DWL \_ MSGRESULT** 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="d266b-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d266b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d266b-126">Requirements</span></span>



| <span data-ttu-id="d266b-127">需求</span><span class="sxs-lookup"><span data-stu-id="d266b-127">Requirement</span></span> | <span data-ttu-id="d266b-128">值</span><span class="sxs-lookup"><span data-stu-id="d266b-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d266b-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d266b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d266b-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d266b-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d266b-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d266b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d266b-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d266b-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d266b-133">標頭</span><span class="sxs-lookup"><span data-stu-id="d266b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d266b-134"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d266b-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d266b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d266b-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="d266b-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="d266b-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d266b-137">**LoadCursor**</span><span class="sxs-lookup"><span data-stu-id="d266b-137">**LoadCursor**</span></span>](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[<span data-ttu-id="d266b-138">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="d266b-138">**LoadIcon**</span></span>](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

<span data-ttu-id="d266b-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="d266b-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d266b-140">Windows</span><span class="sxs-lookup"><span data-stu-id="d266b-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
