---
Description: 以信號的形式傳送視窗或應用程式應終止。
ms.assetid: 19500baf-e0ad-4dfa-804f-6a6e0652cffb
title: 'WM_CLOSE 訊息 (Winuser .h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2f1403050cfd3c98ddf90df4399547158a583c50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000837"
---
# <a name="wm_close-message"></a><span data-ttu-id="73932-103">WM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="73932-103">WM\_CLOSE message</span></span>

<span data-ttu-id="73932-104">以信號的形式傳送視窗或應用程式應終止。</span><span class="sxs-lookup"><span data-stu-id="73932-104">Sent as a signal that a window or an application should terminate.</span></span>

<span data-ttu-id="73932-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="73932-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CLOSE                        0x0010
```



## <a name="parameters"></a><span data-ttu-id="73932-106">參數</span><span class="sxs-lookup"><span data-stu-id="73932-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73932-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73932-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73932-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="73932-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73932-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73932-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73932-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="73932-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73932-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="73932-111">Return value</span></span>

<span data-ttu-id="73932-112">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="73932-112">Type: **LRESULT**</span></span>

<span data-ttu-id="73932-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="73932-113">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="73932-114">範例</span><span class="sxs-lookup"><span data-stu-id="73932-114">Example</span></span>

```cpp
LRESULT CALLBACK WindowProc(
    __in HWND hWindow,
    __in UINT uMsg,
    __in WPARAM wParam,
    __in LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CLOSE:
        DestroyWindow(hWindow);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWindow, uMsg, wParam, lParam);
    }

    return 0;
}
```
<span data-ttu-id="73932-115">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="73932-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="73932-116">備註</span><span class="sxs-lookup"><span data-stu-id="73932-116">Remarks</span></span>

<span data-ttu-id="73932-117">應用程式可以在終結視窗之前提示使用者進行確認，方法是處理 **WM \_ 關閉** 訊息，並只在使用者確認選擇時才呼叫 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) 函數。</span><span class="sxs-lookup"><span data-stu-id="73932-117">An application can prompt the user for confirmation, prior to destroying a window, by processing the **WM\_CLOSE** message and calling the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function only if the user confirms the choice.</span></span>

<span data-ttu-id="73932-118">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會呼叫 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) 函數來終結視窗。</span><span class="sxs-lookup"><span data-stu-id="73932-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function calls the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="73932-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="73932-119">Requirements</span></span>



| <span data-ttu-id="73932-120">需求</span><span class="sxs-lookup"><span data-stu-id="73932-120">Requirement</span></span> | <span data-ttu-id="73932-121">值</span><span class="sxs-lookup"><span data-stu-id="73932-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73932-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73932-122">Minimum supported client</span></span><br/> | <span data-ttu-id="73932-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73932-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="73932-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73932-124">Minimum supported server</span></span><br/> | <span data-ttu-id="73932-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73932-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="73932-126">標頭</span><span class="sxs-lookup"><span data-stu-id="73932-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="73932-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="73932-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73932-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73932-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="73932-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="73932-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="73932-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="73932-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="73932-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="73932-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

<span data-ttu-id="73932-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="73932-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="73932-133">Windows</span><span class="sxs-lookup"><span data-stu-id="73932-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
