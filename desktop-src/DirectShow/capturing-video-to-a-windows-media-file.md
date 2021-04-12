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
# <a name="capturing-video-to-a-windows-media-file"></a><span data-ttu-id="dba6e-103">將影片捕獲到 Windows Media 檔案</span><span class="sxs-lookup"><span data-stu-id="dba6e-103">Capturing Video to a Windows Media File</span></span>

<span data-ttu-id="dba6e-104">若要捕獲影片，並將其編碼為 Windows Media 視訊 (WMV) 檔，請將 capture 釘選到 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="dba6e-104">To capture video and encode it to a Windows Media Video (WMV) file, connect the capture pin to the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the following diagram.</span></span>

![windows media capture 圖形](images/vidcap03.png)

<span data-ttu-id="dba6e-106">建立此圖形最簡單的方式是 \_ 在 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) 方法中 specifing MEDIASUBTYPE Asf：</span><span class="sxs-lookup"><span data-stu-id="dba6e-106">The easiest way to build this graph is by specifing MEDIASUBTYPE\_Asf in the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



<span data-ttu-id="dba6e-107">MEDIASUBTYPE Asf 的值會 \_ 告訴「捕獲圖形產生器」使用「WM Asf 寫入器」篩選器作為檔案接收。</span><span class="sxs-lookup"><span data-stu-id="dba6e-107">The value MEDIASUBTYPE\_Asf tells the Capture Graph Builder to use the WM ASF Writer filter as the file sink.</span></span> <span data-ttu-id="dba6e-108">「捕獲圖形產生器」會建立篩選、將它新增至圖形，然後呼叫 [**IFileSinkFilter：： SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) 來設定輸出檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="dba6e-108">The Capture Graph Builder creates the filter, adds it to the graph, and calls [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) to set the name of the output file.</span></span> <span data-ttu-id="dba6e-109">它會以外寄參數的形式傳回篩選的指標 (</span><span class="sxs-lookup"><span data-stu-id="dba6e-109">It returns a pointer to the filter as an outgoing parameter (</span></span>


```
pASFWriter
```



<span data-ttu-id="dba6e-110">在上述範例中) 。</span><span class="sxs-lookup"><span data-stu-id="dba6e-110">in the previous example).</span></span>

<span data-ttu-id="dba6e-111">使用 WM ASF 寫入器上的 [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) 介面來設定 Windows Media 設定檔。</span><span class="sxs-lookup"><span data-stu-id="dba6e-111">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface on the WM ASF Writer to set the Windows Media profile.</span></span> <span data-ttu-id="dba6e-112">您必須先完成此動作，才能連接 WM ASF 寫入器上的任何 pin。</span><span class="sxs-lookup"><span data-stu-id="dba6e-112">You must do this before you connect any pins on the WM ASF Writer.</span></span>


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



<span data-ttu-id="dba6e-113">如需有關設定設定檔的詳細資訊，請參閱 [在 DirectShow 中建立 ASF](creating-asf-files-in-directshow.md)檔。</span><span class="sxs-lookup"><span data-stu-id="dba6e-113">For more information about setting the profile, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="dba6e-114">呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，將捕獲篩選器連線到 ASF 寫入器：</span><span class="sxs-lookup"><span data-stu-id="dba6e-114">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the capture filter to the ASF Writer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



<span data-ttu-id="dba6e-115">WM ASF 寫入器篩選器上的每個輸入 pin 都對應于 Windows Media 設定檔中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="dba6e-115">Each input pin on the WM ASF Writer filter corresponds to a stream in the Windows Media profile.</span></span> <span data-ttu-id="dba6e-116">您必須連接每個 pin，使檔案內容符合設定檔。</span><span class="sxs-lookup"><span data-stu-id="dba6e-116">You must connect every pin, so that the file content matches the profile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dba6e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="dba6e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dba6e-118">將影片捕獲至檔案</span><span class="sxs-lookup"><span data-stu-id="dba6e-118">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



