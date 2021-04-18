---
description: 下列結構是在 vspixengine 中宣告。
MS-HAID: vspixengine.vspixengine\_structures
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Direct3D 診斷 Capture 介面結構
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 97F142F6-FED1-4AF4-B9E3-BB1E30F3FAD2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e1cefcf539996765b2e8055060277665f3cb9d31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510037"
---
# <a name="span-idvspixenginevspixengine_structuresspandirect3d-diagnostics-capture-interface-structures"></a><span id="vspixengine.vspixengine_structures"></span>Direct3D 診斷 Capture 介面結構

下列結構是在 vspixengine 中宣告。

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>本節內容

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>主題</th><th>描述</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/resourcepair"><strong>ResourcePair</strong></a></p></td><td><p>表示以 COM 字串編碼的共用資源。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptorheaprecord"><strong>DescriptorHeapRecord</strong></a></p></td><td><p>表示描述項堆積資訊。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestageerror"><strong>PipeLineStageError</strong></a></p></td><td><p>表示管線階段中的錯誤。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pipelinestage"><strong>PipeLineStage</strong></a></p></td><td><p>表示管線階段，包括所使用之著色器的詳細資料。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/experimenttrigger"><strong>ExperimentTrigger</strong></a></p></td><td><p>代表實驗觸發程式資訊。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/packedcallpkg"><strong>PackedCallPkg</strong></a></p></td><td><p>代表四個呼叫的封裝。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/symbolserverinfo"><strong>SymbolServerInfo</strong></a></p></td><td><p>表示 debug 符號伺服器的相關資訊。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/callstackframe"><strong>CallStackFrame</strong></a></p></td><td><p>代表呼叫堆疊上框架的相關資訊。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/sourcefileinfo"><strong>SourceFileInfo</strong></a></p></td><td><p>表示原始程式碼檔的相關資訊。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/summaryitem"><strong>SummaryItem</strong></a></p></td><td><p>表示事件的摘要資訊。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/debugshader"><strong>DebugShader</strong></a></p></td><td><p>表示有關偵錯工具下之著色器的資訊。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experiment"><strong>實驗</strong></a></p></td><td><p>表示實驗 (capture) 的相關資訊。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/issue"><strong>問題</strong></a></p></td><td><p>代表問題的相關資訊。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/point2d"><strong>Point2D</strong></a></p></td><td><p>代表具有不帶正負號整數座標的2D 點。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/threaddata3d"><strong>ThreadData3D</strong></a></p></td><td><p>表示線上程資料中的3D 索引</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/inputlayoutstruct"><strong>InputLayoutStruct</strong></a></p></td><td><p>表示頂點緩衝區的輸入配置欄位，在頂點緩衝區中每個欄位一個。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryoperation"><strong>PixelHistoryOperation</strong></a></p></td><td><p>代表圖元歷程記錄的相關資訊。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryintersection"><strong>PixelHistoryIntersection</strong></a></p></td><td><p>代表特定的相關資訊</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/meshdatabufferlayoutentry"><strong>MeshDataBufferLayoutEntry</strong></a></p></td><td><p>表示網格的緩衝區配置中單一專案的相關資訊。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/debugshaderrequestinfo"><strong>DebugShaderRequestInfo</strong></a></p></td><td><p>表示著色器偵錯工具要求的相關資訊。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixengineint4"><strong>PixEngineInt4</strong></a></p></td><td><p>代表具有帶正負號整數座標的4D 向量。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginepoint4d"><strong>PixEnginePoint4D</strong></a></p></td><td><p>表示具有64位浮點數 (雙) 座標的4D 點。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginechanneldesc"><strong>PixEngineChannelDesc</strong></a></p></td><td><p>表示色彩 (範例) 通道的描述。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureformatdesc"><strong>PixEngineTextureFormatDesc</strong></a></p></td><td><p>代表材質格式的描述。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturedescriptor"><strong>PixEngineTextureDescriptor</strong></a></p></td><td><p>代表材質資源的描述。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureslicedescriptor"><strong>PixEngineTextureSliceDescriptor</strong></a></p></td><td><p>代表材質配量的描述。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturesliceindex"><strong>PixEngineTextureSliceIndex</strong></a></p></td><td><p>代表材質配量的索引</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginehistogram"><strong>PixEngineHistogram</strong></a></p></td><td><p>代表材質的長條圖。</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>相關主題

[Direct3D 診斷 Capture 介面參考](vspixengine-reference.md)

 

 
