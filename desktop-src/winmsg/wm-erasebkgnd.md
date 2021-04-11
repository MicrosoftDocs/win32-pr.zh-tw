---
description: 當視窗背景必須清除時傳送 (例如，當調整視窗大小時) 。 傳送訊息以準備視窗的無效部分進行繪製。
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: 'WM_ERASEBKGND 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193703"
---
# <a name="wm_erasebkgnd-message"></a><span data-ttu-id="7aff6-104">WM \_ ERASEBKGND 訊息</span><span class="sxs-lookup"><span data-stu-id="7aff6-104">WM\_ERASEBKGND message</span></span>

<span data-ttu-id="7aff6-105">當視窗背景必須清除時傳送 (例如，當調整視窗大小時) 。</span><span class="sxs-lookup"><span data-stu-id="7aff6-105">Sent when the window background must be erased (for example, when a window is resized).</span></span> <span data-ttu-id="7aff6-106">傳送訊息以準備視窗的無效部分進行繪製。</span><span class="sxs-lookup"><span data-stu-id="7aff6-106">The message is sent to prepare an invalidated portion of a window for painting.</span></span>


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a><span data-ttu-id="7aff6-107">參數</span><span class="sxs-lookup"><span data-stu-id="7aff6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aff6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7aff6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7aff6-109">裝置內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7aff6-109">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="7aff6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7aff6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7aff6-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="7aff6-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aff6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7aff6-112">Return value</span></span>

<span data-ttu-id="7aff6-113">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7aff6-113">Type: **LRESULT**</span></span>

<span data-ttu-id="7aff6-114">如果應用程式清除背景，則應該傳回非零值;否則，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="7aff6-114">An application should return nonzero if it erases the background; otherwise, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aff6-115">備註</span><span class="sxs-lookup"><span data-stu-id="7aff6-115">Remarks</span></span>

<span data-ttu-id="7aff6-116">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會使用 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **hbrBackground** 成員所指定的類別背景筆刷，來清除背景。</span><span class="sxs-lookup"><span data-stu-id="7aff6-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function erases the background by using the class background brush specified by the **hbrBackground** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure.</span></span> <span data-ttu-id="7aff6-117">如果 **hbrBackground** 為 **Null**，則應用程式應該處理 **WM \_ ERASEBKGND** 訊息並清除背景。</span><span class="sxs-lookup"><span data-stu-id="7aff6-117">If **hbrBackground** is **NULL**, the application should process the **WM\_ERASEBKGND** message and erase the background.</span></span>

<span data-ttu-id="7aff6-118">如果應用程式處理訊息並清除背景，則應用程式應該傳回非零以回應 **WM \_ ERASEBKGND** ; 這表示不需要進一步清除。</span><span class="sxs-lookup"><span data-stu-id="7aff6-118">An application should return nonzero in response to **WM\_ERASEBKGND** if it processes the message and erases the background; this indicates that no further erasing is required.</span></span> <span data-ttu-id="7aff6-119">如果應用程式傳回零，視窗將維持標記以進行清除。</span><span class="sxs-lookup"><span data-stu-id="7aff6-119">If the application returns zero, the window will remain marked for erasing.</span></span> <span data-ttu-id="7aff6-120"> (通常表示 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)結構的 **fErase** 成員將會是 **TRUE**。 ) </span><span class="sxs-lookup"><span data-stu-id="7aff6-120">(Typically, this indicates that the **fErase** member of the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure will be **TRUE**.)</span></span>

## <a name="requirements"></a><span data-ttu-id="7aff6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7aff6-121">Requirements</span></span>



| <span data-ttu-id="7aff6-122">需求</span><span class="sxs-lookup"><span data-stu-id="7aff6-122">Requirement</span></span> | <span data-ttu-id="7aff6-123">值</span><span class="sxs-lookup"><span data-stu-id="7aff6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aff6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7aff6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7aff6-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7aff6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7aff6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7aff6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7aff6-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7aff6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7aff6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7aff6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aff6-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7aff6-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aff6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7aff6-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="7aff6-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="7aff6-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7aff6-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7aff6-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7aff6-133">**WNDCLASS**</span><span class="sxs-lookup"><span data-stu-id="7aff6-133">**WNDCLASS**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

<span data-ttu-id="7aff6-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="7aff6-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7aff6-135">圖示</span><span class="sxs-lookup"><span data-stu-id="7aff6-135">Icons</span></span>](../menurc/icons.md)
</dt> <dt>

<span data-ttu-id="7aff6-136">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="7aff6-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7aff6-137">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="7aff6-137">**BeginPaint**</span></span>](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="7aff6-138">**PAINTSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="7aff6-138">**PAINTSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
