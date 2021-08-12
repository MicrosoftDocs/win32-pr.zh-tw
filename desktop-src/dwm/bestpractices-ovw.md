---
title: 效能考慮和最佳作法
description: 本主題提供一組使用桌面視窗管理員 (DWM) Api 的最佳做法。
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- 桌面視窗管理員 (DWM) 、最佳作法
- DWM (桌面視窗管理員) 、最佳作法
- 桌面視窗管理員 (DWM) 、應用程式實務
- DWM (桌面視窗管理員) ，應用程式實務
- 桌面視窗管理員 (DWM) 、繪圖實務
- DWM (桌面視窗管理員) 、繪製實務
- 桌面視窗管理員 (DWM) ，模糊背後效果
- DWM (桌面視窗管理員) ，模糊背後效果
- 應用程式實務
- 繪圖實務
- 模糊背後效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7affbbf5ebca91a4e5172e75f88da4b9fe8e33f6e1e3de1e7a735add816a313f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280271"
---
# <a name="performance-considerations-and-best-practices"></a>效能考慮和最佳作法

本主題提供一組使用桌面視窗管理員 (DWM) Api 的最佳做法。

本主題包含下列幾節：

-   [DWM 的應用程式實務](#application-practices-for-dwm)
-   [DWM 的繪圖實務](#drawing-practices-for-dwm)
-   [DWM Blur-Behind 用戶端區域](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>DWM 的應用程式實務

如果您的應用程式處理每英寸的點 (DPI) 調整，您可以將應用程式宣告為 DPI 感知並防止自動調整，方法是在程式的資訊清單中設定 DPI 感知旗標，或在程式初始化期間呼叫 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函式。

開啟了 DWM 組合之後，隱藏的應用程式就不會再收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，也不會被要求重新呈現。 每個視窗的內容都已經可用來撰寫螢幕影像。

最上層的 [**WS \_ ex \_ 透明**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 視窗應該結合 **WS \_ ex \_ 分層** 樣式來進行點擊測試。 **WS \_例如 \_ ，在傳統** 上，沒有重新導向的一般情況下，適用于屬於相同執行緒的 windows 階層中的子視窗，但不適合最上層視窗。

使用區域或分層來建立成形或混合式視窗。 請注意，在 Windows Vista 和更新版本的 Windows 中，自訂繪圖只是最上層視窗的一部分，並不會在 undrawn 區域中提供所需的過時內容。

您可以使用 [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) 之類的 api 來判斷特定的實際值。 如果您在重新導向的視窗中有 (DC) 的裝置內容， **GetDCOrgEx** 所傳回的原始來源將不會與畫面上視窗的原點相符。 來源會改為視窗的後置緩衝區介面： (0，0) 。

當所有其他動作都失敗時，藉由呼叫 [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) 函數來停用視窗轉譯。

## <a name="drawing-practices-for-dwm"></a>DWM 的繪圖實務

避免直接繪製至主要顯示介面。 這麼做會強制 DWM 停用組合，直到您的應用程式放開主要裝置介面為止。

評估您的應用程式是否必須提供自己的雙重緩衝。 DWM 會有效地雙重緩衝內容，並將視窗呈現在單一框架中。

避免讀取或寫入至顯示 DC。 雖然 DWM 支援，但因為效能降低，所以不建議使用。

避免在非工作區中繪圖。 雖然此區域可以由應用程式存取，而 Microsoft WIN32 API 也支援繪圖，但是這樣做可能會導致視窗遺失任何半透明框線。

避免混合 Windows 圖形裝置介面 (GDI) 和 Microsoft DirectX，除非它們不重迭。 如果需要混合，請將 GDI 內容繪製到 DirectX 軟體介面，並在組合到畫面之前將其合併，或在不同的視窗中繪製。

使用 [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)或 [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt)函式，而不是 Windows GDI+ 來呈現要轉譯的繪圖。 GDI+ 使用軟體轉譯一次轉譯一個掃描行。 這可能會導致您的應用程式發生閃爍。

## <a name="dwm-blur-behind-client-region"></a>DWM Blur-Behind 用戶端區域

轉譯模糊後變效果是 CPU 和圖形處理器 (GPU) 的大量資源操作。 應用程式開發人員呼籲考慮使用用戶端區域模糊的含意，讓它不會消耗過多的資源。 在下列情況下，請特別注意：

-   當您預期用戶端區域模糊的大小變得很明顯，即使沒有任何更新會出現在模糊的區域內也是一樣。 如果在視窗的模糊區域下發生任何更新，就必須轉譯模糊，以產生 CPU 和 GPU 成本。 此外，視窗的視窗作業 (移動/調整大小/轉換) 會產生更多成本。
-   當您預期模糊的用戶端區域有重大更新時。 這將需要在每次更新時重新繪製模糊，並耗用過度的資源。
-   如果模糊預期會涵蓋重要區域，而且也預期會有該區域的更新，強烈建議您不要模糊工作區。

 

 