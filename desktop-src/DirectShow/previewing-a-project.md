---
description: 預覽 Project
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: 預覽 Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159303c175c459b4d5d93ba4c7b4b2622caddac2a35d3474a3059ac703d62645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583557"
---
# <a name="previewing-a-project"></a>預覽 Project

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

若要預覽專案，請先呼叫 **CoCreateInstance** 來建立基本轉譯引擎的實例。 類別識別碼是 CLSID \_ RenderEngine。 然後呼叫 [**IRenderEngine：： SetTimelineObject**](irenderengine-settimelineobject.md) 方法，以指定您要轉譯的時間軸。

當您第一次預覽時程表時，請依列出的循序執行下列呼叫：

1.  呼叫 [**IRenderEngine：： SetRenderRange**](irenderengine-setrenderrange.md) ，以指定要預覽的時間軸部分。 (選用)
2.  呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 來建立圖形的前端。
3.  呼叫 [**IRenderEngine：： RenderOutputPins**](irenderengine-renderoutputpins.md)。 此方法會將每個輸出圖釘連接至影片轉譯器或音訊轉譯器，以完成圖形。

下列程式碼範例會顯示這些步驟：


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



現在執行篩選圖形。 首先，呼叫 [**IRenderEngine：： GetFilterGraph**](irenderengine-getfiltergraph.md)方法，以取得篩選 Graph 管理員的 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)介面指標。 然後查詢 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)介面的篩選 Graph 管理員，然後呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)，如下列程式碼所示：


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



使用 Filter Graph Manager 的 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)介面來等候預覽完成。 您也可以使用 Filter Graph Manager 的 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)介面來搜尋圖形，就像使用檔案播放圖表一樣。

若要再次預覽專案，請將圖形向上搜尋至時間零，然後再次呼叫 **執行** 。 如果您變更時間軸的內容，請執行下列動作：

1.  呼叫 **SetRenderRange**。 (選用)
2.  呼叫 **ConnectFrontEnd**。
3.  如果 **ConnectFrontEnd** 方法傳回 S \_ 警告 \_ OUTPUTRESET，請呼叫 **RenderOutputPins**。  (如果 **ConnectFrontEnd** 傳回 S \_ OK，您可以略過此步驟。 ) 
4.  將圖形向後搜尋至時間零。
5.  執行圖形。

下列範例會顯示這些步驟：


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



如需載入和預覽專案檔的完整範例，請參閱[載入和預覽 Project](loading-and-previewing-a-project.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理影片編輯專案](managing-video-editing-projects.md)
</dt> <dt>

[轉譯 Project](rendering-a-project.md)
</dt> </dl>

 

 



