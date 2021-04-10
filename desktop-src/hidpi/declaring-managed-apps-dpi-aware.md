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
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>開發每個監視器 DPI 感知的 WPF 應用程式

**重要 API**

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **本頁面涵蓋 Windows 8.1 的舊版 WPF 開發。** 如果您正在開發 Windows 10 的 WPF 應用程式，請參閱 <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">GitHub 上的最新檔。</a>

 

Windows 8.1 為開發人員提供新的功能，可讓您建立個別監視器 DPI 感知的桌面應用程式。 為了充分利用這項功能，每個監視器 DPI 感知應用程式必須執行下列動作：

-   變更視窗維度以維持在任何顯示器上顯示一致的實體大小
-   重新配置及重新呈現新視窗大小的圖形
-   選取針對 DPI 層級適當調整的字型
-   選取並載入為 DPI 層級量身打造的點陣圖資產

為了加速製作個別監視器 DPI 感知應用程式，Windows 8.1 提供下列 Microsoft Win32APIs：

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (或 DPI 資訊清單專案) 將進程設定為指定的 DPI 感知層級，然後決定 Windows 如何調整 UI。 這會取代 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)。
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) 會傳回 DPI 感知層級。 這會取代 [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware)。
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) 會傳回監視器的 DPI。
-   當視窗的位置變更時，會將 [**WM \_ DPICHANGED**](wm-dpichanged.md) 視窗通知傳送至每個監視器 DPI 感知的應用程式，使其大部分的區域與在位置變更之前或當使用者移動顯示滑杆時，與 DPI 不同的監視器相交。 若要建立應用程式，以在使用者將它移至不同的顯示器時調整大小並重新呈現，請使用此通知。

如需 Windows 8.1 中桌面應用程式支援之各種 DPI 感知層級的詳細資訊，請參閱 [撰寫 DPI-Aware desktop 和 Win32 應用程式](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))的主題。

## <a name="dpi-scaling-and-wpf"></a>DPI 縮放比例和 WPF

Windows Presentation Foundation (WPF) 應用程式預設會感知系統 DPI 感知。 如需不同 DPI 感知層級的定義，請參閱 [撰寫 DPI-Aware Desktop 和 Win32 應用程式](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))的主題。 WPF 圖形系統使用與裝置無關的單位來啟用解析度和裝置獨立性。 WPF 會根據目前的系統 DPI 自動調整每個裝置的獨立圖元。 這可讓 WPF 應用程式在視窗開啟的監視器 DPI 與系統 DPI 相同時自動調整。 不過，由於 WPF 應用程式是系統 DPI 感知，因此當應用程式移至具有不同 DPI 的監視器，或使用 [控制台] 中的滑杆來變更 DPI 時，作業系統會調整應用程式。 在 OS 中進行調整可能會導致 WPF 應用程式看似模糊，特別是當調整為非整數時。 為了避免調整 WPF 應用程式，必須將其更新為個別監視器 DPI 感知。

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>每個監視器感知 WPF 範例逐步解說

[每個監視器感知 wpf 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)是更新為個別監視器 DPI 感知的範例 wpf 應用程式。 此範例包含了二個專案：

-   NativeHelpers. .vcxproj：這是原生協助程式專案，它會執行核心功能，讓 WPF 應用程式依照上述 Win32APIs 的個別監視器 DPI 感知。 專案包含兩個類別：
    -   PerMonDPIHelpers：提供與 DPI 相關之作業的 helper 函式的類別，例如抓取作用中監視器的目前 DPI、將進程設定為個別監視器 DPI 感知等等。
    -   PerMonitorDPIWindow：衍生自的基類，它會實作為個別監視器 DPI 感知之 WPF 應用程式 **視窗的功能** 。 根據監視器的 DPI 而非系統 DPI，調整視窗大小、圖形轉譯大小和字型大小。
-   WPFApplication .csproj：使用 PerMonitorDPIWindow (PerMonitorDPIWindow) 的範例 WPF 應用程式，並展示當視窗移至具有不同 DPI 的監視器時，或在顯示控制台中的滑杆用來變更 DPI 時，應用程式視窗和轉譯的大小。

若要執行範例，請遵循下列步驟：

1.  下載並解壓縮 [每個監視器感知 WPF 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
2.  開始 Microsoft Visual Studio，然後選取 [檔案] **> 開啟 > 專案/方案**
3.  流覽至包含解壓縮範例的目錄。 移至為範例命名的目錄，然後按兩下 Visual Studio 方案 ( .sln) 檔
4.  按 F7 或使用 **組建 > 組建方案** 來建立範例
5.  按 Ctrl + F5 或使用 **Debug > 啟動但不進行調試** ，以執行範例

若要查看使用範例中的基類，將已更新為個別監視器 DPI 感知之 WPF 應用程式上變更 DPI 的影響，請將應用程式視窗移至具有不同 Dpi 的顯示。 當視窗在監視器之間移動時，系統會使用 WPF 的可擴充圖形系統（而不是由 OS 調整），根據顯示的 DPI 來更新視窗大小和 UI 縮放比例。 應用程式的 UI 會以原生方式轉譯，且不會變得模糊。 如果您沒有兩個顯示器具有不同的 DPI，請變更 [顯示] 控制台中的滑杆來變更 DPI。 變更滑杆 **並按一下 [** 套用]，將會調整應用程式的視窗大小，並自動更新 UI 規模。

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>使用 WPF 範例中的 helper 專案，將現有的 WPF 應用程式更新為個別監視器 DPI 感知

如果您有現有的 WPF 應用程式，並想要利用範例中的 DPI 協助程式專案，讓它成為 DPI 感知，請遵循下列步驟。

1.  下載並解壓縮每個監視器感知 WPF 範例
2.  開始 Visual Studio，然後選取 [檔案] **> 開啟 > 專案/方案**
3.  流覽至包含現有 WPF 應用程式的目錄，然後按兩下 [Visual Studio 方案 ( .sln) 檔
4.  以滑鼠右鍵按一下 [**方案 > 新增 > 現有專案**] ![ 螢幕擷取畫面，其中顯示 [新增：現有專案] 功能表選取專案](images/scrvs-image1.png)
5.  在 [檔案選取] 對話方塊中，流覽至包含解壓縮範例的目錄。 開啟至範例中名為的目錄，流覽至 "NativeHelpers" 資料夾，選取 Visual C++ 專案檔 "NativeHelpers .vcxproj"，然後按一下 **[確定]** 。
6.  以滑鼠右鍵按一下專案 NativeHelpers，然後選取 [ **建立**]。 這會產生 NativeHelpers.dll，在下一個步驟中將新增為 WPF 應用程式的參考，並在下一個步驟中示範 ![ 建立功能表選取專案](images/scrvs-image2.png)
7.  從您的 WPF 應用程式新增 NativeHelpers.dll 的參考。 展開您的 WPF 應用程式專案，以滑鼠右鍵按一下 [**參考**]，然後按一下 [**加入參考**]。
8.  在產生的對話方塊中，展開 [ **方案** ] 區段。 在 [**專案**] 底下，選取 [NativeHelpers]，然後按一下 **[確定]**， ![ 以螢幕擷取畫面說明資源管理員對話方塊](images/scrvs-image3.png)
9.  展開您的 WPF 應用程式專案，展開 [ **屬性**]，然後開啟 [ **AssemblyInfo**]。 對 AssemblyInfo 進行下列新增專案
    -   使用 System. Media (的參考區段中，新增對 system.string 的參考，) 
    -   將 DisableDpiAwareness 屬性新增 (`[assembly: DisableDpiAwareness]`) 

    ![說明其他屬性的螢幕擷取畫面](images/scrvs-image4.png)
10. 從 PerMonitorDPIWindow 基類繼承主要 WPF 視窗類別
    -   更新主要 WPF 視窗的 .cs 檔案，以繼承自 PerMonitorDPIWindow 基類
        -   藉由新增該行，在參考區段中新增 NativeHelpers 的參考 `using NativeHelpers;`
        -   從 PerMonitorDPIWindow 類別繼承主視窗類別

        ![說明 c + + 參考的螢幕擷取畫面](images/scrvs-image5.png)
    -   更新主要 WPF 視窗的 .xaml 檔案，以繼承自 PerMonitorDPIWindow 基類
        -   藉由新增該行，在參考區段中新增 NativeHelpers 的參考 `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   從 PerMonitorDPIWindow 類別繼承主視窗類別

        ![示範新增 .xaml 參考的螢幕擷取畫面](images/scrvs-image6.png)
11. 按 F7 或使用 **組建 > 組建方案** 來建立範例
12. 按 Ctrl + F5 或使用 **Debug > 啟動但不進行調試** ，以執行範例

[每個監視器感知 wpf 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)應用程式說明如何藉由回應 [**WM \_ DPICHANGED**](wm-dpichanged.md)視窗通知，將 wpf 應用程式更新為每個監視器 DPI 感知。 為了回應視窗通知，此範例會根據視窗所在的目前監視器 DPI，更新 WPF 所使用的縮放轉換。 視窗通知的 *wParam* 會在 *wParam* 中包含新的 DPI。 *LParam* 包含一個矩形，其具有新建議視窗的大小和位置，並針對新的 DPI 進行縮放。

附註：

> [!Note]  
> 由於此範例會覆寫 WPF 視窗之根節點的視窗大小和小數位數轉換，因此應用程式開發人員可能需要進一步的工作（如果有的話）：
>
> -   視窗的大小會影響應用程式的其他部分，例如此 WPF 視窗裝載于另一個應用程式內。
> -   擴充此類別的 WPF 應用程式是在根視覺效果上設定其他轉換;範例可能會覆寫 WPF 應用程式本身所套用的其他轉換。

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>WPF 範例中的 helper 專案總覽

若要讓現有的 WPF 應用程式每個監視器 DPI 感知 DPI 感知 NativeHelpers 程式庫提供下列功能：

-   **將 WPF 應用程式標示為每個 PONITOR DPI 感知：** WPF 應用程式會針對目前的進程呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) ，以標示為個別監視器 DPI 感知。 將應用程式標示為每個監視器 DPI 感知，可確保

    -   當系統 DPI 不符合應用程式視窗目前的監視器 DPI 時，作業系統不會調整應用程式的規模
    -   每當視窗的 DPI 變更時，就會傳送 [**WM \_ DPICHANGED**](wm-dpichanged.md) 訊息

-   **調整視窗維度、重新配置和重新呈現圖形內容，並根據視窗所在的監視器初始 DPI 來選取字型：** 一旦將應用程式標示為個別監視器 DPI 感知，WPF 仍會根據系統 DPI 來調整視窗大小、圖形和字型大小。 在應用程式啟動時，系統 DPI 不保證會與啟動視窗的監視器 DPI 相同，因此在載入視窗時，程式庫會調整這些值。 基底類別 **PerMonitorDPIWindow** 會在 **OnLoaded ()** 處理常式中更新這些。

    變更視窗的 **寬度** 和 **高度** 屬性來更新視窗大小。 配置和大小的更新方式是將適當的縮放轉換套用至 WPF 視窗的根節點。

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

    

-   **回應 WM \_DPICHANGED 視窗通知：** 根據視窗通知中傳遞的 DPI，更新視窗大小、圖形和字型大小。 基底類別 **PerMonitorDPIWindow** 會處理 **HandleMessages ()** 方法中的視窗通知。

    使用在視窗訊息 *lparam* 中傳遞的資訊來呼叫 **SetWindowPos** ，以更新視窗大小。 版面配置和圖形大小的更新方式是將適當的縮放轉換套用至 WPF 視窗的根節點。 縮放比例的計算方式是使用在視窗訊息的 *wparam* 中傳遞的 DPI。

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

    

## <a name="handling-dpi-change-for-assets-like-images"></a>處理資產（例如影像）的 DPI 變更

為了更新圖形內容，範例 WPF 應用程式會將縮放轉換套用至 WPF 應用程式的根節點。 雖然這適用于 WPF 以原生方式轉譯的內容 (矩形、文字等 ) ，這表示點陣圖資產（例如影像）會依 WPF 縮放。

為了避免因縮放所造成的模糊點陣圖，WPF 應用程式開發人員可以撰寫自訂的 DPI 影像控制項，以根據視窗所在的目前監視器 DPI 來選取不同的資產。 當 DPI 變更時，影像控制項可以依賴針對從 **PerMonitorDPIWindow** 取用的 WPF 視窗所引發的 **DPIChanged ()** 事件。

> [!Note]  
> 在 **載入的 ()** WPF 視窗事件處理常式中，影像控制項也應該在應用程式啟動期間，選取正確的控制項。

 

 

 