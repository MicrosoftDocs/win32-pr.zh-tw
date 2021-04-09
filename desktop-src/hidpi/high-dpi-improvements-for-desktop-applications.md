---
title: Mixed-Mode DPI 縮放比例和 DPI 感知 Api
description: .
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9f8a8f72b199aaba195002134855155925b30d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933106"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode DPI 縮放比例和 DPI 感知 Api

## <a name="sub-process-dpi-awareness-support"></a>Sub-Process DPI 感知支援

[**SetThreadDpiAwarenessCoNtext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) 可讓您在單一進程中使用不同的 DPI 縮放模式。 在 Windows 10 年度更新版之前，會將視窗的 DPI 感知系結至整個進程的 DPI 感知模式， (DPI 感知、系統 DPI 感知，或 Per-Monitor DPI 感知) 。 但現在，使用 **SetThreadDpiAwarenessCoNtext** 時，最上層的 windows 可以有與整個進程的 DPI 感知模式不同的 DPI 感知模式。 這也會影響子視窗，因為它們一律具有與父視窗相同的 DPI 感知模式。

使用 **SetThreadDpiAwarenessCoNtext** 可讓開發人員在針對桌面應用程式定義 DPI 特定的行為時，決定他們要將其開發工作放在哪裡。 例如，應用程式的主要最上層視窗可根據個別監視器進行調整，而次要最上層視窗則可透過由作業系統進行點陣圖調整來調整。

## <a name="the-dpi-awareness-context"></a>DPI 感知內容

在 **SetThreadDpiAwarenessCoNtext** 可用性之前，進程的 DPI 感知定義在應用程式二進位檔的資訊清單中，或在進程初始化期間透過呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) 。 使用 **SetThreadDpiAwarenessCoNtext** 時，每個執行緒可以有個別的 DPI 感知內容，這可能會與整個進程的 DPI 感知模式不同。 執行緒的 DPI 感知內容會以 [* * * * DPI \_ 感知 \_ 內容 * *](dpi-awareness-context.md) * 類型表示，並以下列方式運作：

-   執行緒可以隨時變更其 DPI 感知內容。
-   在內容變更之後所做的任何 API 呼叫，將會在對應的 DPI 內容中執行 (且可能會虛擬化) 。
-   建立視窗時，會在該時間將其 DPI 感知定義為呼叫執行緒的 DPI 感知。
-   當呼叫視窗的視窗程式時，執行緒會自動切換至建立視窗時所使用的 DPI 感知內容。

使用 **SetThreadDpiAwarenessCoNtext** 的常見案例如下：從以一個 (內容執行的執行緒開始，例如， **\_ \_ \_ 每個 \_ 監視器可 \_ 感知 DPI 感知內容**) 暫時切換到不同的內容 (**DPI \_ 感知內容不 \_ \_ 知道**) 、建立視窗，然後立即將執行緒內容切換回先前的狀態。 建立的視窗將會有不 **\_ 感知 DPI 感知 \_ 內容 \_** 的 DPI 內容，而呼叫執行緒的內容將會還原為 **\_ \_ \_ 每個 \_ 監視器 \_ 的 DPI 感知內容** ，並可感知後續的 **SetThreadDpiAwarenessCoNtext** 呼叫。 在此案例中，與呼叫執行緒相關聯的視窗會以每個監視器的內容執行 (而不是由作業系統) 的點陣圖延伸，而新建立的視窗則不會 (感知 DPI，因此會自動將顯示集上的點陣圖擴充為 >100% 縮放) 。

圖1說明如何使用 **\_ \_ \_ 每個 \_ 監視器的 DPI 感知內容** 來執行主要進程執行緒，將其內容切換至不 **感知的 DPI \_ 感知 \_ 內容 \_**，然後建立新的視窗。 然後，新建立的視窗就會在每次有訊息分派給它或從它發出 API 呼叫時，以 **DPI \_ 感知 \_ 內容 \_** 的 DPI 感知內容執行。 在建立新視窗之後，就會在建立新視窗之後，將主要執行緒還原至其先前的 **DPI \_ 感知內容內容（ \_ \_ 每個 \_ 監視器**）。

![顯示每個監視器 DPI 感知運作方式的圖表](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>新的 DPI 相關 Api

除了在 **SetThreadDpiAwarenessCoNtext** 提供的單一進程內支援不同的 DPI 感知模式之外，還為桌面應用程式新增了下列 DPI 特定功能：<dl> <dd>[EnableNonClientDpiScaling****](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> 個別 **監視器 V2** DPI 感知模式會自動啟用這項功能，因此使用它的應用程式不需要呼叫 **EnableNonClientDpiScaling** 。

 

從視窗 s **WM \_ NCCREATE** 處理常式內呼叫 **EnableNonClientDpiScaling** ，會導致最上層視窗的非工作區自動針對 DPI 進行調整。 如果最上層視窗是個別監視器 DPI 感知的 (，是因為進程本身是個別監視器 DPI 感知，還是在每個監視器 DPI 感知執行緒內建立的視窗) ，則每當視窗的 DPI 變更時，這些視窗的標題列、捲軸、功能表和功能表列都將會進行 DPI 縮放。
</dt> <dt>

請注意，使用此 API 時，子視窗的非用戶端區域（例如子編輯控制項的非用戶端捲軸）將不會自動調整 DPI。
</dt> <dt>

> [!Note]  
> 您必須從 **WM \_ NCCREATE** 處理常式呼叫 **EnableNonClientDpiScaling** 。

</dt> </dl> </dd> <dd> <b> * ForDpi Api </b>

-   數個經常使用的 Api （例如 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) ）沒有 HWND 的任何內容，因此無法針對其傳回值推算出適當的 DPI 感知。 從不同 DPI 感知模式或內容中執行的執行緒呼叫這些 Api，可能會傳回未針對呼叫執行緒內容進行調整的值。 [* * * * GetSystemMetricForDpi * *](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)* *、 [* * * * SystemParametersInfoForDpi * *](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)* 和 * * * * [AdjustWindowRectExForDpi *](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
-   **GetSystemMetricForDpi** 和 **SystemParametersInfoForDpi** 將會根據此方程式傳回 DPI 縮放的系統度量值和系統參數值：

    |                                                                 |
    |-----------------------------------------------------------------|
    | GetSystemMetrics ( ... ) @ DPI = = GetSystemMetricsForDpi ( ...，DPI)  |

    

     

    因此，在具有特定系統 DPI 值的裝置上執行時，呼叫 **GetSystemMetrics** (或 **SystemParametersInfoForDpi**) 將會傳回與其 Dpi 感知變異 (**GetSystemMetricsForDpi** 和 **SystemParametersInfoForDpi**) 相同的值，並提供與輸入相同的 DPI 值。

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) 會採用 HWND，並以 DPI 敏感性的方式計算視窗矩形所需的大小。

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow</b>會傳回與提供之 HWND 相關聯的 DPI。 答案將取決於 HWND 的 DPI 感知模式：

| HWND 的 DPI 感知模式 | 傳回值                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 知道                    | 96                                                                                                                                                                                                            |
| 系統                     | 系統 DPI                                                                                                                                                                                                |
| Per-Monitor                | 相關聯的最上層視窗的顯示 DPI，主要位於 <br/>  (如果提供子視窗，則會傳回對應最上層父視窗的 DPI) <br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

呼叫 **GetDpiForSystem** 比呼叫 [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) 和 [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) 來取得系統 DPI 更有效率。
</dt> <dt>

任何可能在使用子進程 DPI 感知的應用程式中執行的元件，都不應該假設在進程生命週期期間，系統 DPI 是靜態的。 例如，如果在 **DPI \_ 感知 \_ 內容 \_** 感知感知內容下執行的執行緒會查詢系統 DPI，則答案會是96。 但是，如果該相同執行緒切換至 **DPI \_ 感知 \_ 內容 \_ 系統** 感知內容，並重新查詢系統 DPI，則答案可能會不同。 若要避免使用快取的 (且可能過時) 系統 DPI 值，請使用 **GetDpiForSystem** 來抓取相對於呼叫執行緒之 DPI 感知模式的系統 DPI。 
</dt> </dl> </dd> </dl>