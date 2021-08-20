---
description: 將影片捕獲到 Windows 媒體檔案
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: 將影片捕獲到 Windows 媒體檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3268d3a3df4a24c5836dba81f7ef4cf0b872907f09367d3212d27c38c0dd4414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158700"
---
# <a name="capturing-video-to-a-windows-media-file"></a>將影片捕獲到 Windows 媒體檔案

若要捕獲影片，並將其編碼為 Windows Media 視訊 (WMV) 檔，請將 capture 釘選到[WM ASF 寫入](wm-asf-writer-filter.md)器篩選器，如下圖所示。

![windows media capture 圖形](images/vidcap03.png)

建立此圖形最簡單的方式是 \_ 在 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) 方法中 specifing MEDIASUBTYPE Asf：


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



MEDIASUBTYPE Asf 的值會 \_ 告知 Capture Graph Builder 使用 WM Asf 寫入器篩選器作為檔案接收。 Capture Graph 產生器會建立篩選、將它新增至圖形，然後呼叫 [**IFileSinkFilter：： SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename)來設定輸出檔的名稱。 它會以外寄參數的形式傳回篩選的指標 (


```
pASFWriter
```



在上述範例中) 。

使用 WM ASF 寫入器上的 [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)介面來設定 Windows 媒體設定檔。 您必須先完成此動作，才能連接 WM ASF 寫入器上的任何 pin。


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



如需有關設定設定檔的詳細資訊，請參閱[在 DirectShow 中建立 ASF](creating-asf-files-in-directshow.md)檔。

呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，將捕獲篩選器連線到 ASF 寫入器：


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



在 WM ASF 寫入器篩選器上的每個輸入 pin 都對應于 Windows 媒體設定檔中的資料流程。 您必須連接每個 pin，使檔案內容符合設定檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將影片捕獲至檔案](capturing-video-to-a-file.md)
</dt> </dl>

 

 



