---
description: 將影片捕獲到 Windows Media 檔案
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: 將影片捕獲到 Windows Media 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195740"
---
# <a name="capturing-video-to-a-windows-media-file"></a>將影片捕獲到 Windows Media 檔案

若要捕獲影片，並將其編碼為 Windows Media 視訊 (WMV) 檔，請將 capture 釘選到 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器，如下圖所示。

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



MEDIASUBTYPE Asf 的值會 \_ 告訴「捕獲圖形產生器」使用「WM Asf 寫入器」篩選器作為檔案接收。 「捕獲圖形產生器」會建立篩選、將它新增至圖形，然後呼叫 [**IFileSinkFilter：： SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) 來設定輸出檔的名稱。 它會以外寄參數的形式傳回篩選的指標 (


```
pASFWriter
```



在上述範例中) 。

使用 WM ASF 寫入器上的 [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) 介面來設定 Windows Media 設定檔。 您必須先完成此動作，才能連接 WM ASF 寫入器上的任何 pin。


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



如需有關設定設定檔的詳細資訊，請參閱 [在 DirectShow 中建立 ASF](creating-asf-files-in-directshow.md)檔。

呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，將捕獲篩選器連線到 ASF 寫入器：


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



WM ASF 寫入器篩選器上的每個輸入 pin 都對應于 Windows Media 設定檔中的資料流程。 您必須連接每個 pin，使檔案內容符合設定檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將影片捕獲至檔案](capturing-video-to-a-file.md)
</dt> </dl>

 

 



