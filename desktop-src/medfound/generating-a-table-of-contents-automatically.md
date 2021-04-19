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
# <a name="generating-a-table-of-contents-automatically"></a>自動產生目錄

本主題示範如何使用目錄產生器 (TOC 產生器) 元件來自動產生影片檔案 [**的目錄。**](/previous-versions/ee264297(v=vs.85))

TOC 產生器是 (SQL-DMO) 的 DirectX 媒體物件。 若要使用 TOC 產生器，請建立具有影片檔案作為其來源的 DirectX 篩選圖形。 在篩選圖形中插入 TOC 發電機，然後執行圖形。 然後，您可以從 TOC 產生器中取得自動產生的目錄。

下列程式提供更詳細的步驟。

1.  呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立篩選繪圖物件 (**CLSID \_ FilterGraph**) 並取得 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) 介面。
2.  Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.
3.  將 **CLSID \_ CTocGeneratorDmo** 傳遞至您的 sql-dmo 包裝函式篩選器的 [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) 方法。 這會建立 TOC 產生器，並將它包裝在您的 SQL-DMO 包裝函式篩選器中。
4.  呼叫 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)介面的 [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter)方法，將包裝的 TOC 產生器，加入至篩選圖形。
    > [!Note]  
    > [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) 繼承自 [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph)。

     

5.  呼叫 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)介面的 [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter)方法，以建立源篩選，並將其新增至圖形。
6.  在 SQL-DMO 包裝函式篩選和來源篩選上列舉圖釘。 這牽涉到取得 [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) 介面和 [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) 介面。
7.  藉由呼叫 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)介面的 [**connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect)方法，來連接來源篩選器和包裝函式篩選。
8.  藉由呼叫 [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder)介面的 [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render)方法來完成圖形。
9.  執行 graph ([**IMediaControl：： run**](/windows/win32/api/control/nf-control-imediacontrol-run)) ，並等候它完成 ([**IMediaEvent：： WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)) 。
10. 取得您的 SQL-DMO 篩選包裝函式的 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面，並取得 [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) 屬性的值。 視需要重複執行，直到目錄就緒為止。
11. 您可以使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面來取得 [**MFPKEY \_ TOCGENERATOR \_ TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) 屬性的值。 這個屬性是 [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) 介面，代表自動產生的目錄。

下列程式碼示範自動產生目錄的程式。 此程式碼會使用三個 helper 函式 ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md)、 [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)和 [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) ，這些功能會顯示在本檔的其他頁面上。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[用來產生目錄的 BuildGraph 函式](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[用來產生目錄的 GetToc 函式](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[用來產生目錄的 RunGraphAndWait 函式](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[目錄剖析器程式設計指南](toc-parser-programming-guide.md)
</dt> </dl>

 

 
