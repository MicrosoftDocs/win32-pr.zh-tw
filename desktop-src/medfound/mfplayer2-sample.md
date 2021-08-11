---
description: 重要事項已淘汰。
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: MFPlayer2 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ead2df415af1584f34661a0c1d18751350d59bd1a94ac48f41d3bf9dca2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241727"
---
# <a name="mfplayer2-sample"></a>MFPlayer2 範例

> [!IMPORTANT]
> 已取代。 此 API 可能會從 Windows 的未來版本中移除。 應用程式應該使用 [媒體會話](media-session.md) 來播放。

 

示範 [SimplePlay](simpleplay-sample.md) 範例中省略的一些播放功能，例如：

-   尋求
-   速率控制 (向前快轉和倒轉) 
-   音訊音量和靜音控制項
-   影片縮放

下圖顯示這些功能所使用的控制項。

![mfplayer 範例的螢幕擷取畫面 ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a>示範的 Api

此範例示範下列 Api。

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [**IAudioSessionManager**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在[Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
