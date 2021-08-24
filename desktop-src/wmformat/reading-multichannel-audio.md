---
title: 讀取多頻道音訊
description: 讀取多頻道音訊
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows媒體格式 SDK，讀取多頻道音訊
- Advanced Systems Format (ASF) 、讀取多頻道音訊
- ASF (Advanced Systems Format) ，讀取多頻道音訊
- Advanced Systems Format (ASF) 、多頻道音訊
- ASF (Advanced Systems Format) 、多頻道音訊
- 編解碼器，讀取多頻道音訊
- 多頻道音訊，讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ba314c6f2579bb18cd73593a775089c4b04b1c4a8ecd34868af911da29a67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658528"
---
# <a name="reading-multichannel-audio"></a>讀取多頻道音訊

Windows Media 音訊 9 Professional 編解碼器可將多頻道音訊編碼 (兩個以上的通道) 。 使用多頻道音訊讀取檔案時，您必須正確地設定輸出，否則音訊會以較低的品質和身歷聲傳遞。 若要設定多頻道音訊傳遞的輸出，您必須設定兩個輸出設定： g \_ wszEnableDiscreteOutput 和 g \_ wszSpeakerConfig。

將 g \_ wszEnableDiscreteOutput 設為 **TRUE** ，會設定編解碼器以傳遞高定義音訊輸出。 高定義音訊是由 Windows Media 音訊9編解碼器，以身歷聲或多個通道中的24位樣本進行編碼。 如果此設定為 **FALSE**，則只會傳遞16位的身歷聲輸出。

播放電腦上的喇叭數目設定為 g \_ wszSpeakerConfig。 這項設定是設定為下表所列的其中一個 DirectSound 喇叭常數的 **DWORD** 值。 若要為您的編譯器解析這些常數名稱，您必須包含 dsound。



| 常數             | 值      | 描述                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | 系統會直接傳遞音訊，而不是針對喇叭進行設定。 |
| DSSPEAKER \_ 耳機 | 0x00000001 | 用戶端電腦配備耳機。                             |
| DSSPEAKER \_ MONO      | 0x00000002 | 用戶端電腦配備了 monaural 喇叭。                     |
| DSSPEAKER \_ 四      | 0x00000003 | 用戶端電腦配備了 quadraphonic 喇叭。                  |
| DSSPEAKER \_ 身歷聲    | 0x00000004 | 用戶端電腦配備了身歷聲喇叭。                        |
| DSSPEAKER \_ 環繞  | 0x00000005 | 用戶端電腦配備四個聲道的環繞音效喇叭。   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | 用戶端電腦配備了五個喇叭和一個喇叭。          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | 用戶端電腦配備了七個喇叭和一個喇叭。         |



 

若要設定這些設定，請使用 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)。

最後，若要讓通道成為輸出分開，而不將任何折迭到身歷聲，您必須遵循下列步驟，在輸出上設定正確的媒體類型：

1.  呼叫 [**IWMReader：： GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) 可取得相關音訊輸出的支援格式數目。 輸出格式索引是以零為基底。
2.  針對每個支援的格式，呼叫 [**IWMReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) ，以取出輸出媒體屬性物件上的 [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) 介面。
3.  呼叫 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) 來取得媒體類型。
4.  如果取出的媒體類型是所需的多重通道類型，請呼叫 [**IWMReader：： SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops)來設定它。

設定離散輸出和說話者設定之後，讀取器列舉的輸出格式應包含使用 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) 結構的多重通道格式。 如果您在設定屬性之前列舉輸出格式，則只會包含1或2個通道的格式，且每個通道最多可包含16個位。 與其他音訊格式一樣，您應該只使用讀取器列舉的格式;請勿設定您自己的。

> [!Note]  
> 只有當您的應用程式是在 microsoft Windows XP 或更新版本的 microsoft Windows 上執行時，才可以輸出多頻道音訊。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**輸入、串流和輸出**](inputs-streams-and-outputs.md)
</dt> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> <dt>

[**輸出設定**](output-settings.md)
</dt> <dt>

[**使用 High-Resolution PCM 音訊**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 