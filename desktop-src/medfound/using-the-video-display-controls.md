---
description: 使用影片顯示控制項
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: 使用影片顯示控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691591"
---
# <a name="using-the-video-display-controls"></a>使用影片顯示控制項

[**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)介面可控制增強型影片轉譯器 (EVR) 在應用程式視窗內顯示影片。 此介面可用於 DirectShow 或媒體基礎。 就內部而言，影片顯示控制項是由 EVR 的預設展示者所提供。 如果您撰寫自訂的簡報者，就可以提供相同的介面或定義自訂介面。

取得 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面指標的正確方式，取決於您使用的是 EVR 的 DirectShow 版本或媒體基礎版本。 針對媒體基礎 EVR，它也取決於您是直接使用 EVR，還是透過媒體會話使用它， (這是較常見的) 。

若要取得 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面的指標，請執行下列動作：

1.  取得 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面的指標。

    -   如果您使用的是 DirectShow EVR 篩選器，請在篩選器上呼叫 **QueryInterface** 。

    -   如果您直接使用 EVR 媒體接收，請在媒體接收器上呼叫 **QueryInterface** 。

    -   如果您使用媒體會話，請呼叫媒體會話上的 **QueryInterface** 。

2.  如果您使用媒體會話，請等候媒體會話傳送 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件，其狀態值為 [已就緒的 MF TOPOSTATUS] \_ \_ 。  (略過此步驟，否則請 ) 

3.  呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面。 服務識別碼是 MR \_ 影片轉譯 \_ \_ 服務。

您可以使用 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面來執行下列工作：

-   設定裁剪視窗。

-   設定來源和目的地矩形。

-   更新影片視窗以回應視窗訊息。

-   啟用或停用全螢幕模式。

## <a name="clipping-window"></a>裁剪視窗

應用程式必須提供 EVR 繪製影片的視窗。 若要設定裁剪視窗，請以應用程式視窗的控制碼呼叫 [**IMFVideoDisplayControl：： SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) 。

如果您透過其啟用物件建立 EVR 媒體接收，則不需要執行此步驟。 啟用物件會使用您在 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)函數中提供的視窗控制碼，自動呼叫 [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow)。

## <a name="source-and-destination-rectangles"></a>來源和目的地矩形

在播放期間，展示者會取得局部影片影像的一部分，並將其繪製至影片視窗的區域。 複合影像的部分是 *來源矩形*，而影片視窗的區域是 *目的地矩形*。

來源矩形是使用標準化座標定義的，其中 point (0.0、0.0) 對應至影片的左上角，而 (1.0，1.0) 對應到影片的右下角。 來源矩形可以是此矩形內的任何區域。 相對於視窗的工作區，目的矩形會以圖元為單位來指定。 預設的來源矩形是整個影像，而預設的目的地矩形是空的矩形。

若要設定來源和目的地矩形，請呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)。

如果您透過其啟用物件建立 EVR 媒體接收，則不需要執行此步驟。 啟用物件會自動將目的地矩形設定為等於視窗的整個工作區。 但是，如果您想要變更來源矩形或設定不同的目的地矩形，您應該呼叫 [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) 。

## <a name="window-messages"></a>視窗訊息

在播放期間，您的應用程式應該回應特定的視窗訊息，如下所示：

-   WM \_ 油漆：呼叫 [**IMFVideoDisplayControl：： RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) 來重新繪製影片。 此外，請避免在播放影片時，在目的地矩形上進行繪製，因為這可能會導致閃爍。

-   WM \_ 大小：您可能需要呼叫 [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) 來調整目的地矩形的大小。

不同于視頻混合轉譯器 (VMR 中) 篩選器，當您收到 WM DISPLAYCHANGE 訊息時，不需要通知 EVR \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> </dl>

 

 



