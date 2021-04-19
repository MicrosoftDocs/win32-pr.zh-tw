---
description: Windows Search 使用語言資源（例如斷詞工具和字幹分析器），在建立索引和查詢處理期間中斷文字的原生地區設定。
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: 擴充語言資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727f5812d0aee370c96d98f1c57dfffcbea5bc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973613"
---
# <a name="extending-language-resources"></a><span data-ttu-id="9b79c-103">擴充語言資源</span><span class="sxs-lookup"><span data-stu-id="9b79c-103">Extending Language Resources</span></span>

<span data-ttu-id="9b79c-104">Windows Search 使用語言資源（例如斷詞工具和字幹分析器），在建立索引和查詢處理期間中斷文字的原生地區設定。</span><span class="sxs-lookup"><span data-stu-id="9b79c-104">Windows Search uses language resources such as word breakers and stemmers to break text in its native locale during index creation and query processing.</span></span> <span data-ttu-id="9b79c-105">Microsoft 提供數種語言的斷詞工具和字幹分析器。</span><span class="sxs-lookup"><span data-stu-id="9b79c-105">Microsoft provides word breakers and stemmers for several languages.</span></span> <span data-ttu-id="9b79c-106">本節說明如何在 Microsoft 提供的語言和地區設定之外，執行及使用自訂斷詞工具和字幹分析器。</span><span class="sxs-lookup"><span data-stu-id="9b79c-106">This section describes how to implement and use custom word breakers and stemmers for languages and locales beyond those provided by Microsoft.</span></span>

-   [<span data-ttu-id="9b79c-107">瞭解語言資源元件</span><span class="sxs-lookup"><span data-stu-id="9b79c-107">Understanding Language Resource Components</span></span>](understanding-language-resource-components.md)
-   [<span data-ttu-id="9b79c-108">執行斷詞工具和字幹分析器</span><span class="sxs-lookup"><span data-stu-id="9b79c-108">Implementing a Word Breaker and Stemmer</span></span>](implementing-a-word-breaker-and-stemmer.md)
-   [<span data-ttu-id="9b79c-109">語言和 Unicode 考慮</span><span class="sxs-lookup"><span data-stu-id="9b79c-109">Linguistic and Unicode Considerations</span></span>](linguistic-and-unicode-considerations.md)
-   [<span data-ttu-id="9b79c-110">疑難排解語言資源和最佳作法</span><span class="sxs-lookup"><span data-stu-id="9b79c-110">Troubleshooting Language Resources and Best Practices</span></span>](troubleshooting-language-resources.md)

## <a name="additional-resources"></a><span data-ttu-id="9b79c-111">其他資源</span><span class="sxs-lookup"><span data-stu-id="9b79c-111">Additional Resources</span></span>

-   <span data-ttu-id="9b79c-112">如需斷詞工具所支援的 lanuages 清單，請參閱 [Windows Search 所支援的語言](-search-3x-wds-language-support.md)。</span><span class="sxs-lookup"><span data-stu-id="9b79c-112">For a list of lanuages supported by word breakers, see [Languages Supported by Windows Search](-search-3x-wds-language-support.md).</span></span>
-   <span data-ttu-id="9b79c-113">如果您需要識別某段文字的語言，您可以使用 Windows 7 和更新版本中提供的語言自動偵測 (LAD) 。</span><span class="sxs-lookup"><span data-stu-id="9b79c-113">If you need to identify the language of a piece of text, you can use Language Auto-Detection (LAD), which is available in Windows 7 and later.</span></span> <span data-ttu-id="9b79c-114">如需詳細資訊，請參閱 (ELS) 的 [擴充語言服務](../intl/extended-linguistic-services.md) 。</span><span class="sxs-lookup"><span data-stu-id="9b79c-114">For more information, see [Extended Linguistic Services](../intl/extended-linguistic-services.md) (ELS).</span></span>
-   <span data-ttu-id="9b79c-115">如需適用的參考檔，請參閱 [資料增益集介面](-search-data-addins-interfaces-entry-page.md)。</span><span class="sxs-lookup"><span data-stu-id="9b79c-115">For applicable reference documentation, see [Data Add-in Interfaces](-search-data-addins-interfaces-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b79c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b79c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b79c-117">管理索引</span><span class="sxs-lookup"><span data-stu-id="9b79c-117">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="9b79c-118">以程式設計方式查詢索引</span><span class="sxs-lookup"><span data-stu-id="9b79c-118">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="9b79c-119">擴充索引</span><span class="sxs-lookup"><span data-stu-id="9b79c-119">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
