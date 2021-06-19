---
description: 本總覽描述列印架構和列印架構參考主題的連結。 列印架構包括列印架構關鍵字和架構。
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: 舊版列印架構參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407131"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="e6189-104">舊版列印架構參考</span><span class="sxs-lookup"><span data-stu-id="e6189-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="e6189-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e6189-105">This topic is not current.</span></span> <span data-ttu-id="e6189-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e6189-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e6189-107">您可以在 Microsoft .NET Framework 3.0、Microsoft Windows Vista 及更新版本中取得列印架構和相關技術。</span><span class="sxs-lookup"><span data-stu-id="e6189-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="e6189-108">列印架構會提供以 XML 為基礎的格式來表示和組織一組大量的屬性，這些屬性會以階層結構化的方式來描述作業格式或 PrintCapabilities。</span><span class="sxs-lookup"><span data-stu-id="e6189-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="e6189-109">列印架構是一種涵蓋了兩個元件、Print Schema 關鍵字和 Print Schema Framework 的廣義詞彙。</span><span class="sxs-lookup"><span data-stu-id="e6189-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="e6189-110">Print Schema 關鍵字檔是一個公用架構，它會定義一組可用來描述裝置屬性和列印工作格式的元素實例。</span><span class="sxs-lookup"><span data-stu-id="e6189-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="e6189-111">Print Schema Framework 是一個公用架構，可定義 XML 專案型別的階層式結構化集合，並指定如何一起使用專案類型。</span><span class="sxs-lookup"><span data-stu-id="e6189-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="e6189-112">Print Schema 關鍵字和 Print Schema Framework 構成兩個列印架構相關技術、PrintCapabilities 架構和 PrintTicket 架構的基礎。</span><span class="sxs-lookup"><span data-stu-id="e6189-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="e6189-113">請務必記住，列印架構的其中一個目標是要讓提供者支援架構延伸。</span><span class="sxs-lookup"><span data-stu-id="e6189-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="e6189-114">也就是說，提供者不會限制為只使用在 Print Schema Framework 上建的技術中，在 Print Schema 關鍵字中定義的屬性、功能、選項或 ParameterInit 實例。</span><span class="sxs-lookup"><span data-stu-id="e6189-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="e6189-115">提供者特定的元素實例可以自由地在 Print Schema 關鍵字中定義的元素實例內。</span><span class="sxs-lookup"><span data-stu-id="e6189-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="e6189-116">唯一的需求是提供者特定的 (，也就是私用) 屬性實例必須屬於與提供者清楚相關聯的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e6189-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="e6189-117">列印架構背景</span><span class="sxs-lookup"><span data-stu-id="e6189-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="e6189-118">列印 Schema-Related 技術</span><span class="sxs-lookup"><span data-stu-id="e6189-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="e6189-119">列印架構中使用的詞彙</span><span class="sxs-lookup"><span data-stu-id="e6189-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="e6189-120">列印架構的語法</span><span class="sxs-lookup"><span data-stu-id="e6189-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="e6189-121">元素類型的摘要</span><span class="sxs-lookup"><span data-stu-id="e6189-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="e6189-122">Print Schema Framework</span><span class="sxs-lookup"><span data-stu-id="e6189-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="e6189-123">列印架構公用關鍵字</span><span class="sxs-lookup"><span data-stu-id="e6189-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="e6189-124">PrintCapabilities 架構和檔結構</span><span class="sxs-lookup"><span data-stu-id="e6189-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="e6189-125">PrintTicket 架構和檔結構</span><span class="sxs-lookup"><span data-stu-id="e6189-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="e6189-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6189-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6189-127">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e6189-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



