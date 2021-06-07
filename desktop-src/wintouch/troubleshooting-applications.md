---
title: 針對應用程式進行疑難排解
description: 本節提供常見問題的解決方案。
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows Touch，疑難排解應用程式
- Windows Touch，棕櫚拒絕
- 手掌拒絕
- Windows Touch，舊版支援
- 疑難排解 Windows Touch
- 慣性，針對應用程式進行疑難排解
- 操作，疑難排解應用程式
- 手勢，疑難排解應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389d200cedc57b7f128a535355b12a9288c6e9eb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443141"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="3cdcc-111">針對應用程式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="3cdcc-111">Troubleshooting Applications</span></span>

<span data-ttu-id="3cdcc-112">本節提供常見問題的解決方案。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="3cdcc-113">一般疑難排解</span><span class="sxs-lookup"><span data-stu-id="3cdcc-113">General Troubleshooting</span></span>



| <span data-ttu-id="3cdcc-114">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-114">Category</span></span> | <span data-ttu-id="3cdcc-115">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-115">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-116">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-116">Issue</span></span>    | <span data-ttu-id="3cdcc-117">我正在執行 Windows Server 2008，但 Windows Touch 功能無法運作。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-117">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="3cdcc-118">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-118">Cause</span></span>    | <span data-ttu-id="3cdcc-119">您尚未啟用桌面體驗。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-119">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3cdcc-120">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-120">Solution</span></span> | <span data-ttu-id="3cdcc-121">開啟伺服器管理員系統管理工具：按一下 [ **開始**]，指向 [系統 **管理工具**]，然後按一下 [ **伺服器管理員**]。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-121">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="3cdcc-122">按一下左側資料行中的 [ **功能** ] 專案。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-122">Click the **Features** item in the left column.</span></span> <span data-ttu-id="3cdcc-123">按一下 [**功能**] 區段中的 [**新增功能**]。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-123">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="3cdcc-124">選取 [ **桌面體驗**]，按 **[下一步]**，然後按一下 [ **安裝**]。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-124">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



| <span data-ttu-id="3cdcc-125">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-125">Category</span></span> | <span data-ttu-id="3cdcc-126">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-126">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-127">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-127">Issue</span></span>    | <span data-ttu-id="3cdcc-128">當我在應用程式中快速移動手指時，會出現箭號，而我的手勢或操作並未正確註冊。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-128">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="3cdcc-129">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-129">Cause</span></span>    | <span data-ttu-id="3cdcc-130">在不需要筆觸的情況下啟用筆觸。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-130">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="3cdcc-131">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-131">Solution</span></span> | <span data-ttu-id="3cdcc-132">當您想要停用筆觸時，會啟用筆觸。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-132">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="3cdcc-133">如需停用筆觸的詳細資訊，請參閱 [使用捲軸來移動流覽的舊版支援](legacy-support-for-panning-with-scrollbars.md) 。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-133">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3cdcc-134">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-134">Issue</span></span></td>
<td><span data-ttu-id="3cdcc-135">我無法分辨滑鼠輸入和 Windows Touch 輸入。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-135">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cdcc-136">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-136">Cause</span></span></td>
<td><span data-ttu-id="3cdcc-137">當使用者按一下螢幕時，Windows 會針對舊版支援產生滑鼠訊息。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-137">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cdcc-138">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-138">Solution</span></span></td>
<td><span data-ttu-id="3cdcc-139">您可以呼叫<strong>WM_LBUTTONDOWN</strong>的<a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> ，並<strong>WM_LBUTTONUP</strong>訊息來判斷來源。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-139">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="3cdcc-140">下列程式碼顯示如何完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-140">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cdcc-141">C++</span><span class="sxs-lookup"><span data-stu-id="3cdcc-141">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#define MOUSEEVENTF_FROMTOUCH 0xFF515700

if ((GetMessageExtraInfo() & MOUSEEVENTF_FROMTOUCH) == MOUSEEVENTF_FROMTOUCH) { 
    // Click was generated by wisptis / Windows Touch
}else{ 
    // Click was generated by the mouse.
}
</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="3cdcc-142">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-142">Category</span></span> | <span data-ttu-id="3cdcc-143">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-143">Description</span></span> |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-144">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-144">Issue</span></span>    | <span data-ttu-id="3cdcc-145">如何? 在 Windows 7 上執行 Microsoft PixelSense 應用程式？</span><span class="sxs-lookup"><span data-stu-id="3cdcc-145">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="3cdcc-146">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-146">Cause</span></span>    | <span data-ttu-id="3cdcc-147">Windows Touch 與 Microsoft PixelSense 不相容。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-147">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="3cdcc-148">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-148">Solution</span></span> | <span data-ttu-id="3cdcc-149">您需要將目標設為 Windows 7 平臺或 Microsoft PixelSense 平臺。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-149">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="3cdcc-150">針對操作和慣性進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="3cdcc-150">Troubleshooting Manipulations and Inertia</span></span>



| <span data-ttu-id="3cdcc-151">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-151">Category</span></span> | <span data-ttu-id="3cdcc-152">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-152">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-153">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-153">Issue</span></span>    | <span data-ttu-id="3cdcc-154">我的應用程式因為沒有原因而凍結。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-154">My application is freezing for no reason.</span></span> <span data-ttu-id="3cdcc-155">我在初始化物件介面時遇到存取違規。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-155">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="3cdcc-156">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-156">Cause</span></span>    | <span data-ttu-id="3cdcc-157">使用 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)或 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)介面時遺漏 **CoInitialize** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-157">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="3cdcc-158">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-158">Solution</span></span> | <span data-ttu-id="3cdcc-159">這可能是因為將 Windows Touch 元件物件模型具現化 (COM) 物件，而不呼叫 CoInitialize。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-159">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="3cdcc-160">有時候，當您將專案從使用筆勢轉換成使用操作或慣性介面時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-160">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



| <span data-ttu-id="3cdcc-161">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-161">Category</span></span> | <span data-ttu-id="3cdcc-162">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-162">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-163">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-163">Issue</span></span>    | <span data-ttu-id="3cdcc-164">我的物件在轉譯時的旋轉不正確。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-164">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="3cdcc-165">單一手指旋轉無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-165">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3cdcc-166">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-166">Cause</span></span>    | <span data-ttu-id="3cdcc-167">設定物件的透視表不當。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-167">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3cdcc-168">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-168">Solution</span></span> | <span data-ttu-id="3cdcc-169">您未正確設定操作樞紐分析表點。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-169">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="3cdcc-170">將 [ [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) ] 和 [ [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) ] 屬性設定為您想要旋轉的物件或點中央，然後將 [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) 屬性設定為物件的半徑。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-170">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="3cdcc-171">針對 Windows Touch 輸入進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="3cdcc-171">Troubleshooting Windows Touch Input</span></span>



| <span data-ttu-id="3cdcc-172">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-172">Category</span></span> | <span data-ttu-id="3cdcc-173">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-173">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-174">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-174">Issue</span></span>    | <span data-ttu-id="3cdcc-175">我在處理 [**WM \_ 觸控**](wm-touchdown.md) 訊息之後，就會停止取得界限意見反應。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-175">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="3cdcc-176">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-176">Cause</span></span>    | <span data-ttu-id="3cdcc-177">使用 [**WM \_ 觸控**](wm-touchdown.md) 訊息而不加以處理。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-177">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3cdcc-178">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-178">Solution</span></span> | <span data-ttu-id="3cdcc-179">您可能會耗用 Windows Touch 的訊息，而不將它轉送至 **DefWindowProc**，這會導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-179">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="3cdcc-180">如需有關如何適當處理 [**WM \_ 觸控**](wm-touchdown.md)訊息的詳細資訊，請參閱 [Windows Touch 訊息的開始使用](getting-started-with-multi-touch-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-180">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3cdcc-181">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-181">Issue</span></span></td>
<td><span data-ttu-id="3cdcc-182">我要加入的是 windows .h，但是它仍指出未定義 <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-182">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cdcc-183">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-183">Cause</span></span></td>
<td><span data-ttu-id="3cdcc-184">Targetver.h 中的 Windows 版本不正確。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-184">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cdcc-185">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-185">Solution</span></span></td>
<td><span data-ttu-id="3cdcc-186">您未在專案中設定正確的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-186">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="3cdcc-187">下列程式碼說明 Windows 7 中適用于 Windows Touch 的正確設定 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-187">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cdcc-188">C++</span><span class="sxs-lookup"><span data-stu-id="3cdcc-188">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifndef WINVER                  // Specify that the minimum required platform is Windows 7.
#define WINVER 0x0601           
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3cdcc-189">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-189">Issue</span></span></td>
<td><span data-ttu-id="3cdcc-190">我的觸控輸入 x 座標和 y 座標似乎無效。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-190">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="3cdcc-191">它們是比預期值更大的值，或者它們是負數值。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-191">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cdcc-192">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-192">Cause</span></span></td>
<td><span data-ttu-id="3cdcc-193">您可能需要將觸控點轉換成圖元，或者您可能需要轉換螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-193">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cdcc-194">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-194">Solution</span></span></td>
<td><span data-ttu-id="3cdcc-195">請確定您呼叫 <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> 和 <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-195">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="3cdcc-196">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-196">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cdcc-197">C++</span><span class="sxs-lookup"><span data-stu-id="3cdcc-197">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>      POINT ptInput;
      if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
        for (int i=0; i < static_cast<INT>(cInputs); i++){
          TOUCHINPUT ti = pInputs[i];                       
          if (ti.dwID != 0){                
            // Do something with your touch input handle.
            ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
            ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
            ScreenToClient(hWnd, &ptInput);
            points[ti.dwID][0] = ptInput.x;
            points[ti.dwID][1] = ptInput.y;
          }
        }
      }</code></pre></td>
</tr>
</tbody>
</table>

<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="3cdcc-198">若要使用 <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> 函式，您的應用程式中必須有高 DPI 支援。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-198">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="3cdcc-199">如需支援高 DPI 的詳細資訊，請造訪 MSDN 的 <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">高 DPI</a> 區段。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-199">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="3cdcc-200">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-200">Category</span></span> | <span data-ttu-id="3cdcc-201">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-201">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-202">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-202">Issue</span></span>    | <span data-ttu-id="3cdcc-203">我看不到 [**wm 的 \_ 觸控**](wm-touchdown.md) 訊息，但我知道 Windows Touch 正在運作，因為我看到了 [**wm \_ 手勢**](wm-gesture.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-203">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="3cdcc-204">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-204">Cause</span></span>    | <span data-ttu-id="3cdcc-205">遺漏 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-205">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="3cdcc-206">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-206">Solution</span></span> | <span data-ttu-id="3cdcc-207">[**WM \_觸控**](wm-touchdown.md) 和 [**WM \_ 手勢**](wm-gesture.md) 訊息都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-207">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="3cdcc-208">如果您未呼叫 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)，則只會收到 **WM \_ 手勢** 訊息。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-208">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



| <span data-ttu-id="3cdcc-209">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-209">Category</span></span> | <span data-ttu-id="3cdcc-210">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-210">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-211">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-211">Issue</span></span>    | <span data-ttu-id="3cdcc-212">我注意到我在我的應用程式中收到輸入時，從我接觸到的時候，會有很小的延遲。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-212">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="3cdcc-213">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-213">Cause</span></span>    | <span data-ttu-id="3cdcc-214">手掌拒絕會導致輸入延遲。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-214">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3cdcc-215">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-215">Solution</span></span> | <span data-ttu-id="3cdcc-216">如果 **TWF \_ WANTPALM** 設定在對 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)的呼叫中，則會啟用 palm 拒絕。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-216">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="3cdcc-217">如此一來，當軟體測試輸入是來自手指、手寫筆或使用者的掌上時，就會導致短暫的 (100 ms) 延遲。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-217">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="3cdcc-218">藉由呼叫 **RegisterTouchWindow** 並清除 **TWF \_ WANTPALM** 旗標來停用 palm 拒絕。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-218">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="3cdcc-219">針對 Windows Touch 手勢進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="3cdcc-219">Troubleshooting Windows Touch Gestures</span></span>



| <span data-ttu-id="3cdcc-220">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-220">Category</span></span> | <span data-ttu-id="3cdcc-221">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-221">Description</span></span> |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-222">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-222">Issue</span></span>    | <span data-ttu-id="3cdcc-223">在處理 [**WM \_ 手勢**](wm-gesture.md) 訊息之後，我會停止取得界限意見反應。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-223">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="3cdcc-224">或者，先前工作的手勢目前無法運作。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-224">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="3cdcc-225">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-225">Cause</span></span>    | <span data-ttu-id="3cdcc-226">使用 [**WM \_ 手勢**](wm-gesture.md) 訊息而不加以處理。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-226">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3cdcc-227">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-227">Solution</span></span> | <span data-ttu-id="3cdcc-228">您可能會耗用 Windows Touch 的訊息，而不將它轉送至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)，這會導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-228">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="3cdcc-229">如需如何正確處理 [**WM \_ 手勢**](wm-gesture.md)訊息的詳細資訊，請參閱 [開始使用的 Windows 手勢](getting-started-with-multi-touch-gestures.md)。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-229">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



| <span data-ttu-id="3cdcc-230">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-230">Category</span></span> | <span data-ttu-id="3cdcc-231">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-231">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-232">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-232">Issue</span></span>    | <span data-ttu-id="3cdcc-233">我看不到 [**wm \_ 手勢**](wm-gesture.md) 訊息，但我知道 Windows Touch 正在運作，因為我看到了 [**wm \_ 觸控**](wm-touchdown.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-233">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="3cdcc-234">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-234">Cause</span></span>    | <span data-ttu-id="3cdcc-235">呼叫 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-235">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="3cdcc-236">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-236">Solution</span></span> | <span data-ttu-id="3cdcc-237">[**WM \_觸控**](wm-touchdown.md) 和 [**WM \_ 手勢**](wm-gesture.md) 訊息都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-237">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="3cdcc-238">如果您呼叫 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)，就不會收到 **WM \_ 手勢** 訊息。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-238">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3cdcc-239">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-239">Issue</span></span></td>
<td><span data-ttu-id="3cdcc-240">我看不到我預期看到的所有手勢。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-240">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="3cdcc-241">例如，我看到有識別碼 <strong>GID_PAN</strong> 但未 <strong>GID_ROTATE</strong>的手勢。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-241">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cdcc-242">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-242">Cause</span></span></td>
<td><span data-ttu-id="3cdcc-243">某些手勢（例如旋轉手勢）預設不會啟用。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-243">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cdcc-244">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-244">Solution</span></span></td>
<td><span data-ttu-id="3cdcc-245">當您收到<a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a>訊息（如<strong>WM_GESTURENOTIFY</strong>參考中所述）時，您必須呼叫<a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> ，否則您必須加入<strong>WM_GESTURENOTIFY</strong>訊息的處理常式。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-245">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="3cdcc-246">下列程式碼示範如何執行處理常式來啟用旋轉支援。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-246">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cdcc-247">C++</span><span class="sxs-lookup"><span data-stu-id="3cdcc-247">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// The message map.
BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
     ... ... ...
    ON_MESSAGE(WM_GESTURENOTIFY, OnWindowsGestureNotify)
END_MESSAGE_MAP()  

LRESULT CTestWndApp::OnWindowsGestureNotify(
    UINT    uMsg,
    WPARAM  wParam,
    LPARAM  lParam,
    BOOL&   bHandled
    ){
    GESTURECONFIG gc;
    gc.dwID    = GID_ROTATE; // The gesture identifier.
    gc.dwWant  = GC_ROTATE;  // The gesture command you are enabling for GID_ROTATE.
    gc.dwBlock = 0;          // Don&#39;t block anything.
    UINT uiGcs = 1;          // The number of gestures being set.

  BOOL bResult = SetGestureConfig(g_hMainWnd, 0, uiGcs, &gc, sizeof(GESTURECONFIG));
    if(!bResult) {
        // Something went wrong, report the error using your preferred logging.
    }

  return 0;
}  </code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3cdcc-248">如需一般手勢設定的更多範例，請參閱 <strong>SetGestureConfig</strong>。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-248">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="3cdcc-249">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-249">Category</span></span> | <span data-ttu-id="3cdcc-250">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-250">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-251">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-251">Issue</span></span>    | <span data-ttu-id="3cdcc-252">當我執行平移手勢時，我的應用程式中的自訂捲軸不會滾動。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-252">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3cdcc-253">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-253">Cause</span></span>    | <span data-ttu-id="3cdcc-254">遺漏正確 WM \_ \* 捲軸訊息的處理常式。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-254">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3cdcc-255">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-255">Solution</span></span> | <span data-ttu-id="3cdcc-256">您未 \_ \* 在自訂捲軸中處理所有的 WM 捲軸訊息。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-256">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="3cdcc-257">建議您處理 [**WM \_ 手勢**](wm-gesture.md) 訊息，而不是透過舊版支援保留自訂捲軸功能。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-257">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="3cdcc-258">您需要支援的訊息，如 [舊版支援移動捲軸的支援](legacy-support-for-panning-with-scrollbars.md)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-258">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



| <span data-ttu-id="3cdcc-259">類別</span><span class="sxs-lookup"><span data-stu-id="3cdcc-259">Category</span></span> | <span data-ttu-id="3cdcc-260">描述</span><span class="sxs-lookup"><span data-stu-id="3cdcc-260">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-261">問題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-261">Issue</span></span>    | <span data-ttu-id="3cdcc-262">我遇到手勢的延遲。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-262">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3cdcc-263">原因</span><span class="sxs-lookup"><span data-stu-id="3cdcc-263">Cause</span></span>    | <span data-ttu-id="3cdcc-264">筆觸可能會導致手勢的延遲。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-264">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="3cdcc-265">解決方法</span><span class="sxs-lookup"><span data-stu-id="3cdcc-265">Solution</span></span> | <span data-ttu-id="3cdcc-266">筆觸可能會導致應用程式收到 [**WM \_ 手勢**](wm-gesture.md) 訊息所需的時間延遲。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-266">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="3cdcc-267">如需停用筆觸的詳細資訊，請參閱 [使用捲軸來移動流覽的舊版支援](legacy-support-for-panning-with-scrollbars.md) 。</span><span class="sxs-lookup"><span data-stu-id="3cdcc-267">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3cdcc-268">相關主題</span><span class="sxs-lookup"><span data-stu-id="3cdcc-268">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cdcc-269">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="3cdcc-269">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 