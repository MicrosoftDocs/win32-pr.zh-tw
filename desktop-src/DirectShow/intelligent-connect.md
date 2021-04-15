---
description: 智慧型連接
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: 智慧型連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aead305867ccec1f1f1f0cbd76c652ba3ec412
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467837"
---
# <a name="intelligent-connect"></a>智慧型連接

智慧型 Connect 是篩選圖形管理員用來建立篩選圖形的機制。 它包含數個相關的演算法，這些演算法會選取篩選並將它們加入至篩選圖形。

如果您在建立特定的篩選圖形時遇到問題，或是您要撰寫自己的篩選準則，而且想要讓它可供自動圖形建立使用，請閱讀本主題。

智慧型連接牽涉到下列 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 方法：

-   [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**IGraphBuilder：： Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>IGraphBuilder::AddSourceFilter

[**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)方法會新增可轉譯指定檔案的來源篩選。 首先，它會在登錄中尋找並比對通訊協定 (例如 `https://`) 、副檔名或預先決定的 *檢查位元組* 集，這是檔案中符合特定模式之特定位移的位元組。 如需詳細資訊，請參閱 [註冊自訂檔案類型](registering-a-custom-file-type.md)。 假設方法找出適當的來源篩選器，則會建立該篩選的實例、將它新增至圖形，然後以檔案名呼叫篩選器的 [**IFileSourceFilter：： Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) 方法。

### <a name="igraphbuilderrender"></a>IGraphBuilder：： Render

[**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)方法會建立圖形的子區段。 它會從未連接的輸出圖釘開始並在下游運作，視需要新增篩選。 起始篩選必須已經在圖形中。 在每個步驟中， **轉譯方法會** 搜尋可連接到先前篩選準則的篩選準則。 如果連接的篩選器有多個輸出圖釘，則資料流程可以分支。 當每個資料流程都有轉譯器時，就會停止搜尋。 如果轉譯 **方法停滯，則可能** 會進行備份，並使用一組不同的篩選器再試一次。

若要連接每個輸出圖釘， [**轉譯方法會**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 執行下列動作：

1.  如果 pin 支援 [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) 介面，則篩選圖形管理員會將整個進程委派給釘選的 [**IStreamBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) 方法。 藉由公開此介面，釘選會負責將圖形的其餘部分分配至轉譯器。 不過，很少 pin 支援此介面。
2.  篩選圖形管理員會嘗試使用在記憶體中快取的篩選（如果有的話）。 在整個智慧型 Connect 程式中，篩選圖形管理員可能會快取程式中先前步驟的篩選。  (也請參閱 [動態圖形建築物](dynamic-graph-building.md)。 ) 
3.  如果篩選圖形包含任何具有未連線輸入圖釘的篩選，則篩選圖形管理員會在接下來嘗試這些篩選器。 您可以藉由 [**在呼叫**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)轉譯之前將該篩選新增至圖形，來強制轉譯方法嘗試特定 **篩選。**
4.  從 Windows 7 開始，DirectShow 有特定媒體子類型的慣用篩選清單。 如果要轉譯的媒體類型有慣用的篩選，則篩選圖形管理員會嘗試下一個篩選準則。 應用程式可以使用 [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) 介面來修改慣用篩選器的清單。 對清單所做的變更會影響應用程式目前的進程，並且會在進程結束之後捨棄。
5.  最後，如果找不到適合的篩選，則篩選圖形管理員會使用 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) 方法來搜尋登錄。 它會嘗試比對輸出 pin 的慣用媒體類型與登錄中列出的媒體類型。

    每個篩選器都是 *以一個好用的值* 來註冊，指出篩選的偏好程度（相對於其他篩選）。 [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters)方法會依下階的順序傳回篩選準則，而最小的優點是 **\_ \_ 不 \_ 使用**+ 1。 它會略過具有 **\_ \_ 未 \_ 使用** 或較少之業績的篩選。 篩選準則也會分組為依 GUID 定義的類別。 類別本身也有其優點，而 **EnumMatchingFilters** 方法會忽略任何具有最少 **\_ \_ \_ 用途** 的類別，即使該類別中的篩選具有較高的業績值也是如此。

    從 Windows 7 開始，DirectShow 具有特定媒體子類型的封鎖篩選清單。 篩選圖形管理員會略過這份清單上的篩選。 應用程式可以使用 [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) 介面來修改封鎖的篩選器清單。 對這份清單所做的變更會影響應用程式目前的進程，並在進程結束之後捨棄。

總而言之， [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 方法會依下列順序嘗試篩選：

1.  使用 [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder)。
2.  嘗試快取篩選。
3.  嘗試在圖形中篩選。
4.  Windows 7 或更新版本：嘗試媒體類型的慣用篩選（如果有的話）。
5.  查閱登錄中的篩選準則。

### <a name="igraphbuilderrenderfile"></a>IGraphBuilder：： RenderFile

[**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)方法會從檔案名建立預設播放圖形。 這個方法會在內部使用 [**AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) 來找出正確的來源篩選 [**，並轉譯**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 以建立圖形的其餘部分。

### <a name="igraphbuilderconnect"></a>IGraphBuilder：： Connect

[**IGraphBuilder：： Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)方法會將輸出圖釘連接至輸入圖釘。 此方法會視需要新增中繼篩選，並使用 [**轉譯方法所**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 述的演算法變化：

1.  嘗試在篩選之間進行直接連接，而不使用中繼篩選。
2.  嘗試快取篩選。
3.  嘗試在圖形中篩選。
4.  Windows 7 或更新版本：嘗試媒體類型的慣用篩選（如果有的話）。
5.  查閱登錄中的篩選準則。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選準則分類](filter-categories.md)
</dt> <dt>

[優點](merit.md)
</dt> <dt>

[使用 GraphEdit 模擬圖表建立](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[建立篩選圖形](building-the-filter-graph.md)
</dt> </dl>

 

 



