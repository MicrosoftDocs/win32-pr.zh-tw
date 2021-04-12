---
description: 使用 OpenSearch 技術對遠端資料存放區進行搜尋同盟的 Windows 7 支援，可讓使用者從 Windows 檔案總管記憶體取遠端資料並與其互動。
ms.assetid: 2014b7ac-4885-4f17-b6d4-5fd95872ed59
title: Windows 中的同盟搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d7718bb5215072ceeb8786f5728017ed329e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468804"
---
# <a name="federated-search-in-windows"></a><span data-ttu-id="e1e64-103">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="e1e64-103">Federated Search in Windows</span></span>

<span data-ttu-id="e1e64-104">使用 OpenSearch 技術對遠端資料存放區進行搜尋同盟的 Windows 7 支援，可讓使用者從 Windows 檔案總管記憶體取遠端資料並與其互動。</span><span class="sxs-lookup"><span data-stu-id="e1e64-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span>

<span data-ttu-id="e1e64-105">下列主題清單說明如何建立可使用 Windows 同盟搜尋來搜尋的 web 資料存放區，並透過 Windows 檔案總管啟用豐富的遠端資料源整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。</span><span class="sxs-lookup"><span data-stu-id="e1e64-105">The following list of topics describe how you can build a web-based data store that can be searched using Windows federated search, and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

-   [<span data-ttu-id="e1e64-106">在 Windows 中使用同盟搜尋開始使用</span><span class="sxs-lookup"><span data-stu-id="e1e64-106">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
-   [<span data-ttu-id="e1e64-107">在 Windows 同盟搜尋中連接您的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="e1e64-107">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
-   [<span data-ttu-id="e1e64-108">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="e1e64-108">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
-   [<span data-ttu-id="e1e64-109">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="e1e64-109">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
-   [<span data-ttu-id="e1e64-110">遵循 Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="e1e64-110">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
-   [<span data-ttu-id="e1e64-111">在 Windows 同盟搜尋中部署搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="e1e64-111">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
-   [<span data-ttu-id="e1e64-112">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="e1e64-112">Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)

## <a name="additional-resources"></a><span data-ttu-id="e1e64-113">其他資源</span><span class="sxs-lookup"><span data-stu-id="e1e64-113">Additional Resources</span></span>

-   <span data-ttu-id="e1e64-114">[ [Opensearch](-search-sample-opensearch.md) 程式碼] 範例示範如何使用 [ [opensearch](https://github.com/dewitt/opensearch) ] 通訊協定建立同盟搜尋服務，以及 ( 的 [ (搜尋) 連接器]) 檔案的 [.osdx]。</span><span class="sxs-lookup"><span data-stu-id="e1e64-114">The [OpenSearch](-search-sample-opensearch.md) code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>
-   <span data-ttu-id="e1e64-115">如需建立 SQL database 的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務的示範影片，請參閱 [Windows 7：讓使用者能夠使用程式庫和 Explorer 來尋找、視覺化及組織其資料](https://channel9.msdn.com/pdc2008/PC16/)。</span><span class="sxs-lookup"><span data-stu-id="e1e64-115">For a video demonstration of creating an [OpenSearch](https://github.com/dewitt/opensearch) web service for a SQL database, see [Windows 7: Empower Users to Find, Visualize and Organize their Data with Libraries and the Explorer](https://channel9.msdn.com/pdc2008/PC16/).</span></span>
-   <span data-ttu-id="e1e64-116">如果您要撰寫用戶端的 [OpenSearch](https://github.com/dewitt/opensearch) 提供者，請參閱：</span><span class="sxs-lookup"><span data-stu-id="e1e64-116">If you are writing a client-side [OpenSearch](https://github.com/dewitt/opensearch) provider, see:</span></span>
    -   <span data-ttu-id="e1e64-117">關於使用專屬資料存放區的通訊協定或 Api 連接至用戶端提供者的詳細資訊，則是「 [OpenSearch 開發人員」指南](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) 。</span><span class="sxs-lookup"><span data-stu-id="e1e64-117">The [OpenSearch Developer How To Guide](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) for more information on connecting to a client-side provider by using a proprietary data store's protocols or APIs.</span></span>
    -   <span data-ttu-id="e1e64-118">[搜尋連接器描述架構的總覽](search-sconn-desc-schema-entry.md) ( searchconnector-ms) 架構檔。</span><span class="sxs-lookup"><span data-stu-id="e1e64-118">The [Overview of the Search Connector Description Schema](search-sconn-desc-schema-entry.md) (.searchconnector-ms) schema documentation.</span></span>
-   <span data-ttu-id="e1e64-119">如需下列可下載資源，請參閱 [Microsoft 下載中心](https://www.microsoft.com/DOWNLOADS/en/default.aspx) 網站：搜尋伺服器2008範例：同盟搜尋連接器範例。</span><span class="sxs-lookup"><span data-stu-id="e1e64-119">See the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) website for the following downloadable resource: Search Server 2008 Sample: Federated Search Connector Sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1e64-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1e64-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1e64-121">Windows Search 概觀</span><span class="sxs-lookup"><span data-stu-id="e1e64-121">Windows Search Overview</span></span>](-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="e1e64-122">Windows Search 開發人員指南</span><span class="sxs-lookup"><span data-stu-id="e1e64-122">Windows Search Developer's Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="e1e64-123">Windows Search 參考</span><span class="sxs-lookup"><span data-stu-id="e1e64-123">Windows Search Reference</span></span>](-search-reference-entry-page.md)
</dt> <dt>

[<span data-ttu-id="e1e64-124">Windows Search 程式碼範例</span><span class="sxs-lookup"><span data-stu-id="e1e64-124">Windows Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

[<span data-ttu-id="e1e64-125">相關搜尋技術</span><span class="sxs-lookup"><span data-stu-id="e1e64-125">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)
</dt> <dt>

[<span data-ttu-id="e1e64-126">Windows Search 詞彙</span><span class="sxs-lookup"><span data-stu-id="e1e64-126">Windows Search Glossary</span></span>](search-glossary.md)
</dt> </dl>

 

 



