---
description: XAudio2 用戶端具有從語音通道到每個目的地語音通道的完全控制。
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: XAudio2 預設通道對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d77371223ccef02d6f0831a7aea182326f8477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469516"
---
# <a name="xaudio2-default-channel-mapping"></a>XAudio2 預設通道對應

XAudio2 用戶端具有從語音通道到其每個目的地 voicesIt 的通道的完整控制權，可透過使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 方法來控制對應。 不過，在某些情況下，XAudio2 會自動設定預設的傳送矩陣，以簡化這項工作。 它會使用與聲音音訊頻道相關聯的通道遮罩（如果有的話）來執行這項工作。 通道遮罩是 \_ X3DAudio 和其他地方所定義的喇叭 xxx 位遮罩的組合。 XAudio2 要求通道遮罩必須為0，或將相同數目的位設定為通道數目。

下表顯示 XAudio2 所支援格式的通道遮罩需求和預設值。 

| 格式 | 通道遮罩需求             | 預設遮罩                        | 對應的結構成員                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | 檔案可能包含通道遮罩    | 通道遮罩為0或不存在        | WAVEFORMATEXTENSIBLE. dwChannelMask 或 none (WAVEFORMATEX)  |
| ADPCM  | 檔案不包含通道遮罩 | 一律使用預設通道遮罩 | 無 (ADPCMWAVEFORMAT)                                     |



 

針對 submix 和掌控語音，以及沒有通道遮罩或通道遮罩為0的來源語音，XAudio2 會根據下表來採用預設的喇叭位置。 

| 通道  | 隱含通道位置                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | 一律對應至 FrontLeft，並在兩個喇叭中以完整的 FrontRight， (mono 音效的特殊情況)                  |
| 2         | FrontLeft，FrontRight (基本身歷聲配置)                                                                     |
| 3         | FrontLeft、FrontRight、LowFrequency (2.1 configuration)                                                                |
| 4         | FrontLeft、FrontRight、BackLeft、BackRight (quadraphonic)                                                              |
| 5         | FrontLeft、FrontRight、FrontCenter、SideLeft、SideRight (5.0 configuration)                                            |
| 6         | FrontLeft、FrontRight、FrontCenter、LowFrequency、SideLeft、SideRight (5.1 configuration)  (請參閱下列備註)  |
| 7         | FrontLeft、FrontRight、FrontCenter、LowFrequency、SideLeft、SideRight、BackCenter (6.1 configuration)                  |
| 8         | FrontLeft、FrontRight、FrontCenter、LowFrequency、BackLeft、BackRight、SideLeft、SideRight (7.1 configuration)         |
| 9個以上 |  (一對一的對應沒有隱含的位置)                                                                             |



 

如果音訊圖形中指定的語音配對沒有與來源或目標語音相關聯的喇叭位置 (一個語音有八個以上的頻道) ，則在來源語音使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 方法明確設定傳送矩陣之前，都不會播放語音。 針對任一個聲音呼叫 [**IXAudio2SourceVoice：： Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) 方法將會失敗，直到您這樣做為止。

如果來源語音和目標聲音具有不同的說話者位置數目，而 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 尚未在來源語音上呼叫，則 XAudio2 會將每個來源頻道傳送到最接近的目標喇叭 (或說話者) 可供使用，按比例排列到預期的喇叭。 有兩個特殊案例，預設行為是不同的。

1.  如果來源音訊為 mono，且位於喇叭 \_ 前端 \_ 或沒有定義的位置，則一律會傳送給說話者 \_ \_ 的左側，而如果在 \_ \_ 輸出音訊中，則會直接傳送給講師前方。 如果不存在，則會回復為正常情況。
2.  如果來源和目的地都是6通道，而且位於標準5.1 說話者的任何一項， (Left + Right + Center + Sub + BackL + BackR 或 Left + Right + Center + Sub + SideL + Client-sider-monitoring) ，則通道會透過一個對應到一個。 換句話說，SideLeft/Right 和 BackLeft/Right 被視為同等的。 這是因為這項設置的歷程記錄有混淆。 因此，假設的意圖一律會對應到一個。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[語音](voices.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[**GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
