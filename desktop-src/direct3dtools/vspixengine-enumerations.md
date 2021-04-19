---
description: 下列列舉是在 vspixengine 中宣告。
MS-HAID: vspixengine.vspixengine\_enumerations
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Direct3D 診斷 Capture 介面列舉
ms.topic: article
ms.date: 05/31/2018
ms.assetid: A67402DE-8CBF-470A-97B4-3CF531731F24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 059f91aa806afd60d5efe755d015495eb2f445f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106998041"
---
# <a name="span-idvspixenginevspixengine_enumerationsspandirect3d-diagnostics-capture-interface-enumerations"></a><span id="vspixengine.vspixengine_enumerations"></span>Direct3D 診斷 Capture 介面列舉

下列列舉是在 vspixengine 中宣告。

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>本節內容

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>主題</th><th>描述</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/xml-resource-ids"><strong>Xml_Resource_Ids</strong></a></p></td><td><p>由呼叫端設定以視覺化物件的 xml 資料傳回的資源字串識別碼</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/resource-id"><strong>Resource_Id</strong></a></p></td><td><p>定義共用字串資源的資源識別碼。 這些會從主機傳遞至 capture engine。 它們可用來顯示所要抬頭顯示器之應用程式的重迭字串，或是將登錄值從 Visual Studio 選項傳遞至 capture engi</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/hresult"><strong>Hresult</strong></a></p></td><td><p>圖形診斷捕捉介面的自訂 HRESULT 值。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/remotecommandtype"><strong>RemoteCommandType</strong></a></p></td><td><p>用來在 capture 引擎和主機 (（例如 Visual Studio 圖形診斷) ）之間進行通訊的列舉。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/callbackcommandtype"><strong>CallbackCommandType</strong></a></p></td><td><p>用來在 capture 引擎和主機 (（例如 Visual Studio 圖形診斷) ）之間進行通訊的列舉。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixpiperesponse"><strong>PixPipeResponse</strong></a></p></td><td><p>用來將回應從捕捉引擎傳送至圖形診斷的列舉。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/remotingversion"><strong>REMOTINGVERSION</strong></a></p></td><td><p>列舉，用來指出正在使用的遠端 protocul 版本。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelkillreason"><strong>PIXELKILLREASON</strong></a></p></td><td><p>用來指出如何拒絕圖元的列舉。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryflags"><strong>PIXELHISTORYFLAGS</strong></a></p></td><td><p>列舉，其中包含用來描述圖元歷程記錄結果的旗標。 請參閱 PixelHistoryOperation。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/eventcolumnid"><strong>EVENTCOLUMNID</strong></a></p></td><td><p>用來指出已知資料行識別碼的列舉;這些都是所有執行都應該支援的資料行識別碼。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/objectstatetype"><strong>OBJECTSTATETYPE</strong></a></p></td><td><p>內部</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/objecttablecolumnid"><strong>OBJECTTABLECOLUMNID</strong></a></p></td><td><p>列舉，用來指出從物件資料表要求傳回的資料屬性。 如需詳細資訊，請參閱 IObjectTableRequest。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestages"><strong>PIPELINESTAGES</strong></a></p></td><td><p>用來表示圖形管線階段的列舉。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/checksumalgorithm"><strong>CHECKSUMALGORITHM</strong></a></p></td><td><p>用來指出要使用之總和檢查碼演算法的列舉。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/eventtype"><strong>事件</strong></a></p></td><td><p>用來表示事件種類的列舉。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-header-columns"><strong>DESCRIPTOR_HEAP_HEADER_COLUMNS</strong></a></p></td><td><p>用來指出描述項堆積檢視器中 coumn 標頭的列舉</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-columns"><strong>DESCRIPTOR_HEAP_COLUMNS</strong></a></p></td><td><p>列舉，用來表示描述項堆積檢視器中的資料行。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttype"><strong>EXPERIMENTTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/dumpertype"><strong>DUMPERTYPE</strong></a></p></td><td><p>列舉，用來指出 IGenericBufferDataRequest 傳回的緩衝區類型。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttriggertype"><strong>EXPERIMENTTRIGGERTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/register-format"><strong>REGISTER_FORMAT</strong></a></p></td><td><p>內部</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/primitive-topology"><strong>PRIMITIVE_TOPOLOGY</strong></a></p></td><td><p>用來表示網格拓撲的列舉。 請參閱 MeshDataVertCallback。</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysisstage"><strong>OFFLINEANALYSISSTAGE</strong></a></p></td><td><p>用來表示畫面格分析中進度階段的列舉。</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysissource"><strong>OFFLINEANALYSISSOURCE</strong></a></p></td><td><p>用於表示畫面格分析之圖形資訊來源的列舉。</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>相關主題

[Direct3D 診斷 Capture 介面參考](vspixengine-reference.md)

 

 
