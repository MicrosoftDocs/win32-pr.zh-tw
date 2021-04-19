---
description: 您可以擴充 Windows Search，以使用資料增益集介面來編制新檔案格式和資料存放區的內容和屬性的索引。
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: 擴充索引 (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972607"
---
# <a name="extending-the-index-windows-search"></a><span data-ttu-id="0ab50-103">擴充索引 (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="0ab50-103">Extending the Index (Windows Search)</span></span>

<span data-ttu-id="0ab50-104">您可以擴充 Windows Search，以使用 [資料增益集介面](./-search-data-addins-interfaces-entry-page.md)來編制新檔案格式和資料存放區的內容和屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="0ab50-104">You can extend Windows Search to index the contents and properties of new file formats, and data stores using [data add-in interfaces](./-search-data-addins-interfaces-entry-page.md).</span></span> <span data-ttu-id="0ab50-105">若要建立 Windows Search 增益集，協力廠商開發人員必須先執行 Shell 資料存放區，然後再開發通訊協定處理常式，讓 Windows Search 可以存取資料來編制索引。</span><span class="sxs-lookup"><span data-stu-id="0ab50-105">To create Windows Search add-ins, third-party developers must first implement a Shell data store, and then develop a protocol handler so that Windows Search can access the data for indexing.</span></span> <span data-ttu-id="0ab50-106">如果您有自訂的檔案格式，您必須開發篩選處理常式來為檔案內容編制索引，以及將每個檔案類型的屬性處理常式建立為索引屬性。</span><span class="sxs-lookup"><span data-stu-id="0ab50-106">If you have a custom file format, you must develop a filter handler to index file contents, and a property handler for every file type to index properties.</span></span>

<span data-ttu-id="0ab50-107">Windows Search 目前支援將超過200種類型的專案編制索引 (例如 .txt、.html 和 .xml 檔案格式) 而且可以使用多種類型的資料存放區 (例如 NTFS 檔案系統和 Microsoft Outlook) 。</span><span class="sxs-lookup"><span data-stu-id="0ab50-107">Windows Search currently supports the indexing of over 200 types of items (such as .txt, .html, and .xml file formats) and can work with multiple types of data stores (such as the NTFS file system and Microsoft Outlook).</span></span> <span data-ttu-id="0ab50-108">Windows Search 使用與 SharePoint Server 類似的篩選和通訊協定處理常式技術。</span><span class="sxs-lookup"><span data-stu-id="0ab50-108">Windows Search uses filter and protocol handler technology similar to SharePoint Server.</span></span> <span data-ttu-id="0ab50-109">因此，如果您已經有檔案格式的執行，您可以使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 來更新要使用資料流程初始化的執行，以便讓篩選準則可以使用 Windows Search。</span><span class="sxs-lookup"><span data-stu-id="0ab50-109">Hence, if you already have implementations for your file format, you can update the implementations to be initialized with a stream by using [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) so that the filter will work with Windows Search.</span></span>

> [!Note]  
> <span data-ttu-id="0ab50-110">篩選處理常式、屬性處理常式和通訊協定處理常式必須以機器碼撰寫。</span><span class="sxs-lookup"><span data-stu-id="0ab50-110">Filter handlers, property handlers, and protocol handlers must be written in native code.</span></span> <span data-ttu-id="0ab50-111">這是因為可能的 common language runtime (CLR) 在中執行多個增益集的進程的版本控制問題。</span><span class="sxs-lookup"><span data-stu-id="0ab50-111">This is due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

 

<span data-ttu-id="0ab50-112">使用增益集擴充索引的這一節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="0ab50-112">This section on extending the index with add-ins contains the following topics:</span></span>

-   [<span data-ttu-id="0ab50-113">開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="0ab50-113">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
-   [<span data-ttu-id="0ab50-114">開發 Windows Search 的屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="0ab50-114">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="0ab50-115">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0ab50-115">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a><span data-ttu-id="0ab50-116">其他資源</span><span class="sxs-lookup"><span data-stu-id="0ab50-116">Additional Resources</span></span>

<span data-ttu-id="0ab50-117">如需相關的程式碼範例，請參閱 [Windows Search 程式碼範例](-search-samples-ovw.md)。</span><span class="sxs-lookup"><span data-stu-id="0ab50-117">For related code samples, see [Windows Search Code Samples](-search-samples-ovw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ab50-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ab50-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ab50-119">Windows Search 開發指南</span><span class="sxs-lookup"><span data-stu-id="0ab50-119">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="0ab50-120">管理索引</span><span class="sxs-lookup"><span data-stu-id="0ab50-120">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="0ab50-121">以程式設計方式查詢索引</span><span class="sxs-lookup"><span data-stu-id="0ab50-121">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="0ab50-122">擴充語言資源</span><span class="sxs-lookup"><span data-stu-id="0ab50-122">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
