---
description: 將影片捕獲到 AVI 檔案
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: 將影片捕獲到 AVI 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5ec58c021c5f37fed992959b33965efddb5603798ff756909879d307bca1f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689031"
---
# <a name="capturing-video-to-an-avi-file"></a>將影片捕獲到 AVI 檔案

下圖顯示將影片捕獲到 AVI 檔案的最簡單圖形。

![avi 影片捕獲圖形](images/vidcap02.png)

[AVI Mux](avi-mux-filter.md)篩選器會從 capture 釘選影片串流，並將其封裝成 AVI 資料流程。 音訊串流也可以連接到 AVI Mux 篩選器，在這種情況下，Mux 會交錯兩個數據流。 檔案 [寫入](file-writer-filter.md) 器篩選器會將 AVI 資料流程寫入磁片。

若要建立圖形，請先呼叫 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) 方法，如下所示：


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



第一個參數會指定檔案類型，在此案例中為 AVI。 第二個參數會提供檔案名。 針對 AVI，SetOutputFileName 方法會 cocreates AVI Mux 篩選器和檔案寫入器篩選器，並將它們新增至圖形。 它也會藉由呼叫 [**IFileSinkFilter：： SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) 方法來設定檔案寫入器篩選器上的檔案名，並連接這兩個篩選器。 方法會傳回第三個參數中 AVI Mux 的指標。 （選擇性）它會傳回第四個參數中 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) 介面的指標。 如果您不需要此介面，您可以將此參數設定為 **Null**，如先前的範例所示。

接下來，呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，將捕獲篩選器連線到 AVI Mux，如下所示：


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



第一個參數會提供 pin 類別，也就是 \_ 用於捕捉的釘選類別 \_ 捕獲。 第二個參數會提供媒體類型。 第三個參數是捕獲篩選器 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。 第四個參數是選擇性的;它可讓您透過中繼篩選（例如編碼器）路由傳送影片串流，然後再將它傳遞至 mux 篩選器。 否則，請將此參數設定為 **Null**，如先前的範例所示。 第五個參數是 mux 篩選器的指標。 呼叫 SetOutputFileName 方法即可取得這個指標。

若要捕獲音訊，請使用媒體類型媒體類型來呼叫 RenderStream \_ 。 如果您從兩部不同的裝置捕獲音訊和影片，最好讓音訊串流成為主要串流。 這有助於防止兩個數據流之間的漂移，因為 AVI Mux 篩選器會調整影片資料流程的播放速率以符合音訊串流。 若要設定主要串流，請在 AVI Mux 篩選器上呼叫 [**IConfigAviMux：： SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) 方法：


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



SetMasterStream 的參數是資料流程號碼，由您呼叫 RenderStream 的順序決定。 例如，如果您先針對影片呼叫 RenderStream，然後針對音訊撥號，則影片為串流0，而音訊為串流1。

您也可能想要設定 AVI Mux 篩選器交錯音訊和影片資料流程的方式，方法是呼叫 [**IConfigInterleaving：:p ui \_ 模式**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) 方法。


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



使用交錯 \_ 捕獲旗標，AVI Mux 會以適用于影片捕獲的速率來執行交錯。 您也可以使用交錯 \_ 無，也就是沒有交錯的，AVI Mux 只會以抵達的順序寫入資料。 交錯的 \_ 完整旗標表示 AVI Mux 會執行完全交錯的功能; 不過，此模式較不適合用于影片捕獲，因為它需要最多段無意。

編碼影片串流

您可以藉由在捕獲篩選器和 AVI Mux 篩選器之間插入編碼器篩選器，將影片串流編碼。 使用 [系統裝置列舉](system-device-enumerator.md) 值或 [篩選器](filter-mapper.md) 對應程式來選取編碼器篩選器。  (需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。 ) 

將編碼器篩選器指定為要 RenderStream 的第四個參數，以粗體顯示在下列範例中：


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



編碼器篩選器可能支援 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 或其他介面來設定編碼參數。 如需可能的介面清單，請參閱檔案 [編碼和解碼介面](file-encoding-and-decoding-interfaces.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將影片捕獲至檔案](capturing-video-to-a-file.md)
</dt> </dl>

 

 



