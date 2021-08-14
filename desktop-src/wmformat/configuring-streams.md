---
title: 設定資料流程
description: 設定資料流程
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows媒體格式 SDK，資料流程
- 設定檔，資料流程
- 資料流程，設定
- 編解碼器，設定資料流程
- 設定檔，IWMStreamConfig 介面
- 資料流程，IWMStreamConfig 介面
- IWMStreamConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d55db0d02c8eae3ddd3ec780f5d6470d87628a6f7b12feceb5faa413b2e4546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199314"
---
# <a name="configuring-streams"></a>設定資料流程

設定檔中唯一需要的就是至少一個資料流程。 其他選項可讓您存取更先進的功能，但至少有一個資料流程可讓您建立一個 ASF 檔。 您必須先瞭解如何設定串流，然後再建立複雜的設定檔。

基於設定檔的目的，資料流程可以分為兩種類型：使用 Windows 媒體編解碼器壓縮的類型，以及未使用任何編解碼器處理的任意資料流程。 音訊串流和影片串流是使用 Windows 媒體編解碼器的類型。 當然，串流可以包含使用協力廠商編解碼器壓縮的音訊或影片，但設定這類串流的程式是特殊案例。 如需詳細資訊，請參閱 [使用協力廠商編解碼器建立 ASF](to-create-asf-files-using-third-party-codecs.md)檔案。

下列清單摘要說明設定資料流程的流程。

1.  取得資料流程的資料流程設定物件。
    -   如果您要使用其中一個 Windows 媒體編解碼器來建立資料流程，您必須使用 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)方法，以編解碼器格式取得串流設定物件。
    -   如果資料流程是任意類型，請使用 [**IWMProfile：： CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)取得空的資料流程設定物件。
2.  設定串流以符合您的需求。
    -   所有類型的資料流程都應該指派名稱、連接名稱和資料流程號碼。
    -   使用 Windows 媒體編解碼器的資料流程應該只以編解碼器格式的預先定義方式改變。 針對音訊串流，只應變更雙階段 VBR (VBR) 設定的變動位元速率。 影片串流需要使用所需的框架屬性進行設定。
    -   任意資料流程依類型有不同的設定需求。 全部都需要位元速率和緩衝區視窗。
3.  藉由呼叫 [**IWMProfile：： AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)，將資料流程新增至設定檔。

所有串流都是使用資料流程設定物件來定義。 資料流程設定物件的主要介面是 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)，它提供了設定資料流程基本設定的方法，例如串流號碼、位元速率等等。 **IWMStreamConfig** 是由較新的介面（ [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) 和 [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)）所繼承。 如同所有編號的介面修訂，您應該一律使用 **QueryInterface** 方法來取得最新版本。

資料流程中的大部分設定都是透過 [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)來存取。 這些設定會封裝在 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構中。 針對音訊和影片， **WM \_ 媒體 \_ 類型** 結構會指向另一個結構，其中包含媒體類型特定的進一步資訊。 此次要結構通常是 [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) 音訊和 [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) 的影片。 此外，影片串流有三個結構 **BITMAPINFOHEADER**，描述個別影片框架的特性。 **BITMAPINFOHEADER** 是常見的結構，可以在 Platform SDK 的圖形裝置介面 (GDI) 區段中找到。

下列各節說明如何設定資料流程。



| 區段                                                                                                          | 描述                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [所有資料流程通用的設定](configuration-common-to-all-streams.md)                                   | 描述所有資料流程類型通用的基本資料流程設定。                                                                                        |
| [從編解碼器取得串流設定資訊](getting-stream-configuration-information-from-codecs.md) | 說明如何從編解碼器取得串流設定資訊，以確保使用 Windows Media 音訊和影片編解碼器正確設定串流。 |
| [設定音訊串流](configuring-audio-streams.md)                                                       | 說明如何設定音訊串流。                                                                                                                       |
| [設定影片串流](configuring-video-streams.md)                                                       | 說明如何設定影片串流。                                                                                                                       |
| [設定影片串流以搜尋效能](configuring-video-streams-for-seeking-performance.md)       | 說明如何設定有效率的搜尋很重要的影片串流。                                                                              |
| [設定畫面抓取資料流程](configuring-screen-capture-streams.md)                                     | 說明如何設定螢幕擷取畫面的影片串流。                                                                                                    |
| [設定影像串流](configuring-image-streams.md)                                                       | 說明如何設定影像串流。                                                                                                                       |
| [使用未壓縮的音訊和影片串流](using-uncompressed-audio-and-video-streams.md)                     | 說明如何設定未壓縮的音訊或影片串流。                                                                                                  |
| [設定任意資料流程類型](configuring-arbitrary-stream-types.md)                                     | 描述如何將資料流程設定為使用預先定義的任意資料流程類型。                                                                                |
| [設定 VBR 資料流程](configuring-vbr-streams.md)                                                           | 描述如何將資料流程設定為使用變數位元速率編碼 (VBR) 。                                                                                     |
| [設定資料單位延伸模組](configuring-data-unit-extensions.md)                                         | 描述如何設定資料流程，以便在寫入檔案時附加資料單位延伸模組。                                                      |
| [重複使用串流設定](reusing-stream-configurations.md)                                               | 描述您可以使用現有設定檔中的串流設定物件來建立新設定檔的方式。                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**輸入、串流和輸出**](inputs-streams-and-outputs.md)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

 