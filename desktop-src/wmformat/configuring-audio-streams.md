---
title: 設定音訊串流
description: 設定音訊串流
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- 串流，設定音訊串流
- 編解碼器，設定音訊串流
- 音訊串流，設定
- 編解碼器，格式
- 資料流程，IWMCodecInfo 介面
- IWMCodecInfo，音訊串流
- 資料流程，A/V 同步處理
- 音訊串流，A/V 同步處理
- A/V 同步處理
- 資料流程，同步處理 A/V
- 音訊串流，同步處理 A/V
- 串流，低延遲音訊格式
- 音訊串流，低延遲音訊格式
- 編解碼器、低延遲音訊格式
- '資料流程、變數位元速率 (VBR) '
- '音訊串流，變數位元速率 (VBR) '
- '編解碼器、變數位元速率 (VBR) '
- 變數位元速率 (VBR) ，設定
- VBR (變數位速率) ，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3931ec41e73c125417d39cdd177dc16056e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106979670"
---
# <a name="configuring-audio-streams"></a>設定音訊串流

音訊串流通常是最直接的設定。 使用 [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) 的方法取得編解碼器的串流設定，如 [從編解碼器取得串流設定資訊](getting-stream-configuration-information-from-codecs.md)中所述。 在大多數情況下，您不應該從抓取的設定改變設定。

您從列舉所選取的編解碼器格式，取決於使用設定檔所建立之 ASF 檔案的用途。 [**IWMCodecInfo2：： GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc)所取出的編解碼器格式描述會摘要說明格式的特性。 如果您的應用程式未顯示在它們之間選擇的描述，您可以在編解碼器格式的 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)介面上呼叫 **QueryInterface** ，以取得 [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)介面。 然後，您可以藉由呼叫 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)來取出 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構。 藉由檢查 **WM \_ 媒體 \_ 類型** 結構和其指向的 [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) 結構，您可以判斷編解碼器格式的設定，並將其與您的需求進行比較。

## <a name="getting-audio-formats-for-av-synchronization"></a>取得/V 同步處理的音訊格式

Windows Media 音訊編解碼器和 Windows Media 音訊 Professional 編解碼器都支援僅限音訊檔案和音訊/影片檔案的格式。 僅限音訊格式可針對只包含音訊資料的檔案進行優化，而音訊/影片格式則是針對具有影片串流之檔案中的音訊進行優化。 列舉這些編解碼器的編解碼器格式時，音訊/影片格式會出現在僅限音訊格式的之後。 音訊/影片格式描述全都包含 " (A/V) " 字串。 您可以藉由檢查每秒的封包數，以程式設計方式識別針對音訊/影片同步處理設計的格式。 如果位元速率大於或等於每秒32000位，則同步處理的格式有5個或更多的封包。 位元速率小於每秒32000位的格式，如果每秒使用3個或更多封包，則可以搭配同步處理的影片使用。 [ [尋找音訊格式](to-find-audio-formats.md) ] 主題中的程式碼範例包含進行這項檢查所需的程式碼：


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>取得 Low-Delay 的音訊格式

Windows Media 9.1 編解碼器和 Windows Media 音訊 9.1 Professional 編解碼器都支援低延遲格式。 這些格式的緩衝區視窗比其他音訊格式小。 低延遲音訊的目的在於改善檔案或資料流程經常切換的案例中的效能;例如，應用程式會列出在使用者介面中進行串流處理的許多歌曲，並允許使用者在兩者之間進行切換。

低延遲格式只能在 CBR 模式下使用， (一次或兩次傳遞) 。 低延遲格式的描述全都包含「低延遲」字串。 您可以藉由檢查格式的位元速率值，以程式設計方式識別格式。 低延遲格式的指派位速率為1，小於相等一般格式的位元速率。 例如，Windows Media 音訊9.1 編解碼器支援使用位元速率為 192 kbps 的單一傳遞 CBR 格式。 相等的低延遲格式的位元速率為 191 kbps。 此外，除了 Windows Media 音訊9.1 編解碼器所支援的 5 kbps mono 格式之外，低延遲格式是具有奇數位元速率值的唯一格式。

## <a name="configuring-variable-bit-rate-audio"></a>設定變數位元速率音訊

當您的其中一個 Windows Media 音訊編解碼器需要變數位元速率 (VBR) 格式時，您可以在 [**IWMCodecInfo3：： SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) 方法中設定列舉設定來取得它。 將 g \_ wszVBREnabled 設為 True，並針對以品質為基礎的 vbr 將 g wszNumPasses 設定為1，並將 \_ 兩個進行 vbr (受限或未受限制的) 設定為2。 如果您使用受限制的雙向 VBR，您必須使用 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) 的方法（如設定 [VBR 資料流程](configuring-vbr-streams.md)中所述），手動設定資料流程的最大位元速率和緩衝區視窗。

在以品質為基礎的 VBR 設定檔中， **WAVEFORMATEX** 結構的 **nAvgBytesPerSec** 成員會包含低序位位元組 (1 到 100) 的品質層級，而三個高序位的位元組則會設定為0x7fffff。 請勿嘗試手動修改此值以修改品質設定;您必須使用從編解碼器取出的格式。 若要使用不同的品質值，您必須列舉格式，直到找到符合您需求的格式為止。 此外， **nAvgBytesPerSec** 不會保留在 ASF 檔案中;當您取得使用 reader 物件開啟之檔案的 **WAVEFORMATEX** 結構時， **nAvgBytesPerSec** 會包含代表每秒位元組平均位元組數的近似值。

> [!Note]  
> 設定音訊串流時，您的音訊緩衝區視窗值絕對不能大於檔案中任何影片資料流程的值。 通常這並不成問題，因為音訊緩衝區視窗值的範圍應介於1.5 到3秒之間，而影片值的範圍應介於3到5秒之間。 如果 [音訊緩衝區] 視窗大於 [影片緩衝區] 視窗，檔案將會播放到與同步處理稍微不同的資料流程。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**尋找音訊格式**](to-find-audio-formats.md)
</dt> </dl>

 

 