---
title: 'WM ASF 寫入器篩選器 (Windows Media Format 11 SDK) '
description: WM ASF 寫入器篩選器
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK，WM ASF 寫入器
- DirectShow、WM ASF 寫入器
- QASF 篩選，WM ASF 寫入器
- WM ASF 寫入器，關於
- Advanced Systems Format (ASF) 、WM ASF 寫入器
- ASF (Advanced Systems Format) ，WM ASF 寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967940"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>WM ASF 寫入器篩選器 (Windows Media Format 11 SDK) 

WM ASF 寫入器篩選器可接受數量不定的輸入資料流程，並建立一個 ASF 檔案。 此篩選器會處理所有的壓縮和多工處理 (雖然可以略過壓縮機制) 。 您可以在各種案例中使用 WM ASF 寫入器篩選器，包括數位視訊 (DV) 捕捉、音訊 recompression，以及 Audio-Video 交錯式 (AVI) 或 MPEG 數位媒體檔案來進行網路串流處理的轉換。 此篩選器提供在 DirectShow 中建立 Microsoft Windows Media 音訊和 Windows Media 視訊檔案的唯一方法。

如需詳細資訊，請參閱 [在 DirectShow 中建立 ASF](creating-asf-files-in-directshow.md)檔。

下表包含有關 WM ASF 寫入器篩選器的資訊，例如它所支援的介面和媒體類型。



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面      | **IAMFilterMiscFlags**、 **IBaseFilter**、 **IConfigAsfWriter**、 **IFileSinkFilter2**、IMediaSeeking、IPersistStream、IServiceProvider、ISpecifyPropertyPages、 **IWMIndexer2**、 **IWMHeaderInfo**、 **IWMWriterAdvanced2** |
| 輸入 pin 媒體類型  | 相依于設定檔。 一般未壓縮的類型（例如媒體媒體 \_ 或媒體媒體或媒體類型 \_ ），雖然可以在符合設定檔時接受壓縮類型                                                   |
| 輸入 pin 介面   | **IPin**、 **IMemInputPin**、 **IAMStreamConfig**、 **IServiceProvider**、 **IAMWMBufferPass**、 **IWMStreamConfig2** (到 **IServiceProvider**)                                                                          |
| 輸出 pin 媒體類型 | 不適用                                                                                                                                                                                                          |
| 輸出 pin 介面  | 不適用                                                                                                                                                                                                          |
| 篩選 CLSID           | CLSID \_ WMAsfWriter                                                                                                                                                                                                      |
| 屬性頁 CLSID    | CLSID \_ WMAsfWriterProperties                                                                                                                                                                                            |
| 可執行檔             | Qasf.dll                                                                                                                                                                                                                |
| 優點                  | \_ \_ 未 \_ 使用的業績                                                                                                                                                                                                     |
| 篩選準則分類        | 未指定                                                                                                                                                                                                           |



 

## <a name="remarks"></a>備註

篩選器上的輸入 pin 數目取決於傳遞給篩選器的設定檔。 針對設定檔中定義的每個資料流程，各建立一個適當媒體類型的 pin。

輸入 pin 支援來自 **IAMStreamConfig** 介面的一種方法： **IAMStreamConfig：： >iformatprovider.getformat**。 所有其他方法都會傳回 E \_ >notimpl。 呼叫 **>iformatprovider.getformat** 方法來查詢釘選的目的地壓縮格式，此格式是由目前的設定檔所定義。 使用 [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) 介面設定設定檔。

篩選器的 **IServiceProvider** 介面可讓應用程式取出 [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) 介面，此介面定義于 Windows Media 格式 SDK 中。 **IWMWriterAdvanced2** 介面會控制 video 去交錯，而且如果輸入是 [*交錯*](wmformat-glossary.md)式來源（例如 DV (數位視訊) ，就很有用）。 使用 **GetInputSetting** 和 **SetInputSetting** 方法來控制去交錯。 不建議用戶端使用此介面上的任何其他方法。 只有將篩選準則加入至篩選圖形之後，才能取得這個介面。 下列範例顯示如何查詢此介面：


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DirectShow QASF 參考**](directshow-qasf-reference.md)
</dt> </dl>

 

 
