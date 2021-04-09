---
description: Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: 針對 Windows Search 開發篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026119"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="c058e-103">針對 Windows Search 開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="c058e-103">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="c058e-104">Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="c058e-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="c058e-105">您可以藉由撰寫篩選器來解壓縮內容，並使用屬性處理常式來解壓縮檔案的屬性，藉此擴充 Windows Search 來編制新的或專屬檔案類型的索引。</span><span class="sxs-lookup"><span data-stu-id="c058e-105">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="c058e-106">本節提供在 () 的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面上執行篩選處理常式所需的概念架構。</span><span class="sxs-lookup"><span data-stu-id="c058e-106">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="c058e-107">瞭解 Windows Search 中的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="c058e-107">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="c058e-108">在 Windows Search 中建立篩選處理常式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="c058e-108">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="c058e-109">從篩選處理常式傳回屬性</span><span class="sxs-lookup"><span data-stu-id="c058e-109">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="c058e-110">Windows 隨附的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="c058e-110">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="c058e-111">在 Windows Search 中執行篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="c058e-111">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="c058e-112">註冊篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="c058e-112">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="c058e-113">測試篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="c058e-113">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="c058e-114">其他資源</span><span class="sxs-lookup"><span data-stu-id="c058e-114">Additional Resources</span></span>

- <span data-ttu-id="c058e-115">[GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。</span><span class="sxs-lookup"><span data-stu-id="c058e-115">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="c058e-116">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="c058e-116">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="c058e-117">如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="c058e-117">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="c058e-118">若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c058e-118">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
