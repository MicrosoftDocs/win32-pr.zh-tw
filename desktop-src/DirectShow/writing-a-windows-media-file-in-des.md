---
description: 以 DES 撰寫 Windows Media 檔案
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: 以 DES 撰寫 Windows Media 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986450"
---
# <a name="writing-a-windows-media-file-in-des"></a><span data-ttu-id="5a8cd-103">以 DES 撰寫 Windows Media 檔案</span><span class="sxs-lookup"><span data-stu-id="5a8cd-103">Writing a Windows Media File in DES</span></span>

<span data-ttu-id="5a8cd-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5a8cd-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5a8cd-105">本節說明如何使用 (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md) 來撰寫 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-105">This section describes how to write a Windows Media file using [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a8cd-106">請勿使用智慧型轉譯引擎來寫入 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-106">Do not use the Smart Render Engine to write Windows Media files.</span></span> <span data-ttu-id="5a8cd-107">請一律使用基本轉譯引擎 (CLSID \_ RenderEngine) 。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-107">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

 

<span data-ttu-id="5a8cd-108">若要寫入 Windows Media 檔案，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="5a8cd-108">To write a Windows Media file, do the following:</span></span>

1.  <span data-ttu-id="5a8cd-109">使用您的金鑰提供者指標，在轉譯引擎上呼叫 **SetSite** 。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-109">Call **SetSite** on the render engine, with a pointer to your key provider.</span></span>
2.  <span data-ttu-id="5a8cd-110">建立圖形的前端。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-110">Build the front end of the graph.</span></span> <span data-ttu-id="5a8cd-111"> (查看轉譯 [專案](rendering-a-project.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="5a8cd-111">(See [Rendering a Project](rendering-a-project.md).)</span></span>
3.  <span data-ttu-id="5a8cd-112">建立 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器，並將它新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-112">Create the [WM ASF Writer](wm-asf-writer-filter.md) filter and add it to the graph.</span></span>
4.  <span data-ttu-id="5a8cd-113">使用 WM ASF 寫入器篩選器上的 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) 介面來設定檔案名。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-113">Use the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface on the WM ASF Writer filter to set the file name.</span></span>
5.  <span data-ttu-id="5a8cd-114">將 WM ASF 寫入器設定為使用 Windows Media 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-114">Configure the WM ASF Writer to use a Windows Media profile.</span></span> <span data-ttu-id="5a8cd-115">每個設定檔都有預先定義的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-115">Each profile has a predefined number of streams.</span></span> <span data-ttu-id="5a8cd-116">您必須選擇符合專案中群組的設定檔。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-116">You must choose a profile that matches the groups in your project.</span></span>

    <span data-ttu-id="5a8cd-117">[**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)介面包含一些不同的方法來設定設定檔。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-117">The [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface contains a few different methods for setting the profile.</span></span> <span data-ttu-id="5a8cd-118">例如， **ConfigureFilterUsingProfileGuid** 方法會指定系統設定檔做為 GUID。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-118">For example, the **ConfigureFilterUsingProfileGuid** method specifies a system profile as a GUID.</span></span> <span data-ttu-id="5a8cd-119">或者，您可以使用 Windows Media 格式方法來取得 **IWMProfile** 指標，然後呼叫 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile)。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-119">Or, you can use Windows Media Format methods to get an **IWMProfile** pointer and then call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span></span> <span data-ttu-id="5a8cd-120">如需詳細資訊，請參閱設定 [ASF 寫入器](configuring-the-asf-writer.md)。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-120">For more information, see [Configuring the ASF Writer](configuring-the-asf-writer.md).</span></span>

6.  <span data-ttu-id="5a8cd-121">將前端連接到 ASF 寫入器。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-121">Connect the front end to the ASF Writer.</span></span> <span data-ttu-id="5a8cd-122">圖形的前端包含每個群組的一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-122">The front end of the graph contains one output pin for each group.</span></span> <span data-ttu-id="5a8cd-123">假設您指定了相容的設定檔，ASF 寫入器應該會有一組相符的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-123">Assuming that you specified a compatible profile, the ASF Writer should have a matching set of input pins.</span></span> <span data-ttu-id="5a8cd-124">將每個輸出圖釘連接至對應的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-124">Connect each output pin to the corresponding input pin.</span></span> <span data-ttu-id="5a8cd-125">最簡單的方法是使用 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-125">The easiest way to do this is using the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="5a8cd-126">首先，建立「 [Capture graph](capture-graph-builder.md) 產生器」的新實例，並使用篩選圖形管理員的指標將它初始化：</span><span class="sxs-lookup"><span data-stu-id="5a8cd-126">First, create a new instance of the [Capture Graph Builder](capture-graph-builder.md) and initialize it with a pointer to the Filter Graph Manager:</span></span>

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    <span data-ttu-id="5a8cd-127">接下來，藉由呼叫 [**IRenderEngine：： GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) 方法，取得每個群組的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="5a8cd-127">Next, retrieve the output pin for each group by calling the [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) method.</span></span> <span data-ttu-id="5a8cd-128">呼叫 **RenderStream** 將 pin 連接至 ASF 寫入器：</span><span class="sxs-lookup"><span data-stu-id="5a8cd-128">Call **RenderStream** to connect the pin to the ASF Writer:</span></span>

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5a8cd-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a8cd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a8cd-130">使用具有 DirectShow 編輯服務的 Windows Media</span><span class="sxs-lookup"><span data-stu-id="5a8cd-130">Using Windows Media With DirectShow Editing Services</span></span>](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



