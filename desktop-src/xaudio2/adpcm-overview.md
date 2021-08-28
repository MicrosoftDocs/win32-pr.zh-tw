---
description: 彈性差異脈衝程式碼 (ADPCM) 是針對 XAudio2 所執行的失真壓縮格式，可提供額外的功能來指定壓縮範例區塊的大小。
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: ADPCM 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1be1155d6d9f5a542b605c497ce28aa34191c0ac129582c18ec4a47b9f510f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962717"
---
# <a name="adpcm-overview"></a>ADPCM 總覽

彈性差異脈衝程式碼 (ADPCM) 是針對 XAudio2 所執行的失真壓縮格式，可提供額外的功能來指定壓縮範例區塊的大小。 使用失真壓縮格式時，某些資料會在壓縮期間改變並遺失。 ADPCM 可達到最高4:1 的壓縮比例。

適用于 XAudio2 的 ADPCM 會提供額外的功能來指定壓縮範例區塊的大小。 ADPCM 可讓音訊設計工具選擇適當的折衷方式，也就是將迴圈點放在) 的大小、品質和解析度 (。

XAudio2 會使用 Microsoft ADPCM 編解碼器的修改版本，以支援提供自訂範例區塊大小所需的擴充資料格式。 基於這個理由，不支援這個 ADPCM 編解碼器版本的音訊引擎無法播放 XAudio2 音訊資料。

> [!Note]  
> 目前，ADPCM 壓縮僅適用于 Windows，包括適用于 Windows 部署的適用遊戲 Studio Express。

 

## <a name="adpcm-encoding"></a>ADPCM 編碼

使用 AdpcmEncode 命令列工具，將音訊資料編碼為 ADPCM。

-   AdpcmEncode

    為了將音訊檔案編碼為 ADPCM 以搭配 XAudio2 使用，請使用 **AdpcmEncode** 命令列工具。

## <a name="adpcm-decoding"></a>ADPCM 解碼

XAudio2 支援 ADPCM 的軟體解碼。

-   XAudio2

    若要在 XAudio2 中使用 ADPCM 編碼的資料，您必須初始化具有 ADPCM 特定值的 **ADPCMWAVEFORMAT** 結構，並在建立來源語音時，將其當作引數傳遞至 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) 。 如需在 XAudio2 中載入和播放音效的範例，請參閱 [如何：使用 XAudio2 播放音效](how-to--play-a-sound-with-xaudio2.md)。

## <a name="samplesperblock"></a>SamplesPerBlock

ADPCM 壓縮的運作方式是將波形分割成區塊，並預測每個區塊內波形取樣的變化。 區塊的大小會以範例來測量。 最小的區塊大小為32個樣本，最高為512個樣本。

較大的區塊可提供較佳的壓縮功能，這會產生較小的檔案大小，但代價是要調整迴圈點的音效品質和解析度。

一般而言，修改 SamplesPerBlock 值會導致這些取捨：



| 如果 SamplesPerBlock .。。      | 檔案壓縮 | 音效品質 | 迴圈點解析 |
|----------------------------|------------------|---------------|-----------------------|
| 將 (增加到最大的 512)   | 增加        | 減少     | 減少             |
| 降低 (到最小的 32)  | 減少        | 增加     | 增加             |



 

## <a name="restrictions"></a>限制

由於 ADPCM 會使用彼此對齊的範例區塊，因此以 ADPCM 壓縮的 wave 可能會在結尾處有未完成的部分區塊。 ADPCM 解碼器會針對這個部分區塊的其餘部分產生無回應，讓 wave 無縫地迴圈。

*SamplesPerBlock* 參數的值會影響您可以用來對齊 wave 資料和迴圈點的解析度。

如果您嘗試將壓縮套用至非對齊的 wave，您將會收到錯誤或警告，取決於是否在任何迴圈播放事件中使用 wave。 您無法壓縮任何迴圈播放事件中所使用的 wave。 將它從迴圈播放事件中移除，然後重新套用壓縮。

如果您在非迴圈模式中以獨佔方式使用 wave，則不適用範例區塊對齊限制。

## <a name="adpcm-file-structure"></a>ADPCM 檔案結構

ADPCM 檔案是具有下列區塊類型的標準 RIFF 檔。



| 區塊 FCC     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | 標準 RIFF 區塊包含檔案類型，其資料區段的前四個位元組中的值為 WAVE，以及其資料區段其餘部分中檔案的其他區塊。                                                                                                                                                                                                                                                                 |
| Fmt           | 包含 ADPCM 檔案的格式標頭。 這個區塊中的資料會對應至 **ADPCMWAVEFORMAT** 結構。                                                                                                                                                                                                                                                                                                                             |
| data          | 包含編碼的 ADPCM 音訊資料。 當您在 XAudio2 中使用 ADPCM 時，您需要將資料區塊的內容讀取至緩衝區，並將其傳遞至來源聲音，作為 [**XAudio2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構的 **pAudioData** 成員。 您不需要位元組交換資料區塊的內容。                                                                                                                            |
| smpl 和 wsmp | 選用的區塊類型，包含 ADPCM 檔案的迴圈資訊。 當您在 XAudio2 中使用 ADPCM 時，smpl 或 wsmp 區塊中包含的值會用來填入 [**LoopBeginLoopLength \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構的 **LoopCount** 和 **XAudio2** 成員。 在 Xbox 360 上，您必須以位元組交換從 smpl 區塊載入的資料，以考慮 Windows 和 Xbox 360 之間的位元組順序差異。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計指南](programming-guide.md)
</dt> </dl>

 

 
