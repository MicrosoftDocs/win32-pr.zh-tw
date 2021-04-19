---
title: 設定影片串流
description: 設定影片串流
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- 串流，設定影片串流
- 編解碼器，設定影片串流
- 影片串流，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966841"
---
# <a name="configuring-video-streams"></a>設定影片串流

影片串流的設定比音訊串流更有彈性。 這是因為組成影片的框架屬性可能會與下一個檔案有很大的差異。 當您針對所使用的編解碼器取得編解碼器格式時，您必須設定影片串流設定物件的下列值。



| 值                                 | 描述                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 位元速率                              | 呼叫 [**IWMStreamConfig：： SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) ，將設定為所需的值。 影片編解碼器將會嘗試壓縮媒體以符合您的規格。 如果您的值太低，則產生的壓縮影片將會變得很差。           |
| 緩衝區視窗                         | 呼叫 [**IWMStreamConfig：： SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) ，將設定為所需的值。 影片編解碼器將會嘗試壓縮媒體以符合您的規格。 如果您的值太低，則產生的壓縮影片將會變得很差。 |
| **WMVIDEOINFOHEADER.rcSource**        | 左上角必須設定為0、0。 右下角必須設定為框架維度。 例如，在640x480 資料流程中，這些設定會是0、0640480。                                                                                                |
| **WMVIDEOINFOHEADER.rcTarget**        | 必須符合 **rcSource**。                                                                                                                                                                                                                                                    |
| **WMVIDEOINFOHEADER.dwBitRate**       | 必須符合為數據流設定的位元速率。                                                                                                                                                                                                                                 |
| **WMVIDEOINFOHEADER.AvgTimePerFrame** | 設定為每個畫面格的大約時間。                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER.biWidth**          | 設定為所需框架大小的寬度（以圖元為單位）。                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER.biHeight**         | 設定為所需框架大小的高度（以圖元為單位）。                                                                                                                                                                                                                    |



 

如果影片內容的大小為四個的寬度和高度的倍數，則無法正確播放影片內容。 例外狀況是 [*RGB*](wmformat-glossary.md) 未壓縮影片，可能是任何大小。 如果您嘗試設定的大小不是4的倍數，則寫入器會傳回下列其中一個錯誤：

-   NS \_ E \_ 不正確 \_ 輸入 \_ 格式
-   NS \_ E \_ 不正確 \_ 輸出 \_ 格式
-   NS \_ E \_ INVALIDPROFILE

如果您使用變數位元速率編碼，則可能需要進行其他調整。 如需詳細資訊，請參閱設定 [VBR 資料流程](configuring-vbr-streams.md)。

某些 Windows Media 視訊編解碼器支援多個複雜度層級。 複雜性層級會決定編解碼器在編碼影片資料流程時所要使用的演算法。 使用高複雜性層級需要更多處理能力才能進行編碼和解碼。

每個支援複雜性設定的編解碼器都會公開下列設定，您可以使用 [**IWMCodecInfo3：： GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) 方法來取得這些設定。



| 設定                 | Description                                         |
|-------------------------|-----------------------------------------------------|
| g \_ wszComplexityMax     | 編解碼器支援的最高品質層級。   |
| g \_ wszComplexityOffline | 離線播放的建議品質層級。   |
| g \_ wszComplexityLive    | 串流播放的建議品質層級。 |



 

若要在設定檔中設定影片串流的複雜度，請使用 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) 方法，並使用 g \_ wszComplexity 屬性。 您設定的值必須小於或等於編解碼器支援的最大複雜度。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**影片複雜性設定**](video-complexity-settings.md)
</dt> </dl>

 

 




