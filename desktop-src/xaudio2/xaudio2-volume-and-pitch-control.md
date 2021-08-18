---
description: 本主題說明 XAudio2 音量和音調控制。
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: XAudio2 音量和音調控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6376ad599b496a640b49d7eb539e1da774e31c71a3bf2a8e0c863fc140e19b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962487"
---
# <a name="xaudio2-volume-and-pitch-control"></a>XAudio2 音量和音調控制

本主題說明 XAudio2 音量和音調控制。

## <a name="volume-control"></a>音量控制

磁片區層級會表示為-XAUDIO2 \_ max \_ 磁片區 \_ 層級與 XAUDIO2 max 磁片區層級之間的浮點振幅， \_ \_ \_ (-224 到 224) ，最大增益為 144.5 dB。 磁片區1.0 表示沒有衰減或增益;0表示無聲;和負數層級可以用來將音訊的階段反轉。 XAudio2 中提供兩個內嵌函數以在磁片區單位之間轉換： [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) 和 [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)。

當音訊流經 XAudio2 圖時，您可以在數個點將磁片區層級套用至音訊：

-   所有語音類型都會將整體磁片區層級套用至其輸入，其會使用 [**IXAudio2Voice：： SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) 方法來控制。 在 submix 和掌控語音中，整體音量層級會在語音的內建篩選和效果鏈之前套用。 在來源語音中，整體音量層級會在語音的內建篩選和效果鏈之後套用。
-   語音會將每個通道的磁片區層級套用至其輸出，其會使用 [**IXAudio2Voice：： SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) 方法來控制它們。 每個頻道的音量層級會在語音的最終取樣率轉換之後，以及傳送到其他語音之前套用。
-   每個語音之間的每個連線都有一份層級表格，可用來從每個來源頻道將音訊傳送至每個目標通道（使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 方法來控制）。

所有的整體磁片區和通道磁片區一開始都會預設為1.0。 所有的傳送層級矩陣都會預設為適當的值，以盡可能精確地保留信號電源和通道定位。 如需詳細資訊，請參閱 [XAudio2 預設通道對應](xaudio2-default-channel-mapping.md) 總覽。

> [!Note]  
> XAudio2 會根據使用者的說話者設定自動調整音量層級，以維持一致的磁片區層級之間的設定。 如果使用者的設定不符合其實體設定，則磁片區會太遠或太過軟，相較于具有正確設定的系統。 例如，針對5.1 設定的系統會將只有兩個喇叭連線的音效喇叭設為不太軟。 XAudio2 無法偵測使用者說話者設定是否正確地符合其實體安裝。

 

## <a name="pitch-control"></a>音調控制項

簡報會表示為輸入速率/輸出速率比例，介於 1/1024 與 1024/1 （含）之間。 1/1024 的比率會減少 10 octaves，而 1024/1 的比率則會引發 10 octaves。 您只能使用 [**IXAudio2SourceVoice：： SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 方法，將音調調整套用至來源語音，而且只有在不是使用 XAUDIO2 \_ VOICE NOPITCH 旗標建立時 \_ 。 預設頻率比例為1/1：也就是不會有任何間距變更。 XAudio2 中提供兩個內嵌函式，以便在頻率比例和 semitones： [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) 和 [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)之間進行轉換。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音量和音調控制項](volume-and-pitch-control.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[如何：變更聲音音調](how-to--change-voice-pitch.md)
</dt> <dt>

[如何：變更聲音音量](how-to--change-voice-volume.md)
</dt> </dl>

 

 
