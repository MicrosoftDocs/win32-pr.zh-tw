---
description: 建立音訊捕獲 Graph
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: 建立音訊捕獲 Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ff89cff8662bb5da81860053221596b18e89ab2300134cf2ff8826ae99b787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108218"
---
# <a name="creating-an-audio-capture-graph"></a>建立音訊捕獲 Graph

音訊捕獲應用程式的第一個步驟是建立篩選圖形。 圖形的設定取決於您想要建立的檔案類型。

-   僅限音訊的 AVI 檔：將音訊捕獲篩選至 [Avi mux](avi-mux-filter.md) 篩選，並將 Avi mux 篩選至檔案 [寫入](file-writer-filter.md) 器篩選器。
-   WAV 檔：音訊捕獲篩選器可將 [篩選範例 WavDest](wavdest-filter-sample.md) 至檔案寫入器篩選
-   WindowsMedia Audio ( .wma) 檔案：音訊捕獲篩選至[WM ASF 寫入](wm-asf-writer-filter.md)器篩選器。

WavDest 篩選器會以 SDK 範例的形式提供。 若要使用它，您必須建立並註冊篩選準則。

若要使用 ASF 寫入器篩選器，您必須安裝 Windows 媒體 SDK，並取得軟體金鑰以解除鎖定篩選。 如需詳細資訊，請參閱[在 DirectShow 中使用 Windows 媒體](using-windows-media-in-directshow.md)。

您可以使用[Capture Graph Builder](capture-graph-builder.md)物件來建立篩選圖形，也可以「手動」建立圖形;也就是，讓應用程式以程式設計方式新增並連接每個篩選準則。 本文描述手動方法。 如需使用 Capture Graph Builder 的詳細資訊，請參閱[影片捕獲](video-capture.md)。 本文中大部分的資訊都適用于僅限音訊的圖形。

新增音訊捕獲裝置

因為音訊捕獲篩選器會與特定硬體裝置通訊，所以您無法直接呼叫 **CoCreateInstance** 來建立篩選器。 相反地，請使用 [系統裝置](system-device-enumerator.md) 列舉值來列舉 [音訊捕獲來源] 類別目錄中的所有裝置（由類別識別碼 CLSID AudioInputDeviceCategory 來識別） \_ 。

系統裝置列舉值會傳回裝置的名字組清單;每個名字標記的易記名稱都會對應到裝置的名稱。 選擇其中一個傳回的名字，並使用它來建立該裝置的音訊捕獲篩選準則實例。 將篩選準則加入至篩選圖形。 使用者的慣用音訊錄製裝置會先出現在 [標記清單] 中。  (使用者選取慣用的裝置，方法是按一下主控台中的 [音效和多媒體]。 ) 

如需詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。

若要指定要從中取得的輸入，請從音訊捕獲篩選器取得 [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) 介面，然後呼叫 **put \_ Enable** 方法來指定輸入。 不過，此方法的一項限制是，不同的硬體裝置可能會使用不同的字串來識別其輸入。 例如，一張卡片可能會使用「麥克風」來識別麥克風輸入，而另一張卡片可能會使用「Mic」。 若要判斷指定輸入的字串識別碼，請使用 Windows 多媒體函數 [**waveOutOpen**](/previous-versions//dd743866(v=vs.85))、 [**mixerOpen**](/previous-versions//dd757308(v=vs.85))和 [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85))。 如需詳細資訊，請參閱 MSDN 主題[Mixer 裝置查詢](/windows/desktop/Multimedia/mixer-device-queries)。

新增多工器和檔案寫入器

音訊捕獲圖形必須包含多工器和檔案寫入器。

多工器是一種篩選器， *可將一* 或多個資料流程合併為具有特定格式的單一資料流程。 例如，AVI Mux 篩選器會將音訊和影片串流合併到交錯的 AVI 資料流程中。 針對音訊捕獲，通常只有一個音訊串流，但音訊資料仍然必須封裝成可儲存至磁片的格式，而這需要多工器。 多工器的選擇取決於目標格式：

-   AVI： AVI 多工器
-   WAV： WavDest
-   WMA： ASF 寫入器

檔案 *寫入器* 是一種篩選器，可將傳入的資料寫入檔案。 若是 AVI 或 WAV 檔案，請使用檔案 [寫入器篩選器](file-writer-filter.md)。 針對 WMA 檔案，ASF 寫入器可作為多工器和檔案寫入器。

在您建立篩選並將它們新增至圖形之後，請將音訊捕獲篩選器的輸出接點連接到多工器的輸入 pin，然後將多工器的輸出圖釘連接到篩選寫入器的輸入 pin 碼 (假設這些是個別的篩選) 。 若要指定檔案名，請查詢 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) 介面的檔案寫入器，然後呼叫 [**IFileSinkFilter：： SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) 方法。

### <a name="example-code"></a>範例程式碼

下列範例說明如何使用 WavDest 篩選器來建立音訊捕獲圖形。 相同的原則也適用于其他檔案類型。


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



這個範例會使用 `AddFilterByCLSID` 在 [[加入篩選依據 CLSID](add-a-filter-by-clsid.md)] 中所述的函式，以及 `ConnectFilters` [連線兩個篩選器](connect-two-filters.md)中所述的函數。 這些都不是 DirectShow API。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊捕獲](audio-capture.md)
</dt> </dl>

 

 
