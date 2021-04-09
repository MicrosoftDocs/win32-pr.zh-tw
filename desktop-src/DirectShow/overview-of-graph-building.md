---
description: 圖表建立的總覽
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: 圖表建立的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109077"
---
# <a name="overview-of-graph-building"></a>圖表建立的總覽

若要建立篩選圖形，請先建立篩選圖形管理員的實例：


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



篩選圖形管理員支援下列圖表建立方法：

-   [**IFilterGraph：： ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) 會嘗試在兩個 pin 之間進行直接連接。 如果 pin 無法連接，則方法會失敗。
-   [**IGraphBuilder：： Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) 連接兩個圖釘。 可能的話，它會直接連接。 否則，它會使用中繼篩選來完成連接。
-   [**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 會從輸出圖釘開始，並建立圖形的其餘部分。 此方法會視需要新增篩選準則，直到到達轉譯器篩選器為止。
-   [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 會建立完整的檔案播放圖形。
-   [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將篩選新增至圖形。 它不會連接篩選。 您必須藉由呼叫 **CoCreateInstance** 或使用篩選器對應程式或系統裝置列舉值，在呼叫這個方法之前建立篩選。

這些方法提供三種基本的方法來建立圖形：

1.  篩選圖形管理員會建立整個圖形。
2.  篩選圖形管理員會建立圖形的一部分。
3.  應用程式會建立整個圖形。

**篩選圖形管理員會建立整個圖形**

如果您只想要播放以可辨識格式（例如 AVI、MPEG、WAV 或 MP3）撰寫的檔案，請使用 **RenderFile** 方法。 如何 [播放](how-to-play-a-file.md) 檔案的文章會說明如何進行。

**RenderFile** 方法一開始會在登錄中查看可剖析檔案的來源篩選。 它會使用通訊協定 (例如 URL) 中的 " `https://` "、副檔名，或檔案中預先定義的位元組模式，以決定來源篩選。 如需詳細資訊，請參閱 [註冊自訂檔案類型](registering-a-custom-file-type.md)。

若要建立圖形的其餘部分，篩選圖形管理員會使用反復的程式，其中會採用篩選器在其輸出圖釘上支援的媒體類型，並搜尋登錄中是否接受該媒體類型作為輸入的篩選器。 它會使用數個準則來縮小搜尋範圍並設定篩選優先順序：

-   *篩選準則類別* 識別篩選準則的一般功能。
-   媒體類型描述篩選可接受做為輸入或作為輸出傳遞的資料類型。
-   這些 *業績* 決定了篩選準則的嘗試順序。 如果相同篩選準則類別中的兩個篩選準則都支援相同的輸入類型，則篩選圖形管理員會選取具有最高品質值的篩選。 某些篩選器會刻意獲得較低的價值，因為它們是針對特定用途而設計，而且只應由應用程式新增至圖形。

篩選圖形管理員會使用 [篩選器](filter-mapper.md) 對應程式物件來搜尋登錄。

新增每個篩選器時，篩選圖形管理員會嘗試將它連接到先前篩選的輸出圖釘。 篩選準則會進行協調以判斷它們是否可以連接，如果是，要使用哪種媒體類型來連接。 如果新的篩選無法連接，則篩選圖形管理員會捨棄它，並嘗試另一個篩選準則。 此程式會繼續進行，直到轉譯每個資料流程為止。

**篩選圖形管理員會建立圖形的一部分**

若要執行不只是播放檔案的動作，您的應用程式至少必須執行部分圖形建築工作。 例如，影片捕獲應用程式必須選取捕獲來源篩選器，並將它新增至圖形。 如果您要將資料寫入至 AVI 檔案，您必須將 AVI Mux 和檔案寫入器篩選器新增至圖形。 不過，通常可以讓篩選圖形管理員完成圖形。 例如，您可以藉由呼叫 **render** 方法來呈現預覽的 pin。

**應用程式會建立整個圖形**

在某些情況下，您的應用程式可能需要加入並連接每個篩選器來建立圖形。 在此情況下，您可能會特別知道哪些篩選準則應該新增至圖形。 使用這個方法時，應用程式會藉由呼叫 **AddFilter** 來新增每個篩選，列舉篩選上的釘選，然後藉由呼叫 **Connect** 或 **ConnectDirect** 來連接它們。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Capture Graph Builder 建立圖形](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[列舉裝置和篩選器](enumerating-devices-and-filters.md)
</dt> <dt>

[列舉篩選圖形中的物件](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[一般 Graph-Building 技術](general-graph-building-techniques.md)
</dt> <dt>

[建立篩選圖形](building-the-filter-graph.md)
</dt> </dl>

 

 



