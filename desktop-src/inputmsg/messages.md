---
title: 訊息
description: 本節中的主題提供特定指標輸入訊息和通知的參考規格。
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3e143990c65daad306ef6f743d25ef4e0cca8001
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375277"
---
# <a name="messages"></a><span data-ttu-id="26e85-103">訊息</span><span class="sxs-lookup"><span data-stu-id="26e85-103">Messages</span></span>

<span data-ttu-id="26e85-104">本節中的主題提供特定 [指標輸入訊息和通知](messages-and-notifications-portal.md)的參考規格。</span><span class="sxs-lookup"><span data-stu-id="26e85-104">The topics in this section provide the reference specifications for specific [Pointer Input Messages and Notifications](messages-and-notifications-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="26e85-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="26e85-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26e85-106">主題</span><span class="sxs-lookup"><span data-stu-id="26e85-106">Topic</span></span></th>
<th><span data-ttu-id="26e85-107">描述</span><span class="sxs-lookup"><span data-stu-id="26e85-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26e85-108">[<strong>DM_POINTERHITTEST</strong>] (dm-pointerhittest.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-108">[<strong>DM_POINTERHITTEST</strong>](dm-pointerhittest.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-109">傳送至視窗時，在第一次偵測到指標輸入時，為了判斷 [直接操作](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)最可能的輸入目標。</span><span class="sxs-lookup"><span data-stu-id="26e85-109">Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-110">[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-110">[<strong>WM_NCPOINTERDOWN</strong>](wm-ncpointerdown.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-111">當指標在視窗的非工作區上進行聯繫時公佈。</span><span class="sxs-lookup"><span data-stu-id="26e85-111">Posted when a pointer makes contact over the non-client area of a window.</span></span> <span data-ttu-id="26e85-112">訊息會以指標所要接觸的視窗為目標。</span><span class="sxs-lookup"><span data-stu-id="26e85-112">The message targets the window over which the pointer makes contact.</span></span> <span data-ttu-id="26e85-113">指標會隱含地捕捉至視窗，讓視窗繼續接收指標的輸入，直到它中斷 contact 為止。</span><span class="sxs-lookup"><span data-stu-id="26e85-113">The pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span> <br/> <span data-ttu-id="26e85-114">如果視窗已捕捉到此指標，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-114">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="26e85-115">相反地，[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md) 會張貼至已捕捉到此指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-115">Instead, a [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md) is posted to the window that has captured this pointer.</span></span> <br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-116">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-116">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-117">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-117">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-118">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-118">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-119">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-119">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-120">[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-120">[<strong>WM_NCPOINTERUP</strong>](wm-ncpointerup.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-121">在視窗的非工作區上建立連絡人的指標中斷連絡人時張貼。</span><span class="sxs-lookup"><span data-stu-id="26e85-121">Posted when a pointer that made contact over the non-client area of a window breaks contact.</span></span> <span data-ttu-id="26e85-122">這則訊息會以視窗為目標，指標會在該視窗上變成連絡人，而指標會在該時間點以隱含方式捕捉至視窗，讓視窗繼續接收指標的輸入，直到中斷連絡人為止，包括 [<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="26e85-122">The message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact, including the [<strong>WM_NCPOINTERUP</strong>](wm-ncpointerup.md) notification.</span></span> <br/> <span data-ttu-id="26e85-123">如果視窗已捕捉到此指標，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-123">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="26e85-124">相反地，[<strong>WM_POINTERUP</strong>] (wm-pointerup.md) 會張貼至已捕捉到此指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-124">Instead, a [<strong>WM_POINTERUP</strong>](wm-pointerup.md) is posted to the window that has captured this pointer.</span></span> <br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-125">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-125">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-126">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-126">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-127">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-127">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-128">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-128">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-129">[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-129">[<strong>WM_NCPOINTERUPDATE</strong>](wm-ncpointerupdate.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-130">張貼以提供指標的更新，以在視窗的非工作區上建立連絡人，或是當滑鼠停留 uncaptured 連絡人在視窗的非工作區上移動時。</span><span class="sxs-lookup"><span data-stu-id="26e85-130">Posted to provide an update on a pointer that made contact over the non-client area of a window or when a hovering uncaptured contact moves over the non-client area of a window.</span></span> <span data-ttu-id="26e85-131">當指標停留時，訊息會以指標發生的任何視窗為目標。</span><span class="sxs-lookup"><span data-stu-id="26e85-131">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="26e85-132">當指標與介面聯繫時，指標就會隱含地捕捉到指標所變成的視窗，而該視窗會繼續接收指標的輸入，直到中斷連絡人為止。</span><span class="sxs-lookup"><span data-stu-id="26e85-132">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span> <br/> <span data-ttu-id="26e85-133">如果視窗已捕捉到此指標，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-133">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="26e85-134">相反地，[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md) 會張貼至已捕捉到此指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-134">Instead, a [<strong>WM_POINTERUPDATE</strong>](wm-pointerupdate.md) is posted to the window that has captured this pointer.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-135">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-135">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-136">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-136">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-137">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-137">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-138">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-138">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-139">[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-139">[<strong>WM_PARENTNOTIFY</strong>](wm-parentnotify.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-140">當子系視窗發生重大動作時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-140">Sent to a window when a significant action occurs on a descendant window.</span></span> <span data-ttu-id="26e85-141">此訊息現在已擴充為包含 [<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="26e85-141">This message is now extended to include the [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md) event.</span></span> <span data-ttu-id="26e85-142">建立子視窗時，系統會在建立視窗的 [<strong>CreateWindow</strong>] (/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [<strong>CreateWindowEx</strong>] (/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式之前，傳送 [<strong>WM_PARENTNOTIFY</strong>] (/previous-versions/windows/desktop/inputmsg/wm-parentnotify) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-142">When the child window is being created, the system sends [<strong>WM_PARENTNOTIFY</strong>](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) just before the [<strong>CreateWindow</strong>](/windows/win32/api/winuser/nf-winuser-createwindowa) or [<strong>CreateWindowEx</strong>](/windows/win32/api/winuser/nf-winuser-createwindowexa) function that creates the window returns.</span></span> <span data-ttu-id="26e85-143">當子視窗被終結時，系統會先傳送訊息，然後再進行任何損毀視窗的處理。</span><span class="sxs-lookup"><span data-stu-id="26e85-143">When the child window is being destroyed, the system sends the message before any processing to destroy the window takes place.</span></span><br/> <span data-ttu-id="26e85-144">視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-144">A window receives this message through its [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-145">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-145">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-146">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-146">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-147">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-147">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-148">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-148">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-149">[<strong>WM_POINTERACTI加值稅E</strong>] (wm-pointeractivate.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-149">[<strong>WM_POINTERACTIVATE</strong>](wm-pointeractivate.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-150">當主要指標在視窗上產生 [<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md) 時，傳送至非使用中的視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-150">Sent to an inactive window when a primary pointer generates a [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md) over the window.</span></span> <span data-ttu-id="26e85-151">只要訊息保持未處理狀態，它就會向上移動父視窗鏈，直到到達最上層視窗為止。</span><span class="sxs-lookup"><span data-stu-id="26e85-151">As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window.</span></span> <span data-ttu-id="26e85-152">應用程式可以回應此訊息，以指定是否要啟用它們。</span><span class="sxs-lookup"><span data-stu-id="26e85-152">Applications can respond to this message to specify whether they wish to be activated.</span></span><br/> <span data-ttu-id="26e85-153">視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-153">A window receives this message through its [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-154">[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-154">[<strong>WM_POINTERCAPTURECHANGED</strong>](wm-pointercapturechanged.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-155">傳送至遺失輸入指標之捕捉的視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-155">Sent to a window that is losing capture of an input pointer.</span></span><br/> <span data-ttu-id="26e85-156">視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-156">A window receives this message through its [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-157">[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-157">[<strong>WM_POINTERDEVICECHANGE</strong>](wm-pointerdevicechange.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-158">當已連接數位板的監視器設定有變更時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-158">Sent to a window when there is a change in the settings of a monitor that has a digitizer attached to it.</span></span> <span data-ttu-id="26e85-159">此訊息包含顯示模式調整的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26e85-159">This message contains information regarding the scaling of the display mode.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-160">[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-160">[<strong>WM_POINTERDEVICEINRANGE</strong>](wm-pointerdeviceinrange.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-161">在輸入數位板的範圍內偵測到指標裝置時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-161">Sent to a window when a pointer device is detected within range of an input digitizer.</span></span> <span data-ttu-id="26e85-162">此訊息包含裝置及其鄰近性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26e85-162">This message contains information regarding the device and its proximity.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-163">[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-163">[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>](wm-pointerdeviceoutofrange.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-164">當指標裝置已決策與輸入數位板的範圍時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-164">Sent to a window when a pointer device has departed the range of an input digitizer.</span></span> <span data-ttu-id="26e85-165">此訊息包含裝置及其鄰近性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26e85-165">This message contains information regarding the device and its proximity.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-166">[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-166">[<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-167">當指標在視窗的工作區上進行接觸時張貼。</span><span class="sxs-lookup"><span data-stu-id="26e85-167">Posted when a pointer makes contact over the client area of a window.</span></span> <span data-ttu-id="26e85-168">此輸入訊息會以指標所用的視窗為目標，並以隱含方式將指標捕捉至視窗，讓視窗繼續接收指標的輸入，直到中斷連絡人為止。</span><span class="sxs-lookup"><span data-stu-id="26e85-168">This input message targets the window over which the pointer makes contact, and the pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span> <br/> <span data-ttu-id="26e85-169">視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-169">A window receives this message through its [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-170">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-170">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-171">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-171">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-172">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-172">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-173">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-173">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-174">[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-174">[<strong>WM_POINTERENTER</strong>](wm-pointerenter.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-175">當新指標在視窗上進入偵測範圍時傳送至視窗 (停留) ，或當現有指標在視窗界限內移動時。</span><span class="sxs-lookup"><span data-stu-id="26e85-175">Sent to a window when a new pointer enters detection range over the window (hover) or when an existing pointer moves within the boundaries of the window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-176">[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-176">[<strong>WM_POINTERLEAVE</strong>](wm-pointerleave.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-177">當指標在視窗上離開偵測範圍時傳送至視窗 (停留) 或指標移至視窗界限之外。</span><span class="sxs-lookup"><span data-stu-id="26e85-177">Sent to a window when a pointer leaves detection range over the window (hover) or when a pointer moves outside the boundaries of the window.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-178">[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-178">[<strong>WM_POINTERROUTEDAWAY</strong>](wm-pointerroutedaway.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-179">當指標輸入路由傳送至另一個進程時，在接收輸入的進程上發生。</span><span class="sxs-lookup"><span data-stu-id="26e85-179">Occurs on the process receiving input when the pointer input is routed to another process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-180">[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-180">[<strong>WM_POINTERROUTEDRELEASED</strong>](wm-pointerroutedreleased.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-181">傳送至所有進程， (透過 [<strong>AddContentWithCrossProcessChaining</strong>] 設定跨進程連結的所有進程 (/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) ，且目前的進程在收到 [<strong>WM_POINTERUP</strong>] (wm-pointerup.md) 訊息時，不會處理指標輸入) 與特定指標識別碼相關聯。</span><span class="sxs-lookup"><span data-stu-id="26e85-181">Sent to all processes (configured for cross-process chaining through [<strong>AddContentWithCrossProcessChaining</strong>](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) and not currently handling pointer input) ever associated with a specific pointer ID, when a [<strong>WM_POINTERUP</strong>](wm-pointerup.md) message is received on the current process.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-182">[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-182">[<strong>WM_POINTERROUTEDTO</strong>](wm-pointerroutedto.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-183">在進行中指標輸入時傳送，針對現有的指標識別碼，會在針對跨進程連結 ( [<strong>AddContentWithCrossProcessChaining</strong>] (/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) ) 的內容之間，從一個進程轉換成另一個進程。</span><span class="sxs-lookup"><span data-stu-id="26e85-183">Sent when ongoing pointer input, for an existing pointer ID, transitions from one process to another across content configured for cross-process chaining ([<strong>AddContentWithCrossProcessChaining</strong>](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-184">[<strong>WM_POINTERUP</strong>] (wm-pointerup.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-184">[<strong>WM_POINTERUP</strong>](wm-pointerup.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-185">當在視窗的工作區上建立連絡人的指標中斷連絡人時張貼。</span><span class="sxs-lookup"><span data-stu-id="26e85-185">Posted when a pointer that made contact over the client area of a window breaks contact.</span></span> <span data-ttu-id="26e85-186">此輸入訊息的目標視窗是指標所用的視窗，而指標會在該視窗上以隱含方式捕捉至視窗，讓視窗繼續接收輸入訊息，包括 [<strong>WM_POINTERUP</strong>] (wm-pointerup.md) 指標的通知，直到中斷連絡人為止。</span><span class="sxs-lookup"><span data-stu-id="26e85-186">This input message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input messages including the [<strong>WM_POINTERUP</strong>](wm-pointerup.md) notification for the pointer until it breaks contact.</span></span> <br/> <span data-ttu-id="26e85-187">視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-187">A window receives this message through its [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-188">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-188">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-189">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-189">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-190">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-190">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-191">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-191">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-192">[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-192">[<strong>WM_POINTERUPDATE</strong>](wm-pointerupdate.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-193">張貼以提供指標的更新，而該指標是在視窗的工作區上，或是在視窗的工作區上停留在滑鼠停留 uncaptured 指標上。</span><span class="sxs-lookup"><span data-stu-id="26e85-193">Posted to provide an update on a pointer that made contact over the client area of a window or on a hovering uncaptured pointer over the client area of a window.</span></span> <span data-ttu-id="26e85-194">當指標停留時，訊息會以指標發生的任何視窗為目標。</span><span class="sxs-lookup"><span data-stu-id="26e85-194">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="26e85-195">當指標與介面聯繫時，指標就會隱含地捕捉到指標所變成的視窗，而該視窗會繼續接收指標的輸入，直到中斷連絡人為止。</span><span class="sxs-lookup"><span data-stu-id="26e85-195">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span> <br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-196">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-196">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-197">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-197">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-198">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-198">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-199">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-199">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-200">[<strong>WM_POINTERWHEEL</strong>] (wm-pointerwheel.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-200">[<strong>WM_POINTERWHEEL</strong>](wm-pointerwheel.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-201">當滾動滾輪旋轉時，張貼至具有前景鍵盤焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-201">Posted to the window with foreground keyboard focus when a scroll wheel is rotated.</span></span> <br/> <span data-ttu-id="26e85-202">視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-202">A window receives this message through its [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-203">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-203">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-204">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-204">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-205">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-205">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-206">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-206">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26e85-207">[<strong>WM_POINTERHWHEEL</strong>] (wm-pointerhwheel.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-207">[<strong>WM_POINTERHWHEEL</strong>](wm-pointerhwheel.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-208">當水準滾輪旋轉時，張貼至具有前景鍵盤焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="26e85-208">Posted to the window with foreground keyboard focus when a horizontal scroll wheel is rotated.</span></span> <br/> <span data-ttu-id="26e85-209">視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="26e85-209">A window receives this message through its [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="26e85-210">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="26e85-210">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="26e85-211">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="26e85-211">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="26e85-212">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="26e85-212">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="26e85-213">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="26e85-213">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26e85-214">[<strong>WM_TOUCHHITTESTING</strong>] (wm-touchhittesting.md) </span><span class="sxs-lookup"><span data-stu-id="26e85-214">[<strong>WM_TOUCHHITTESTING</strong>](wm-touchhittesting.md)</span></span><br/></td>
<td><span data-ttu-id="26e85-215">傳送至觸控下的視窗，以便判斷最可能的觸控目標。</span><span class="sxs-lookup"><span data-stu-id="26e85-215">Sent to a window on a touch down in order to determine the most probable touch target.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="26e85-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="26e85-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26e85-217">指標輸入訊息參考</span><span class="sxs-lookup"><span data-stu-id="26e85-217">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

