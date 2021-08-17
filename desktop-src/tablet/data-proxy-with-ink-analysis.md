---
description: 如同筆跡分析總覽中所述，筆墨分析技術會在內部維護以樹狀結構為基礎的檔模型，以包含分析結果和關聯性。
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: 具有筆跡分析的資料 Proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad79a37a3220351adad56c0a131392e96964714114ba1e0a982833b07bc85077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092777"
---
# <a name="data-proxy-with-ink-analysis"></a>具有筆跡分析的資料 Proxy

如同 [筆跡分析總覽](ink-analysis-overview.md)中所述，筆墨分析技術會在內部維護以樹狀結構為基礎的檔模型，以包含分析結果和關聯性。 如果您的應用程式已經建立不同的檔存放區，您將需要使用針對不同檔模型之間的 proxy 資料而設計的筆墨分析功能。

## <a name="types-of-data-proxy"></a>資料 Proxy 的類型

資料 proxy 功能可讓您的應用程式：

-   將分析結果資料整合回現有的檔模型。
-   將 (或狀態) 的先前結果傳達回 [**InkAnalyzer**](inkanalyzer.md)。
-   將非筆墨狀態傳達給 [**InkAnalyzer**](inkanalyzer.md)。
-   只會將最小的資料集 () 所需的最小資料集與非筆墨狀態進行通訊，以完成分析作業。
-   流量分析結果輕鬆更新內部應用程式檔模型。

筆墨分析資料 proxy 有兩種基本方法。 這些差異會在檔模型之間進行同步處理的時間和方式的詳細資料中進行版面配置。 第一個方法（同步更新）需要在應用程式檔中進行變更時修改筆墨分析檔模型。 第二種方法是隨選更新，只需要將應用程式檔模型變更所影響的資料傳遞給 [**InkAnalyzer**](inkanalyzer.md)。 也就是說，只有筆跡分析檔模型中的資料，與應用程式檔的修改相同區域中的資料，必須在需要時傳遞給 **InkAnalyzer** 。

### <a name="synchronous-update"></a>同步更新

同步更新方法需要在 [**InkAnalyzer**](inkanalyzer.md) 物件的 [**CoNtextNode**](icontextnode.md) 物件集合中，修改 (建立和刪除節點的) ，因為它們會在應用程式檔中發生。 例如，每次將文字單字加入至應用程式時，就會在 **InkAnalyzer** 中建立對應的 **TextWord** 樣式 **CoNtextNode** 。 如果頁面上文字文字的位置變更，則會同時更新對應 **CoNtextNode** 的位置。 這種方法比隨選方法更有效率，因為每個檔變更都牽涉到 **InkAnalyzer** 的更新，即使變更不會影響正在分析的筆跡。

下列範例旨在示範同步更新的運作方式。 Imagine 具有現有檔模型的應用程式。 當使用者對檔進行變更（例如新增文字）時，變更會以下列方式處理：

1.  終端使用者會建立新的資料。
2.  應用程式會決定如何處理資料、儲存資料，以及呈現資料。
3.  針對實際用途，下列步驟會同時進行。
    1.  應用程式會將資料放入其檔模型。
    2.  應用程式會建立 [**InkAnalyzer**](inkanalyzer.md) 並加以更新。 這麼做可同時確保 **InkAnalyzer** 一律具有最新的資訊。
    3.  應用程式會在 [**InkAnalyzer**](inkanalyzer.md)上呼叫 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)來開始分析。
4.  如果變更牽涉到筆跡，而 [**InkAnalyzer**](inkanalyzer.md) 決定新的結果，則會引發一連串的事件。 針對 **InkAnalyzer** 中 [**CoNtextNode**](icontextnode.md)物件的集合所做的每項變更，會引發一個事件。 這些事件包括 [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)、 [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md)、 [**CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)、 [**CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md)、 [**CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)、 [**CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)和 [**CoNtextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)。 應用程式會處理這些事件，以適當地將分析作業的結果 proxy 回檔模型。
5.  應用程式會更新檔的版面配置，從檔模型中提取新的資料。
6.  新的資料會轉譯回給終端使用者。

### <a name="on-demand-update"></a>隨選更新

隨選方法只需要針對正在分析之區域中的那些 [**CoNtextNode**](icontextnode.md) 物件傳遞資料。 所需的 **CoNtextNode** 物件是在叫用分析作業之後，以及在協調結果之前，從應用程式的檔模型中解壓縮。 比起同步更新更複雜的是，此方法會產生較佳的效能結果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[筆墨分析總覽](ink-analysis-overview.md)
</dt> <dt>

[**InkAnalyzer 類別 (c + +)**](inkanalyzer.md)
</dt> <dt>

[**InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**CoNtextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
