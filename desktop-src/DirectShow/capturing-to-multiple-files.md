---
description: 捕捉至多個檔案
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: 捕捉至多個檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b40091acff8edffbe84550b03d1ccd4073ddb6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108893"
---
# <a name="capturing-to-multiple-files"></a><span data-ttu-id="d6546-103">捕捉至多個檔案</span><span class="sxs-lookup"><span data-stu-id="d6546-103">Capturing to Multiple Files</span></span>

<span data-ttu-id="d6546-104">將部分影片捕獲到檔案之後，您可以藉由停止圖形並在檔案 [寫入](file-writer-filter.md) 器篩選器上設定檔案名，切換至新的檔案。</span><span class="sxs-lookup"><span data-stu-id="d6546-104">After you have captured some video to a file, you can switch to a new file by stopping the graph and setting the file name on the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="d6546-105">在檔案寫入器上呼叫 [**IFileSinkFilter：： SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) 方法。</span><span class="sxs-lookup"><span data-stu-id="d6546-105">Call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method on the File Writer.</span></span> <span data-ttu-id="d6546-106">您可以在建立圖形時，透過 SetOutputFileName 方法的 *pSink* 參數取得 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d6546-106">You can get a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface when you build the graph, through the *pSink* parameter of the SetOutputFileName method.</span></span> <span data-ttu-id="d6546-107">下列程式碼示範如何執行這項作業：</span><span class="sxs-lookup"><span data-stu-id="d6546-107">The following code shows how to do this:</span></span>


```C++
IBaseFilter *pMux;
IFileSinkFilter *pSink
hr = pBuild->SetOutputFileName(&MEDIASUBTYPE_Avi, L"C:\\YourFileName.avi", 
    &pMux, &pSink);
if (SUCCEEDED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
        pCap, NULL, pMux);

    if (SUCCEEDED(hr))
    {
        pControl->Run();
        /* Wait awhile, then stop the graph. */
        pControl->Stop();
        // Change the file name and run the graph again.
        pSink->SetFileName(L"YourFileName02.avi", 0);
        pControl->Run();
    }
    pMux->Release();
    pSink->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="d6546-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6546-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6546-109">將影片捕獲至檔案</span><span class="sxs-lookup"><span data-stu-id="d6546-109">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



