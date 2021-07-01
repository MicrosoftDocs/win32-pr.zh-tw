---
description: 對使用者而言，系統似乎是開啟或關閉。
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: 系統電源狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efde8a130d6dbe2b44c34e8ab45b973a64f3b255
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120813"
---
# <a name="system-power-states"></a><span data-ttu-id="372ba-103">系統電源狀態</span><span class="sxs-lookup"><span data-stu-id="372ba-103">System Power States</span></span>

<span data-ttu-id="372ba-104">對使用者而言，系統似乎是開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="372ba-104">To the user, the system appears to be either on or off.</span></span> <span data-ttu-id="372ba-105">沒有其他可偵測的狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-105">There are no other detectable states.</span></span> <span data-ttu-id="372ba-106">不過，系統支援多個電源狀態，對應至進階組態與電源介面 (ACPI) 規格中定義的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-106">However, the system supports multiple power states that correspond to the power states defined in the Advanced Configuration and Power Interface (ACPI) specification.</span></span> <span data-ttu-id="372ba-107">這些狀態也有變化，例如混合式睡眠和快速啟動。</span><span class="sxs-lookup"><span data-stu-id="372ba-107">There are also variations of these states, such as hybrid sleep and fast startup.</span></span> <span data-ttu-id="372ba-108">本主題將介紹這些狀態，並說明它們彼此之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="372ba-108">This topic introduces these states and describes how they relate to each other.</span></span>

> [!NOTE]
> <span data-ttu-id="372ba-109">使用系統服務建立驅動程式或應用程式的系統整合者和開發人員，應該特別注意驅動程式品質問題，例如記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="372ba-109">System integrators and developers creating drivers or applications with a system service should be particularly careful of driver quality issues, such as memory leaks.</span></span> <span data-ttu-id="372ba-110">雖然驅動程式品質一直很重要，但核心重新開機之間的時間可能會比舊版作業系統長很多，因為使用者起始睡眠和關機時，核心、驅動程式和服務將會保留並還原，而不會重新開機。</span><span class="sxs-lookup"><span data-stu-id="372ba-110">While driver quality has always been important, the up time between kernel reboots may be significantly longer than on previous versions of the OS because on user initiated sleeps and shutdowns, the kernel, drivers, and services will be preserved and restored, not re-started.</span></span>

 

<span data-ttu-id="372ba-111">下表列出從最高到最低電源耗用量的 ACPI 電源狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-111">The following table lists the ACPI power states from highest to lowest power consumption.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="372ba-112">電源狀態</span><span class="sxs-lookup"><span data-stu-id="372ba-112">Power state</span></span></th>
<th><span data-ttu-id="372ba-113">ACPI 狀態</span><span class="sxs-lookup"><span data-stu-id="372ba-113">ACPI state</span></span></th>
<th><span data-ttu-id="372ba-114">描述</span><span class="sxs-lookup"><span data-stu-id="372ba-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="372ba-115">運作中</span><span class="sxs-lookup"><span data-stu-id="372ba-115">Working</span></span><br/></td>
<td><span data-ttu-id="372ba-116">S0</span><span class="sxs-lookup"><span data-stu-id="372ba-116">S0</span></span><br/></td>
<td><span data-ttu-id="372ba-117">系統完全可用。</span><span class="sxs-lookup"><span data-stu-id="372ba-117">The system is fully usable.</span></span> <span data-ttu-id="372ba-118">未使用的硬體元件可以輸入較低的電源狀態，以節省電源。</span><span class="sxs-lookup"><span data-stu-id="372ba-118">Hardware components that are not in use can save power by entering a lower power state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="372ba-119">睡眠</span><span class="sxs-lookup"><span data-stu-id="372ba-119">Sleep</span></span><br/> <span data-ttu-id="372ba-120"> (新式待命) </span><span class="sxs-lookup"><span data-stu-id="372ba-120">(Modern Standby)</span></span><br/></td>
<td><span data-ttu-id="372ba-121">S0 低電力閒置</span><span class="sxs-lookup"><span data-stu-id="372ba-121">S0 low-power idle</span></span><br/></td>
<td><span data-ttu-id="372ba-122">某些 SoC 系統支援所謂的低電源閒置狀態，稱為 <a href="/windows-hardware/design/device-experiences/modern-standby">新式待命</a>。</span><span class="sxs-lookup"><span data-stu-id="372ba-122">Some SoC systems support a low-power idle state known as <a href="/windows-hardware/design/device-experiences/modern-standby">Modern Standby</a>.</span></span> <span data-ttu-id="372ba-123">在此狀態下，系統可能會非常快速地從低電源狀態切換至高電源狀態，讓它能夠快速回應硬體和網路事件。</span><span class="sxs-lookup"><span data-stu-id="372ba-123">In this state, the system can very quickly switch from a low-power state to high-power state, so that it can respond quickly to hardware and network events.</span></span> <span data-ttu-id="372ba-124">支援新式待命的系統不會使用 S1-S3。</span><span class="sxs-lookup"><span data-stu-id="372ba-124">Systems that support Modern Standby do not use S1-S3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="372ba-125">睡眠</span><span class="sxs-lookup"><span data-stu-id="372ba-125">Sleep</span></span><br/></td>
<td><span data-ttu-id="372ba-126">S1</span><span class="sxs-lookup"><span data-stu-id="372ba-126">S1</span></span><br/> <span data-ttu-id="372ba-127">S2</span><span class="sxs-lookup"><span data-stu-id="372ba-127">S2</span></span><br/> <span data-ttu-id="372ba-128">S3</span><span class="sxs-lookup"><span data-stu-id="372ba-128">S3</span></span><br/></td>
<td><span data-ttu-id="372ba-129">系統似乎已關閉。</span><span class="sxs-lookup"><span data-stu-id="372ba-129">The system appears to be off.</span></span> <span data-ttu-id="372ba-130">這些狀態中耗用的電源 (S1-S3) 小於 S0 且超過 S4;S3 耗用的電源比 S2 低，而 S2 耗用的電力低於 S1。</span><span class="sxs-lookup"><span data-stu-id="372ba-130">Power consumed in these states (S1-S3) is less than S0 and more than S4; S3 consumes less power than S2, and S2 consumes less power than S1.</span></span> <span data-ttu-id="372ba-131">系統通常支援這三種狀態的其中一種，而不是全部三種狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-131">Systems typically support one of these three states, not all three.</span></span><br/> <span data-ttu-id="372ba-132">在這些狀態中 (S1-S3) ，動態記憶體會保持重新整理狀態，以維護系統狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-132">In these states (S1-S3), volatile memory is kept refreshed to maintain the system state.</span></span> <span data-ttu-id="372ba-133">某些元件仍維持電源，因此電腦可以從鍵盤、LAN 或 USB 裝置的輸入喚醒。</span><span class="sxs-lookup"><span data-stu-id="372ba-133">Some components remain powered so the computer can wake from input from the keyboard, LAN, or a USB device.</span></span><br/> <span data-ttu-id="372ba-134">在桌上型電腦上使用的「<em>混合式睡眠</em>」（system）是指系統使用具有 S1-S3 的休眠檔。</span><span class="sxs-lookup"><span data-stu-id="372ba-134"><em>Hybrid sleep</em>, used on desktops, is where a system uses a hibernation file with S1-S3.</span></span> <span data-ttu-id="372ba-135">休眠檔會儲存系統狀態，以防系統在睡眠時失去電源。</span><span class="sxs-lookup"><span data-stu-id="372ba-135">The hibernation file saves the system state in case the system loses power while in sleep.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="372ba-136">支援新式待命的 SoC 系統 (低電源閒置狀態) 不使用 S1-S3。</span><span class="sxs-lookup"><span data-stu-id="372ba-136">SoC systems that support modern standby (the low-power idle state) do not use S1-S3.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="372ba-137">休眠</span><span class="sxs-lookup"><span data-stu-id="372ba-137">Hibernate</span></span><br/></td>
<td><span data-ttu-id="372ba-138">S4</span><span class="sxs-lookup"><span data-stu-id="372ba-138">S4</span></span><br/></td>
<td><span data-ttu-id="372ba-139">系統似乎已關閉。</span><span class="sxs-lookup"><span data-stu-id="372ba-139">The system appears to be off.</span></span> <span data-ttu-id="372ba-140">功率耗用量會縮減為最低層級。</span><span class="sxs-lookup"><span data-stu-id="372ba-140">Power consumption is reduced to the lowest level.</span></span> <span data-ttu-id="372ba-141">系統會將 volatile 記憶體的內容儲存至休眠檔，以保留系統狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-141">The system saves the contents of volatile memory to a hibernation file to preserve system state.</span></span> <span data-ttu-id="372ba-142">某些元件仍維持電源，因此電腦可以從鍵盤、LAN 或 USB 裝置的輸入喚醒。</span><span class="sxs-lookup"><span data-stu-id="372ba-142">Some components remain powered so the computer can wake from input from the keyboard, LAN, or a USB device.</span></span> <span data-ttu-id="372ba-143">如果工作內容儲存在非靜態媒體上，則可以還原。</span><span class="sxs-lookup"><span data-stu-id="372ba-143">The working context can be restored if it is stored on nonvolatile media.</span></span> <br/> <span data-ttu-id="372ba-144"><em>快速啟動</em> 是在休眠檔案建立之前登出使用者的位置。</span><span class="sxs-lookup"><span data-stu-id="372ba-144"><em>Fast startup</em> is where the user is logged off before the hibernation file is created.</span></span> <span data-ttu-id="372ba-145">這樣可以讓較小的休眠檔案更適合儲存功能較少的系統使用。</span><span class="sxs-lookup"><span data-stu-id="372ba-145">This allows for a smaller hibernation file, more appropriate for systems with less storage capabilities.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="372ba-146">軟關閉</span><span class="sxs-lookup"><span data-stu-id="372ba-146">Soft Off</span></span><br/></td>
<td><span data-ttu-id="372ba-147">S5</span><span class="sxs-lookup"><span data-stu-id="372ba-147">S5</span></span><br/></td>
<td><span data-ttu-id="372ba-148">系統似乎已關閉。</span><span class="sxs-lookup"><span data-stu-id="372ba-148">The system appears to be off.</span></span> <span data-ttu-id="372ba-149">此狀態是由完整關機和啟動週期所組成。</span><span class="sxs-lookup"><span data-stu-id="372ba-149">This state is comprised of a full shutdown and boot cycle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="372ba-150">機械關閉</span><span class="sxs-lookup"><span data-stu-id="372ba-150">Mechanical Off</span></span><br/></td>
<td><span data-ttu-id="372ba-151">G3</span><span class="sxs-lookup"><span data-stu-id="372ba-151">G3</span></span><br/></td>
<td><span data-ttu-id="372ba-152">系統已完全關閉，且不會使用任何電源。</span><span class="sxs-lookup"><span data-stu-id="372ba-152">The system is completely off and consumes no power.</span></span> <span data-ttu-id="372ba-153">只有在完整重新開機後，系統才會返回工作狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-153">The system returns to the working state only after a full reboot.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="372ba-154">[**系統 \_ 電源 \_ 狀態**](/windows/desktop/api/WinNT/ne-winnt-system_power_state)列舉會定義用來指定系統電源狀態的值。</span><span class="sxs-lookup"><span data-stu-id="372ba-154">The [**SYSTEM\_POWER\_STATE**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) enumeration defines values that are used to specify system power states.</span></span>

## <a name="working-state-s0"></a><span data-ttu-id="372ba-155">工作狀態 (S0) </span><span class="sxs-lookup"><span data-stu-id="372ba-155">Working state (S0)</span></span>

<span data-ttu-id="372ba-156">在工作狀態期間，系統會處於喚醒並正在執行。</span><span class="sxs-lookup"><span data-stu-id="372ba-156">During the working state, the system is awake and running.</span></span> <span data-ttu-id="372ba-157">簡單來說，裝置是「開啟」。</span><span class="sxs-lookup"><span data-stu-id="372ba-157">In simple terms, the device is "on."</span></span> <span data-ttu-id="372ba-158">無論是開啟或關閉畫面，裝置都處於完整執行狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-158">Whether the screen is on or off, the device is in a full running state.</span></span> <span data-ttu-id="372ba-159">為了節省能源（尤其是在電源供電的裝置上），我們強烈建議您在未使用硬體元件時進行開機。</span><span class="sxs-lookup"><span data-stu-id="372ba-159">To conserve energy, especially on battery powered devices, we highly recommend powering-down hardware components when they're not being used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="372ba-160">無論狀態為何，都不使用電源關閉的硬體元件。</span><span class="sxs-lookup"><span data-stu-id="372ba-160">Power-down hardware components whenever they're not being used - regardless of the state.</span></span> <span data-ttu-id="372ba-161">低功率耗用量是行動裝置取用者的重要考慮。</span><span class="sxs-lookup"><span data-stu-id="372ba-161">Low power consumption is an important consideration for mobile device consumers.</span></span>

 

## <a name="sleep-state-modern-standby"></a><span data-ttu-id="372ba-162">睡眠狀態 (新式待命) </span><span class="sxs-lookup"><span data-stu-id="372ba-162">Sleep state (Modern Standby)</span></span>

<span data-ttu-id="372ba-163">在工作狀態的 S0 低電源閒置模式中（也稱為 [新式待命](/windows-hardware/design/device-experiences/modern-standby)），系統會維持部分執行。</span><span class="sxs-lookup"><span data-stu-id="372ba-163">In the S0 low-power idle mode of the working state, also referred to as [Modern Standby](/windows-hardware/design/device-experiences/modern-standby), the system remains partially running.</span></span> <span data-ttu-id="372ba-164">在新式待命期間，只要有適當的網路可用，系統就會隨時保持最新狀態，而且也會在需要即時動作（例如 OS 維護）時喚醒。</span><span class="sxs-lookup"><span data-stu-id="372ba-164">During Modern Standby, the system can stay up-to-date whenever a suitable network is available and also wake when real-time action is required, such as OS maintenance.</span></span> <span data-ttu-id="372ba-165">新式待命喚醒的速度遠優於 S1-S3。</span><span class="sxs-lookup"><span data-stu-id="372ba-165">Modern Standby wakes significantly faster than S1-S3.</span></span> <span data-ttu-id="372ba-166">如需詳細資訊，請參閱 [新式待命](/windows-hardware/design/device-experiences/modern-standby)。</span><span class="sxs-lookup"><span data-stu-id="372ba-166">For more info, see [Modern Standby](/windows-hardware/design/device-experiences/modern-standby).</span></span>

> [!Note]  
> <span data-ttu-id="372ba-167">新式待命僅適用于一些 SoC 系統。</span><span class="sxs-lookup"><span data-stu-id="372ba-167">Modern Standby is only available on some SoC systems.</span></span> <span data-ttu-id="372ba-168">當系統支援時，系統不支援 S1-S3。</span><span class="sxs-lookup"><span data-stu-id="372ba-168">When it's supported, the system does not support S1-S3.</span></span>

 

## <a name="sleep-state-s1-s3"></a><span data-ttu-id="372ba-169">睡眠狀態 (S1-S3) </span><span class="sxs-lookup"><span data-stu-id="372ba-169">Sleep state (S1-S3)</span></span>

<span data-ttu-id="372ba-170">系統會根據數個準則進入睡眠狀態，包括使用者或應用程式活動，以及使用者在 [**設定**] 應用程式的 [**電源 & 睡眠**] 頁面上設定的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="372ba-170">The system enters sleep based on a number of criteria, including user or application activity and preferences that the user sets on the **Power & sleep** page of the **Settings** app.</span></span> <span data-ttu-id="372ba-171">根據預設，系統會使用所有啟用的喚醒裝置所支援的最低電源睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-171">By default, the system uses the lowest-powered sleep state supported by all enabled wake-up devices.</span></span> <span data-ttu-id="372ba-172">如需系統如何判斷何時進入睡眠狀態的詳細資訊，請參閱 [系統睡眠準則](system-sleep-criteria.md)。</span><span class="sxs-lookup"><span data-stu-id="372ba-172">For more information about how the system determines when to enter sleep, see [System Sleep Criteria](system-sleep-criteria.md).</span></span>

<span data-ttu-id="372ba-173">在系統進入睡眠狀態之前，它會判斷適當的睡眠狀態、通知應用程式和驅動程式的暫止轉換，然後將系統轉換成睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-173">Before the system enters sleep, it determines the appropriate sleep state, notifies applications and drivers of the pending transition, and then transitions the system to the sleep state.</span></span> <span data-ttu-id="372ba-174">在重大轉換的情況下，例如當達到電力不足閾值時，系統不會通知應用程式和驅動程式。</span><span class="sxs-lookup"><span data-stu-id="372ba-174">In the case of a critical transition, such as when the critical battery threshold is reached, the system does not notify applications and drivers.</span></span> <span data-ttu-id="372ba-175">應用程式必須做好準備，並在系統返回工作狀態時採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="372ba-175">Applications need to be prepared for this and take the appropriate action when the system returns to the working state.</span></span>

<span data-ttu-id="372ba-176">在這些狀態中 (S1-S3) ，動態記憶體會保持重新整理狀態，以維護系統狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-176">In these states (S1-S3), volatile memory is kept refreshed to maintain the system state.</span></span> <span data-ttu-id="372ba-177">某些元件仍維持電源，因此電腦可以從鍵盤、LAN 或 USB 裝置的輸入喚醒。</span><span class="sxs-lookup"><span data-stu-id="372ba-177">Some components remain powered so the computer can wake from input from the keyboard, LAN, or a USB device.</span></span>

<span data-ttu-id="372ba-178">系統也會從睡眠狀態喚醒，以回應使用者活動或應用程式所定義的喚醒事件。</span><span class="sxs-lookup"><span data-stu-id="372ba-178">The system also wakes from sleep in response to user activity or a wake-up event defined by an application.</span></span> <span data-ttu-id="372ba-179">如需詳細資訊，請參閱 [系統喚醒事件](system-wake-up-events.md)。</span><span class="sxs-lookup"><span data-stu-id="372ba-179">For more information, see [System Wake-up Events](system-wake-up-events.md).</span></span> <span data-ttu-id="372ba-180">系統喚醒所需的時間量，取決於它所喚醒的睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-180">The amount of time it takes the system to wake depends on the sleep state it is waking from.</span></span> <span data-ttu-id="372ba-181">系統需要更多時間從較低電源的狀態 (S3) ，而不是從較高的電源 (S1) 因為硬體可能必須執行的額外工作 (穩定的電源供應器、重新初始化處理器等等) 。</span><span class="sxs-lookup"><span data-stu-id="372ba-181">The system takes more time to wake from a lower-powered state (S3) than from a higher-powered state (S1) because of the extra work the hardware may have to do (stabilize the power supply, reinitialize the processor, and so forth).</span></span>

> [!Caution]  
> <span data-ttu-id="372ba-182">呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)時，只有在需要系統執行背景工作（例如，將電視內容或串流媒體錄製至其他裝置，而系統似乎處於睡眠狀態）時，才應該使用 **ES \_ 離開模式 \_ 必要** 值。</span><span class="sxs-lookup"><span data-stu-id="372ba-182">When calling [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate), the **ES\_AWAYMODE\_REQUIRED** value should be used only when absolutely necessary by media applications that require the system to perform background tasks such as recording television content or streaming media to other devices while the system appears to be sleeping.</span></span> <span data-ttu-id="372ba-183">不需要進行重要背景處理或在可攜式電腦上執行的應用程式不應啟用離開模式，因為它會進入真正的睡眠狀態，以防止系統節省電源。</span><span class="sxs-lookup"><span data-stu-id="372ba-183">Applications that do not require critical background processing or that run on portable computers should not enable away mode because it prevents the system from conserving power by entering true sleep.</span></span>

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a><span data-ttu-id="372ba-184">混合式睡眠 (S1-S3 + 休眠檔案) </span><span class="sxs-lookup"><span data-stu-id="372ba-184">Hybrid sleep (S1-S3 + hibernation file)</span></span>

<span data-ttu-id="372ba-185">「*混合式睡眠*」是一種特殊狀態，也就是睡眠和休眠狀態的組合，這是當系統使用具有 S1-S3 的休眠檔時。</span><span class="sxs-lookup"><span data-stu-id="372ba-185">*Hybrid sleep* is a special state that's a combination of the sleep and hibernation states, it's when a system uses a hibernation file with S1-S3.</span></span> <span data-ttu-id="372ba-186">只有在某些系統上才可使用。</span><span class="sxs-lookup"><span data-stu-id="372ba-186">It's only available on some systems.</span></span> <span data-ttu-id="372ba-187">啟用時，系統會寫入休眠檔案，但會進入較高的睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-187">When enabled, the system writes a hibernation file but enters a higher-powered sleep state.</span></span> <span data-ttu-id="372ba-188">如果在系統睡眠時遺失電源，系統就會從休眠喚醒，這需要較長的時間，但會還原使用者的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-188">If power is lost while the system is sleeping, the system wakes from hibernation, which takes longer but restores the user's system state.</span></span>

## <a name="hibernate-state-s4"></a><span data-ttu-id="372ba-189">休眠狀態 (S4) </span><span class="sxs-lookup"><span data-stu-id="372ba-189">Hibernate state (S4)</span></span>

<span data-ttu-id="372ba-190">Windows 使用休眠功能來提供快速的啟動體驗。</span><span class="sxs-lookup"><span data-stu-id="372ba-190">Windows uses hibernation to provide a fast startup experience.</span></span> <span data-ttu-id="372ba-191">如果有的話，也可以在行動裝置上使用，藉由在關閉系統之前，提供一種機制來儲存所有使用者的狀態，以延長系統的可用電池壽命。</span><span class="sxs-lookup"><span data-stu-id="372ba-191">When available, it's also used on mobile devices to extend the usable battery life of a system by giving a mechanism to save all of the user s state prior to shutting down the system.</span></span> <span data-ttu-id="372ba-192">在休眠轉換中，記憶體的所有內容都會寫入至主要系統磁片磁碟機上的檔案，也就是 *休眠* 檔。</span><span class="sxs-lookup"><span data-stu-id="372ba-192">In a Hibernate transition, all the contents of memory are written to a file on the primary system drive, the *hibernation file*.</span></span> <span data-ttu-id="372ba-193">這會保留作業系統、應用程式和裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-193">This preserves the state of the operating system, applications, and devices.</span></span> <span data-ttu-id="372ba-194">在合併記憶體使用量耗用所有實體記憶體的情況下，休眠檔必須夠大，以確保會有空間可儲存實體記憶體的所有內容。</span><span class="sxs-lookup"><span data-stu-id="372ba-194">In the case where the combined memory footprint consumes all of physical memory, the hibernation file must be large enough to ensure there will be space to save all the contents of physical memory.</span></span> <span data-ttu-id="372ba-195">由於資料會寫入至非暫時性的儲存空間，因此 DRAM 不需要維護自我重新整理並可關閉電源，這表示休眠的電源耗用量非常低，幾乎與關閉電源一樣。</span><span class="sxs-lookup"><span data-stu-id="372ba-195">Since data is written to non-volatile storage, DRAM does not need to maintain self-refresh and can be powered off, which means power consumption of hibernation is very low, almost the same as power off.</span></span>

<span data-ttu-id="372ba-196">在完整關機和開機 (S5) 中，會在下一次開機時將整個使用者會話關機並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="372ba-196">During a full shutdown and boot (S5), the entire user session is torn down and restarted on the next boot.</span></span> <span data-ttu-id="372ba-197">相反地，在休眠 (S4) 期間，使用者會話會關閉並儲存使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-197">In contrast, during a hibernation (S4), the user session is closed and the user state is saved.</span></span>

### <a name="fast-startup-reduced-hibernation-file"></a><span data-ttu-id="372ba-198">快速啟動 (縮減休眠檔案) </span><span class="sxs-lookup"><span data-stu-id="372ba-198">Fast startup (reduced hibernation file)</span></span>

<span data-ttu-id="372ba-199">*快速啟動* 是一種關機類型，使用休眠檔來加速後續開機。</span><span class="sxs-lookup"><span data-stu-id="372ba-199">*Fast startup* is a type of shutdown that uses a hibernation file to speed up the subsequent boot.</span></span> <span data-ttu-id="372ba-200">在這種關閉類型期間，使用者會先登出，再建立休眠檔。</span><span class="sxs-lookup"><span data-stu-id="372ba-200">During this type of shutdown, the user is logged off before the hibernation file is created.</span></span> <span data-ttu-id="372ba-201">快速啟動可讓您使用較小的休眠檔，更適合儲存功能較少的系統使用。</span><span class="sxs-lookup"><span data-stu-id="372ba-201">Fast startup allows for a smaller hibernation file, more appropriate for systems with less storage capabilities.</span></span> <span data-ttu-id="372ba-202">如需詳細資訊，請參閱 [休眠檔案類型](#hibernation-file-types)。</span><span class="sxs-lookup"><span data-stu-id="372ba-202">For more info, see [Hibernation file types](#hibernation-file-types).</span></span>

<span data-ttu-id="372ba-203">當使用 [快速啟動] 時，系統會向使用者顯示，因為已發生完整關機 (S5) ，即使系統真的已透過 S4 完成也是一樣。</span><span class="sxs-lookup"><span data-stu-id="372ba-203">When using fast startup, the system appears to the user as though a full shutdown (S5) has occurred, even though the system has actually gone through S4.</span></span> <span data-ttu-id="372ba-204">這包括系統如何回應裝置喚醒警報。</span><span class="sxs-lookup"><span data-stu-id="372ba-204">This includes how the system responds to device wake alarms.</span></span>

<span data-ttu-id="372ba-205">使用者會話的快速啟動記錄，但是核心 (會話 0) 的內容會寫入硬碟。</span><span class="sxs-lookup"><span data-stu-id="372ba-205">Fast startup logs off user sessions, but the contents of kernel (session 0) are written to hard disk.</span></span> <span data-ttu-id="372ba-206">這樣可加快開機速度。</span><span class="sxs-lookup"><span data-stu-id="372ba-206">This enables faster boot.</span></span>

<span data-ttu-id="372ba-207">若要以程式設計方式起始快速啟動樣式的關機，請使用 **關閉 \_ 混合** 式旗標或 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex)函式搭配 **EWX \_ 混合式 \_ 關機** 旗標來呼叫 [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna)函式。</span><span class="sxs-lookup"><span data-stu-id="372ba-207">To programmatically initiate a fast startup-style shutdown, call the [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) function with the **SHUTDOWN\_HYBRID** flag or the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function with the **EWX\_HYBRID\_SHUTDOWN** flag.</span></span>

> [!Note]  
> <span data-ttu-id="372ba-208">從 Windows 8 開始，在要求系統關機時，[快速啟動] 是預設的轉換。</span><span class="sxs-lookup"><span data-stu-id="372ba-208">Starting in Windows 8, fast startup is the default transition when a system shutdown is requested.</span></span> <span data-ttu-id="372ba-209">當要求系統重新開機 (或應用程式呼叫關機 API) 時，會發生完整關機 (S5) 。</span><span class="sxs-lookup"><span data-stu-id="372ba-209">A full shutdown (S5) occurs when a system restart is requested (or an application calls a shutdown API).</span></span>

 

### <a name="entering-hibernation"></a><span data-ttu-id="372ba-210">進入休眠</span><span class="sxs-lookup"><span data-stu-id="372ba-210">Entering hibernation</span></span>

<span data-ttu-id="372ba-211">進行休眠要求時，會在系統進入休眠狀態時進行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="372ba-211">When a hibernate request is made, the following steps occur as the system enters hibernation:</span></span>

1.  <span data-ttu-id="372ba-212">應用程式和服務會收到通知</span><span class="sxs-lookup"><span data-stu-id="372ba-212">Apps and services are notified</span></span>
2.  <span data-ttu-id="372ba-213">驅動程式會收到通知</span><span class="sxs-lookup"><span data-stu-id="372ba-213">Drivers are notified</span></span>
3.  <span data-ttu-id="372ba-214">以壓縮格式將使用者和系統狀態儲存到磁片</span><span class="sxs-lookup"><span data-stu-id="372ba-214">User and system state is saved to disk in a compressed format</span></span>
4.  <span data-ttu-id="372ba-215">已通知固件</span><span class="sxs-lookup"><span data-stu-id="372ba-215">Firmware is notified</span></span>

> [!Note]  
> <span data-ttu-id="372ba-216">從 Windows 8 開始，系統上的所有核心都是用來壓縮記憶體中的資料，並將資料寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="372ba-216">Starting in Windows 8, all cores on the system are used to compress the data in memory and write it to disk.</span></span>

 

<span data-ttu-id="372ba-217">若要以程式設計方式起始休眠轉換，請呼叫 [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) 函式。</span><span class="sxs-lookup"><span data-stu-id="372ba-217">To programmatically initiate a hibernate transition, call the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

### <a name="resuming-from-hibernation"></a><span data-ttu-id="372ba-218">從休眠狀態繼續</span><span class="sxs-lookup"><span data-stu-id="372ba-218">Resuming from hibernation</span></span>

<span data-ttu-id="372ba-219">當系統從休眠狀態恢復時。</span><span class="sxs-lookup"><span data-stu-id="372ba-219">When a system resumes from hibernation.</span></span>

<span data-ttu-id="372ba-220">當系統開機時，會在系統從休眠狀態恢復時進行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="372ba-220">When a system is powered on, the following steps occur as the system resumes from hibernation.</span></span>

1.  <span data-ttu-id="372ba-221">系統文章</span><span class="sxs-lookup"><span data-stu-id="372ba-221">System POST</span></span>
2.  <span data-ttu-id="372ba-222">從休眠檔解壓縮和還原系統記憶體</span><span class="sxs-lookup"><span data-stu-id="372ba-222">System memory is decompressed and restored from the hibernation file</span></span>
3.  <span data-ttu-id="372ba-223">裝置初始化</span><span class="sxs-lookup"><span data-stu-id="372ba-223">Device initialization</span></span>
4.  <span data-ttu-id="372ba-224">驅動程式會還原至休眠之前的狀態</span><span class="sxs-lookup"><span data-stu-id="372ba-224">Drivers are restored to the state they were in prior to hibernation</span></span>
5.  <span data-ttu-id="372ba-225">服務會還原至休眠之前的狀態</span><span class="sxs-lookup"><span data-stu-id="372ba-225">Services are restored to the state they were in prior to hibernation</span></span>
6.  <span data-ttu-id="372ba-226">系統變成可供登入</span><span class="sxs-lookup"><span data-stu-id="372ba-226">System becomes available for login</span></span>

<span data-ttu-id="372ba-227">從休眠狀態開始會以類似于 S5 關機的系統 POST 開始。</span><span class="sxs-lookup"><span data-stu-id="372ba-227">A resume from hibernation starts with a system POST that is similar to an S5 shutdown.</span></span> <span data-ttu-id="372ba-228">OS 開機管理程式會偵測到有效的休眠檔，以判斷是否需要從休眠狀態繼續進行。</span><span class="sxs-lookup"><span data-stu-id="372ba-228">The OS boot manager determines that a resume from hibernation is required by detecting a valid hibernation file.</span></span> <span data-ttu-id="372ba-229">然後，它會指示系統繼續執行，並還原記憶體和所有架構暫存器的內容。</span><span class="sxs-lookup"><span data-stu-id="372ba-229">Then it directs the system to resume, restoring the contents of memory and all architectural registers.</span></span> <span data-ttu-id="372ba-230">在從休眠狀態恢復時，系統記憶體的內容會從磁片讀取、解壓縮和還原，讓系統處於休眠狀態時的確切狀態中。</span><span class="sxs-lookup"><span data-stu-id="372ba-230">In the case of a resume from hibernation, the contents of the system memory are read back in from the disk, decompressed, and restored, putting the system in the exact state it was in when it was hibernated.</span></span> <span data-ttu-id="372ba-231">還原記憶體之後，會重新開機裝置，電腦會回到執行狀態，準備好進行登入。</span><span class="sxs-lookup"><span data-stu-id="372ba-231">After memory is restored, the devices are re-started, the machine returns to a running state, ready for login.</span></span>

> [!Note]  
> <span data-ttu-id="372ba-232">從休眠狀態繼續進行時，驅動程式和服務會收到通知，但不會重新開機。</span><span class="sxs-lookup"><span data-stu-id="372ba-232">During a resume from hibernation, drivers and services are notified, but are not restarted.</span></span> <span data-ttu-id="372ba-233">它們只會還原至休眠之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-233">They are only restored to the state they were in prior to hibernation.</span></span>

 

### <a name="hibernation-file-types"></a><span data-ttu-id="372ba-234">休眠檔案類型</span><span class="sxs-lookup"><span data-stu-id="372ba-234">Hibernation file types</span></span>

<span data-ttu-id="372ba-235">休眠檔案用於互動式睡眠、快速啟動和標準休眠 (，如先前的) 所述。</span><span class="sxs-lookup"><span data-stu-id="372ba-235">Hibernation files are used for hybrid sleep, fast startup, and standard hibernation (described earlier).</span></span> <span data-ttu-id="372ba-236">有兩種類型可依大社區分，也就是完整和縮減大小的休眠檔。</span><span class="sxs-lookup"><span data-stu-id="372ba-236">There are two types, differentiated by size, a full and reduced size hibernation file.</span></span> <span data-ttu-id="372ba-237">只有快速啟動才能使用較少的休眠檔。</span><span class="sxs-lookup"><span data-stu-id="372ba-237">Only fast startup can use a reduced hibernation file.</span></span>



| <span data-ttu-id="372ba-238">休眠檔案類型</span><span class="sxs-lookup"><span data-stu-id="372ba-238">Hibernation file type</span></span> | <span data-ttu-id="372ba-239">預設大小</span><span class="sxs-lookup"><span data-stu-id="372ba-239">Default size</span></span>           | <span data-ttu-id="372ba-240">支援。。。</span><span class="sxs-lookup"><span data-stu-id="372ba-240">Supports...</span></span>                           |
|-----------------------|------------------------|---------------------------------------|
| <span data-ttu-id="372ba-241">完整</span><span class="sxs-lookup"><span data-stu-id="372ba-241">Full</span></span>                  | <span data-ttu-id="372ba-242">40% 的實體記憶體</span><span class="sxs-lookup"><span data-stu-id="372ba-242">40% of physical memory</span></span> | <span data-ttu-id="372ba-243">休眠、混合式睡眠、快速啟動</span><span class="sxs-lookup"><span data-stu-id="372ba-243">hibernate, hybrid sleep, fast startup</span></span> |
| <span data-ttu-id="372ba-244">減少</span><span class="sxs-lookup"><span data-stu-id="372ba-244">Reduced</span></span>               | <span data-ttu-id="372ba-245">20% 的實體記憶體</span><span class="sxs-lookup"><span data-stu-id="372ba-245">20% of physical memory</span></span> | <span data-ttu-id="372ba-246">快速啟動</span><span class="sxs-lookup"><span data-stu-id="372ba-246">fast startup</span></span>                          |



 

<span data-ttu-id="372ba-247">若要確認或變更所用休眠檔案的類型，請執行 **powercfg.exe** 公用程式。</span><span class="sxs-lookup"><span data-stu-id="372ba-247">To verify or change the type of hibernation file used, run the **powercfg.exe** utility.</span></span> <span data-ttu-id="372ba-248">下列範例示範如何。</span><span class="sxs-lookup"><span data-stu-id="372ba-248">The following examples demonstrate how.</span></span> <span data-ttu-id="372ba-249">如需詳細資訊，請執行 `powercfg /? hibernate`。</span><span class="sxs-lookup"><span data-stu-id="372ba-249">For more information, run `powercfg /? hibernate`.</span></span>



| <span data-ttu-id="372ba-250">範例</span><span class="sxs-lookup"><span data-stu-id="372ba-250">Example</span></span>                                                                        | <span data-ttu-id="372ba-251">描述</span><span class="sxs-lookup"><span data-stu-id="372ba-251">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powercfg /a`<br/>                                                | <span data-ttu-id="372ba-252">**確認休眠檔案類型。**</span><span class="sxs-lookup"><span data-stu-id="372ba-252">**Verify the hibernation file type.**</span></span> <span data-ttu-id="372ba-253">使用完整休眠檔案時，會產生休眠狀態，表示休眠是可用的選項。</span><span class="sxs-lookup"><span data-stu-id="372ba-253">When a full hibernation file is used, the results state that hibernation is an available option.</span></span> <span data-ttu-id="372ba-254">使用較少的休眠檔案時，結果會顯示為不支援休眠。</span><span class="sxs-lookup"><span data-stu-id="372ba-254">When a reduced hibernation file is used, the results will say hibernation is not supported.</span></span> <span data-ttu-id="372ba-255">如果系統完全沒有休眠檔，則結果會指出尚未啟用休眠。</span><span class="sxs-lookup"><span data-stu-id="372ba-255">If the system has no hibernation file at all, the results will say hibernation has not been enabled.</span></span><br/> |
| `powercfg /h /type full`<br/>                                     | <span data-ttu-id="372ba-256">**將休眠檔案類型變更為 [完整]。**</span><span class="sxs-lookup"><span data-stu-id="372ba-256">**Change the hibernation file type to full.**</span></span> <span data-ttu-id="372ba-257">不建議在儲存體低於32GB 的系統上使用此選項。</span><span class="sxs-lookup"><span data-stu-id="372ba-257">This is not recommended on systems with less than 32GB of storage.</span></span><br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | <span data-ttu-id="372ba-258">**將休眠檔案類型變更為 [已縮減]。**</span><span class="sxs-lookup"><span data-stu-id="372ba-258">**Change the hibernation file type to reduced.**</span></span> <span data-ttu-id="372ba-259">如果命令傳回「參數不正確」，請參閱下列範例。</span><span class="sxs-lookup"><span data-stu-id="372ba-259">If the command returns "the parameter is incorrect", see the following example.</span></span><br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | <span data-ttu-id="372ba-260">**請重試將休眠檔案類型變更為「減少」。**</span><span class="sxs-lookup"><span data-stu-id="372ba-260">**Retry changing the hibernation file type to reduced.**</span></span> <span data-ttu-id="372ba-261">如果休眠檔設為大於40% 的自訂大小，您必須先將檔案大小設定為零。</span><span class="sxs-lookup"><span data-stu-id="372ba-261">If the hibernation file is set to a custom size greater than 40%, you must first set the size of the file to zero.</span></span> <span data-ttu-id="372ba-262">然後重試縮減的設定。</span><span class="sxs-lookup"><span data-stu-id="372ba-262">Then retry the reduced configuration.</span></span><br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a><span data-ttu-id="372ba-263"> (S5) 的軟關閉狀態</span><span class="sxs-lookup"><span data-stu-id="372ba-263">Soft Off state (S5)</span></span>

<span data-ttu-id="372ba-264">當系統完全關閉而沒有休眠檔案時，就會進入「軟關閉」狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-264">The soft off state is when the system fully shuts down without a hibernation file.</span></span> <span data-ttu-id="372ba-265">軟關閉也稱為「完整關機」。</span><span class="sxs-lookup"><span data-stu-id="372ba-265">Soft off is also known as a "full shutdown."</span></span> <span data-ttu-id="372ba-266">在完整關機和開機期間，會在下一次開機時將整個使用者會話關機並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="372ba-266">During a full shutdown and boot, the entire user session is torn down and restarted on the next boot.</span></span> <span data-ttu-id="372ba-267">因此，從這個狀態開機/啟動的時間會比 S1-S4 長很多。</span><span class="sxs-lookup"><span data-stu-id="372ba-267">Consequently, a boot/startup from this state takes significantly longer than S1-S4.</span></span> <span data-ttu-id="372ba-268">當要求系統重新開機 (或應用程式呼叫關機 API) 時，會發生完整關機 (S5) 。</span><span class="sxs-lookup"><span data-stu-id="372ba-268">A full shutdown (S5) occurs when a system restart is requested (or an application calls a shutdown API).</span></span>

## <a name="mechanical-off-state-g3"></a><span data-ttu-id="372ba-269">機械關閉狀態 (G3) </span><span class="sxs-lookup"><span data-stu-id="372ba-269">Mechanical Off state (G3)</span></span>

<span data-ttu-id="372ba-270">在此狀態下，系統會完全關閉，且不會使用任何電源。</span><span class="sxs-lookup"><span data-stu-id="372ba-270">In this state, the system is completely off and consumes no power.</span></span> <span data-ttu-id="372ba-271">只有在完整重新開機後，系統才會返回工作狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-271">The system returns to the working state only after a full reboot.</span></span>

## <a name="wake-on-lan-behavior"></a><span data-ttu-id="372ba-272">網路喚醒行為</span><span class="sxs-lookup"><span data-stu-id="372ba-272">Wake-on-LAN behavior</span></span>

<span data-ttu-id="372ba-273">網路介面卡偵測到 WOL 事件 (通常是特殊的乙太網路封包) 時，網路喚醒 (WOL) 功能將電腦從低電源狀態喚醒。</span><span class="sxs-lookup"><span data-stu-id="372ba-273">The wake-on-LAN (WOL) feature wakes the computer from a low power state when a network adapter detects a WOL event (typically, a specially constructed Ethernet packet).</span></span>

<span data-ttu-id="372ba-274">從睡眠 (S3) 或休眠 (S4) 支援 WOL。</span><span class="sxs-lookup"><span data-stu-id="372ba-274">WOL is supported from sleep (S3) or hibernate (S4).</span></span> <span data-ttu-id="372ba-275">不支援從快速啟動或軟關閉 (S5) 關機狀態。</span><span class="sxs-lookup"><span data-stu-id="372ba-275">It is not supported from fast startup or soft off (S5) shutdown states.</span></span> <span data-ttu-id="372ba-276">Nic 無法在這些狀態中喚醒，因為使用者不會預期系統會自行喚醒。</span><span class="sxs-lookup"><span data-stu-id="372ba-276">NICs are not armed for wake in these states because users do not expect their systems to wake up on their own.</span></span>

> [!Note]  
> <span data-ttu-id="372ba-277">未正式支援的 WOL (S5) 。</span><span class="sxs-lookup"><span data-stu-id="372ba-277">WOL is not officially supported from soft off (S5).</span></span> <span data-ttu-id="372ba-278">不過，在某些系統上的 BIOS 可能會支援提供 Nic 進行喚醒，即使是 Windows 不包含在程式中也一樣。</span><span class="sxs-lookup"><span data-stu-id="372ba-278">However, the BIOS on some systems may support arming NICs for wake, even though Windows is not involved in the process.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="372ba-279">相關主題</span><span class="sxs-lookup"><span data-stu-id="372ba-279">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="372ba-280">關於電源管理</span><span class="sxs-lookup"><span data-stu-id="372ba-280">About Power Management</span></span>](about-power-management.md)
</dt> </dl>
