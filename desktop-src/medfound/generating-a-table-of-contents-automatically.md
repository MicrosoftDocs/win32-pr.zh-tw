---
description: 自動產生目錄
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: 自動產生目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22adc4d48ad7f4b1d89a446eb28c25d6011804a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966653"
---
# <a name="generating-a-table-of-contents-automatically"></a><span data-ttu-id="0f99a-103">自動產生目錄</span><span class="sxs-lookup"><span data-stu-id="0f99a-103">Generating a Table of Contents Automatically</span></span>

<span data-ttu-id="0f99a-104">本主題示範如何使用目錄產生器 (TOC 產生器) 元件來自動產生影片檔案 [**的目錄。**](/previous-versions/ee264297(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f99a-104">This topic demonstrates how to use [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (TOC Generator) component to automatically generate a table of contents for a video file.</span></span>

<span data-ttu-id="0f99a-105">TOC 產生器是 (SQL-DMO) 的 DirectX 媒體物件。</span><span class="sxs-lookup"><span data-stu-id="0f99a-105">TOC Generator is a DirectX Media Object (DMO).</span></span> <span data-ttu-id="0f99a-106">若要使用 TOC 產生器，請建立具有影片檔案作為其來源的 DirectX 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="0f99a-106">To use the TOC Generator DMO, build a DirectX filter graph that has a video file as its source.</span></span> <span data-ttu-id="0f99a-107">在篩選圖形中插入 TOC 發電機，然後執行圖形。</span><span class="sxs-lookup"><span data-stu-id="0f99a-107">Insert the TOC Generator DMO into the filter graph, and run the graph.</span></span> <span data-ttu-id="0f99a-108">然後，您可以從 TOC 產生器中取得自動產生的目錄。</span><span class="sxs-lookup"><span data-stu-id="0f99a-108">You can then obtain the automatically generated table of contents from the TOC Generator DMO.</span></span>

<span data-ttu-id="0f99a-109">下列程式提供更詳細的步驟。</span><span class="sxs-lookup"><span data-stu-id="0f99a-109">The following procedure gives the steps in more detail.</span></span>

1.  <span data-ttu-id="0f99a-110">呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立篩選繪圖物件 (**CLSID \_ FilterGraph**) 並取得 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) 介面。</span><span class="sxs-lookup"><span data-stu-id="0f99a-110">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a Filter Graph object (**CLSID\_FilterGraph**) and obtain an [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
2.  <span data-ttu-id="0f99a-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span><span class="sxs-lookup"><span data-stu-id="0f99a-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="0f99a-112">將 **CLSID \_ CTocGeneratorDmo** 傳遞至您的 sql-dmo 包裝函式篩選器的 [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) 方法。</span><span class="sxs-lookup"><span data-stu-id="0f99a-112">Pass **CLSID\_CTocGeneratorDmo** to the [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) method of your DMO wrapper filter.</span></span> <span data-ttu-id="0f99a-113">這會建立 TOC 產生器，並將它包裝在您的 SQL-DMO 包裝函式篩選器中。</span><span class="sxs-lookup"><span data-stu-id="0f99a-113">This creates a TOC Generator DMO and wraps it in your DMO wrapper filter.</span></span>
4.  <span data-ttu-id="0f99a-114">呼叫 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)介面的 [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter)方法，將包裝的 TOC 產生器，加入至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="0f99a-114">Call the [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to add the wrapped TOC Generator DMO to the filter graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="0f99a-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) 繼承自 [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph)。</span><span class="sxs-lookup"><span data-stu-id="0f99a-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) inherits from [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span></span>

     

5.  <span data-ttu-id="0f99a-116">呼叫 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)介面的 [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter)方法，以建立源篩選，並將其新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="0f99a-116">Call the [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to create a souce filter and add it to the graph.</span></span>
6.  <span data-ttu-id="0f99a-117">在 SQL-DMO 包裝函式篩選和來源篩選上列舉圖釘。</span><span class="sxs-lookup"><span data-stu-id="0f99a-117">Enumerate pins on the DMO wrapper filter and the source filter.</span></span> <span data-ttu-id="0f99a-118">這牽涉到取得 [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) 介面和 [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) 介面。</span><span class="sxs-lookup"><span data-stu-id="0f99a-118">This involves obtaining [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) interfaces and [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) interfaces.</span></span>
7.  <span data-ttu-id="0f99a-119">藉由呼叫 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)介面的 [**connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect)方法，來連接來源篩選器和包裝函式篩選。</span><span class="sxs-lookup"><span data-stu-id="0f99a-119">Connect the source filter and the wrapper filter by calling the [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
8.  <span data-ttu-id="0f99a-120">藉由呼叫 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)介面的 [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render)方法來完成圖形。</span><span class="sxs-lookup"><span data-stu-id="0f99a-120">Complete the graph by calling the [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
9.  <span data-ttu-id="0f99a-121">執行 graph ([**IMediaControl：： run**](/windows/win32/api/control/nf-control-imediacontrol-run)) ，並等候它完成 ([**IMediaEvent：： WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)) 。</span><span class="sxs-lookup"><span data-stu-id="0f99a-121">Run the graph ([**IMediaControl::Run**](/windows/win32/api/control/nf-control-imediacontrol-run)), and wait for it to complete ([**IMediaEvent::WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span></span>
10. <span data-ttu-id="0f99a-122">取得您的 SQL-DMO 篩選包裝函式的 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面，並取得 [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0f99a-122">Obtain an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface on your DMO filter wrapper, and get the value of the [**MFPKEY\_TOCGENERATOR\_TOCREADY**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="0f99a-123">視需要重複執行，直到目錄就緒為止。</span><span class="sxs-lookup"><span data-stu-id="0f99a-123">Repeat if necessary until the table of contents is ready.</span></span>
11. <span data-ttu-id="0f99a-124">您可以使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面來取得 [**MFPKEY \_ TOCGENERATOR \_ TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0f99a-124">Use your [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to get the value of the [**MFPKEY\_TOCGENERATOR\_TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="0f99a-125">這個屬性是 [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) 介面，代表自動產生的目錄。</span><span class="sxs-lookup"><span data-stu-id="0f99a-125">This property is an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface that represents the automatically generated table of contents.</span></span>

<span data-ttu-id="0f99a-126">下列程式碼示範自動產生目錄的程式。</span><span class="sxs-lookup"><span data-stu-id="0f99a-126">The following code demonstrates the procedure for generating a table of contents automatically.</span></span> <span data-ttu-id="0f99a-127">此程式碼會使用三個 helper 函式 ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md)、 [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)和 [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) ，這些功能會顯示在本檔的其他頁面上。</span><span class="sxs-lookup"><span data-stu-id="0f99a-127">The code uses three helper functions ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md), and [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) that are shown on other pages of this documentation.</span></span>


```C++
#include <dshow.h>
#include <dmodshow.h>
#include <wmcodecdsp.h>
#include <dmoreg.h>
#include <propsys.h>
#include <propidl.h>
#include <initguid.h>

HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc);
HRESULT RunGraphAndWait(IGraphBuilder* pGraph);
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap);

WCHAR g_sourceFile[] = L"c:\\experiment\\Seattle.wmv";

void main()
{
   HRESULT hr = E_FAIL;
   hr = CoInitialize(NULL);

   if(SUCCEEDED(hr))
   {
      IGraphBuilder* pBuilder = NULL;
      hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
         IID_IGraphBuilder, (VOID**)&pBuilder);

      if(SUCCEEDED(hr))
      {
         IDMOWrapperFilter* pWrap = NULL;
         hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, CLSCTX_INPROC, 
            IID_IDMOWrapperFilter, (VOID**)&pWrap);

         if(SUCCEEDED(hr))
         {
            hr = pWrap->Init(CLSID_CTocGeneratorDmo, DMOCATEGORY_VIDEO_EFFECT); 

            if(SUCCEEDED(hr))
            {
               hr = BuildGraph(pBuilder, pWrap);

               if(SUCCEEDED(hr))
               {
                  hr = RunGraphAndWait(pBuilder);

                  if(SUCCEEDED(hr))
                  {
                     IToc* pToc = NULL;
                     hr = GetToc(pWrap, &pToc);

                     if(SUCCEEDED(hr))
                     {
                        // Inspect the table of contents by calling IToc methods.

                        pToc->Release();
                        pToc = NULL;
                     }
                  }
               }
            }

            pWrap->Release();
            pWrap = NULL;
         }

         pBuilder->Release();
         pBuilder = NULL;
      }

      CoUninitialize();
   }
}
```



## <a name="related-topics"></a><span data-ttu-id="0f99a-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f99a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f99a-129">用來產生目錄的 BuildGraph 函式</span><span class="sxs-lookup"><span data-stu-id="0f99a-129">BuildGraph Function for Generating a Table of Contents</span></span>](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="0f99a-130">用來產生目錄的 GetToc 函式</span><span class="sxs-lookup"><span data-stu-id="0f99a-130">GetToc Function for Generating a Table of Contents</span></span>](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="0f99a-131">用來產生目錄的 RunGraphAndWait 函式</span><span class="sxs-lookup"><span data-stu-id="0f99a-131">RunGraphAndWait Function for Generating a Table of Contents</span></span>](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="0f99a-132">目錄剖析器程式設計指南</span><span class="sxs-lookup"><span data-stu-id="0f99a-132">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
