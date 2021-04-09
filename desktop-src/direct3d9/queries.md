---
description: 有數種類型的查詢是設計用來查詢資源的狀態。
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: " (Direct3D 9) 的查詢"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845732"
---
# <a name="queries-direct3d-9"></a> (Direct3D 9) 的查詢

有數種類型的查詢是設計用來查詢資源的狀態。 指定資源的狀態包括圖形處理單位 (GPU) 狀態、驅動程式狀態或執行時間狀態。 若要瞭解不同查詢類型之間的差異，您需要瞭解查詢狀態。 下列狀態轉換圖說明每個查詢狀態。

![顯示查詢狀態之間轉換的圖表](images/queries.png)

下圖顯示三種狀態，每個都是由圓形所定義。 每一條實線都是導致狀態轉換的應用程式驅動事件。 虛線是資源驅動事件，會將查詢從發出的狀態切換至已發出信號的狀態。 這些狀態各有不同的用途：

-   信號狀態就像是閒置狀態。 已產生查詢物件，並正在等候應用程式發出查詢。 當查詢完成並轉換回已發出信號的狀態之後，就可以取出查詢的答案。
-   建築物狀態就像是查詢的臨時區域。 從大樓狀態中， (藉由呼叫 [**D3DISSUE \_ BEGIN**](d3dissue-begin.md)) 來發出查詢，但尚未轉換成已發行的狀態。 當應用程式透過呼叫 [**D3DISSUE \_ end**](d3dissue-end.md)) 發出查詢結束 (時，查詢會轉換成已發出的狀態。
-   「已發出」狀態表示所查詢的資源具有查詢的控制權。 一旦資源完成其工作，資源就會將狀態機器轉換成已發出信號的狀態。 在「已發出」狀態期間，應用程式必須輪詢以偵測轉換為已發出信號的狀態。 一旦轉換至已發出信號的 [**狀態，則**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 會透過應用程式) 引數傳回查詢結果 (。

下表列出可用的查詢類型。



| 查詢類型        | 問題事件                                                                      | 有其的緩衝區                                                              | 執行階段      | 查詢的隱含開頭                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| BANDWIDTHTIMINGS  | [**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | 零售/Debug | N/A                                              |
| CACHEUTILIZATION  | [**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | 零售/Debug | N/A                                              |
| 事件             | [**D3DISSUE \_ 結束**](d3dissue-end.md)                                            | BOOL                                                                        | 零售/Debug | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| INTERFACETIMINGS  | [**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | 零售/Debug | N/A                                              |
| 閉塞         | [**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md) | DWORD                                                                       | 零售/Debug | N/A                                              |
| PIPELINETIMINGS   | [**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | 零售/Debug | N/A                                              |
| RESOURCEMANAGER   | [**D3DISSUE \_ 結束**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md)           | 僅限 Debug   | [**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**D3DISSUE \_ 結束**](d3dissue-end.md)                                            | UINT64                                                                      | 零售/Debug | N/A                                              |
| TIMESTAMPDISJOINT | [**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md) | BOOL                                                                        | 零售/Debug | N/A                                              |
| TIMESTAMPFREQ     | [**D3DISSUE \_ 結束**](d3dissue-end.md)                                            | UINT64                                                                      | 零售/Debug | N/A                                              |
| VCACHE            | [**D3DISSUE \_ 結束**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ VCACHE**](d3ddevinfo-vcache.md)                             | 零售/Debug | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| VERTEXSTATS       | [**D3DISSUE \_ 結束**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | 僅限 Debug   | [**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| VERTEXTIMINGS     | [**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | 零售/Debug | N/A                                              |



 

有些查詢需要 begin 和 end 事件，有些則只需要 end 事件。 當另一個隱含事件發生時，只需要結束事件的查詢就會開始 (此) 表中列出。 所有查詢都會傳回答案，但答案一律 **為 TRUE** 的事件查詢除外。 應用程式會使用查詢的狀態或有 [**可能的傳回碼。**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)

## <a name="create-a-query"></a>建立查詢

在您建立查詢之前，您可以藉由呼叫 [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) 與 **Null** 指標（如下所示）來檢查執行時間是否支援查詢：


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



如果可以建立查詢，這個方法會傳回成功的程式碼;否則會傳回錯誤碼。 [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)成功之後，您就可以建立如下的查詢物件：


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



如果此呼叫成功，則會建立查詢物件。 此查詢基本上是閒置的信號狀態 (有未初始化的回應) 等候發出。 當您完成查詢時，請將它當作任何其他介面來釋放。

## <a name="issue-a-query"></a>發出查詢

應用程式會藉由發出查詢來變更查詢狀態。 以下是發出查詢的範例：


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



發出信號狀態的查詢會在發出時轉換如下：



| 問題類型                                | 查詢會轉換至。 . . |
|-------------------------------------------|--------------------------------|
| [**D3DISSUE \_ 開始**](d3dissue-begin.md) | 建立狀態。                |
| [**D3DISSUE \_ 結束**](d3dissue-end.md)     | 已發行狀態。                  |



 

發出時，建立狀態的查詢會如下所示轉換：



| 問題類型                                | 查詢會轉換至。 . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**D3DISSUE \_ 開始**](d3dissue-begin.md) |  (沒有任何轉換，則會維持在大樓狀態。 重新開機查詢括弧。 )  |
| [**D3DISSUE \_ 結束**](d3dissue-end.md)     | 已發行狀態。                                                             |



 

發出時，發出狀態的查詢會如下所示轉換：



| 問題類型                                | 查詢會轉換至。 . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**D3DISSUE \_ 開始**](d3dissue-begin.md) | 建立狀態並重新啟動查詢括弧。    |
| [**D3DISSUE \_ 結束**](d3dissue-end.md)     | 放棄常設查詢之後發出的狀態。 |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>檢查查詢狀態並取得查詢的答案

[](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)有兩個專案：

1.  傳回傳回碼中的查詢狀態。
2.  傳回 *.pdata* 中的查詢答案。

從三個查詢狀態中的每一個，以下是有 [**數量的傳回**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 碼：



| 查詢狀態 | 有其傳回碼 |
|-------------|---------------------|
| 暗示    | S \_ 確定               |
| 建置    | 錯誤碼          |
| 已發出      | S \_ FALSE            |



 

例如，當查詢處於「已發行」 [**狀態，而**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 查詢的答案無法使用時，[操作] 會傳回 \_ FALSE。 當資源完成其工作，且應用程式已發出查詢結束時，資源會將查詢轉換為已發出信號的狀態。 從信號的狀態中 **，「** 操作」 \_ 會傳回「確定」，表示查詢的答案也會在 *.pdata* 中傳回。 例如，以下是傳回轉譯順序中所繪製之圖元數目的事件順序：

-   建立查詢。
-   發出開始事件。
-   繪製一些東西。
-   發出結束事件。

以下是對應的程式碼序列：


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



這幾行程式碼會執行幾項作業：

-   呼叫 [**，**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 以傳回繪製的圖元數。
-   指定 [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) ，讓資源能夠將查詢轉換為已發出信號的狀態。
-   藉 [**由從迴圈**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 呼叫 [已建立] 來輪詢查詢資源。 **只要操作** 單位 \_ 傳回 FALSE，這表示資源尚未傳回答案。

[確定 [**] 的傳回值基本上會**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 告知您該查詢的狀態。 可能的值為 \_ [確定]、[ \_ FALSE] 和 [錯誤]。 請勿在處於建立狀態的 **查詢上呼叫** [操作]。

-   S \_ OK 表示資源 (GPU 或驅動程式，或執行時間) 已完成。 此查詢會返回信號狀態。 如果有任何) 是由 [**操作者傳回，就**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)會 (答案。
-   \_FALSE 表示資源 (GPU 或驅動程式，或執行時間) 無法傳回答案。 這可能是因為 GPU 未完成或尚未看過工作。
-   錯誤表示查詢產生了無法復原的錯誤。 如果裝置在查詢期間遺失，就可能發生這種情況。 一旦查詢產生的錯誤 (不是 \_ FALSE) ，就必須重新建立查詢，這會從已發出信號的狀態重新開機查詢順序。

除了指定 [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md)（這會提供最新的資訊）之外，您還可以提供零，如果查詢處於「已發行」狀態，這會是較輕量的檢查。 提供零 [**會導致無法**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 排清命令緩衝區。 基於這個理由，請務必小心避免 infinate 迴圈 **(如需** 詳細資料，請參閱 [) ]。 由於執行時間會在命令緩衝區中排入佇列，所以 D3DGETDATA 排清是將命令緩衝區排到驅動程式 (的機制，因此也是 GPU; 請參閱 [ (direct3d 9) ) 中正確分析 DIRECT3D API 呼叫](accurately-profiling-direct3d-api-calls.md)。 **\_** 在命令緩衝區排清期間，查詢可能會轉換成已發出信號的狀態。

## <a name="example-an-event-query"></a>範例：事件查詢

事件查詢不支援 begin 事件。

-   建立查詢。
-   發出結束事件。
-   輪詢直到 GPU 閒置為止。
-   發出結束事件。


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



這是事件查詢用來分析應用程式開發介面 (API) 呼叫的命令順序 (請參閱 [ (direct3d 9) ) 中正確分析 DIRECT3D API 呼叫 ](accurately-profiling-direct3d-api-calls.md) 。 此順序會使用標記來協助控制命令緩衝區中的工作量。

請注意，應用程式應該特別注意與清除命令緩衝區相關聯的大型成本，因為這會導致作業系統切換至核心模式，因此會造成相當大的效能影響。 應用程式也應該注意，藉由等候查詢完成來浪費 CPU 週期。

查詢是在轉譯期間用來提升效能的優化。 因此，花時間等候查詢完成並不會有説明。 如果發出查詢，而且應用程式在檢查這些結果時尚未準備好這些結果，則優化的嘗試不會成功，且轉譯應正常地繼續進行。

此範例的典型範例是在遮蔽的剔除期間。 使用查詢的應用程式不會使用上述 **while** 迴圈，而是會執行遮蔽的剔除，以查看查詢是否在需要結果時完成。 如果查詢尚未完成，請在最糟的情況下繼續 (，) 就像是針對進行測試的物件不是 pixels occluded 一樣 (也就是可見) 並加以呈現。 程式碼看起來會如下所示。


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 主題](advanced-topics.md)
</dt> </dl>

 

 
