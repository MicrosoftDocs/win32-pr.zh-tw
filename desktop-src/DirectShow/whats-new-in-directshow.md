---
description: DirectShow 的新功能
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: DirectShow 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd05d11931d7c23a078643724b99dfed84b65e3a7db3e4ed60df9cd2a3273f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071882"
---
# <a name="whats-new-in-directshow"></a>DirectShow 的新功能

## <a name="whats-new-for-directshow-in-windows-7"></a>Windows 7 DirectShow 的新功能

新介面：

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

新的或更新的篩選：

-   [**Microsoft MPEG-1/DD/AAC 音訊解碼器**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Microsoft MPEG-2 影片解碼**](microsoft-mpeg-2-video-decoder.md)

"智慧型 connect" 演算法已經過修改，可支援慣用和封鎖的篩選。 如需詳細資訊，請參閱[智慧型連線](intelligent-connect.md)。

DVD 播放： [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) 方法的新選項。

## <a name="whats-new-for-directshow-in-windows-vista"></a>Windows Vista DirectShow 的新功能

-   DirectShow 現在是 Windows SDK 的一部分。 DirectShow 的標頭、程式庫、範例和工具不再包含于 DirectX SDK 中。
-   DirectX Video 加速 (DXVA) 2.0 包含許多來自 DXVA 1.0 的增強功能。

    -   硬體視頻管線已大幅改進。
    -   例如，您可以直接存取 DXVA 2.0 的元件，而不需要透過影片轉譯器進行通訊。
    -   Direct3D 裝置管理員可讓元件共用相同的 Direct3D 裝置。

    如需 DXVA 2.0 的詳細資訊，請參閱 [DirectX Video 加速 2.0](../medfound/directx-video-acceleration-2-0.md) 檔，這是 [Microsoft 媒體基礎](../medfound/microsoft-media-foundation-sdk.md) 檔的一部分。

-   [**增強型影片**](enhanced-video-renderer-filter.md)轉譯器 (EVR) 是一種功能強大的新影片轉譯器，它會與媒體基礎版本的 EVR 共用相同的外掛程式模型。 如需 EVR 的詳細資訊，請參閱 [Microsoft 媒體基礎](../medfound/microsoft-media-foundation-sdk.md) 檔。
-   支援 Windows Vista 顯示驅動程式模型 (WDDM) capture。 這項功能可讓篩選器充分利用視訊卡與整合式影片捕獲，減少影片記憶體和系統記憶體之間的不必要複本。 如需詳細資訊，請參閱[在 DirectShow 中使用 WDDM Capture](using-wddm-capture-in-directshow.md)。
-   MPEG-2 圖層 II 音訊解碼器現在使用浮點算術，以改善解碼品質。
-   DVD 播放的增強功能。 如需詳細資訊，請參閱[Windows Vista 中的 DVD 播放增強功能](dvd-playback-enhancements-in-windows-vista.md)。
    -   更好的訣竅模式支援：在速率之間進行平滑轉換;向前與反向播放之間的轉換;支援向前快轉和反向播放音訊。
    -   增強的快取。 應用程式可以設定 DVD 導覽器預先讀取的資料量。 設定較大的快取可以延長電池壽命，並在磁片磁碟機) 關閉之後 (啟用無訊息播放。 如需詳細資訊，請參閱 [**DVD \_ 選項 \_ 旗**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag)標。
-   音訊端點裝置：應用程式可以將 DirectSound 轉譯 [器篩選器](directsound-renderer-filter.md) 與特定的音訊端點裝置產生關聯。 應用程式可以使用多媒體裝置 (MMDevice) API 來列舉和選取端點裝置。 如需詳細資訊，請參閱 Windows SDK 中的核心音訊 API 檔。
-   下列篩選器已從 Windows Vista 中移除：
    -   [BDA IP 接收篩選器](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [BDA 單 Deframer 篩選](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [CC 解碼篩選](cc-decoder-filter.md)
    -   [NABTS/FEC VBI 編解碼器篩選](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [QT 解壓縮程式篩選器](qt-decompressor-filter.md)
    -   [QuickTime 影片剖析器篩選](quicktime-movie-parser-filter.md)
    -   [WST 編解碼器篩選](wst-codec-filter.md)
    -   [WST 解碼篩選](wst-decoder-filter.md)
-   許多 DirectShow 介面的 proxy/stub 程式碼已從 quartz.dll 移至 proppage.dll。 這段程式碼已從 quartz.dll 中移除，因為它不適合應用程式使用。 不過，它很適合用於偵錯工具，因為它可讓測試應用程式從遠端連線到另一個進程中的 DirectShow 篩選圖形。 若要在 Windows Vista 中使用這項功能，您必須先註冊 proppage.dll。 此 DLL 可在 Windows SDK tools 目錄中取得。  (需詳細資訊，請參閱[從外部進程載入 Graph](loading-a-graph-from-an-external-process.md)。 ) 

 

 
