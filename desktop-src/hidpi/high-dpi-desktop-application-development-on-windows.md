---
title: Windows 上的高 DPI 桌面應用程式開發
description: 此內容的目標物件是想要更新桌面應用程式以處理動態顯示器縮放比例 (的開發人員也稱為
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104093444"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a><span data-ttu-id="92e49-103">Windows 上的高 DPI 桌面應用程式開發</span><span class="sxs-lookup"><span data-stu-id="92e49-103">High DPI Desktop Application Development on Windows</span></span>

<span data-ttu-id="92e49-104">此內容的目標物件是想要更新傳統型應用程式的開發人員，以處理顯示比例因素 (每英寸的點或 DPI) 變更，讓其應用程式在轉譯的任何顯示器上都有清晰的外觀。</span><span class="sxs-lookup"><span data-stu-id="92e49-104">This content is targeted at developers who are looking to update desktop applications to handle display scale factor (dots per inch, or DPI) changes dynamically, allowing their applications to be crisp on any display they're rendered on.</span></span>

<span data-ttu-id="92e49-105">首先，如果您要從頭開始建立新的 Windows 應用程式，強烈建議您建立 [通用 Windows 平臺 (UWP) ](/windows/uwp/get-started/whats-a-uwp) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="92e49-105">To start, if you're creating a new Windows app from scratch, it is highly recommended that you create a [Universal Windows Platform (UWP)](/windows/uwp/get-started/whats-a-uwp) application.</span></span> <span data-ttu-id="92e49-106">UWP 應用程式會自動 &mdash; 動態 &mdash; 調整其執行所在的每個顯示器。</span><span class="sxs-lookup"><span data-stu-id="92e49-106">UWP applications automatically&mdash;and dynamically&mdash;scale for each display that they're running on.</span></span>

<span data-ttu-id="92e49-107">使用舊版 Windows 程式設計技術的桌面應用程式 (原始 Win32 程式設計、Windows Forms、Windows Presentation Framework (WPF) 等），) 無法自動處理不需要其他開發人員工作的 DPI 縮放比例。</span><span class="sxs-lookup"><span data-stu-id="92e49-107">Desktop applications using older Windows programming technologies (raw Win32 programming, Windows Forms, Windows Presentation Framework (WPF), etc.) are unable to automatically handle DPI scaling without additional developer work.</span></span> <span data-ttu-id="92e49-108">如果沒有這樣的工作，應用程式會在許多常見的使用案例中呈現模糊或大小不正確。</span><span class="sxs-lookup"><span data-stu-id="92e49-108">Without such work, applications will appear blurry or incorrectly-sized in many common usage scenarios.</span></span> <span data-ttu-id="92e49-109">本檔提供有關更新桌面應用程式以正確轉譯的相關內容和資訊。</span><span class="sxs-lookup"><span data-stu-id="92e49-109">This document provides context and information about what is involved in updating a desktop application to render correctly.</span></span>

## <a name="display-scale-factor--dpi"></a><span data-ttu-id="92e49-110">顯示縮放比例 & DPI</span><span class="sxs-lookup"><span data-stu-id="92e49-110">Display Scale Factor & DPI</span></span>

<span data-ttu-id="92e49-111">隨著顯示器技術的進展，顯示器面板製造商已將遞增的圖元數封裝到其面板上的每個實體空間單位中。</span><span class="sxs-lookup"><span data-stu-id="92e49-111">As display technology has progressed, display panel manufacturers have packed an increasing number of pixels into each unit of physical space on their panels.</span></span> <span data-ttu-id="92e49-112">這會導致新式顯示器面板的每英寸 (DPI) 比以往更高。</span><span class="sxs-lookup"><span data-stu-id="92e49-112">This has resulted in the dots per inch (DPI) of modern display panels being much higher than they have historically been.</span></span> <span data-ttu-id="92e49-113">在過去，大部分顯示器的實體空間每個線性英寸都有96圖元 (96 DPI) ;在2017中，可以立即取得幾乎 300 DPI 或更高版本的顯示器。</span><span class="sxs-lookup"><span data-stu-id="92e49-113">In the past, most displays had 96 pixels per linear inch of physical space (96 DPI); in 2017, displays with nearly 300 DPI or higher are readily available.</span></span>

<span data-ttu-id="92e49-114">大部分舊版桌面 UI 架構都有內建的假設，在進程存留期間，顯示 DPI 不會變更。</span><span class="sxs-lookup"><span data-stu-id="92e49-114">Most legacy desktop UI frameworks have built-in assumptions that the display DPI will not change during the lifetime of the process.</span></span>  <span data-ttu-id="92e49-115">此假設不再成立，因為在應用程式進程的存留期內，顯示 Dpi 經常變更數次。</span><span class="sxs-lookup"><span data-stu-id="92e49-115">This assumption no longer holds true, with display DPIs commonly changing several times throughout an application process's lifetime.</span></span> <span data-ttu-id="92e49-116">顯示比例因數/DPI 變更的一些常見案例如下：</span><span class="sxs-lookup"><span data-stu-id="92e49-116">Some common scenarios where the display scale factor/DPI changes are:</span></span>

-   <span data-ttu-id="92e49-117">多重監視器的安裝，其中每個顯示器都有不同的縮放比例，而應用程式會從一個顯示器移至另一個 (例如4K 和1080p 顯示器) </span><span class="sxs-lookup"><span data-stu-id="92e49-117">Multiple-monitor setups where each display has a different scale factor and the application is moved from one display to another (such as a 4K and a 1080p display)</span></span>
-   <span data-ttu-id="92e49-118">使用低 DPI 的外部顯示器來停駐和移除高 DPI 的膝上型電腦 (或反之亦然) </span><span class="sxs-lookup"><span data-stu-id="92e49-118">Docking and undocking a high DPI laptop with a low-DPI external display (or vice versa)</span></span>
-   <span data-ttu-id="92e49-119">從高 DPI 膝上型電腦/平板電腦透過遠端桌面連線至低 DPI 裝置 (或反之亦然) </span><span class="sxs-lookup"><span data-stu-id="92e49-119">Connecting via Remote Desktop from a high DPI laptop/tablet to a low-DPI device (or vice versa)</span></span>
-   <span data-ttu-id="92e49-120">在應用程式執行時變更顯示比例因數設定</span><span class="sxs-lookup"><span data-stu-id="92e49-120">Making a display-scale-factor settings change while applications are running</span></span>

<span data-ttu-id="92e49-121">在這些情況下，UWP 應用程式會自動為新的 DPI 重繪其本身。</span><span class="sxs-lookup"><span data-stu-id="92e49-121">In these scenarios, UWP applications redraw themselves for the new DPI automatically.</span></span> <span data-ttu-id="92e49-122">在預設情況下，如果沒有其他開發人員工作，桌面應用程式就不會執行。</span><span class="sxs-lookup"><span data-stu-id="92e49-122">By default, and without additional developer work, desktop applications do not.</span></span> <span data-ttu-id="92e49-123">未執行此額外工作來回應 DPI 變更的桌面應用程式，可能會對使用者顯示模糊或大小不正確。</span><span class="sxs-lookup"><span data-stu-id="92e49-123">Desktop applications that don't do this extra work to respond to DPI changes may appear blurry or incorrectly-sized to the user.</span></span>

## <a name="dpi-awareness-mode"></a><span data-ttu-id="92e49-124">DPI 感知模式</span><span class="sxs-lookup"><span data-stu-id="92e49-124">DPI Awareness Mode</span></span>

<span data-ttu-id="92e49-125">如果桌面應用程式支援 DPI 調整，則必須告訴 Windows。</span><span class="sxs-lookup"><span data-stu-id="92e49-125">Desktop applications must tell Windows if they support DPI scaling.</span></span> <span data-ttu-id="92e49-126">根據預設，系統會將桌面應用程式的 DPI 感知和點陣圖延伸到其視窗。</span><span class="sxs-lookup"><span data-stu-id="92e49-126">By default, the system considers desktop applications DPI unaware and bitmap-stretches their windows.</span></span> <span data-ttu-id="92e49-127">藉由設定下列其中一種可用的 DPI 感知模式，應用程式可以明確地告訴 Windows 他們要如何處理 DPI 調整：</span><span class="sxs-lookup"><span data-stu-id="92e49-127">By setting one of the following available DPI awareness modes, applications can explicitly tell Windows how they wish to handle DPI scaling:</span></span>

### <a name="dpi-unaware"></a><span data-ttu-id="92e49-128">不知道 DPI</span><span class="sxs-lookup"><span data-stu-id="92e49-128">DPI Unaware</span></span>

<span data-ttu-id="92e49-129">DPI 感知應用程式會以固定的 DPI 值 96 (100% ) 轉譯。</span><span class="sxs-lookup"><span data-stu-id="92e49-129">DPI unaware applications render at a fixed DPI value of 96 (100%).</span></span> <span data-ttu-id="92e49-130">當這些應用程式在顯示比例大於 96 DPI 的螢幕上執行時，Windows 會將應用程式點陣圖延展到預期的實體大小。</span><span class="sxs-lookup"><span data-stu-id="92e49-130">Whenever these applications are run on a screen with a display scale greater than 96 DPI, Windows will stretch the application bitmap to the expected physical size.</span></span> <span data-ttu-id="92e49-131">這會導致應用程式出現模糊。</span><span class="sxs-lookup"><span data-stu-id="92e49-131">This results in the application appearing blurry.</span></span>

### <a name="system-dpi-awareness"></a><span data-ttu-id="92e49-132">系統 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="92e49-132">System DPI Awareness</span></span>

<span data-ttu-id="92e49-133">以系統 DPI 感知的桌面應用程式，通常會在使用者登入的時間內，收到主要連線監視器的 DPI。</span><span class="sxs-lookup"><span data-stu-id="92e49-133">Desktop applications that are system DPI aware typically receive the DPI of the primary connected monitor as of the time of user sign-in.</span></span> <span data-ttu-id="92e49-134">在初始化期間，它們會適當地配置 UI， (調整大小控制項、選擇字型大小、載入資產等 ) 使用該系統的 DPI 值。</span><span class="sxs-lookup"><span data-stu-id="92e49-134">During initialization, they lay out their UI appropriately (sizing controls, choosing font sizes, loading assets, etc.) using that System DPI value.</span></span> <span data-ttu-id="92e49-135">如此一來，系統 DPI 感知的應用程式不會縮放 (點陣圖，) 由 Windows 在以該單一 DPI 呈現的顯示器呈現。</span><span class="sxs-lookup"><span data-stu-id="92e49-135">As such, System DPI-aware applications are not DPI scaled (bitmap stretched) by Windows on displays rendering at that single DPI.</span></span> <span data-ttu-id="92e49-136">當應用程式移至具有不同縮放比例的顯示器時，或如果顯示比例因數變更時，Windows 會以點陣圖調整應用程式的視窗，使其顯示為模糊。</span><span class="sxs-lookup"><span data-stu-id="92e49-136">When the application is moved to a display with a different scale factor, or if the display scale factor otherwise changes, Windows will bitmap scale the application's windows, making them appear blurry.</span></span> <span data-ttu-id="92e49-137">實際上，系統 DPI 感知的桌面應用程式只會在單一顯示器縮放比例轉譯 crisply，每次 DPI 變更時變得模糊。</span><span class="sxs-lookup"><span data-stu-id="92e49-137">Effectively, System DPI-aware desktop applications only render crisply at a single display scale factor, becoming blurry whenever the DPI changes.</span></span>

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a><span data-ttu-id="92e49-138">Per-Monitor 和 Per-Monitor (V2) DPI 感知</span><span class="sxs-lookup"><span data-stu-id="92e49-138">Per-Monitor and Per-Monitor (V2) DPI Awareness</span></span>

<span data-ttu-id="92e49-139">建議您更新傳統型應用程式，以使用個別監視器 DPI 感知模式，讓它們可以在每次 DPI 變更時立即正確轉譯。</span><span class="sxs-lookup"><span data-stu-id="92e49-139">It is recommended that desktop applications be updated to use per-monitor DPI awareness mode, allowing them to immediately render correctly whenever the DPI changes.</span></span> <span data-ttu-id="92e49-140">當應用程式向 Windows 報告它想要在此模式中執行時，Windows 不會在 DPI 變更時以點陣圖延展應用程式，而是將 [WM \_ DPICHANGED](wm-dpichanged.md) 傳送至應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="92e49-140">When an application reports to Windows that it wants to run in this mode, Windows will not bitmap stretch the application when the DPI changes, instead sending [WM\_DPICHANGED](wm-dpichanged.md) to the application window.</span></span> <span data-ttu-id="92e49-141">然後，應用程式必須負責處理新 DPI 的大小調整。</span><span class="sxs-lookup"><span data-stu-id="92e49-141">It is then the complete responsibility of the application to handle resizing itself for the new DPI.</span></span> <span data-ttu-id="92e49-142">大部分的桌面應用程式使用的 UI 架構 (Windows 通用控制項 (comctl32.dll) 、Windows Forms、Windows Presentation Framework 等等。 ) 不支援自動 DPI 縮放，因此開發人員需要調整其視窗內容的大小並重新調整其大小。</span><span class="sxs-lookup"><span data-stu-id="92e49-142">Most UI frameworks used by desktop applications (Windows common controls (comctl32), Windows Forms, Windows Presentation Framework, etc.) do not support automatic DPI scaling, requiring developers to resize and reposition the contents of their windows themselves.</span></span>

<span data-ttu-id="92e49-143">有兩個版本的 Per-Monitor 認知，應用程式可以將自己註冊為：第1版和第2版 (PMv2) 。</span><span class="sxs-lookup"><span data-stu-id="92e49-143">There are two versions of Per-Monitor awareness that an application can register itself as: version 1 and version 2 (PMv2).</span></span> <span data-ttu-id="92e49-144">註冊在 PMv2 感知模式中執行的進程會導致：</span><span class="sxs-lookup"><span data-stu-id="92e49-144">Registering a process as running in PMv2 awareness mode results in:</span></span>

1.  <span data-ttu-id="92e49-145">當 DPI 變更 (最上層和子系 Hwnd 時，所要通知的應用程式) </span><span class="sxs-lookup"><span data-stu-id="92e49-145">The application being notified when the DPI changes (both the top-level and child HWNDs)</span></span>
2.  <span data-ttu-id="92e49-146">應用程式查看每個顯示的原始圖元</span><span class="sxs-lookup"><span data-stu-id="92e49-146">The application seeing the raw pixels of each display</span></span>
3.  <span data-ttu-id="92e49-147">應用程式永遠不會由 Windows 縮放點陣圖</span><span class="sxs-lookup"><span data-stu-id="92e49-147">The application never being bitmap scaled by Windows</span></span>
4.  <span data-ttu-id="92e49-148">自動的非工作區 (視窗標題、捲軸等 ) DPI 縮放比例（依 Windows）</span><span class="sxs-lookup"><span data-stu-id="92e49-148">Automatic non-client area (window caption, scroll bars, etc.) DPI scaling by Windows</span></span>
5.  <span data-ttu-id="92e49-149">從 [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) 的 Win32 對話方塊 (，由 Windows 自動調整 DPI</span><span class="sxs-lookup"><span data-stu-id="92e49-149">Win32 dialogs (from [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatically DPI scaled by Windows</span></span>
6.  <span data-ttu-id="92e49-150">主題-在通用控制項中繪製點陣圖資產 (核取方塊、按鈕背景等 ) 會自動以適當的 DPI 縮放比例呈現</span><span class="sxs-lookup"><span data-stu-id="92e49-150">Theme-drawn bitmap assets in common controls (checkboxes, button backgrounds, etc.) being automatically rendered at the appropriate DPI scale factor</span></span>

<span data-ttu-id="92e49-151">在 Per-Monitor v2 感知模式中執行時，會在應用程式的 DPI 變更時通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="92e49-151">When running in Per-Monitor v2 Awareness mode, applications are notified when their DPI has changed.</span></span> <span data-ttu-id="92e49-152">如果應用程式不會為新的 DPI 調整本身的大小，則應用程式 UI 會出現太小或太大的 (，視先前和新的 DPI 值) 的差異而定。</span><span class="sxs-lookup"><span data-stu-id="92e49-152">If an application does not resize itself for the new DPI, the application UI will appear too small or too large (depending on the difference in the previous and new DPI values).</span></span>

> [!Note]  
> <span data-ttu-id="92e49-153">Per-Monitor V1 (PMv1) 感知的功能非常有限。</span><span class="sxs-lookup"><span data-stu-id="92e49-153">Per-Monitor V1 (PMv1) awareness is very limited.</span></span> <span data-ttu-id="92e49-154">建議應用程式使用 PMv2。</span><span class="sxs-lookup"><span data-stu-id="92e49-154">It is recommended that applications use PMv2.</span></span>

<span data-ttu-id="92e49-155">下表顯示應用程式如何在不同的情況下呈現：</span><span class="sxs-lookup"><span data-stu-id="92e49-155">The following table shows how applications will render under different scenarios:</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="92e49-156">DPI 感知模式</span><span class="sxs-lookup"><span data-stu-id="92e49-156">DPI Awareness Mode</span></span></th>
<th><span data-ttu-id="92e49-157">引進的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="92e49-157">Windows Version Introduced</span></span></th>
<th><span data-ttu-id="92e49-158">應用程式的 DPI 視圖</span><span class="sxs-lookup"><span data-stu-id="92e49-158">Application's view of DPI</span></span></th>
<th><span data-ttu-id="92e49-159">DPI 變更的行為</span><span class="sxs-lookup"><span data-stu-id="92e49-159">Behavior on DPI change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="92e49-160">知道</span><span class="sxs-lookup"><span data-stu-id="92e49-160">Unaware</span></span></td>
<td><span data-ttu-id="92e49-161">N/A</span><span class="sxs-lookup"><span data-stu-id="92e49-161">N/A</span></span></td>
<td><span data-ttu-id="92e49-162">所有顯示器都是 96 DPI</span><span class="sxs-lookup"><span data-stu-id="92e49-162">All displays are 96 DPI</span></span></td>
<td><span data-ttu-id="92e49-163">點陣圖延展 (模糊) </span><span class="sxs-lookup"><span data-stu-id="92e49-163">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92e49-164">系統</span><span class="sxs-lookup"><span data-stu-id="92e49-164">System</span></span></td>
<td><span data-ttu-id="92e49-165">Vista</span><span class="sxs-lookup"><span data-stu-id="92e49-165">Vista</span></span></td>
<td><span data-ttu-id="92e49-166">所有顯示器都有相同的 DPI (在目前的使用者會話開始時主顯示器的 DPI) </span><span class="sxs-lookup"><span data-stu-id="92e49-166">All displays have the same DPI (the DPI of the primary display at the time the current user session was started)</span></span></td>
<td><span data-ttu-id="92e49-167">點陣圖延展 (模糊) </span><span class="sxs-lookup"><span data-stu-id="92e49-167">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92e49-168">Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="92e49-168">Per-Monitor</span></span></td>
<td><span data-ttu-id="92e49-169">8.1</span><span class="sxs-lookup"><span data-stu-id="92e49-169">8.1</span></span></td>
<td><span data-ttu-id="92e49-170">應用程式視窗主要所在的顯示器 DPI</span><span class="sxs-lookup"><span data-stu-id="92e49-170">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="92e49-171">最上層 HWND 會收到 DPI 變更的通知</span><span class="sxs-lookup"><span data-stu-id="92e49-171">Top-level HWND is notified of DPI change</span></span></li>
<li><span data-ttu-id="92e49-172">沒有任何 UI 元素的 DPI 縮放比例。</span><span class="sxs-lookup"><span data-stu-id="92e49-172">No DPI scaling of any UI elements.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92e49-173">Per-Monitor V2</span><span class="sxs-lookup"><span data-stu-id="92e49-173">Per-Monitor V2</span></span></td>
<td><span data-ttu-id="92e49-174">Windows 10 Creators Update (1703) </span><span class="sxs-lookup"><span data-stu-id="92e49-174">Windows 10 Creators Update (1703)</span></span></td>
<td><span data-ttu-id="92e49-175">應用程式視窗主要所在的顯示器 DPI</span><span class="sxs-lookup"><span data-stu-id="92e49-175">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="92e49-176">最上層 <span class="underline">和</span> 子系 hwnd 會收到 DPI 變更的通知</span><span class="sxs-lookup"><span data-stu-id="92e49-176">Top-level <span class="underline">and</span> child HWNDs are notified of DPI change</span></span></li>
</ul>
<br/> <span data-ttu-id="92e49-177"><span class="underline">自動調整 DPI 規模：</span>
</span><span class="sxs-lookup"><span data-stu-id="92e49-177"><span class="underline">Automatic DPI scaling of:</span>
</span></span><ul>
<li><span data-ttu-id="92e49-178">非工作區</span><span class="sxs-lookup"><span data-stu-id="92e49-178">Non-client area</span></span></li>
<li><span data-ttu-id="92e49-179">主題- (comctl32.dll V6) 的通用控制項中繪製的點陣圖</span><span class="sxs-lookup"><span data-stu-id="92e49-179">Theme-drawn bitmaps in common controls (comctl32 V6)</span></span></li>
<li><span data-ttu-id="92e49-180">對話方塊 (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>) </span><span class="sxs-lookup"><span data-stu-id="92e49-180">Dialogs (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a><span data-ttu-id="92e49-181">每台監視器 (V1) DPI 感知</span><span class="sxs-lookup"><span data-stu-id="92e49-181">Per Monitor (V1) DPI Awareness</span></span>

<span data-ttu-id="92e49-182">Per-Monitor V1 DPI 感知模式 (PMv1) 是 Windows 8.1 引進的。</span><span class="sxs-lookup"><span data-stu-id="92e49-182">Per-Monitor V1 DPI awareness mode (PMv1) was introduced with Windows 8.1.</span></span> <span data-ttu-id="92e49-183">此 DPI 感知模式相當有限，僅提供下列功能。</span><span class="sxs-lookup"><span data-stu-id="92e49-183">This DPI awareness mode is very limited and only offers the functionality listed below.</span></span> <span data-ttu-id="92e49-184">建議桌面應用程式使用 Windows 10 1703 或更新版本上支援的 Per-Monitor v2 感知模式。</span><span class="sxs-lookup"><span data-stu-id="92e49-184">It is recommended that desktop applications use Per-Monitor v2 awareness mode, supported on Windows 10 1703 or above.</span></span>

<span data-ttu-id="92e49-185">針對個別監視器感知的初始支援僅提供下列應用程式：</span><span class="sxs-lookup"><span data-stu-id="92e49-185">The initial support for per-monitor awareness only offered applications the following:</span></span>

1.  <span data-ttu-id="92e49-186">最上層的 Hwnd 會收到 DPI 變更的通知，並提供新的建議大小</span><span class="sxs-lookup"><span data-stu-id="92e49-186">Top-level HWNDs are notified of a DPI change and provided a new suggested size</span></span>
2.  <span data-ttu-id="92e49-187">Windows 不會將應用程式 UI 延伸為點陣圖</span><span class="sxs-lookup"><span data-stu-id="92e49-187">Windows will not bitmap stretch the application UI</span></span>
3.  <span data-ttu-id="92e49-188">應用程式會看到所有顯示的實體圖元 (請參閱虛擬化) </span><span class="sxs-lookup"><span data-stu-id="92e49-188">The application sees all displays in physical pixels (see virtualization)</span></span>

<span data-ttu-id="92e49-189">在 Windows 10 1607 或更新版本中，PMv1 應用程式也可能會在 WM NCCREATE 期間呼叫 [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) ， \_ 要求 Windows 正確地調整視窗的非工作區。</span><span class="sxs-lookup"><span data-stu-id="92e49-189">On Windows 10 1607 or above, PMv1 applications may also call [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) during WM\_NCCREATE to request that Windows correctly scale the window's non-client area.</span></span>

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a><span data-ttu-id="92e49-190">UI 架構/技術的每個監視器 DPI 調整支援</span><span class="sxs-lookup"><span data-stu-id="92e49-190">Per Monitor DPI Scaling Support by UI Framework / Technology</span></span>

<span data-ttu-id="92e49-191">下表顯示從 Windows 10 1703 的各種 Windows UI 架構所提供的每個監視器 DPI 感知支援層級：</span><span class="sxs-lookup"><span data-stu-id="92e49-191">The table below shows the level of per-monitor DPI awareness support offered by various Windows UI frameworks as of Windows 10 1703:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="92e49-192">架構/技術</span><span class="sxs-lookup"><span data-stu-id="92e49-192">Framework / Technology</span></span></th>
<th><span data-ttu-id="92e49-193">支援</span><span class="sxs-lookup"><span data-stu-id="92e49-193">Support</span></span></th>
<th><span data-ttu-id="92e49-194">作業系統版本</span><span class="sxs-lookup"><span data-stu-id="92e49-194">OS Version</span></span></th>
<th><span data-ttu-id="92e49-195">處理的 DPI 縮放比例</span><span class="sxs-lookup"><span data-stu-id="92e49-195">DPI Scaling handled by</span></span></th>
<th><span data-ttu-id="92e49-196">深入閱讀</span><span class="sxs-lookup"><span data-stu-id="92e49-196">Further Reading</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="92e49-197">通用 Windows 平台 (UWP)</span><span class="sxs-lookup"><span data-stu-id="92e49-197">Universal Windows Platform (UWP)</span></span></td>
<td><span data-ttu-id="92e49-198">完整</span><span class="sxs-lookup"><span data-stu-id="92e49-198">Full</span></span></td>
<td><span data-ttu-id="92e49-199">1607</span><span class="sxs-lookup"><span data-stu-id="92e49-199">1607</span></span></td>
<td><span data-ttu-id="92e49-200">UI 架構</span><span class="sxs-lookup"><span data-stu-id="92e49-200">UI framework</span></span></td>
<td><span data-ttu-id="92e49-201"><a href="/windows/uwp/get-started/whats-a-uwp">通用 Windows 平台 (UWP)</a></span><span class="sxs-lookup"><span data-stu-id="92e49-201"><a href="/windows/uwp/get-started/whats-a-uwp">Universal Windows Platform (UWP)</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92e49-202">原始 Win32/通用控制項 V6 (comctl32.dll) </span><span class="sxs-lookup"><span data-stu-id="92e49-202">Raw Win32/Common Controls V6 (comctl32.dll)</span></span></td>
<td><ul>
<li><span data-ttu-id="92e49-203">傳送至所有 Hwnd 的 DPI 變更通知訊息</span><span class="sxs-lookup"><span data-stu-id="92e49-203">DPI change notification messages sent to all HWNDs</span></span></li>
<li><span data-ttu-id="92e49-204">主題-繪製的資產會在通用控制項中正確呈現</span><span class="sxs-lookup"><span data-stu-id="92e49-204">Theme-drawn assets render correctly in common controls</span></span></li>
<li><span data-ttu-id="92e49-205">自動調整對話方塊的 DPI</span><span class="sxs-lookup"><span data-stu-id="92e49-205">Automatic DPI scaling for dialogs</span></span></li>
</ul></td>
<td><span data-ttu-id="92e49-206">1703</span><span class="sxs-lookup"><span data-stu-id="92e49-206">1703</span></span></td>
<td><span data-ttu-id="92e49-207">應用程式</span><span class="sxs-lookup"><span data-stu-id="92e49-207">Application</span></span></td>
<td><span data-ttu-id="92e49-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub 範例</a></span><span class="sxs-lookup"><span data-stu-id="92e49-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92e49-209">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="92e49-209">Windows Forms</span></span></td>
<td><span data-ttu-id="92e49-210">某些控制項的每個監視器的自動 DPI 縮放比例有限</span><span class="sxs-lookup"><span data-stu-id="92e49-210">Limited automatic per-monitor DPI scaling for some controls</span></span></td>
<td><span data-ttu-id="92e49-211">1703</span><span class="sxs-lookup"><span data-stu-id="92e49-211">1703</span></span></td>
<td><span data-ttu-id="92e49-212">UI 架構</span><span class="sxs-lookup"><span data-stu-id="92e49-212">UI framework</span></span></td>
<td><span data-ttu-id="92e49-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Windows Forms 中的高 DPI 支援</a></span><span class="sxs-lookup"><span data-stu-id="92e49-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">High DPI Support in Windows Forms</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92e49-214">Windows Presentation Framework (WPF)</span><span class="sxs-lookup"><span data-stu-id="92e49-214">Windows Presentation Framework (WPF)</span></span></td>
<td><span data-ttu-id="92e49-215">原生 WPF 應用程式將會以 DPI 比例調整裝載于其他架構中的 WPF，而 WPF 中裝載的其他架構則不會自動調整</span><span class="sxs-lookup"><span data-stu-id="92e49-215">Native WPF applications will DPI scale WPF hosted in other frameworks and other frameworks hosted in WPF do not automatically scale</span></span></td>
<td><span data-ttu-id="92e49-216">1607</span><span class="sxs-lookup"><span data-stu-id="92e49-216">1607</span></span></td>
<td><span data-ttu-id="92e49-217">UI 架構</span><span class="sxs-lookup"><span data-stu-id="92e49-217">UI framework</span></span></td>
<td><span data-ttu-id="92e49-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub 範例</a></span><span class="sxs-lookup"><span data-stu-id="92e49-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92e49-219">GDI</span><span class="sxs-lookup"><span data-stu-id="92e49-219">GDI</span></span></td>
<td><span data-ttu-id="92e49-220">無</span><span class="sxs-lookup"><span data-stu-id="92e49-220">None</span></span></td>
<td><span data-ttu-id="92e49-221">N/A</span><span class="sxs-lookup"><span data-stu-id="92e49-221">N/A</span></span></td>
<td><span data-ttu-id="92e49-222">應用程式</span><span class="sxs-lookup"><span data-stu-id="92e49-222">Application</span></span></td>
<td><span data-ttu-id="92e49-223">查看 <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI 高 DPI 縮放比例</a></span><span class="sxs-lookup"><span data-stu-id="92e49-223">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92e49-224">GDI+</span><span class="sxs-lookup"><span data-stu-id="92e49-224">GDI+</span></span></td>
<td><span data-ttu-id="92e49-225">無</span><span class="sxs-lookup"><span data-stu-id="92e49-225">None</span></span></td>
<td><span data-ttu-id="92e49-226">N/A</span><span class="sxs-lookup"><span data-stu-id="92e49-226">N/A</span></span></td>
<td><span data-ttu-id="92e49-227">應用程式</span><span class="sxs-lookup"><span data-stu-id="92e49-227">Application</span></span></td>
<td><span data-ttu-id="92e49-228">查看 <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI 高 DPI 縮放比例</a></span><span class="sxs-lookup"><span data-stu-id="92e49-228">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92e49-229">MFC</span><span class="sxs-lookup"><span data-stu-id="92e49-229">MFC</span></span></td>
<td><span data-ttu-id="92e49-230">無</span><span class="sxs-lookup"><span data-stu-id="92e49-230">None</span></span></td>
<td><span data-ttu-id="92e49-231">N/A</span><span class="sxs-lookup"><span data-stu-id="92e49-231">N/A</span></span></td>
<td><span data-ttu-id="92e49-232">應用程式</span><span class="sxs-lookup"><span data-stu-id="92e49-232">Application</span></span></td>
<td><span data-ttu-id="92e49-233">N/A</span><span class="sxs-lookup"><span data-stu-id="92e49-233">N/A</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a><span data-ttu-id="92e49-234">更新現有的應用程式</span><span class="sxs-lookup"><span data-stu-id="92e49-234">Updating Existing Applications</span></span>

<span data-ttu-id="92e49-235">若要更新現有的桌面應用程式，以適當地處理 DPI 調整，必須更新其 UI 的重要部分，以回應 DPI 變更。</span><span class="sxs-lookup"><span data-stu-id="92e49-235">In order to update an existing desktop application to handle DPI scaling properly, it needs to be updated such that, at a minimum, the important parts of its UI are updated to respond to DPI changes.</span></span>

<span data-ttu-id="92e49-236">大部分的桌面應用程式都是以系統 DPI 感知模式來執行。</span><span class="sxs-lookup"><span data-stu-id="92e49-236">Most desktop applications run under system DPI awareness mode.</span></span> <span data-ttu-id="92e49-237">系統 DPI 感知的應用程式通常會調整為主顯示器的 DPI， (系統匣在 Windows 會話啟動) 時的顯示器。</span><span class="sxs-lookup"><span data-stu-id="92e49-237">System-DPI-aware applications typically scale to the DPI of the primary display (the display that the system tray was located on at the time the Windows session was started).</span></span> <span data-ttu-id="92e49-238">當 DPI 變更時，Windows 會將這些應用程式的 UI 延展出來，這通常會導致這些應用程式變得模糊。</span><span class="sxs-lookup"><span data-stu-id="92e49-238">When the DPI changes, Windows will bitmap stretch the UI of these applications, which often results in them being blurry.</span></span> <span data-ttu-id="92e49-239">當更新系統 DPI 感知應用程式，使其變成個別監視器 DPI 感知時，處理 UI 配置的程式碼需要更新，如此一來，它不僅會在應用程式初始化期間執行，還會在收到 Win32) 的情況下 ([WM \_ DPICHANGED](wm-dpichanged.md) 的 DPI 變更通知時執行。</span><span class="sxs-lookup"><span data-stu-id="92e49-239">When updating a System DPI-aware application to become per-monitor-DPI aware, the code which handles UI layout needs to be updated such that it is performed not only during application initialization, but also whenever a DPI change notification ([WM\_DPICHANGED](wm-dpichanged.md) in the case of Win32) is received.</span></span> <span data-ttu-id="92e49-240">這通常需要重新驗證程式代碼中的任何假設，UI 只需要調整一次。</span><span class="sxs-lookup"><span data-stu-id="92e49-240">This typically involves revisiting any assumptions in the code that the UI only needs to be scaled once.</span></span>

<span data-ttu-id="92e49-241">此外，在 Win32 程式設計的情況下，許多 Win32 Api 都沒有任何 DPI 或顯示內容，因此它們只會傳回相對於系統 DPI 的值。</span><span class="sxs-lookup"><span data-stu-id="92e49-241">Also, in the case of Win32 programming, many Win32 APIs do not have any DPI or display context so they will only return values relative to the System DPI.</span></span> <span data-ttu-id="92e49-242">在您的程式碼中尋找某些 Api，並以 DPI 感知的變異數取代這些 Api，可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="92e49-242">It can be useful to grep through your code to look for some of these APIs and replace them with DPI-aware variants.</span></span> <span data-ttu-id="92e49-243">有些具有 DPI 感知變異的常見 Api 如下：</span><span class="sxs-lookup"><span data-stu-id="92e49-243">Some of the common APIs that have DPI-aware variants are:</span></span>



| <span data-ttu-id="92e49-244">單一 DPI 版本</span><span class="sxs-lookup"><span data-stu-id="92e49-244">Single DPI version</span></span>   | <span data-ttu-id="92e49-245">Per-Monitor 版本</span><span class="sxs-lookup"><span data-stu-id="92e49-245">Per-Monitor version</span></span>        |
|----------------------|----------------------------|
| <span data-ttu-id="92e49-246">GetSystemMetrics</span><span class="sxs-lookup"><span data-stu-id="92e49-246">GetSystemMetrics</span></span>     | <span data-ttu-id="92e49-247">GetSystemMetricsForDpi</span><span class="sxs-lookup"><span data-stu-id="92e49-247">GetSystemMetricsForDpi</span></span>     |
| <span data-ttu-id="92e49-248">AdjustWindowRectEx</span><span class="sxs-lookup"><span data-stu-id="92e49-248">AdjustWindowRectEx</span></span>   | <span data-ttu-id="92e49-249">AdjustWindowRectExForDpi</span><span class="sxs-lookup"><span data-stu-id="92e49-249">AdjustWindowRectExForDpi</span></span>   |
| <span data-ttu-id="92e49-250">SystemParametersInfo</span><span class="sxs-lookup"><span data-stu-id="92e49-250">SystemParametersInfo</span></span> | <span data-ttu-id="92e49-251">SystemParametersInfoForDpi</span><span class="sxs-lookup"><span data-stu-id="92e49-251">SystemParametersInfoForDpi</span></span> |
| <span data-ttu-id="92e49-252">GetDpiForMonitor</span><span class="sxs-lookup"><span data-stu-id="92e49-252">GetDpiForMonitor</span></span>     | <span data-ttu-id="92e49-253">GetDpiForWindow</span><span class="sxs-lookup"><span data-stu-id="92e49-253">GetDpiForWindow</span></span>            |



 

<span data-ttu-id="92e49-254">在您的程式碼基底中搜尋採用固定 DPI 的硬式編碼大小也是個不錯的主意，以正確的 DPI 縮放比例的程式碼取代它們。</span><span class="sxs-lookup"><span data-stu-id="92e49-254">It is also a good idea to search for hard-coded sizes in your codebase that assume a constant DPI, replacing them with code that correctly accounts for DPI scaling.</span></span> <span data-ttu-id="92e49-255">以下是包含所有這些建議的範例：</span><span class="sxs-lookup"><span data-stu-id="92e49-255">Below is an example that incorporates all of these suggestions:</span></span>

### <a name="example"></a><span data-ttu-id="92e49-256">範例：</span><span class="sxs-lookup"><span data-stu-id="92e49-256">Example:</span></span>

<span data-ttu-id="92e49-257">下列範例顯示簡化的 Win32 案例，以建立子系 HWND。</span><span class="sxs-lookup"><span data-stu-id="92e49-257">The example below shows a simplified Win32 case of creating a child HWND.</span></span> <span data-ttu-id="92e49-258">對 CreateWindow 的呼叫會假設應用程式是以 96 DPI 執行，而且在較高的 Dpi 中，按鈕的大小或位置都不正確：</span><span class="sxs-lookup"><span data-stu-id="92e49-258">The call to CreateWindow assumes that the application is running at 96 DPI, and neither the button's size nor position will be correct at higher DPIs:</span></span>


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



<span data-ttu-id="92e49-259">下列更新的程式碼顯示：</span><span class="sxs-lookup"><span data-stu-id="92e49-259">The updated code below shows:</span></span>

1.  <span data-ttu-id="92e49-260">視窗建立程式碼 DPI 針對其父視窗的 DPI 調整子 HWND 的位置和大小</span><span class="sxs-lookup"><span data-stu-id="92e49-260">The window-creation code DPI scaling the position and size of the child HWND for the DPI of its parent window</span></span>
2.  <span data-ttu-id="92e49-261">藉由重新置放並調整子系 HWND 的大小來回應 DPI 變更</span><span class="sxs-lookup"><span data-stu-id="92e49-261">Responding to DPI change by repositioning and resizing the child HWND</span></span>
3.  <span data-ttu-id="92e49-262">以回應 DPI 變更的程式碼移除和取代的硬式編碼大小</span><span class="sxs-lookup"><span data-stu-id="92e49-262">Hard-coded sizes removed and replaced with code that responds to DPI changes</span></span>


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



<span data-ttu-id="92e49-263">更新系統 DPI 感知應用程式時，需要遵循的一些常見步驟如下：</span><span class="sxs-lookup"><span data-stu-id="92e49-263">When updating a System DPI-aware application, some common steps to follow are:</span></span>

1.  <span data-ttu-id="92e49-264">使用應用程式資訊清單 (或其他方法，將處理常式標示為個別監視器 DPI 感知 (V2) ，取決於) 使用) 的 UI 架構 (。</span><span class="sxs-lookup"><span data-stu-id="92e49-264">Mark the process as per-monitor DPI aware (V2) using an application manifest (or other method, depending on the UI framework(s) used).</span></span>
2.  <span data-ttu-id="92e49-265">讓 UI 版面配置邏輯可重複使用，並將其移出應用程式初始化程式碼，以便 \_ 在 Windows (Win32) 程式設計) 的情況下，于發生 DPI 變更 (WM DPICHANGED 時重複使用。</span><span class="sxs-lookup"><span data-stu-id="92e49-265">Make UI layout logic reusable and move it out of application-initialization code such that it can be reused when a DPI change occurs (WM\_DPICHANGED in the case of Windows (Win32) programming).</span></span>
3.  <span data-ttu-id="92e49-266">將假設 DPI 機密資料 (DPI/字型/大小/等等的任何程式碼失效。 ) 永遠不需要更新。</span><span class="sxs-lookup"><span data-stu-id="92e49-266">Invalidate any code that assumes that DPI-sensitive data (DPI/fonts/sizes/etc.) never need to be updated.</span></span> <span data-ttu-id="92e49-267">在處理常式初始化時快取字型大小和 DPI 值是非常常見的作法。</span><span class="sxs-lookup"><span data-stu-id="92e49-267">It is a very common practice to cache font sizes and DPI values at process initialization.</span></span> <span data-ttu-id="92e49-268">更新應用程式以使其成為個別監視器 DPI 感知時，必須在每次遇到新的 DPI 時重新評估 DPI 敏感的資料。</span><span class="sxs-lookup"><span data-stu-id="92e49-268">When updating an application to become per-monitor DPI aware, DPI-sensitive data must be reevaluated whenever a new DPI is encountered.</span></span>
4.  <span data-ttu-id="92e49-269">發生 DPI 變更時，請重載新 DPI 的 (或重新圖像) 任何點陣圖資產，或選擇性地將目前載入的資產延展到正確的大小。</span><span class="sxs-lookup"><span data-stu-id="92e49-269">When a DPI change occurs, reload (or re-rasterize) any bitmap assets for the new DPI or, optionally, bitmap stretch the currently loaded assets to the correct size.</span></span>
5.  <span data-ttu-id="92e49-270">不 Per-Monitor DPI 感知的 Api 的 Grep，並將其取代為適用) Per-Monitor DPI 感知 Api (。</span><span class="sxs-lookup"><span data-stu-id="92e49-270">Grep for APIs that are not Per-Monitor DPI aware and replace them with Per-Monitor DPI-aware APIs (where applicable).</span></span> <span data-ttu-id="92e49-271">範例：將 GetSystemMetrics 取代為 GetSystemMetricsForDpi。</span><span class="sxs-lookup"><span data-stu-id="92e49-271">Example: replace GetSystemMetrics with GetSystemMetricsForDpi.</span></span>
6.  <span data-ttu-id="92e49-272">在多重顯示/多 DPI 系統上測試您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="92e49-272">Test your application on a multiple-display/multi-DPI system.</span></span>
7.  <span data-ttu-id="92e49-273">如果您的應用程式中有任何最上層視窗無法更新為適當的 DPI 縮放比例，請使用下列所述的混合模式 DPI 縮放 () ，以允許系統將這些最上層視窗的點陣圖延展。</span><span class="sxs-lookup"><span data-stu-id="92e49-273">For any top-level windows in your application that you are unable to update to properly DPI scale, use mixed-mode DPI scaling (described below) to allow bitmap stretching of these top-level windows by the system.</span></span>

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a><span data-ttu-id="92e49-274">Mixed-Mode DPI 調整 (子進程的 DPI 縮放比例) </span><span class="sxs-lookup"><span data-stu-id="92e49-274">Mixed-Mode DPI Scaling (Sub-Process DPI Scaling)</span></span>

<span data-ttu-id="92e49-275">更新應用程式以支援個別監視器 DPI 感知時，有時可能會使應用程式中的每個視窗不穩定或無法更新一次。</span><span class="sxs-lookup"><span data-stu-id="92e49-275">When updating an application to support per-monitor DPI awareness, it can sometimes become impractical or impossible to update every window in the application in one go.</span></span> <span data-ttu-id="92e49-276">這可能只是因為更新和測試所有 UI 所需的時間和精力，或是因為您的應用程式可能會載入協力廠商 UI) ，而不是您需要執行的所有 UI 程式碼 (。</span><span class="sxs-lookup"><span data-stu-id="92e49-276">This can simply be due to the time and effort required to update and test all UI, or because you do not own all of the UI code that you need to run (if your application perhaps loads third-party UI).</span></span> <span data-ttu-id="92e49-277">在這些情況下，Windows 提供一種方式，讓您能夠輕鬆進入每個監視器的認知，方法是讓您執行一些應用程式視窗 (最上層的) ，同時將您的時間和精力集中在更新 UI 的重要部分。</span><span class="sxs-lookup"><span data-stu-id="92e49-277">In these situations, Windows offers a way to ease into the world of per-monitor awareness by letting you run some of your application windows (top-level only) in their original DPI-awareness mode while you focus your time and energy updating the more important parts of your UI.</span></span>

<span data-ttu-id="92e49-278">以下是這種情況的圖例：您可以將主要的應用程式 UI 更新為圖例中的「主視窗」 () ，以使用個別監視器 DPI 感知來執行，同時在現有的模式中執行其他視窗 ( 「次要視窗」 ) 。</span><span class="sxs-lookup"><span data-stu-id="92e49-278">Below is an illustration of what this could look like: you update your main application UI ("Main Window"  in the illustration) to run with per-monitor DPI awareness while you run other windows in their existing mode ("Secondary Window").</span></span>

![認知模式之間的 DPI 縮放比例差異](images/hub-page-illustrations.png)

<span data-ttu-id="92e49-280">在 Windows 10 年度更新版 (1607) 之前，進程的 DPI 感知模式是整個進程的屬性。</span><span class="sxs-lookup"><span data-stu-id="92e49-280">Prior to the Windows 10 Anniversary Update (1607), the DPI awareness mode of a process was a process-wide property.</span></span> <span data-ttu-id="92e49-281">從 Windows 10 年度更新版開始，現在可以針對每個 **最上層** 視窗設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="92e49-281">Beginning in the Windows 10 Anniversary Update, this property can now be set per **top-level** window.</span></span> <span data-ttu-id="92e49-282"> (**子** 視窗必須繼續符合其父系的縮放大小。 ) 最上層視窗會定義為沒有父系的視窗。</span><span class="sxs-lookup"><span data-stu-id="92e49-282">(**Child** windows must continue to match the scaling size of their parent.) A top-level window is defined as a window with no parent.</span></span> <span data-ttu-id="92e49-283">這通常是具有最小化、最大化和關閉按鈕的「一般」視窗。</span><span class="sxs-lookup"><span data-stu-id="92e49-283">This is typically a "regular" window with minimize, maximize, and close buttons.</span></span> <span data-ttu-id="92e49-284">子進程 DPI 感知的適用案例是讓 Windows (點陣圖擴充的次要 UI，) ，同時將您的時間和資源集中在更新主要 UI 上。</span><span class="sxs-lookup"><span data-stu-id="92e49-284">The scenario that sub-process DPI awareness is intended for is to have secondary UI scaled by Windows (bitmap stretched) while you focus your time and resources on updating your primary UI.</span></span>

<span data-ttu-id="92e49-285">若要啟用子進程 DPI 感知，請在任何視窗建立呼叫之前和之後呼叫 [**SetThreadDpiAwarenessCoNtext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) 。</span><span class="sxs-lookup"><span data-stu-id="92e49-285">To enable sub-process DPI awareness, call [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) before and after any window creation calls.</span></span> <span data-ttu-id="92e49-286">所建立的視窗會與您透過 SetThreadDpiAwarenessCoNtext 設定的 DPI 感知相關聯。</span><span class="sxs-lookup"><span data-stu-id="92e49-286">The window that is created will be associated with the DPI awareness that you set via SetThreadDpiAwarenessContext.</span></span> <span data-ttu-id="92e49-287">使用第二個呼叫來還原目前線程的 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="92e49-287">Use the second call to restore the current thread s DPI awareness.</span></span>

<span data-ttu-id="92e49-288">雖然使用子進程 DPI 調整可讓您依賴 Windows 來為您的應用程式進行某些 DPI 調整，但它可能會增加應用程式的複雜度。</span><span class="sxs-lookup"><span data-stu-id="92e49-288">While using sub-process DPI scaling enables you to rely on Windows to do some of the DPI scaling for your application, it can increase the complexity of your application.</span></span> <span data-ttu-id="92e49-289">請務必瞭解這種方法的缺點，以及它所引進之複雜性的本質。</span><span class="sxs-lookup"><span data-stu-id="92e49-289">It is important that you understand the drawbacks of this approach and nature of the complexities that it introduces.</span></span> <span data-ttu-id="92e49-290">如需子進程 DPI 感知的詳細資訊，請參閱 [混合模式 Dpi 縮放比例和 DPI 感知 api。](high-dpi-improvements-for-desktop-applications.md)</span><span class="sxs-lookup"><span data-stu-id="92e49-290">For more information about sub-process DPI awareness, see [Mixed-Mode DPI Scaling and DPI-aware APIs.](high-dpi-improvements-for-desktop-applications.md)</span></span>

## <a name="testing-your-changes"></a><span data-ttu-id="92e49-291">測試您的變更</span><span class="sxs-lookup"><span data-stu-id="92e49-291">Testing Your Changes</span></span>

<span data-ttu-id="92e49-292">在您更新應用程式以使其成為個別監視器 DPI 感知之後，請務必驗證應用程式是否正確地回應混合 DPI 環境中的 DPI 變更。</span><span class="sxs-lookup"><span data-stu-id="92e49-292">After you have updated your application to become per-monitor DPI aware, it is important to validate your application properly responds to DPI changes in a mixed-DPI environment.</span></span> <span data-ttu-id="92e49-293">測試的一些細節包括：</span><span class="sxs-lookup"><span data-stu-id="92e49-293">Some specifics to test include:</span></span>

1.  <span data-ttu-id="92e49-294">在不同 DPI 值的顯示之間來回移動應用程式視窗</span><span class="sxs-lookup"><span data-stu-id="92e49-294">Moving application windows back and forth between displays of different DPI values</span></span>
2.  <span data-ttu-id="92e49-295">在顯示不同 DPI 值的情況上啟動應用程式</span><span class="sxs-lookup"><span data-stu-id="92e49-295">Starting your application on displays of different DPI values</span></span>
3.  <span data-ttu-id="92e49-296">當應用程式正在執行時，變更監視的縮放比例</span><span class="sxs-lookup"><span data-stu-id="92e49-296">Changing the scale factor for your monitor while the application is running</span></span>
4.  <span data-ttu-id="92e49-297">變更您用來作為主顯示器的顯示器、登出 _Windows_，然後在重新登入之後重新測試您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="92e49-297">Changing the display that you use as the primary display, _signing out of Windows_, then re-testing your application after signing back in.</span></span> <span data-ttu-id="92e49-298">這在尋找使用硬式編碼大小/維度的程式碼時特別有用。</span><span class="sxs-lookup"><span data-stu-id="92e49-298">This is particularly useful in finding code that uses hard-coded sizes/dimensions.</span></span>

## <a name="common-pitfalls-win32"></a><span data-ttu-id="92e49-299">Win32)  (常見的陷阱</span><span class="sxs-lookup"><span data-stu-id="92e49-299">Common Pitfalls (Win32)</span></span>

<span data-ttu-id="92e49-300">**不使用在 WM DPICHANGED 中提供的建議矩形 \_**</span><span class="sxs-lookup"><span data-stu-id="92e49-300">**Not using the suggested rectangle that is provided in WM\_DPICHANGED**</span></span>

<span data-ttu-id="92e49-301">當 Windows 傳送您的應用程式視窗至 [**WM \_ DPICHANGED**](wm-dpichanged.md) 訊息時，此訊息會包含建議的矩形，您應該使用該矩形來調整視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="92e49-301">When Windows sends your application window a [**WM\_DPICHANGED**](wm-dpichanged.md) message, this message includes a suggested rectangle that you should use to resize your window.</span></span> <span data-ttu-id="92e49-302">您的應用程式必須使用這個矩形來調整本身的大小，因為這樣會：</span><span class="sxs-lookup"><span data-stu-id="92e49-302">It is critical that your application use this rectangle to resize itself, as this will:</span></span>

1.  <span data-ttu-id="92e49-303">確定在顯示器之間拖曳時，滑鼠游標會在視窗上保持相同的相對位置</span><span class="sxs-lookup"><span data-stu-id="92e49-303">Ensure that the mouse cursor will stay in the same relative position on the Window when dragging between displays</span></span>
2.  <span data-ttu-id="92e49-304">防止應用程式視窗進入遞迴的 DPI 變更迴圈，其中一個 DPI 變更會觸發後續的 DPI 變更，而這會觸發另一個 DPI 變更。</span><span class="sxs-lookup"><span data-stu-id="92e49-304">Prevent the application window from getting into a recursive dpi-change cycle where one DPI change triggers a subsequent DPI change, which triggers yet another DPI change.</span></span>

<span data-ttu-id="92e49-305">如果您有應用程式特定的需求，而導致無法使用 Windows 在 WM DPICHANGED 訊息中提供的建議矩形 \_ ，請參閱 [**wm \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md)。</span><span class="sxs-lookup"><span data-stu-id="92e49-305">If you have application-specific requirements that prevent you from using the suggested rectangle that Windows provides in the WM\_DPICHANGED message, see [**WM\_GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span></span> <span data-ttu-id="92e49-306">此訊息可以用來提供 Windows 所需的大小，以在發生 DPI 變更時使用，同時仍能避免上述問題。</span><span class="sxs-lookup"><span data-stu-id="92e49-306">This message can be used to give Windows a desired size you'd like used once the DPI change has occurred, while still avoiding the issues described above.</span></span>

<span data-ttu-id="92e49-307">**缺乏虛擬化的相關檔**</span><span class="sxs-lookup"><span data-stu-id="92e49-307">**Lack of documentation about virtualization**</span></span>

<span data-ttu-id="92e49-308">當 HWND 或進程以非 DPI 感知或系統 DPI 感知的形式執行時，它可以是由 Windows 延伸的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="92e49-308">When an HWND or process is running as either DPI unaware or system DPI aware, it can be bitmap stretched by Windows.</span></span> <span data-ttu-id="92e49-309">當發生這種情況時，Windows 會將某些 Api 的 DPI 機密資訊調整並轉換成呼叫執行緒的座標空間。</span><span class="sxs-lookup"><span data-stu-id="92e49-309">When this happens, Windows scales and converts DPI-sensitive information from some APIs to the coordinate space of the calling thread.</span></span> <span data-ttu-id="92e49-310">例如，如果不知道 DPI 的執行緒在高 DPI 顯示器上執行時查詢螢幕大小，則 Windows 會將指定給應用程式的答案虛擬化，就像螢幕是 96 DPI 單位一樣。</span><span class="sxs-lookup"><span data-stu-id="92e49-310">For example, if a DPI-unaware thread queries the screen size while running on a high-DPI display, Windows will virtualize the answer given to the application as if the screen were in 96 DPI units.</span></span> <span data-ttu-id="92e49-311">或者，當目前使用者的會話開始時，當系統 DPI 感知執行緒與使用中的顯示器互動時，Windows 會將某些 API 呼叫調整成以其原始的 DPI 縮放比例執行時所使用的座標空間。</span><span class="sxs-lookup"><span data-stu-id="92e49-311">Alternatively, when a System DPI-aware thread is interacting with a display at a different DPI than was in use when the current user's session was started, Windows will DPI-scale some API calls into the coordinate space that the HWND would be using if it were running at its original DPI scale factor.</span></span>

<span data-ttu-id="92e49-312">當您將傳統型應用程式更新為正確調整時，可能很難知道哪些 API 呼叫可以根據執行緒內容傳回虛擬化值;這項資訊目前不是由 Microsoft 所充分記載。</span><span class="sxs-lookup"><span data-stu-id="92e49-312">When you update your desktop application to DPI scale properly, it can difficult to know which API calls can return virtualized values based on the thread context; this information is not currently sufficiently documented by Microsoft.</span></span> <span data-ttu-id="92e49-313">請注意，如果您從不感知 DPI 或系統 DPI 感知的執行緒內容呼叫任何系統 API，則傳回值可能會虛擬化。</span><span class="sxs-lookup"><span data-stu-id="92e49-313">Be aware that if you call any system API from a DPI-unaware or system-DPI-aware thread context, the return value might be virtualized.</span></span> <span data-ttu-id="92e49-314">因此，請確定您的執行緒是在與螢幕或個別視窗互動時所預期的 DPI 內容中執行。</span><span class="sxs-lookup"><span data-stu-id="92e49-314">As such, make sure your thread is running in the DPI context you expect when interacting with the screen or individual windows.</span></span> <span data-ttu-id="92e49-315">使用 [SetThreadDpiAwarenessCoNtext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)暫時變更執行緒的 DPI 內容時，請務必在您完成時還原舊的內容，以避免在應用程式中的其他位置造成不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="92e49-315">When temporarily changing a thread's DPI context using [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), be sure to restore the old context when you're done to avoid causing incorrect behavior elsewhere in your application.</span></span>

<span data-ttu-id="92e49-316">**許多 Windows Api 都沒有 DPI 內容**</span><span class="sxs-lookup"><span data-stu-id="92e49-316">**Many Windows APIs do not have an DPI context**</span></span>

<span data-ttu-id="92e49-317">許多舊版 Windows Api 都不會在其介面中包含 DPI 或 HWND 內容。</span><span class="sxs-lookup"><span data-stu-id="92e49-317">Many legacy Windows APIs do not include a DPI or HWND context as part of their interface.</span></span> <span data-ttu-id="92e49-318">因此，開發人員通常必須執行額外的工作來處理任何 DPI 機密資訊的調整，例如大小、點或圖示。</span><span class="sxs-lookup"><span data-stu-id="92e49-318">As a result, developers often have to do additional work to handle the scaling of any DPI-sensitive information, such as sizes, points, or icons.</span></span> <span data-ttu-id="92e49-319">例如，使用 [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) 的開發人員必須使用點陣圖延展已載入的圖示，或使用替代的 api 來載入適當 DPI 大小的正確圖示，例如 [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew)。</span><span class="sxs-lookup"><span data-stu-id="92e49-319">As an example, developers using [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) must either bitmap stretch loaded icons or use alternate APIs to load correctly-sized icons for the appropriate DPI, such as [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span></span>

<span data-ttu-id="92e49-320">**強制重設整個進程的 DPI 感知**</span><span class="sxs-lookup"><span data-stu-id="92e49-320">**Forced reset of process-wide DPI awareness**</span></span>

<span data-ttu-id="92e49-321">一般而言，進程初始化之後，就無法變更您進程的 DPI 感知模式。</span><span class="sxs-lookup"><span data-stu-id="92e49-321">In general, the DPI awareness mode of your process cannot be changed after process initialization.</span></span> <span data-ttu-id="92e49-322">但是，如果您嘗試中斷視窗樹狀結構中的所有 Hwnd 都有相同的 DPI 感知模式，則 Windows 可以強制變更您進程的 DPI 感知模式。</span><span class="sxs-lookup"><span data-stu-id="92e49-322">Windows can, however, forcibly change the DPI awareness mode of your process if you attempt to break the requirement that all HWNDs in a window tree have the same DPI awareness mode.</span></span> <span data-ttu-id="92e49-323">在所有版本的 Windows 上，從 Windows 10 1703 版到，在不同的 DPI 感知模式下執行的 HWND 樹狀結構中不能有不同的 Hwnd。</span><span class="sxs-lookup"><span data-stu-id="92e49-323">On all versions of Windows, as of Windows 10 1703, it is not possible to have different HWNDs in an HWND tree run in different DPI awareness modes.</span></span> <span data-ttu-id="92e49-324">如果您嘗試建立中斷此規則的父子式關聯性，可以重設整個進程的 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="92e49-324">If you attempt to create a child-parent relationship that breaks this rule, the DPI awareness of the entire process can be reset.</span></span> <span data-ttu-id="92e49-325">這可以透過下列方式觸發：</span><span class="sxs-lookup"><span data-stu-id="92e49-325">This can be triggered by:</span></span>

1.  <span data-ttu-id="92e49-326">一個 CreateWindow 呼叫，其中傳入的父視窗是與呼叫執行緒不同的 DPI 感知模式。</span><span class="sxs-lookup"><span data-stu-id="92e49-326">A CreateWindow call where the passed in parent window is of a different DPI awareness mode than the calling thread.</span></span>
2.  <span data-ttu-id="92e49-327">這兩個視窗與不同 DPI 感知模式相關聯的 SetParent 呼叫。</span><span class="sxs-lookup"><span data-stu-id="92e49-327">A SetParent call where the two windows are associated with different DPI awareness modes.</span></span>

<span data-ttu-id="92e49-328">下表顯示當您嘗試違反此規則時所發生的情況：</span><span class="sxs-lookup"><span data-stu-id="92e49-328">The table below shows what happens if you attempt to violate this rule:</span></span>



| <span data-ttu-id="92e49-329">作業</span><span class="sxs-lookup"><span data-stu-id="92e49-329">Operation</span></span>                 | <span data-ttu-id="92e49-330">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="92e49-330">Windows 8.1</span></span>                                  | <span data-ttu-id="92e49-331">Windows 10 (1607 及更早版本) </span><span class="sxs-lookup"><span data-stu-id="92e49-331">Windows 10 (1607 and earlier)</span></span>                | <span data-ttu-id="92e49-332">Windows 10 (1703 和更新版本) </span><span class="sxs-lookup"><span data-stu-id="92e49-332">Windows 10 (1703 and later)</span></span>                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| <span data-ttu-id="92e49-333">在進程內) 的 CreateWindow (</span><span class="sxs-lookup"><span data-stu-id="92e49-333">CreateWindow (In-Proc)</span></span>    | <span data-ttu-id="92e49-334">N/A</span><span class="sxs-lookup"><span data-stu-id="92e49-334">N/A</span></span>                                          | <span data-ttu-id="92e49-335">**子系繼承** (混合模式) </span><span class="sxs-lookup"><span data-stu-id="92e49-335">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="92e49-336">**子系繼承** (混合模式) </span><span class="sxs-lookup"><span data-stu-id="92e49-336">**Child inherits** (mixed mode)</span></span>              |
| <span data-ttu-id="92e49-337"> (跨進程) 的 CreateWindow</span><span class="sxs-lookup"><span data-stu-id="92e49-337">CreateWindow (Cross-Proc)</span></span> | <span data-ttu-id="92e49-338">呼叫端進程的 **強制重設** () </span><span class="sxs-lookup"><span data-stu-id="92e49-338">**Forced reset** (of caller's process)</span></span>       | <span data-ttu-id="92e49-339">**子系繼承** (混合模式) </span><span class="sxs-lookup"><span data-stu-id="92e49-339">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="92e49-340">呼叫端進程的 **強制重設** () </span><span class="sxs-lookup"><span data-stu-id="92e49-340">**Forced reset** (of caller's process)</span></span>       |
| <span data-ttu-id="92e49-341">SetParent (同進程) </span><span class="sxs-lookup"><span data-stu-id="92e49-341">SetParent (In-Proc)</span></span>       | <span data-ttu-id="92e49-342">N/A</span><span class="sxs-lookup"><span data-stu-id="92e49-342">N/A</span></span>                                          | <span data-ttu-id="92e49-343">目前進程的 **強制重設** () </span><span class="sxs-lookup"><span data-stu-id="92e49-343">**Forced reset** (of current process)</span></span>        | <span data-ttu-id="92e49-344">**失敗** (錯誤 \_ 的 \_ 狀態無效) </span><span class="sxs-lookup"><span data-stu-id="92e49-344">**Fail** (ERROR\_INVALID\_STATE)</span></span>             |
| <span data-ttu-id="92e49-345">SetParent (跨進程) </span><span class="sxs-lookup"><span data-stu-id="92e49-345">SetParent (Cross-Proc)</span></span>    | <span data-ttu-id="92e49-346">子視窗進程的 **強制重設** () </span><span class="sxs-lookup"><span data-stu-id="92e49-346">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="92e49-347">子視窗進程的 **強制重設** () </span><span class="sxs-lookup"><span data-stu-id="92e49-347">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="92e49-348">子視窗進程的 **強制重設** () </span><span class="sxs-lookup"><span data-stu-id="92e49-348">**Forced reset** (of child window's process)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="92e49-349">相關主題</span><span class="sxs-lookup"><span data-stu-id="92e49-349">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92e49-350">高 DPI API 參考</span><span class="sxs-lookup"><span data-stu-id="92e49-350">High DPI API Reference</span></span>](high-dpi-reference.md)
</dt> <dt>

[<span data-ttu-id="92e49-351">混合模式 DPI 縮放比例和 DPI 感知 Api。</span><span class="sxs-lookup"><span data-stu-id="92e49-351">Mixed-Mode DPI Scaling and DPI-aware APIs.</span></span>](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

