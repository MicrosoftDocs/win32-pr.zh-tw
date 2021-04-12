---
title: 具有 Windows Touch 訊息的開始使用
description: 本節說明在應用程式中取得函式 Windows Touch 輸入相關聯的工作。
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows Touch，訊息
- Windows Touch，註冊觸控輸入
- Windows Touch，測試輸入數位板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375592"
---
# <a name="getting-started-with-windows-touch-messages"></a><span data-ttu-id="bfbf9-106">具有 Windows Touch 訊息的開始使用</span><span class="sxs-lookup"><span data-stu-id="bfbf9-106">Getting Started with Windows Touch Messages</span></span>

<span data-ttu-id="bfbf9-107">本節說明在應用程式中取得函式 Windows Touch 輸入相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-107">This section explains the tasks associated with getting Windows Touch input to function in your application.</span></span>

<span data-ttu-id="bfbf9-108">使用 Windows Touch 訊息時，通常會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="bfbf9-108">The following steps are typically performed when working with Windows Touch messages:</span></span>

1.  <span data-ttu-id="bfbf9-109">測試輸入數位板的功能。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-109">Test the capabilities of the input digitizer.</span></span>
2.  <span data-ttu-id="bfbf9-110">註冊以接收 Windows Touch 的訊息。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-110">Register to receive Windows Touch messages.</span></span>
3.  <span data-ttu-id="bfbf9-111">處理訊息。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-111">Handle the messages.</span></span>

<span data-ttu-id="bfbf9-112">用於 Windows Touch 的訊息為 [**WM \_ 觸控**](wm-touchdown.md)。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-112">The message used for Windows Touch is [**WM\_TOUCH**](wm-touchdown.md).</span></span> <span data-ttu-id="bfbf9-113">此訊息表示與數位板聯繫的各種狀態。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-113">This message indicates the various states of contact with a digitizer.</span></span>

## <a name="testing-the-capabilities-of-the-input-digitizer"></a><span data-ttu-id="bfbf9-114">測試輸入數位板的功能</span><span class="sxs-lookup"><span data-stu-id="bfbf9-114">Testing the Capabilities of the Input Digitizer</span></span>

<span data-ttu-id="bfbf9-115">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)函式可用來查詢輸入數位板的功能，方法是傳入 **SM \_ 數位化** 器的 *nIndex* 值。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-115">The [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function can be used to query the capabilities of the input digitizer by passing in the *nIndex* value of **SM\_DIGITIZER**.</span></span> <span data-ttu-id="bfbf9-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 會傳回位欄位，指出裝置是否就緒、裝置是否支援畫筆或觸控、輸入裝置是否為整合式或外部，以及裝置是否支援多個輸入 (Windows Touch) 。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) returns a bit field that indicates whether the device is ready, whether the device supports pen or touch, whether the input device is integrated or external, and whether the device supports multiple inputs (Windows Touch).</span></span> <span data-ttu-id="bfbf9-117">下表顯示各種欄位的位。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-117">The following table shows the bits for the various fields.</span></span>



| <span data-ttu-id="bfbf9-118">bit</span><span class="sxs-lookup"><span data-stu-id="bfbf9-118">Bit</span></span>   | <span data-ttu-id="bfbf9-119">8</span><span class="sxs-lookup"><span data-stu-id="bfbf9-119">8</span></span>           | <span data-ttu-id="bfbf9-120">7</span><span class="sxs-lookup"><span data-stu-id="bfbf9-120">7</span></span>           | <span data-ttu-id="bfbf9-121">6</span><span class="sxs-lookup"><span data-stu-id="bfbf9-121">6</span></span>        | <span data-ttu-id="bfbf9-122">5</span><span class="sxs-lookup"><span data-stu-id="bfbf9-122">5</span></span>        | <span data-ttu-id="bfbf9-123">4</span><span class="sxs-lookup"><span data-stu-id="bfbf9-123">4</span></span>            | <span data-ttu-id="bfbf9-124">3</span><span class="sxs-lookup"><span data-stu-id="bfbf9-124">3</span></span>              | <span data-ttu-id="bfbf9-125">2</span><span class="sxs-lookup"><span data-stu-id="bfbf9-125">2</span></span>              | <span data-ttu-id="bfbf9-126">1</span><span class="sxs-lookup"><span data-stu-id="bfbf9-126">1</span></span>                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| <span data-ttu-id="bfbf9-127">值</span><span class="sxs-lookup"><span data-stu-id="bfbf9-127">Value</span></span> | <span data-ttu-id="bfbf9-128">堆疊就緒</span><span class="sxs-lookup"><span data-stu-id="bfbf9-128">Stack Ready</span></span> | <span data-ttu-id="bfbf9-129">多重輸入</span><span class="sxs-lookup"><span data-stu-id="bfbf9-129">Multi-input</span></span> | <span data-ttu-id="bfbf9-130">保留</span><span class="sxs-lookup"><span data-stu-id="bfbf9-130">Reserved</span></span> | <span data-ttu-id="bfbf9-131">保留</span><span class="sxs-lookup"><span data-stu-id="bfbf9-131">Reserved</span></span> | <span data-ttu-id="bfbf9-132">外部畫筆</span><span class="sxs-lookup"><span data-stu-id="bfbf9-132">External Pen</span></span> | <span data-ttu-id="bfbf9-133">整合式畫筆</span><span class="sxs-lookup"><span data-stu-id="bfbf9-133">Integrated Pen</span></span> | <span data-ttu-id="bfbf9-134">外部觸控</span><span class="sxs-lookup"><span data-stu-id="bfbf9-134">External Touch</span></span> | <span data-ttu-id="bfbf9-135">整合式觸控</span><span class="sxs-lookup"><span data-stu-id="bfbf9-135">Integrated Touch</span></span> |



 

<span data-ttu-id="bfbf9-136">若要測試特定功能的命令結果，您可以使用位 & 運算子和您要測試的特定位。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-136">To test the result from the command for a particular feature, you can use the bitwise & operator and the particular bit you are testing.</span></span> <span data-ttu-id="bfbf9-137">例如，若要測試 Windows Touch，您會測試第七個順序位是否設定為十六進位)  (0x40。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-137">For example, to test for Windows Touch, you would test that the seventh-order bit is set (0x40 in hex).</span></span> <span data-ttu-id="bfbf9-138">下列程式碼範例顯示如何測試這些值。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-138">The following code example shows how these values could be tested.</span></span>


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



<span data-ttu-id="bfbf9-139">下表列出用來測試輸入數位板之觸控功能的 windows. h 中定義的常數。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-139">The following table lists the constants defined in windows.h for testing touch capabilities of the input digitizer.</span></span>



| <span data-ttu-id="bfbf9-140">Name</span><span class="sxs-lookup"><span data-stu-id="bfbf9-140">Name</span></span>                   | <span data-ttu-id="bfbf9-141">值</span><span class="sxs-lookup"><span data-stu-id="bfbf9-141">Value</span></span>      | <span data-ttu-id="bfbf9-142">描述</span><span class="sxs-lookup"><span data-stu-id="bfbf9-142">Description</span></span>                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfbf9-143">TABLET \_ 設定 \_ 無</span><span class="sxs-lookup"><span data-stu-id="bfbf9-143">TABLET\_CONFIG\_NONE</span></span>   | <span data-ttu-id="bfbf9-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfbf9-144">0x00000000</span></span> | <span data-ttu-id="bfbf9-145">輸入數位板沒有觸控功能。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-145">The input digitizer does not have touch capabilities.</span></span>                                                                                                                                         |
| <span data-ttu-id="bfbf9-146">NID \_ 整合式 \_ 觸控</span><span class="sxs-lookup"><span data-stu-id="bfbf9-146">NID\_INTEGRATED\_TOUCH</span></span> | <span data-ttu-id="bfbf9-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bfbf9-147">0x00000001</span></span> | <span data-ttu-id="bfbf9-148">整合式觸控數位板用於輸入。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-148">An integrated touch digitizer is used for input.</span></span>                                                                                                                                              |
| <span data-ttu-id="bfbf9-149">NID \_ 外部 \_ 觸控</span><span class="sxs-lookup"><span data-stu-id="bfbf9-149">NID\_EXTERNAL\_TOUCH</span></span>   | <span data-ttu-id="bfbf9-150">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bfbf9-150">0x00000002</span></span> | <span data-ttu-id="bfbf9-151">外部觸控數位板用於輸入。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-151">An external touch digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="bfbf9-152">NID \_ 整合式 \_ 畫筆</span><span class="sxs-lookup"><span data-stu-id="bfbf9-152">NID\_INTEGRATED\_PEN</span></span>   | <span data-ttu-id="bfbf9-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="bfbf9-153">0x00000004</span></span> | <span data-ttu-id="bfbf9-154">整合式畫筆數位板用於輸入。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-154">An integrated pen digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="bfbf9-155">NID \_ 外部 \_ 畫筆</span><span class="sxs-lookup"><span data-stu-id="bfbf9-155">NID\_EXTERNAL\_PEN</span></span>     | <span data-ttu-id="bfbf9-156">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bfbf9-156">0x00000008</span></span> | <span data-ttu-id="bfbf9-157">外部畫筆數位板用於輸入。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-157">An external pen digitizer is used for input.</span></span>                                                                                                                                                  |
| <span data-ttu-id="bfbf9-158">NID \_ 多重 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="bfbf9-158">NID\_MULTI\_INPUT</span></span>      | <span data-ttu-id="bfbf9-159">0x00000040</span><span class="sxs-lookup"><span data-stu-id="bfbf9-159">0x00000040</span></span> | <span data-ttu-id="bfbf9-160">輸入支援多個輸入的數位板會用於輸入。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-160">An input digitizer with support for multiple inputs is used for input.</span></span>                                                                                                                        |
| <span data-ttu-id="bfbf9-161">NID \_ 就緒</span><span class="sxs-lookup"><span data-stu-id="bfbf9-161">NID\_READY</span></span>             | <span data-ttu-id="bfbf9-162">0x00000080</span><span class="sxs-lookup"><span data-stu-id="bfbf9-162">0x00000080</span></span> | <span data-ttu-id="bfbf9-163">輸入數位板已備妥可供輸入。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-163">The input digitizer is ready for input.</span></span> <span data-ttu-id="bfbf9-164">如果未設定此值，可能表示 tablet 服務已停止、不支援數位板，或尚未安裝數位板驅動程式。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-164">If this value is unset, it may mean that the tablet service is stopped, the digitizer is not supported, or digitizer drivers have not been installed.</span></span> |



 

<span data-ttu-id="bfbf9-165">檢查 NID \_ \* 值是檢查使用者電腦功能以設定觸控、畫筆或非平板電腦輸入之應用程式的實用方式。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-165">Checking the NID\_\* values is a useful way of checking the capabilities of a user's computer to configure your application for touch, pen, or non-tablet input.</span></span> <span data-ttu-id="bfbf9-166">例如，如果您有動態使用者介面 (UI) 並且想要自動設定它，您可以檢查 NID \_ 整合式 \_ 觸控、NID \_ 多點觸控，並且可以在使用者第一次執行應用程式時取得最大的潤色數目。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-166">For example, if you have a dynamic user interface (UI) and want to automatically configure some of it, you could check for NID\_INTEGRATED\_TOUCH, NID\_MULTITOUCH, and could get the maximum number of touches the first time that a user runs your application.</span></span>

> [!Note]  
> <span data-ttu-id="bfbf9-167">SM GETSYSTEMMETRICS 有一些固有的限制 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-167">There are some inherent limitations for SM\_GETSYSTEMMETRICS.</span></span> <span data-ttu-id="bfbf9-168">例如，不支援隨插即用。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-168">For example, there is no support for plug and play.</span></span> <span data-ttu-id="bfbf9-169">基於這個理由，使用此函式作為永久設定的方法時，請特別小心。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-169">For this reason, use caution when using this function as a means for permanent configuration.</span></span>

 

## <a name="registering-to-receive-windows-touch-input"></a><span data-ttu-id="bfbf9-170">註冊接收 Windows Touch 輸入</span><span class="sxs-lookup"><span data-stu-id="bfbf9-170">Registering to Receive Windows Touch Input</span></span>

<span data-ttu-id="bfbf9-171">在接收 Windows Touch 輸入之前，應用程式必須先註冊才能接收 Windows Touch 輸入。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-171">Before receiving Windows Touch input, applications must first register to receive Windows Touch input.</span></span> <span data-ttu-id="bfbf9-172">藉由註冊應用程式視窗，應用程式會指出它具有觸控相容性。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-172">By registering the application window, the application indicates that it is touch compatible.</span></span> <span data-ttu-id="bfbf9-173">應用程式註冊其視窗之後，就會在視窗上進行輸入時，將來自 Windows Touch 驅動程式的通知轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-173">After the application registers its window, notifications from the Windows Touch driver are forwarded to the application when input is made on the window.</span></span> <span data-ttu-id="bfbf9-174">當應用程式關閉時，它會取消註冊其視窗以停用通知。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-174">When the application shuts down, it unregisters its window to disable notifications.</span></span>

> [!Note]  
> <span data-ttu-id="bfbf9-175">[**WM \_觸控**](wm-touchdown.md) 訊息目前是「貪心的」。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-175">[**WM\_TOUCH**](wm-touchdown.md) messages are currently "greedy."</span></span> <span data-ttu-id="bfbf9-176">在視窗上收到第一個觸控訊息之後，所有觸控訊息都會傳送到該視窗，直到另一個視窗獲得焦點為止。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-176">After the first touch message is received on a window, all touch messages are sent to that window until another window receives focus.</span></span>

 

> [!Note]  
> <span data-ttu-id="bfbf9-177">根據預設，您會收到 [**wm \_ 手勢**](wm-gesture.md) 訊息，而非 [**wm \_ 觸控**](wm-touchdown.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-177">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages instead of [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="bfbf9-178">如果您呼叫 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)，就會停止接收 **WM \_ 手勢** 訊息。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-178">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving **WM\_GESTURE** messages.</span></span>

 

<span data-ttu-id="bfbf9-179">下列程式碼示範如何註冊應用程式，以接收 Win32 應用程式中的 Windows Touch 訊息。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-179">The following code demonstrates how an application could register to receive Windows Touch messages in a Win32 application.</span></span>


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a><span data-ttu-id="bfbf9-180">處理 Windows Touch 訊息</span><span class="sxs-lookup"><span data-stu-id="bfbf9-180">Handling Windows Touch Messages</span></span>

<span data-ttu-id="bfbf9-181">您可以透過許多方式，在 Windows 作業系統中處理來自應用程式的 Windows Touch 訊息。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-181">You can handle the Windows Touch messages from applications in Windows operating systems in many ways.</span></span> <span data-ttu-id="bfbf9-182">如果您正在設計 GUI 應用程式，請在函式內新增程式碼 `WndProc` 以處理感興趣的訊息。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-182">If you are programming a GUI application, you add code within the `WndProc` function to handle the messages of interest.</span></span> <span data-ttu-id="bfbf9-183">如果您要在 MFC) 或 managed 應用程式的 MFC (程式設計，您可以為感興趣的訊息加入處理常式。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-183">If you are programming a Microsoft Foundation Class (MFC) or managed application, you add handlers for the messages of interest.</span></span> <span data-ttu-id="bfbf9-184">下列程式碼範例示範如何在 Windows 應用程式中從 WndProc 處理觸控訊息。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-184">The following code example shows how touch messages could be handled from WndProc in a Windows-based application.</span></span>


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





<span data-ttu-id="bfbf9-185">下列程式碼會示範如何執行訊息對應和訊息處理常式。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-185">The following code shows how you can implement the message map and a message handler.</span></span> <span data-ttu-id="bfbf9-186">請注意，訊息必須在訊息對應中宣告，然後才能執行訊息的處理常式。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-186">Note that the messages must be declared in the message map and then the handler for the message should be implemented.</span></span> <span data-ttu-id="bfbf9-187">例如，在 MFC 應用程式中，可以在對話方塊程式碼中宣告這項功能。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-187">For example, in an MFC application, this could be declared in the dialog code.</span></span> <span data-ttu-id="bfbf9-188">另請注意，交談視窗的函式 `OnInitDialog` 必須包含對 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) 的呼叫，例如 `RegisterTouchWindow(m_hWnd, 0)` 。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-188">Note also, that the `OnInitDialog` function for your dialog window would have to include a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) such as `RegisterTouchWindow(m_hWnd, 0)`.</span></span>


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



<span data-ttu-id="bfbf9-189">觸碰視窗將表示從快顯視窗中的觸控。</span><span class="sxs-lookup"><span data-stu-id="bfbf9-189">Touching the window will indicate touches from a pop-up window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfbf9-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfbf9-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfbf9-191">Windows Touch 輸入</span><span class="sxs-lookup"><span data-stu-id="bfbf9-191">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 