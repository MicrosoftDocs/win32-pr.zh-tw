---
title: 開發每個監視器 DPI 感知的 WPF 應用程式
description: 請注意，本頁面涵蓋 Windows 8.1 的舊版 WPF 開發。 如果您正在開發 Windows 10 的 WPF 應用程式，請參閱 GitHub 上的最新檔。.
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Windows 消費者介面、DPI 感知的應用程式
- Windows 消費者介面，高 DPI
- DPI 感知應用程式
- 高 DPI
- 撰寫 DPI 感知的 Win32 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092731"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a><span data-ttu-id="cf88e-110">開發每個監視器 DPI 感知的 WPF 應用程式</span><span class="sxs-lookup"><span data-stu-id="cf88e-110">Developing a Per-Monitor DPI-Aware WPF Application</span></span>

<span data-ttu-id="cf88e-111">**重要 API**</span><span class="sxs-lookup"><span data-stu-id="cf88e-111">**Important APIs**</span></span>

-   [<span data-ttu-id="cf88e-112">**SetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="cf88e-112">**SetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [<span data-ttu-id="cf88e-113">**GetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="cf88e-113">**GetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [<span data-ttu-id="cf88e-114">**GetDpiForMonitor**</span><span class="sxs-lookup"><span data-stu-id="cf88e-114">**GetDpiForMonitor**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> <span data-ttu-id="cf88e-115">**本頁面涵蓋 Windows 8.1 的舊版 WPF 開發。**</span><span class="sxs-lookup"><span data-stu-id="cf88e-115">**This page covers legacy WPF development for Windows 8.1.**</span></span> <span data-ttu-id="cf88e-116">如果您正在開發 Windows 10 的 WPF 應用程式，請參閱 <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">GitHub 上的最新檔。</a></span><span class="sxs-lookup"><span data-stu-id="cf88e-116">If you are developing WPF applications for Windows 10, please see the <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">latest documentation on GitHub.</a></span></span>

 

<span data-ttu-id="cf88e-117">Windows 8.1 為開發人員提供新的功能，可讓您建立個別監視器 DPI 感知的桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf88e-117">Windows 8.1 gives developers new functionality to create desktop applications that are per-monitor DPI-aware.</span></span> <span data-ttu-id="cf88e-118">為了充分利用這項功能，每個監視器 DPI 感知應用程式必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="cf88e-118">In order to take advantage of this functionality, a per monitor DPI-aware application must do the following:</span></span>

-   <span data-ttu-id="cf88e-119">變更視窗維度以維持在任何顯示器上顯示一致的實體大小</span><span class="sxs-lookup"><span data-stu-id="cf88e-119">Change window dimensions to maintain a physical size that appears consistent on any display</span></span>
-   <span data-ttu-id="cf88e-120">重新配置及重新呈現新視窗大小的圖形</span><span class="sxs-lookup"><span data-stu-id="cf88e-120">Re-layout and re-render graphics for the new window size</span></span>
-   <span data-ttu-id="cf88e-121">選取針對 DPI 層級適當調整的字型</span><span class="sxs-lookup"><span data-stu-id="cf88e-121">Select fonts that are scaled appropriately for the DPI level</span></span>
-   <span data-ttu-id="cf88e-122">選取並載入為 DPI 層級量身打造的點陣圖資產</span><span class="sxs-lookup"><span data-stu-id="cf88e-122">Select and load bitmap assets that are tailored for the DPI level</span></span>

<span data-ttu-id="cf88e-123">為了加速製作個別監視器 DPI 感知應用程式，Windows 8.1 提供下列 Microsoft Win32APIs：</span><span class="sxs-lookup"><span data-stu-id="cf88e-123">To facilitate making a per-monitor DPI-aware application, Windows 8.1 provides the following Microsoft Win32APIs:</span></span>

-   <span data-ttu-id="cf88e-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (或 DPI 資訊清單專案) 將進程設定為指定的 DPI 感知層級，然後決定 Windows 如何調整 UI。</span><span class="sxs-lookup"><span data-stu-id="cf88e-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (or DPI manifest entry) sets the process to a specified DPI awareness level, which then determines how Windows scales the UI.</span></span> <span data-ttu-id="cf88e-125">這會取代 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)。</span><span class="sxs-lookup"><span data-stu-id="cf88e-125">This supersedes [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span></span>
-   <span data-ttu-id="cf88e-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) 會傳回 DPI 感知層級。</span><span class="sxs-lookup"><span data-stu-id="cf88e-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) returns the DPI awareness level.</span></span> <span data-ttu-id="cf88e-127">這會取代 [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware)。</span><span class="sxs-lookup"><span data-stu-id="cf88e-127">This supersedes [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span></span>
-   <span data-ttu-id="cf88e-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) 會傳回監視器的 DPI。</span><span class="sxs-lookup"><span data-stu-id="cf88e-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) returns the DPI for a monitor.</span></span>
-   <span data-ttu-id="cf88e-129">當視窗的位置變更時，會將 [**WM \_ DPICHANGED**](wm-dpichanged.md) 視窗通知傳送至每個監視器 DPI 感知的應用程式，使其大部分的區域與在位置變更之前或當使用者移動顯示滑杆時，與 DPI 不同的監視器相交。</span><span class="sxs-lookup"><span data-stu-id="cf88e-129">The [**WM\_DPICHANGED**](wm-dpichanged.md) window notification is sent to per-monitor DPI-aware applications when a window’s position changes such that most of its area intersects a monitor with a DPI that is different from the DPI before the position change or when the user moves the display slider.</span></span> <span data-ttu-id="cf88e-130">若要建立應用程式，以在使用者將它移至不同的顯示器時調整大小並重新呈現，請使用此通知。</span><span class="sxs-lookup"><span data-stu-id="cf88e-130">To create an application that resizes and re-renders itself when a user moves it to a different display, use this notification.</span></span>

<span data-ttu-id="cf88e-131">如需 Windows 8.1 中桌面應用程式支援之各種 DPI 感知層級的詳細資訊，請參閱 [撰寫 DPI-Aware desktop 和 Win32 應用程式](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))的主題。</span><span class="sxs-lookup"><span data-stu-id="cf88e-131">For more details on various DPI awareness levels supported for desktop applications in Windows 8.1 see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

## <a name="dpi-scaling-and-wpf"></a><span data-ttu-id="cf88e-132">DPI 縮放比例和 WPF</span><span class="sxs-lookup"><span data-stu-id="cf88e-132">DPI Scaling and WPF</span></span>

<span data-ttu-id="cf88e-133">Windows Presentation Foundation (WPF) 應用程式預設會感知系統 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="cf88e-133">Windows Presentation Foundation (WPF) applications are by default system DPI-aware.</span></span> <span data-ttu-id="cf88e-134">如需不同 DPI 感知層級的定義，請參閱 [撰寫 DPI-Aware Desktop 和 Win32 應用程式](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))的主題。</span><span class="sxs-lookup"><span data-stu-id="cf88e-134">For definitions of the different DPI awareness levels see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span> <span data-ttu-id="cf88e-135">WPF 圖形系統使用與裝置無關的單位來啟用解析度和裝置獨立性。</span><span class="sxs-lookup"><span data-stu-id="cf88e-135">The WPF graphics system uses device-independent units to enable resolution and device independence.</span></span> <span data-ttu-id="cf88e-136">WPF 會根據目前的系統 DPI 自動調整每個裝置的獨立圖元。</span><span class="sxs-lookup"><span data-stu-id="cf88e-136">WPF scales each device independent pixel automatically based on current system DPI.</span></span> <span data-ttu-id="cf88e-137">這可讓 WPF 應用程式在視窗開啟的監視器 DPI 與系統 DPI 相同時自動調整。</span><span class="sxs-lookup"><span data-stu-id="cf88e-137">This allows WPF applications to scale automatically when the DPI of the monitor the window is on is same system DPI.</span></span> <span data-ttu-id="cf88e-138">不過，由於 WPF 應用程式是系統 DPI 感知，因此當應用程式移至具有不同 DPI 的監視器，或使用 [控制台] 中的滑杆來變更 DPI 時，作業系統會調整應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf88e-138">However, since WPF applications are system dpi-aware, the application will be scaled by the OS when the application is moved to a monitor with a different DPI or when the slider in the control panel is used to change the DPI.</span></span> <span data-ttu-id="cf88e-139">在 OS 中進行調整可能會導致 WPF 應用程式看似模糊，特別是當調整為非整數時。</span><span class="sxs-lookup"><span data-stu-id="cf88e-139">Scaling in the OS may result in WPF applications to appear blurry especially when the scaling is non-integral.</span></span> <span data-ttu-id="cf88e-140">為了避免調整 WPF 應用程式，必須將其更新為個別監視器 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="cf88e-140">In order to avoid scaling WPF applications, they need to be updated to be per-monitor DPI-aware.</span></span>

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a><span data-ttu-id="cf88e-141">每個監視器感知 WPF 範例逐步解說</span><span class="sxs-lookup"><span data-stu-id="cf88e-141">Per Monitor Aware WPF Sample Walkthrough</span></span>

<span data-ttu-id="cf88e-142">[每個監視器感知 wpf 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)是更新為個別監視器 DPI 感知的範例 wpf 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf88e-142">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) is a sample WPF application updated to be per-monitor DPI-aware.</span></span> <span data-ttu-id="cf88e-143">此範例包含了二個專案：</span><span class="sxs-lookup"><span data-stu-id="cf88e-143">The sample consists of two projects:</span></span>

-   <span data-ttu-id="cf88e-144">NativeHelpers. .vcxproj：這是原生協助程式專案，它會執行核心功能，讓 WPF 應用程式依照上述 Win32APIs 的個別監視器 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="cf88e-144">NativeHelpers.vcxproj: This is a native helper project that implements the core functionality to make a WPF application as per-monitor DPI-aware utilizing the Win32APIs above.</span></span> <span data-ttu-id="cf88e-145">專案包含兩個類別：</span><span class="sxs-lookup"><span data-stu-id="cf88e-145">The project contains two classes:</span></span>
    -   <span data-ttu-id="cf88e-146">PerMonDPIHelpers：提供與 DPI 相關之作業的 helper 函式的類別，例如抓取作用中監視器的目前 DPI、將進程設定為個別監視器 DPI 感知等等。</span><span class="sxs-lookup"><span data-stu-id="cf88e-146">PerMonDPIHelpers: A class that provides helper functions for DPI related operations like retrieving the current DPI of the active monitor, setting a process to be per-monitor DPI-aware, etc.</span></span>
    -   <span data-ttu-id="cf88e-147">PerMonitorDPIWindow：衍生自的基類，它會實作為個別監視器 DPI 感知之 WPF 應用程式 **視窗的功能** 。</span><span class="sxs-lookup"><span data-stu-id="cf88e-147">PerMonitorDPIWindow: A base class derived from **System.Windows.Window** that implements functionality to make a WPF application window to be per-monitor dpi-aware.</span></span> <span data-ttu-id="cf88e-148">根據監視器的 DPI 而非系統 DPI，調整視窗大小、圖形轉譯大小和字型大小。</span><span class="sxs-lookup"><span data-stu-id="cf88e-148">Adjusts window size, graphics rendering size and font size based on the DPI of the monitor rather than the system DPI.</span></span>
-   <span data-ttu-id="cf88e-149">WPFApplication .csproj：使用 PerMonitorDPIWindow (PerMonitorDPIWindow) 的範例 WPF 應用程式，並展示當視窗移至具有不同 DPI 的監視器時，或在顯示控制台中的滑杆用來變更 DPI 時，應用程式視窗和轉譯的大小。</span><span class="sxs-lookup"><span data-stu-id="cf88e-149">WPFApplication.csproj: Sample WPF application that consumes the PerMonitorDPIWindow (PerMonitorDPIWindow), and showcases how the application window and rendering resizes when the window is moved to a monitor with a different DPI or when the slider in the Display control panel is used to change the DPI.</span></span>

<span data-ttu-id="cf88e-150">若要執行範例，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="cf88e-150">To run the sample follow the steps below:</span></span>

1.  <span data-ttu-id="cf88e-151">下載並解壓縮 [每個監視器感知 WPF 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span><span class="sxs-lookup"><span data-stu-id="cf88e-151">Download and unzip the [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span></span>
2.  <span data-ttu-id="cf88e-152">開始 Microsoft Visual Studio，然後選取 [檔案] **> 開啟 > 專案/方案**</span><span class="sxs-lookup"><span data-stu-id="cf88e-152">Start Microsoft Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="cf88e-153">流覽至包含解壓縮範例的目錄。</span><span class="sxs-lookup"><span data-stu-id="cf88e-153">Browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="cf88e-154">移至為範例命名的目錄，然後按兩下 Visual Studio 方案 ( .sln) 檔</span><span class="sxs-lookup"><span data-stu-id="cf88e-154">Go to the directory named for the sample, and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="cf88e-155">按 F7 或使用 **組建 > 組建方案** 來建立範例</span><span class="sxs-lookup"><span data-stu-id="cf88e-155">Press F7 or use **Build > Build Solution** to build the sample</span></span>
5.  <span data-ttu-id="cf88e-156">按 Ctrl + F5 或使用 **Debug > 啟動但不進行調試** ，以執行範例</span><span class="sxs-lookup"><span data-stu-id="cf88e-156">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="cf88e-157">若要查看使用範例中的基類，將已更新為個別監視器 DPI 感知之 WPF 應用程式上變更 DPI 的影響，請將應用程式視窗移至具有不同 Dpi 的顯示。</span><span class="sxs-lookup"><span data-stu-id="cf88e-157">To see the impact of changing DPI on a WPF application that is updated to be per-monitor DPI-aware using the base class in the sample, move the application window to and from displays that have different DPIs.</span></span> <span data-ttu-id="cf88e-158">當視窗在監視器之間移動時，系統會使用 WPF 的可擴充圖形系統（而不是由 OS 調整），根據顯示的 DPI 來更新視窗大小和 UI 縮放比例。</span><span class="sxs-lookup"><span data-stu-id="cf88e-158">As the window is moved between monitors, the window size and the UI scale is updated based on the DPI of the display by using WPF’s scalable graphics system, rather than being scaled by the OS.</span></span> <span data-ttu-id="cf88e-159">應用程式的 UI 會以原生方式轉譯，且不會變得模糊。</span><span class="sxs-lookup"><span data-stu-id="cf88e-159">The application’s UI is rendered natively and does not appear blurry.</span></span> <span data-ttu-id="cf88e-160">如果您沒有兩個顯示器具有不同的 DPI，請變更 [顯示] 控制台中的滑杆來變更 DPI。</span><span class="sxs-lookup"><span data-stu-id="cf88e-160">If you don’t have two displays with different DPI, change the DPI by changing the slider in the Display control panel.</span></span> <span data-ttu-id="cf88e-161">變更滑杆 **並按一下 [** 套用]，將會調整應用程式的視窗大小，並自動更新 UI 規模。</span><span class="sxs-lookup"><span data-stu-id="cf88e-161">Changing the slider and clicking **Apply** will resize the application’s window and update the UI scale automatically.</span></span>

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a><span data-ttu-id="cf88e-162">使用 WPF 範例中的 helper 專案，將現有的 WPF 應用程式更新為個別監視器 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="cf88e-162">Updating an existing WPF Application to be per-monitor dpi-aware using helper project in the WPF Sample</span></span>

<span data-ttu-id="cf88e-163">如果您有現有的 WPF 應用程式，並想要利用範例中的 DPI 協助程式專案，讓它成為 DPI 感知，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="cf88e-163">If you have an existing WPF application and wish to leverage the DPI helper project from the sample to make it DPI aware, follow these steps.</span></span>

1.  <span data-ttu-id="cf88e-164">下載並解壓縮每個監視器感知 WPF 範例</span><span class="sxs-lookup"><span data-stu-id="cf88e-164">Download and unzip the Per Monitor Aware WPF sample</span></span>
2.  <span data-ttu-id="cf88e-165">開始 Visual Studio，然後選取 [檔案] **> 開啟 > 專案/方案**</span><span class="sxs-lookup"><span data-stu-id="cf88e-165">Start Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="cf88e-166">流覽至包含現有 WPF 應用程式的目錄，然後按兩下 [Visual Studio 方案 ( .sln) 檔</span><span class="sxs-lookup"><span data-stu-id="cf88e-166">Browse to the directory which contains an existing WPF application and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="cf88e-167">以滑鼠右鍵按一下 [**方案 > 新增 > 現有專案**] ![ 螢幕擷取畫面，其中顯示 [新增：現有專案] 功能表選取專案](images/scrvs-image1.png)</span><span class="sxs-lookup"><span data-stu-id="cf88e-167">Right click on **Solution > Add > Existing Project**![a screenshot that illustrates the add: existing project menu selection](images/scrvs-image1.png)</span></span>
5.  <span data-ttu-id="cf88e-168">在 [檔案選取] 對話方塊中，流覽至包含解壓縮範例的目錄。</span><span class="sxs-lookup"><span data-stu-id="cf88e-168">In the file selection dialogue browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="cf88e-169">開啟至範例中名為的目錄，流覽至 "NativeHelpers" 資料夾，選取 Visual C++ 專案檔 "NativeHelpers .vcxproj"，然後按一下 **[確定]** 。</span><span class="sxs-lookup"><span data-stu-id="cf88e-169">Open to the directory named for the sample, browse to the folder "NativeHelpers", select the Visual C++ project file "NativeHelpers.vcxproj” and click **OK**</span></span>
6.  <span data-ttu-id="cf88e-170">以滑鼠右鍵按一下專案 NativeHelpers，然後選取 [ **建立**]。</span><span class="sxs-lookup"><span data-stu-id="cf88e-170">Right click on the project NativeHelpers and select **Build**.</span></span> <span data-ttu-id="cf88e-171">這會產生 NativeHelpers.dll，在下一個步驟中將新增為 WPF 應用程式的參考，並在下一個步驟中示範 ![ 建立功能表選取專案](images/scrvs-image2.png)</span><span class="sxs-lookup"><span data-stu-id="cf88e-171">This will generate NativeHelpers.dll that will be added as a reference to the WPF Application in the next step![a screen shot illustrating the build menu selection](images/scrvs-image2.png)</span></span>
7.  <span data-ttu-id="cf88e-172">從您的 WPF 應用程式新增 NativeHelpers.dll 的參考。</span><span class="sxs-lookup"><span data-stu-id="cf88e-172">Add a reference to NativeHelpers.dll from your WPF Application.</span></span> <span data-ttu-id="cf88e-173">展開您的 WPF 應用程式專案，以滑鼠右鍵按一下 [**參考**]，然後按一下 [**加入參考**]。</span><span class="sxs-lookup"><span data-stu-id="cf88e-173">Expand your WPF application project, right click on **References** and click on **Add Reference...**</span></span>
8.  <span data-ttu-id="cf88e-174">在產生的對話方塊中，展開 [ **方案** ] 區段。</span><span class="sxs-lookup"><span data-stu-id="cf88e-174">In the resulting dialogue, expand the **Solution** section.</span></span> <span data-ttu-id="cf88e-175">在 [**專案**] 底下，選取 [NativeHelpers]，然後按一下 **[確定]**， ![ 以螢幕擷取畫面說明資源管理員對話方塊](images/scrvs-image3.png)</span><span class="sxs-lookup"><span data-stu-id="cf88e-175">Under **Projects**, select NativeHelpers, and click **OK**![a screen shot illustrating the resource manager dialog](images/scrvs-image3.png)</span></span>
9.  <span data-ttu-id="cf88e-176">展開您的 WPF 應用程式專案，展開 [ **屬性**]，然後開啟 [ **AssemblyInfo**]。</span><span class="sxs-lookup"><span data-stu-id="cf88e-176">Expand your WPF application project, expand **Properties**, and open **AssemblyInfo.cs**.</span></span> <span data-ttu-id="cf88e-177">對 AssemblyInfo 進行下列新增專案</span><span class="sxs-lookup"><span data-stu-id="cf88e-177">Make the following additions to AssemblyInfo.cs</span></span>
    -   <span data-ttu-id="cf88e-178">使用 System. Media (的參考區段中，新增對 system.string 的參考，) </span><span class="sxs-lookup"><span data-stu-id="cf88e-178">Add reference to System.Windows.Media in the reference section (using System.Windows.Media;)</span></span>
    -   <span data-ttu-id="cf88e-179">將 DisableDpiAwareness 屬性新增 (`[assembly: DisableDpiAwareness]`) </span><span class="sxs-lookup"><span data-stu-id="cf88e-179">Add the DisableDpiAwareness attribute (`[assembly: DisableDpiAwareness]`)</span></span>

    ![說明其他屬性的螢幕擷取畫面](images/scrvs-image4.png)
10. <span data-ttu-id="cf88e-181">從 PerMonitorDPIWindow 基類繼承主要 WPF 視窗類別</span><span class="sxs-lookup"><span data-stu-id="cf88e-181">Inherit the main WPF window class from PerMonitorDPIWindow base class</span></span>
    -   <span data-ttu-id="cf88e-182">更新主要 WPF 視窗的 .cs 檔案，以繼承自 PerMonitorDPIWindow 基類</span><span class="sxs-lookup"><span data-stu-id="cf88e-182">Update the .cs file of the main WPF window to inherit from the PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="cf88e-183">藉由新增該行，在參考區段中新增 NativeHelpers 的參考 `using NativeHelpers;`</span><span class="sxs-lookup"><span data-stu-id="cf88e-183">Add a reference to NativeHelpers in the reference section by adding the line `using NativeHelpers;`</span></span>
        -   <span data-ttu-id="cf88e-184">從 PerMonitorDPIWindow 類別繼承主視窗類別</span><span class="sxs-lookup"><span data-stu-id="cf88e-184">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![說明 c + + 參考的螢幕擷取畫面](images/scrvs-image5.png)
    -   <span data-ttu-id="cf88e-186">更新主要 WPF 視窗的 .xaml 檔案，以繼承自 PerMonitorDPIWindow 基類</span><span class="sxs-lookup"><span data-stu-id="cf88e-186">Update the .xaml file of the main WPF window to inherit from PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="cf88e-187">藉由新增該行，在參考區段中新增 NativeHelpers 的參考 `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span><span class="sxs-lookup"><span data-stu-id="cf88e-187">Add a reference to NativeHelpers in the reference section by adding the line `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span></span>
        -   <span data-ttu-id="cf88e-188">從 PerMonitorDPIWindow 類別繼承主視窗類別</span><span class="sxs-lookup"><span data-stu-id="cf88e-188">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![示範新增 .xaml 參考的螢幕擷取畫面](images/scrvs-image6.png)
11. <span data-ttu-id="cf88e-190">按 F7 或使用 **組建 > 組建方案** 來建立範例</span><span class="sxs-lookup"><span data-stu-id="cf88e-190">Press F7 or use **Build > Build Solution** to build the sample</span></span>
12. <span data-ttu-id="cf88e-191">按 Ctrl + F5 或使用 **Debug > 啟動但不進行調試** ，以執行範例</span><span class="sxs-lookup"><span data-stu-id="cf88e-191">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="cf88e-192">[每個監視器感知 wpf 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)應用程式說明如何藉由回應 [**WM \_ DPICHANGED**](wm-dpichanged.md)視窗通知，將 wpf 應用程式更新為每個監視器 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="cf88e-192">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) application illustrates how a WPF application can be updated to be per-monitor DPI-aware by responding to the [**WM\_DPICHANGED**](wm-dpichanged.md) window notification.</span></span> <span data-ttu-id="cf88e-193">為了回應視窗通知，此範例會根據視窗所在的目前監視器 DPI，更新 WPF 所使用的縮放轉換。</span><span class="sxs-lookup"><span data-stu-id="cf88e-193">In response to the window notification, the sample updates the scale transform used by WPF based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="cf88e-194">視窗通知的 *wParam* 會在 *wParam* 中包含新的 DPI。</span><span class="sxs-lookup"><span data-stu-id="cf88e-194">The *wParam* of the window notification contains the new DPI in the *wParam*.</span></span> <span data-ttu-id="cf88e-195">*LParam* 包含一個矩形，其具有新建議視窗的大小和位置，並針對新的 DPI 進行縮放。</span><span class="sxs-lookup"><span data-stu-id="cf88e-195">The *lParam* contains a rectangle that has the size and position of the new suggested window, scaled for the new DPI.</span></span>

<span data-ttu-id="cf88e-196">附註：</span><span class="sxs-lookup"><span data-stu-id="cf88e-196">Note:</span></span>

> [!Note]  
> <span data-ttu-id="cf88e-197">由於此範例會覆寫 WPF 視窗之根節點的視窗大小和小數位數轉換，因此應用程式開發人員可能需要進一步的工作（如果有的話）：</span><span class="sxs-lookup"><span data-stu-id="cf88e-197">Since this sample overwrites the window size and the scale transform of the root node of the WPF window, further work may be required by application developer if:</span></span>
>
> -   <span data-ttu-id="cf88e-198">視窗的大小會影響應用程式的其他部分，例如此 WPF 視窗裝載于另一個應用程式內。</span><span class="sxs-lookup"><span data-stu-id="cf88e-198">The size of the window impacts other portions of the application like this WPF Window being hosted inside another application.</span></span>
> -   <span data-ttu-id="cf88e-199">擴充此類別的 WPF 應用程式是在根視覺效果上設定其他轉換;範例可能會覆寫 WPF 應用程式本身所套用的其他轉換。</span><span class="sxs-lookup"><span data-stu-id="cf88e-199">The WPF application that is extending this class is setting some other transform on the root visual; the sample may overwrite some other transform that is being applied by the WPF application itself.</span></span>

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a><span data-ttu-id="cf88e-200">WPF 範例中的 helper 專案總覽</span><span class="sxs-lookup"><span data-stu-id="cf88e-200">Overview of the helper project in the WPF sample</span></span>

<span data-ttu-id="cf88e-201">若要讓現有的 WPF 應用程式每個監視器 DPI 感知 DPI 感知 NativeHelpers 程式庫提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="cf88e-201">In order to make an existing WPF application per-monitor DPI-aware the NativeHelpers library provides following functionality:</span></span>

-   <span data-ttu-id="cf88e-202">**將 WPF 應用程式標示為每個 PONITOR DPI 感知：** WPF 應用程式會針對目前的進程呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) ，以標示為個別監視器 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="cf88e-202">**Marks the WPF application as per-ponitor DPI-aware:** The WPF application is marked as per-monitor DPI-aware by calling [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) for the current process.</span></span> <span data-ttu-id="cf88e-203">將應用程式標示為每個監視器 DPI 感知，可確保</span><span class="sxs-lookup"><span data-stu-id="cf88e-203">Marking the application as per-monitor DPI-aware will ensure that</span></span>

    -   <span data-ttu-id="cf88e-204">當系統 DPI 不符合應用程式視窗目前的監視器 DPI 時，作業系統不會調整應用程式的規模</span><span class="sxs-lookup"><span data-stu-id="cf88e-204">The OS does not scale the application when the system DPI does not match the current DPI of the monitor the application window is on</span></span>
    -   <span data-ttu-id="cf88e-205">每當視窗的 DPI 變更時，就會傳送 [**WM \_ DPICHANGED**](wm-dpichanged.md) 訊息</span><span class="sxs-lookup"><span data-stu-id="cf88e-205">The [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent whenever the DPI of the window changes</span></span>

-   <span data-ttu-id="cf88e-206">**調整視窗維度、重新配置和重新呈現圖形內容，並根據視窗所在的監視器初始 DPI 來選取字型：** 一旦將應用程式標示為個別監視器 DPI 感知，WPF 仍會根據系統 DPI 來調整視窗大小、圖形和字型大小。</span><span class="sxs-lookup"><span data-stu-id="cf88e-206">**Adjusts the window dimension, re-layout and re-render graphics content and select fonts based on initial DPI of the monitor the window is on:** Once the application is marked as per-monitor DPI-aware, WPF will still scale the window size, graphics and font size based on the system DPI.</span></span> <span data-ttu-id="cf88e-207">在應用程式啟動時，系統 DPI 不保證會與啟動視窗的監視器 DPI 相同，因此在載入視窗時，程式庫會調整這些值。</span><span class="sxs-lookup"><span data-stu-id="cf88e-207">Since, at app launch, the system DPI is not guaranteed to be the same as the DPI of the monitor the window is launched on, the library adjust these values once the window is loaded.</span></span> <span data-ttu-id="cf88e-208">基底類別 **PerMonitorDPIWindow** 會在 **OnLoaded ()** 處理常式中更新這些。</span><span class="sxs-lookup"><span data-stu-id="cf88e-208">The base class **PerMonitorDPIWindow** updates these in the **OnLoaded()** handler.</span></span>

    <span data-ttu-id="cf88e-209">變更視窗的 **寬度** 和 **高度** 屬性來更新視窗大小。</span><span class="sxs-lookup"><span data-stu-id="cf88e-209">The Window size is updated by changing the **Width** and **Height** properties of the Window.</span></span> <span data-ttu-id="cf88e-210">配置和大小的更新方式是將適當的縮放轉換套用至 WPF 視窗的根節點。</span><span class="sxs-lookup"><span data-stu-id="cf88e-210">The layout and size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span>

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   <span data-ttu-id="cf88e-211">**回應 WM \_DPICHANGED 視窗通知：** 根據視窗通知中傳遞的 DPI，更新視窗大小、圖形和字型大小。</span><span class="sxs-lookup"><span data-stu-id="cf88e-211">**Responds to WM\_DPICHANGED window notification:** Update the window size, graphics and font size based on the DPI passed in the window notification.</span></span> <span data-ttu-id="cf88e-212">基底類別 **PerMonitorDPIWindow** 會處理 **HandleMessages ()** 方法中的視窗通知。</span><span class="sxs-lookup"><span data-stu-id="cf88e-212">The base class **PerMonitorDPIWindow** handles the window notification in the **HandleMessages()** method.</span></span>

    <span data-ttu-id="cf88e-213">使用在視窗訊息 *lparam* 中傳遞的資訊來呼叫 **SetWindowPos** ，以更新視窗大小。</span><span class="sxs-lookup"><span data-stu-id="cf88e-213">The Window size is updated by calling **SetWindowPos** using the information passed in the *lparam* of the window message.</span></span> <span data-ttu-id="cf88e-214">版面配置和圖形大小的更新方式是將適當的縮放轉換套用至 WPF 視窗的根節點。</span><span class="sxs-lookup"><span data-stu-id="cf88e-214">The layout and graphics size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span> <span data-ttu-id="cf88e-215">縮放比例的計算方式是使用在視窗訊息的 *wparam* 中傳遞的 DPI。</span><span class="sxs-lookup"><span data-stu-id="cf88e-215">The scale factor is calculated by using the DPI passed in the *wparam* of the window message.</span></span>

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a><span data-ttu-id="cf88e-216">處理資產（例如影像）的 DPI 變更</span><span class="sxs-lookup"><span data-stu-id="cf88e-216">Handling DPI change for assets like images</span></span>

<span data-ttu-id="cf88e-217">為了更新圖形內容，範例 WPF 應用程式會將縮放轉換套用至 WPF 應用程式的根節點。</span><span class="sxs-lookup"><span data-stu-id="cf88e-217">In order to update graphics content, the sample WPF application applies a scale transform to the root node of the WPF application.</span></span> <span data-ttu-id="cf88e-218">雖然這適用于 WPF 以原生方式轉譯的內容 (矩形、文字等 ) ，這表示點陣圖資產（例如影像）會依 WPF 縮放。</span><span class="sxs-lookup"><span data-stu-id="cf88e-218">While this works well for content that is rendered natively by WPF (rectangle, text etc.), this implies that bitmap assets like images are scaled by WPF.</span></span>

<span data-ttu-id="cf88e-219">為了避免因縮放所造成的模糊點陣圖，WPF 應用程式開發人員可以撰寫自訂的 DPI 影像控制項，以根據視窗所在的目前監視器 DPI 來選取不同的資產。</span><span class="sxs-lookup"><span data-stu-id="cf88e-219">In order to avoid blurred bitmaps caused by scaling, the WPF application developer can write a custom DPI image control that selects a different asset based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="cf88e-220">當 DPI 變更時，影像控制項可以依賴針對從 **PerMonitorDPIWindow** 取用的 WPF 視窗所引發的 **DPIChanged ()** 事件。</span><span class="sxs-lookup"><span data-stu-id="cf88e-220">The image control can rely on the **DPIChanged()** event fired for the WPF window that consumes from the **PerMonitorDPIWindow**, when the DPI changes.</span></span>

> [!Note]  
> <span data-ttu-id="cf88e-221">在 **載入的 ()** WPF 視窗事件處理常式中，影像控制項也應該在應用程式啟動期間，選取正確的控制項。</span><span class="sxs-lookup"><span data-stu-id="cf88e-221">The image control should also select the right control during app launch in the **Loaded()** WPF window event handler.</span></span>

 

 

 