---
description: 在 DirectShow 編輯服務中選取解碼器
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: 在 DirectShow 編輯服務中選取解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467639"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>在 DirectShow 編輯服務中選取解碼器

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

當 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 轉譯影片編輯專案時，轉譯引擎會自動選取必要的解碼器。 這可能會發生在 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法內，或在轉譯期間以動態方式發生。

使用者可能會安裝數個可以解碼特定檔案的解碼器。 當有多個可用的解碼器時，DES 會使用 [智慧型連接](intelligent-connect.md) 演算法來選取解碼器。

沒有任何方法可讓應用程式直接指定要使用哪個解碼器。 不過，您可以透過 [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) 回呼介面間接選擇此解碼器。 藉由在您的應用程式中執行此介面，您可以在圖形建立程式期間收到通知，並從圖形拒絕某些篩選。

首先，執行公開 [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) 介面的類別：


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



然後，建立篩選圖形管理員的實例，並註冊您的類別以接收回呼通知：


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



接下來，請建立轉譯引擎，並呼叫 [**IRenderEngine：： SetFilterGraph**](irenderengine-setfiltergraph.md) 方法，並加上篩選圖形管理員的指標。 這可確保轉譯引擎不會建立自己的篩選圖形管理員，而是會使用您為回呼設定的實例。


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



轉譯專案時，會立即呼叫應用程式的 [**IAMGraphBuilderCallback：： SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) 方法，然後篩選圖形管理員才會建立新的篩選。 **SelectedFilter** 方法會接收 **IMoniker** 介面的指標，該介面表示篩選的標記。 檢查標記，如果您決定拒絕篩選，請從 **SelectedFilter** 方法傳回失敗碼。

困難的部分是找出哪些名字代表了它們，尤其是哪一個名字代表您要拒絕的解碼器。 其中一個解決方案如下：

-   轉譯專案之前，請使用 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) 方法來建立已註冊為接受所需輸入類型的篩選器清單。 針對影片或音訊壓縮類型，此清單應對應至一組解碼器。
-   **EnumMatchingFilters** 方法會傳回一個名字組的集合。 針對集合中的每個標記，取得 **DisplayName** 屬性，如 [使用篩選器](using-the-filter-mapper.md)對應程式中所述。
-   儲存顯示名稱清單，但省略符合您要用於解碼之篩選的顯示名稱。 軟體篩選器的顯示名稱具有下列格式：

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    其中

    ```C++
    CategoryGUID
    ```

    

    這是篩選準則分類的 GUID，而

    ```C++
    FilterCLSID
    ```

    

    這是篩選的 CLSID。 若為 DMOs，格式會相同，但會變更 `sw` 為 `dmo` 。

    清單現在包含輸出所需媒體類型，但不是您慣用篩選的每個篩選器的顯示名稱。

-   在 **SelectedFilter** 方法中，取得建議的標記上的 **DisplayName** 屬性，並針對儲存的清單進行檢查。 如果顯示名稱符合清單中的專案，則拒絕該篩選。 否則，請返回 \_ [確定] 以接受它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯專案](rendering-a-project.md)
</dt> </dl>

 

 



