---
description: DVD 篩選 Graph 設定
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: DVD 篩選 Graph 設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece69f77ac4a4e6674bbcd12404a10b7f765a514e18cb31963d2ed7f981799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653080"
---
# <a name="dvd-filter-graph-configuration"></a>DVD 篩選 Graph 設定

本節說明 DirectShow 中 DVD 播放的各種篩選圖形設定。 這些圖表主要是供參考之用。 DVD 導覽器會建立圖形，因此通常不需要瞭解如何設定圖形的詳細資料。 如需詳細資訊，請參閱[建立 DVD 篩選器 Graph](building-the-dvd-filter-graph.md)。

下圖顯示具有軟體解碼器的 DVD 篩選圖形。

![適用于 windows xp 的 dvd 篩選圖形](images/dvd-graph-xp.png)

當硬體解碼存在時，通常會透過影片埠直接連接到視訊卡。 這可讓已解碼的影片位直接傳送到圖形配接器上的框架緩衝區，而不會傳入主機記憶體。 若要在舊版 Windows 上管理此直接連線，DirectShow 透過重迭[Mixer 篩選器](overlay-mixer-filter.md)上的介面，支援 DirectDraw 的視訊連接埠延伸 (VPE) 。

> [!Note]  
> 覆迭 Mixer 現在已被取代。

 

在 Windows XP 及更新版本中，硬體解碼器可以連線到[視訊連接埠管理員](video-port-manager.md)篩選器。

![具有硬體解碼的 windows xp dvd graph](images/dvd-hwgraph-xp.png)

在所有這些圖形中，DVD 導覽器是來源篩選;它會執行幾項工作：

-   從光碟讀取導覽和影片資料。
-   將影片、音訊和子圖片資料 Demultiplexes 至不同的串流。
-   將資料流程提取到圖形中，以進行進一步的處理和最終呈現。
-   通知您應用程式 DVD 相關事件。

在音訊串流中，DVD 導覽器會連線到音訊解碼器，以連接到 DirectSound 轉譯 [器篩選器](directsound-renderer-filter.md)，也就是預設的音訊轉譯器。 在影片和子圖片串流上，下游篩選器為協力廠商的影片解碼，而影片混合轉譯器 (或重迭[Mixer](overlay-mixer-filter.md)，以及繼承應用程式) 的[影片](video-renderer-filter.md)轉譯器。 如果您的應用程式將處理第21行的已關閉標題資料，您必須將 DirectShow 行21解碼器2篩選器新增至圖形。 這牽涉到單一方法呼叫;篩選器會自動連接。

您的應用程式會透過 DVD 導覽器所公開的自訂介面，與 DVD 導覽器進行通訊及控制： [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)-"set" 方法（以及 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)） "get" 方法。 它也必須透過 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) 與篩選 graph 管理員 (進行通訊，以停止、啟動及控制圖形。 您可能也需要控制其他個別篩選器，例如覆迭 Mixer 篩選，以便在視窗間和全螢幕顯示之間切換。 如需詳細資訊，請參閱 [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2)。 圖形的確切設定取決於您已安裝的 MPEG-2 解碼器類型、是否需要處理第21行的已隱藏標題資料，以及其他因素。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



