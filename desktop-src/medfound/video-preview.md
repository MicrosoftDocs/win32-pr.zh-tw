---
description: 本主題說明如何使用 MFPlay 來預覽攝影機的影片。
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: 影片預覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974158"
---
# <a name="video-preview"></a>影片預覽

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

本主題說明如何使用 MFPlay 來預覽攝影機的影片。

MFPlay 提供最簡單的方式，讓您從「捕獲裝置」 Microsoft 媒體基礎預覽影片。 如果下列條件都成立，則應該使用 MFPlay：

-   您不需要將影片捕獲到檔案。
-   您不需要對影片的呈現方式進行細微的控制。  (例如，您不需要控制建立 Direct3D 裝置。 ) 
-   在轉譯之前，您不需要處理相機的影片資料。

否則， [來源讀取器](source-reader.md) 可能會是更好的選項。

若要使用 MFPlay 搭配影片捕獲裝置，請執行下列步驟：

1.  建立 capture 裝置的媒體來源。 請參閱 [列舉影片捕獲裝置](enumerating-video-capture-devices.md)。
2.  呼叫 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 來建立 player 物件的實例。
3.  呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) 方法。 將指標傳入媒體來源的 IMFMediaSource 介面。 方法會接收指向 [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) 介面的指標。
4.  呼叫 [**IMFPMediaPlayer：： SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem)。
5.  呼叫 [**IMFPMediaPlayer：:P 版面**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) 配置以開始預覽。

下列程式碼顯示這些步驟：


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



在一般應用程式中，您會在 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 函式中提供回呼介面的指標，並使用回呼介面從播放程式取得事件。 為了簡單起見，此處所示的程式碼會略過這些步驟。 如需詳細資訊，請參閱 [使用 MFPlay 開始使用](getting-started-with-mfplay.md)。

### <a name="shutting-down"></a>關閉

在應用程式結束之前，請關閉媒體來源和 player 物件，如下所示：

1.  呼叫媒體來源上的 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 。
2.  呼叫 player 物件上的 [**IMFPMediaPlayer：： Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) 。


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MFPlay](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[影片捕獲](audio-video-capture.md)
</dt> </dl>

 

 



