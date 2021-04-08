---
title: 桌面活動仲裁者
description: 桌面活動仲裁者
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- 電池壽命
- 連線待命
- 懸 架
- 節流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b8bb3d7925633d3feca8bb6ed5af191670af681
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103683212"
---
# <a name="desktop-activity-moderator"></a><span data-ttu-id="cf9e3-107">桌面活動仲裁者</span><span class="sxs-lookup"><span data-stu-id="cf9e3-107">Desktop Activity Moderator</span></span>

## <a name="platform"></a><span data-ttu-id="cf9e3-108">平台</span><span class="sxs-lookup"><span data-stu-id="cf9e3-108">Platform</span></span>

<span data-ttu-id="cf9e3-109">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="cf9e3-109">**Clients** – Windows 8</span></span> 


> [!Note]  
> <span data-ttu-id="cf9e3-110">只有在支援連線待命的 Windows 8 用戶端電腦上才會出現此 DAM。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-110">The DAM is present only on Windows 8 client machines that support connected standby.</span></span> <span data-ttu-id="cf9e3-111">伺服器 Sku 上沒有該 DAM。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-111">The DAM is not present on server SKUs.</span></span>

 

  

> [!Note]  
> <span data-ttu-id="cf9e3-112">針對 Windows 8 所建立的 Windows Store 應用程式不會受到 DAM 的影響。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-112">Windows Store apps built for Windows 8 are not impacted by the DAM.</span></span>

 

  
</dl>

## <a name="description"></a><span data-ttu-id="cf9e3-113">Description</span><span class="sxs-lookup"><span data-stu-id="cf9e3-113">Description</span></span>

<span data-ttu-id="cf9e3-114">我們的客戶轉向更輕量、更小、更多行動平臺，以滿足其運算需求。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-114">Our customers are shifting towards lighter, smaller, more mobile platforms to satisfy their computing needs.</span></span> <span data-ttu-id="cf9e3-115">在轉移至行動裝置的過程中，使用者已越來越在意其裝置的電池壽命。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-115">As part of the shift to mobile devices, users have become increasingly concerned about battery life of their devices.</span></span> <span data-ttu-id="cf9e3-116">「桌面活動仲裁者」 (「DAM) 是 Windows 8 的其中一項新功能，其設計目的是為了確保支援連線待命的裝置具有一致且長時間的電池壽命。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-116">The Desktop Activity Moderator (DAM) is one of several new features in Windows 8 designed to ensure consistent, long battery life for devices that support connected standby.</span></span>

<span data-ttu-id="cf9e3-117">當裝置開啟電源，但畫面已關閉時，就會發生連線待命。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-117">Connected standby occurs when the device is powered on, but the screen is turned off.</span></span> <span data-ttu-id="cf9e3-118">在此電源狀態中，系統在技術上一律會「開啟」 (，以支援郵件、VoIP、社交網路和 Windows Store 應用程式的立即訊息) 等重要案例。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-118">In this power state, the system is technically always “on” (to support key scenarios like mail, VoIP, social networking, and instant messaging with Windows Store apps).</span></span> <span data-ttu-id="cf9e3-119">它類似于當使用者按下電源按鈕時，智慧型手機所在的狀態。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-119">It is analogous to the state a smart phone is in when the user presses the power button.</span></span>

<span data-ttu-id="cf9e3-120">因此，軟體 (包括應用程式和作業系統軟體) 在連線待命期間必須有良好的行為。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-120">As such, software (including apps and operating system software) must be well-behaved during connected standby.</span></span> <span data-ttu-id="cf9e3-121">建立的 DAM 是為了隱藏桌面應用程式執行，其方式類似于 ACPI 裝置上的睡眠狀態 (S3) 。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-121">The DAM was created to suppress desktop app execution in a manner similar to the Sleep state (S3 on ACPI devices).</span></span> <span data-ttu-id="cf9e3-122">這樣做的方法是，在連線待命專案的情況下，暫停或節流整個系統上的桌面軟體處理常式。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-122">It does this by suspending or throttling desktop software processes across the system upon connected standby entry.</span></span> <span data-ttu-id="cf9e3-123">這可讓支援連線待命的系統提供最小化的資源使用量和長時間一致的電池壽命，同時讓 Windows Store 應用程式能夠提供其所保證的連線體驗。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-123">This enables systems that support connected standby to deliver minimized resource usage and long, consistent battery life while enabling Windows Store apps to deliver the connected experiences they promise.</span></span>

## <a name="details"></a><span data-ttu-id="cf9e3-124">詳細資料</span><span class="sxs-lookup"><span data-stu-id="cf9e3-124">Details</span></span>

<span data-ttu-id="cf9e3-125">如果系統支援連線待命，則是在系統開機時載入和初始化的一種核心模式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-125">The DAM is a kernel -mode driver that is loaded and initialized at system boot if the system supports connected standby.</span></span> <span data-ttu-id="cf9e3-126"> (這是藉由評估 CallNtPowerInformation 所傳回之系統電源功能結構中的 AOAC 欄位 \_ \_ 是否設定為 TRUE) 來決定。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-126">(This is determined by evaluating if the AOAC field in the SYSTEM\_POWER\_CAPABILITIES structure returned by CallNtPowerInformation is set to TRUE).</span></span>

<span data-ttu-id="cf9e3-127">當啟用了 DAM 並建立您的桌面進程時，[DAM] 會將您的進程新增至系統管理的工作物件：</span><span class="sxs-lookup"><span data-stu-id="cf9e3-127">When the DAM is enabled and your desktop process is created, the DAM adds your process to system-managed job objects:</span></span>

-   <span data-ttu-id="cf9e3-128">如果進程是在會話0中建立的，則會將進程新增至受限於 **節流** 的工作物件</span><span class="sxs-lookup"><span data-stu-id="cf9e3-128">If the process was created in session 0, DAM adds the process to a job object subject to **throttling**</span></span>
-   <span data-ttu-id="cf9e3-129">如果程式是在互動式會話中建立 (會話1或更高的) ，則 [DAM] 會將處理常式新增 **至可能** 擱置的工作物件。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-129">If the process was created in an interactive session (session 1 or higher), DAM adds the process to a job object subject to **suspension**</span></span>

> [!Note]  
> <span data-ttu-id="cf9e3-130">針對 Windows 8，工作物件可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-130">For Windows 8, job objects can be nested.</span></span> <span data-ttu-id="cf9e3-131">這表示，使用工作物件的 DAM 時，不會干擾應用程式的現有工作物件使用方式。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-131">This means that the DAM’s usage of job objects does not interfere with an app’s existing usage of job objects.</span></span>

 

<span data-ttu-id="cf9e3-132">當畫面開啟時，會未佔用 DAM，且不會影響系統上的任何處理程式。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-132">When the screen is on, the DAM is disengaged and does not impact any processes on the system.</span></span> <span data-ttu-id="cf9e3-133">當系統處於連線待命狀態時，根據系統上的活動而定，DAM 可能會節流或暫停處理常式。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-133">When the system is in connected standby, depending on activity on the system, DAM might throttle or suspend processes.</span></span>

-   <span data-ttu-id="cf9e3-134">受擱置的進程會擱置其所有線程 (不允許在任何情況下執行) ;維護應用程式狀態 (進程記憶體) </span><span class="sxs-lookup"><span data-stu-id="cf9e3-134">Processes that are subject to suspension have all their threads suspended (not allowed to run under any circumstances); app state (process memory) is maintained</span></span>
-   <span data-ttu-id="cf9e3-135">受擱置和 unsuspended 之間的節流週期所限制的進程， (很長的時間會花在暫停的狀態) </span><span class="sxs-lookup"><span data-stu-id="cf9e3-135">Processes that are subject to throttling cycle between suspended and unsuspended (a large majority of time is spent in the suspended state)</span></span>
    -   <span data-ttu-id="cf9e3-136">請注意，Windows 可能也會偵測到重要的活動發生，而且可能會在此活動期間，在較長的時間內將節流的服務暫停</span><span class="sxs-lookup"><span data-stu-id="cf9e3-136">Be aware that Windows might also detect that critical activities are occurring and might unsuspend throttled services for longer periods of time during this activity</span></span>
    -   <span data-ttu-id="cf9e3-137">此外，請注意，在連線待命環境中，感應器和網路可能無法使用，因此，您應該針對大部分的程式設計節流的程式以復原網路狀況不佳的 (情況，這並不需要進行任何變更) </span><span class="sxs-lookup"><span data-stu-id="cf9e3-137">Also, note that while in connected standby, sensors and networks might not be available, so throttled processes should be designed to be resilient to poor network conditions (for most processes, this doesn’t require any change)</span></span>

<span data-ttu-id="cf9e3-138">當您參與或未佔用 DAM 暫止時，會觸發將 WM \_ POWERBROADCAST 訊息傳遞給那些處理常式的處理常式，而這些進程可能會透過 API 呼叫或相容性填充碼來進入訊息傳遞 (，稍後) 所述。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-138">When DAM suspension is engaged or disengaged, DAM triggers delivery of a WM\_POWERBROADCAST message to those processes subject to suspension that have opted-in to message delivery (via API call or compatibility shim, described later).</span></span> <span data-ttu-id="cf9e3-139">在幾秒鐘的延遲之後，DAM 會暫停處理常式。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-139">After a few seconds delay, DAM suspends the process.</span></span>

<span data-ttu-id="cf9e3-140">當您參與或未佔用 DAM 節流時，不會有任何通知。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-140">There are no notifications when DAM throttling is engaged or disengaged.</span></span> <span data-ttu-id="cf9e3-141">進程應該不需要修改;進程會繼續運作，但速度較慢。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-141">Processes should not need modification; processes continue to function, albeit at a slower rate.</span></span>

## <a name="manifestation"></a><span data-ttu-id="cf9e3-142">表現</span><span class="sxs-lookup"><span data-stu-id="cf9e3-142">Manifestation</span></span>

<span data-ttu-id="cf9e3-143">處理常式通常會在連線的待命狀態期間暫停或節流。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-143">Processes are often suspended or throttled during the connected standby state.</span></span> <span data-ttu-id="cf9e3-144">在大部分的已暫止的應用程式中，這應該與 S3 暫停/繼續或 S4 休眠/繼續轉換非常類似。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-144">To the majority of suspended apps, this should be very similar to an S3 suspend / resume or S4 hibernate / resume transition.</span></span> <span data-ttu-id="cf9e3-145">表徵可能包含但不限於執行時間/執行時間與時鐘時間的不一致、計時器行為不一致，或在暫停完成之前和之後的作業系統狀態大幅變更。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-145">Manifestations might include but are not limited to inconsistencies in uptime / runtime vs. wall clock time, inconsistencies in timer behavior, or dramatic changes in operating system state before and after the suspend completes.</span></span>

<span data-ttu-id="cf9e3-146">暫止和節流會以一個單位的形式進行， (所有可暫停的進程都已暫止並 unsuspended，而且所有可進行節流處理的處理常式會在一致的) 中進行節流和調節，因此兩個已暫止進程或兩個節流程式之間的通訊不會造成問題</span><span class="sxs-lookup"><span data-stu-id="cf9e3-146">Suspension and throttling happens as a unit (all suspendable processes are suspended and unsuspended in unison, and all processes that can be throttled are throttled and unthrottled in unison), so communication between two suspended processes or two throttled processes does not pose a problem.</span></span>

<span data-ttu-id="cf9e3-147">依賴跨進程通訊的軟體可能需要特別考慮：</span><span class="sxs-lookup"><span data-stu-id="cf9e3-147">Software that relies on cross-process communication might need special consideration:</span></span>

-   <span data-ttu-id="cf9e3-148">**會話0中處理常式之間的通訊 (節流) 和會話 1 + (暫止)** –範例包括代表目前服務狀態的紙匣圖示或 UI 元件</span><span class="sxs-lookup"><span data-stu-id="cf9e3-148">**Communication between processes in session 0 (throttled) and session 1+ (suspended)** – examples include tray icons or UI components that represent current service state</span></span>
-   <span data-ttu-id="cf9e3-149">**使用者模式中元件之間的通訊 (會話0或 1) 和驅動程式 (但兩者都不會受到節流或暫停)** –範例包括代表驅動程式運作的服務</span><span class="sxs-lookup"><span data-stu-id="cf9e3-149">**Communication between components in user mode (session 0 or 1) and drivers (which are neither throttled nor suspended)** – examples include services that do work on behalf of a driver</span></span>

<span data-ttu-id="cf9e3-150">在這些情況下，如果未正確處理跨進程通訊，則應用程式可能會顯示為無回應或沒有回應 (雖然使用者可能不會直接看到這種影響，因為在連線待命) 中，畫面將會關閉。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-150">In these cases, if cross-process communication is not handled correctly, apps can appear hung or unresponsive (though the user might not see this impact directly, as the screen will be off when in connected standby).</span></span> <span data-ttu-id="cf9e3-151">不過，在大部分情況下，應該已經開發服務和驅動程式，以針對跨進程通訊問題進行穩固的處理。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-151">In most cases, however, services and drivers should already be developed to be robust against cross-process communication issues.</span></span>

<span data-ttu-id="cf9e3-152">建立或相依于網站之軟體的廠商，應該考慮程式暫止如何影響連接存留期和交握。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-152">Vendors who create software for, or dependent on, the web should consider how process suspension affects connection lifetimes and handshakes.</span></span> <span data-ttu-id="cf9e3-153">此外，因為在連線待命模式時可能無法使用網路連線能力，所以在會話0中建立之進程的開發人員應該特別注意間歇性網路連接對進程有何影響。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-153">Additionally, because network connectivity might not be available when in Connected Standby mode, developers of processes created in session 0 should be especially aware of how intermittent network connections affect the process.</span></span>

## <a name="solution"></a><span data-ttu-id="cf9e3-154">解決方法</span><span class="sxs-lookup"><span data-stu-id="cf9e3-154">Solution</span></span>

<span data-ttu-id="cf9e3-155">Microsoft Store 應用程式不會受到 DAM 的影響。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-155">Windows Store apps are not impacted by the DAM.</span></span> <span data-ttu-id="cf9e3-156">如果您的桌面應用程式受到了 DAM 的影響，您可以在暫停進行之前要求通知 (例如，使用下列其中一種方法來儲存狀態或關閉網路連接) ：</span><span class="sxs-lookup"><span data-stu-id="cf9e3-156">If your desktop app is impacted by the DAM, you can request notifications before suspension is engaged (for example, to save state or close network connections) using one of these methods:</span></span>

-   <span data-ttu-id="cf9e3-157">如果您的應用程式有 (HWND) 的視窗，而您想要透過視窗程式處理這些通知，請呼叫 [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) 來註冊這些訊息 (或 [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) 以取消註冊) 。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-157">If your app has a window (HWND) and you want to handle these notifications through your window procedure, call [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) to register for these messages (or [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) to unregister).</span></span> <span data-ttu-id="cf9e3-158">您可以使用 \_ \_ \_ 旗標參數中的裝置通知視窗控制碼，並將視窗的 HWND 以收件者參數的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-158">You can use DEVICE\_NOTIFY\_WINDOW\_HANDLE in the Flags parameter, and pass your window’s HWND in as the Recipient parameter.</span></span> <span data-ttu-id="cf9e3-159">收到的訊息是 WM \_ POWERBROADCAST 訊息。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-159">The message received is the WM\_POWERBROADCAST message.</span></span>
-   <span data-ttu-id="cf9e3-160">如果您的應用程式沒有 (HWND) 的視窗，或您想要直接回呼，請呼叫 [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) 來註冊這些訊息 (或 [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) 以取消註冊) 。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-160">If your app does not have a window (HWND) or you want a direct callback, call [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) to register for these messages (or [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) to unregister).</span></span> <span data-ttu-id="cf9e3-161">您必須 \_ \_ 在旗標參數中使用裝置通知回呼，並 \_ \_ \_ 在收件者參數中傳遞類型 PDEVICE 通知訂閱參數的值。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-161">You must use DEVICE\_NOTIFY\_CALLBACK in the Flags parameter and pass a value of type PDEVICE\_NOTIFY\_SUBSCRIBE\_PARAMETERS in the Recipient parameter.</span></span>
-   <span data-ttu-id="cf9e3-162">如果無法重新編譯您的應用程式，您可以 \_ 使用 PromoteDAM 填充碼) ，選擇透過 [AppCompat 工具](../win7appqual/application-compatibility-toolkit--act-.md) 組 (接收這些 WM 的 POWERBROADCAST 訊息。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-162">If your app cannot be recompiled, you can opt in to receive these WM\_POWERBROADCAST messages via the [AppCompat toolkit](../win7appqual/application-compatibility-toolkit--act-.md) (using the PromoteDAM shim).</span></span>

<span data-ttu-id="cf9e3-163">暫止訊息是 \_ 使用 wParam = PBT APMSUSPEND 的 WM POWERBROADCAST \_ ; 此訊息會同時廣播到系統上所有已選擇的進程。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-163">The suspend message is WM\_POWERBROADCAST with wParam=PBT\_APMSUSPEND; this message is broadcast concurrently to all opted in processes on the system.</span></span> <span data-ttu-id="cf9e3-164">您的應用程式必須快速且有效率地在暫止路徑上執行任何工作。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-164">Your app must perform any work on the suspend path quickly and efficiently.</span></span> <span data-ttu-id="cf9e3-165">廣播通知是全域的，而不是每個進程，因此，如果此路徑中所需的工作很廣泛，則您的進程可能會爭用系統資源。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-165">The timeout after the broadcast notification is global, not per process, so your process might be contending for system resources if the work required in this path is extensive.</span></span>

<span data-ttu-id="cf9e3-166">Resume 訊息是 \_ 具有 wParam = PBT APMRESUME 的 WM POWERBROADCAST \_ ; 此訊息會在繼續進行時，同時廣播到所有選擇的進程。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-166">The resume message is WM\_POWERBROADCAST with wParam=PBT\_APMRESUME; this message is broadcast concurrently to all opted in processes after a resume.</span></span> <span data-ttu-id="cf9e3-167">不保證從連線待命傳遞到系統結束的相對時間。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-167">Relative time of delivery to the system exit from connected standby is not guaranteed.</span></span>

<span data-ttu-id="cf9e3-168">針對相機相關的應用程式，當發生電源狀態轉換時，應用程式必須釋放所有對相機的參考 (所有的 capture 管線物件都必須關閉並處置) 。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-168">For camera related applications, when power state transition is taking place, during the suspension notification, applications must release all references to the camera (all capture pipeline objects must be shutdown and disposed of).</span></span>  <span data-ttu-id="cf9e3-169">若要避免可能的電池耗盡，在 Windows 10 RS3 + 系統上 Windows 相機框架伺服器服務會在應用程式未正確處理擱置通知時關閉所有的捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-169">To avoid possible battery drain, on Windows 10 RS3+ systems Windows Camera Frame Server service will close all capture sessions if the application does not handle the suspension notification properly.</span></span>  <span data-ttu-id="cf9e3-170">這是因為當系統離開待命或 S3/S4 狀態時，應用程式的「捕捉管線」將不再處於「作用中」狀態。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-170">The side effect of this is that when the system comes out of standby or S3/S4 state, the application’s capture pipeline is no longer in a working state.</span></span>

## <a name="tests"></a><span data-ttu-id="cf9e3-171">測試</span><span class="sxs-lookup"><span data-stu-id="cf9e3-171">Tests</span></span>

<span data-ttu-id="cf9e3-172">在連線的待命轉換之間測試您的軟體。</span><span class="sxs-lookup"><span data-stu-id="cf9e3-172">Test your software across connected standby transitions.</span></span>

## <a name="resources"></a><span data-ttu-id="cf9e3-173">資源</span><span class="sxs-lookup"><span data-stu-id="cf9e3-173">Resources</span></span>

-   <span data-ttu-id="cf9e3-174">[適用于 Windows 7 的行動電池壽命解決方案](/previous-versions/windows/hardware/design/dn641606(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf9e3-174">[Mobile Battery Life Solutions for Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))</span></span>
-   [<span data-ttu-id="cf9e3-175">系統 \_ 電源 \_ 功能</span><span class="sxs-lookup"><span data-stu-id="cf9e3-175">SYSTEM\_POWER\_CAPABILITIES</span></span>](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [<span data-ttu-id="cf9e3-176">CallNtPowerInformation 函式</span><span class="sxs-lookup"><span data-stu-id="cf9e3-176">CallNtPowerInformation function</span></span>](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [<span data-ttu-id="cf9e3-177">工作物件</span><span class="sxs-lookup"><span data-stu-id="cf9e3-177">Job Objects</span></span>](../procthread/job-objects.md)
-   [<span data-ttu-id="cf9e3-178">RegisterSuspendResumeNotification</span><span class="sxs-lookup"><span data-stu-id="cf9e3-178">RegisterSuspendResumeNotification</span></span>](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [<span data-ttu-id="cf9e3-179">UnregisterSuspendResumeNotification</span><span class="sxs-lookup"><span data-stu-id="cf9e3-179">UnregisterSuspendResumeNotification</span></span>](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [<span data-ttu-id="cf9e3-180">PowerRegisterSuspendResumeNotification</span><span class="sxs-lookup"><span data-stu-id="cf9e3-180">PowerRegisterSuspendResumeNotification</span></span>](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [<span data-ttu-id="cf9e3-181">PowerUnregisterSuspendResumeNotification</span><span class="sxs-lookup"><span data-stu-id="cf9e3-181">PowerUnregisterSuspendResumeNotification</span></span>](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [<span data-ttu-id="cf9e3-182">AppCompat 工具組</span><span class="sxs-lookup"><span data-stu-id="cf9e3-182">AppCompat toolkit</span></span>](../win7appqual/application-compatibility-toolkit--act-.md)

 

 