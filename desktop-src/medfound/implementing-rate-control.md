---
description: 本主題說明自訂管線物件如何支援可變的播放率，包括反向播放。 如需從應用程式使用速率控制的詳細資訊，請參閱速率控制。
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: 執行速率控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5fd78cbbb95316a0d4ed12a50c9d3aa8954fe8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027134"
---
# <a name="implementing-rate-control"></a>執行速率控制

本主題說明自訂管線物件如何支援可變的播放率，包括反向播放。 如需從應用程式使用速率控制的詳細資訊，請參閱 [速率控制](rate-control.md)。

本主題包含下列幾節：

-   [媒體來源](#media-sources)
-   [媒體基礎轉換](#media-foundation-transforms)
    -   [反向播放](#reverse-playback)
-   [媒體接收器](#media-sinks)
-   [相關主題](#related-topics)

如果您要 (媒體來源、轉換或媒體接收) 來撰寫 Microsoft 媒體基礎管線物件，您可能需要支援變數播放速率。 若要這樣做，請執行下列介面：

1.  執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。
2.  支援 **MF \_ 速率 \_ 控制 \_ 服務** 服務。  (查看 [服務介面](service-interfaces.md)。 ) 
3.  執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 介面，以取得物件所支援的播放速率。
4.  執行可取得或設定播放速率的 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。

## <a name="media-sources"></a>媒體來源

如果媒體來源支援速率控制，則應該同時執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 和 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)。 否則，媒體會話會報告最小和最大播放速率為1.0，不論管線中有哪些其他元件。

播放速率不會影響樣本的呈現時間，因此媒體來源不應調整其時間戳記。 相反地，標記法會以較快或較慢的速度執行。 若為反向播放，來源會以相反的順序傳遞範例，並減少時間戳記。

[**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)方法的 *fThin* 參數會指出媒體來源是否應將內容 *精簡*。 Thinning 主要適用于影片串流。 在 thinned 模式中，來源會卸載差異畫面格，並只提供主要畫面格。 在非常高的播放速率中，來源可能會略過一些主要畫面格 (例如，將每個其他主要畫面格) 。

來源不需要以 thinned 模式卸載音訊樣本。 不過，以非常高的播放速度，來源可能無法讀取資料快速 nough 以填滿管線的範例要求。 在這種情況下，來源可能需要卸載某些音訊資料。 如果是，則應該嘗試將接近時間的音訊範例傳遞給影片範例， (假設來源同時有兩種類型的資料流程) 。

當資料流程在 thinned 和非 thinned 模式之間轉換時，它會傳送 [MEStreamThinMode](mestreamthinmode.md) 事件。

當媒體來源完成呼叫 [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)時，它會傳送 [MESourceRateChanged](mesourceratechanged.md) 事件。

在反向播放期間：

-   媒體來源會以反向順序傳遞範例，而不會調整時間戳記。
-   資料流程中的時間戳記應該單純地減少。
-   內容的開頭會視為資料流程的結尾。 在每個媒體資料流程提供資料流程中的第一個範例之後 (也就是說，presentation time = 0) ，它會傳送 [MEEndOfStream](meendofstream.md) 事件。

## <a name="media-foundation-transforms"></a>媒體基礎轉換

一般來說，媒體基礎轉換 (MFT) 不需要明確支援速率控制，除非該 MFT 會執行非 thinned 的反向播放。

如果 MFT 未執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 介面，媒體會話會假設下列各項：

-   此 MFT 支援用於向前播放的任意播放速率，也就是 thinned 和非 thinned。
-   此 MFT 支援 thinned 反向播放，但不支援非 thinned 反向播放。

如果上述任一條件不成立，則 MFT 應執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 和 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)。

### <a name="reverse-playback"></a>反向播放

即使管線中的一或多個轉換未明確支援反向播放，媒體會話仍可反向播放。

如果 MFT 未公開 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 介面，媒體會話就會使用 *thinning* 來進行反向播放，如下所示：

-   媒體會話藉由呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)，以平常的方式將主要畫面格傳送到 MFT。

-   媒體會話會卸載 delta 框架，並將其取代為 [MEStreamTick](mestreamtick.md) 事件。

-   在每個範例之間，媒體會話都會排清 MFT，以避免因為時間戳記減少而造成的任何錯誤。

如果範例的 [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) 屬性設定為 **TRUE**，則會將其視為主要畫面格，如果這個屬性為 **FALSE** 或未設定，則會被視為差異框架。

如果 MFT 執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)，媒體會話就會使用此介面來探索 MFT 是否支援非 thinned 反向播放。 如果 MFT 支援非 thinned 反向播放，媒體會話會以反向順序傳遞所有範例，而不會卸載樣本或清除 MFT。

如果某個 MFT 支援非 thinned 反向播放，它應該會執行 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。 當進行反向播放時，媒體會話將會使用此介面來通知 MFT。 屆時，必須針對時間戳記進行縮減，以使差異框架以相反的順序抵達。 解碼器通常需要緩衝範例，直到它收到整個圖形群組 (GOP) ，然後將整個 GOP 解碼，然後以正確的 (反向) 順序輸出已解碼的框架。

## <a name="media-sinks"></a>媒體接收器

如果媒體接收器 *rateless*，媒體會話會假設媒體接收器可以處理任何播放速率。 媒體接收器不需要執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)。  (rateless 媒體接收會 \_ 從 [**IMFMediaSink：： GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) 方法傳回 MEDIASINK rateless 旗標 ) 。

否則，如果媒體接收器可以處理1.0 以外的播放率，則應該執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 。

媒體接收器不應執行 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)。 當播放速率變更時，呈現時鐘會呼叫媒體接收器的 [**IMFClockStateSink：： OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[速率控制](rate-control.md)
</dt> <dt>

[搜尋、向前快轉及反向播放](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



