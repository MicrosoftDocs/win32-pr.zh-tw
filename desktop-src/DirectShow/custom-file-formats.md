---
description: 自訂檔案格式
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: 自訂檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361dca97fcd34b30e3c29d6ba189ad26968d4fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935851"
---
# <a name="custom-file-formats"></a><span data-ttu-id="0edf7-103">自訂檔案格式</span><span class="sxs-lookup"><span data-stu-id="0edf7-103">Custom File Formats</span></span>

<span data-ttu-id="0edf7-104">如果您有支援您自己的檔案格式的自訂 mux 或檔案寫入器篩選器，則可以指定 CLSID 作為 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) 方法的第一個參數：</span><span class="sxs-lookup"><span data-stu-id="0edf7-104">If you have a custom mux or file-writer filter that supports your own file format, you can specify the CLSID as the first parameter of the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



<span data-ttu-id="0edf7-105">如需此用法的詳細資訊，請參閱 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename)。</span><span class="sxs-lookup"><span data-stu-id="0edf7-105">For more information about this usage, see [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0edf7-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="0edf7-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0edf7-107">將影片捕獲至檔案</span><span class="sxs-lookup"><span data-stu-id="0edf7-107">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



