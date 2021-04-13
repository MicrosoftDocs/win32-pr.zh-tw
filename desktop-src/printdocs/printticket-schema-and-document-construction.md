---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: PrintTicket 架構和檔結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe386638a7f119c52982f1911d602691455343f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195819"
---
# <a name="printticket-schema-and-document-construction"></a><span data-ttu-id="a745c-104">PrintTicket 架構和檔結構</span><span class="sxs-lookup"><span data-stu-id="a745c-104">PrintTicket Schema and Document Construction</span></span>

<span data-ttu-id="a745c-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a745c-105">This topic is not current.</span></span> <span data-ttu-id="a745c-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a745c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a745c-107">目前使用 DEVMODE 結構指定裝置設定資訊的方法，有數項限制。</span><span class="sxs-lookup"><span data-stu-id="a745c-107">The current method of specifying device configuration information using a DEVMODE structure suffers from several limitations.</span></span> <span data-ttu-id="a745c-108">首先，DEVMODE 結構是二進位結構，可能會導致不同版本的問題。</span><span class="sxs-lookup"><span data-stu-id="a745c-108">First, the DEVMODE structure is a binary structure, which can lead to problems of differing versions.</span></span> <span data-ttu-id="a745c-109">其次，它會分成 nonextensible 的公開部分和私用部分，只能由驅動程式存取，而且只能由建立它的特定驅動程式存取。</span><span class="sxs-lookup"><span data-stu-id="a745c-109">Second, it is divided into a nonextensible public portion and a private portion that can be accessed only by drivers, and only then by the specific driver that created it.</span></span> <span data-ttu-id="a745c-110">PrintTicket 格式使用以 XML 為基礎的列印架構架構來表示設定資訊，以消除這些 DEVMODE 結構的缺點。</span><span class="sxs-lookup"><span data-stu-id="a745c-110">The PrintTicket format expresses configuration information using the XML-based Print Schema Framework, thereby eliminating these shortcomings of the DEVMODE structure.</span></span>

<span data-ttu-id="a745c-111">PrintTicket 架構會解決剛剛提到的兩個問題。</span><span class="sxs-lookup"><span data-stu-id="a745c-111">The PrintTicket Schema addresses each of the two problems just mentioned.</span></span> <span data-ttu-id="a745c-112">首先，PrintTicket 架構是以 XML 為基礎的文字檔，因此會排除擴充性和版本設定的問題。</span><span class="sxs-lookup"><span data-stu-id="a745c-112">First, the PrintTicket Schema is an XML-based text file, so problems with extensibility and versioning are eliminated.</span></span> <span data-ttu-id="a745c-113">其次，所有用戶端都可以使用設定資訊，也就是說，任何用戶端或提供者都可以儲存和取出 PrintTicket 中包含的任何資訊。</span><span class="sxs-lookup"><span data-stu-id="a745c-113">Second, configuration information is available to all clients, meaning that any client or provider can store and retrieve any information contained in a PrintTicket.</span></span> <span data-ttu-id="a745c-114">選項的描述方式是使用 Print Schema Framework 和衍生的 PrintCapabilities 檔所使用的相同技術。</span><span class="sxs-lookup"><span data-stu-id="a745c-114">Options are described using the same technique used by the Print Schema Framework and the derived PrintCapabilities document.</span></span> <span data-ttu-id="a745c-115">基於這個理由，PrintTicket 可提供要實現之選項定義模型的所有潛在可攜性優點。</span><span class="sxs-lookup"><span data-stu-id="a745c-115">For this reason, the PrintTicket provides all of the potential portability benefits of the Option definition model to be realized.</span></span> <span data-ttu-id="a745c-116">如需詳細資訊，請參閱 [Print Schema Framework](print-schema-framework.md) 。</span><span class="sxs-lookup"><span data-stu-id="a745c-116">See [Print Schema Framework](print-schema-framework.md) for more information.</span></span> <span data-ttu-id="a745c-117">本章節的目標物件包括下列群組：</span><span class="sxs-lookup"><span data-stu-id="a745c-117">The intended audience for this section includes the following groups:</span></span>

-   <span data-ttu-id="a745c-118">PrintTicket/PrintCapabilities 提供者介面的實作者</span><span class="sxs-lookup"><span data-stu-id="a745c-118">Implementers of a PrintTicket / PrintCapabilities Provider interface</span></span>

-   <span data-ttu-id="a745c-119">PrintTicket 的取用者</span><span class="sxs-lookup"><span data-stu-id="a745c-119">Consumers of the PrintTicket</span></span>

-   <span data-ttu-id="a745c-120">PrintTicket/PrintCapabilities 提供者介面的用戶端</span><span class="sxs-lookup"><span data-stu-id="a745c-120">Clients of a PrintTicket / PrintCapabilities Provider interface</span></span>

<span data-ttu-id="a745c-121">上述清單中第一個類別目錄的成員在本節的其餘部分稱為「PrintTicket 提供者」。</span><span class="sxs-lookup"><span data-stu-id="a745c-121">Members of the first category in the preceding list are referred to as PrintTicket providers in the remainder of this section.</span></span> <span data-ttu-id="a745c-122">最後兩個類別的成員稱為「PrintTicket 取用者」。</span><span class="sxs-lookup"><span data-stu-id="a745c-122">Members of the last two categories are referred to as PrintTicket consumers.</span></span>

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a><span data-ttu-id="a745c-123">與列印架構和 PrintCapabilities 架構的關聯性</span><span class="sxs-lookup"><span data-stu-id="a745c-123">Relationship to Print Schema and PrintCapabilities Schema</span></span>

<span data-ttu-id="a745c-124">PrintTicket 和 PrintCapabilities 架構都是列印架構的特殊部分。</span><span class="sxs-lookup"><span data-stu-id="a745c-124">The PrintTicket and PrintCapabilities schemas are both specialized parts of the Print Schema.</span></span> <span data-ttu-id="a745c-125">這兩個列印架構子集之間的主要結構差異，是 PrintTicket 架構包含未包含在 PrintCapabilities 架構中的屬性和 ParameterInit 實例，而 PrintCapabilities 架構則包含不包含在 PrintTicket 架構中的屬性和 ParameterDef 實例。</span><span class="sxs-lookup"><span data-stu-id="a745c-125">The main structural differences between these subsets of the Print Schema is that the PrintTicket Schema contains Property and ParameterInit instances that are not contained in the PrintCapabilities Schema, while the PrintCapabilities Schema includes Property and ParameterDef instances that are not contained in the PrintTicket Schema.</span></span> <span data-ttu-id="a745c-126">除了這些差異之外，PrintCapabilities 和 PrintTicket 架構通常會在內容、共用功能、選項、ScoredProperty 和值實例中彼此進行鏡像。</span><span class="sxs-lookup"><span data-stu-id="a745c-126">Except for these differences, the PrintCapabilities and PrintTicket schemas generally mirror each other in content, sharing Feature, Option, ScoredProperty, and Value instances.</span></span> <span data-ttu-id="a745c-127">任何這類共用內容都必須保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="a745c-127">Any such shared content must be kept up-to-date.</span></span> <span data-ttu-id="a745c-128">例如，如果在 PrintCapabilities 架構的 MediaSize 功能中進行了變更，則必須在 PrintTicket 架構中進行相同的變更。</span><span class="sxs-lookup"><span data-stu-id="a745c-128">For example, if a change is made in the MediaSize Feature in the PrintCapabilities Schema, the same change must be made in the PrintTicket Schema.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a745c-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a745c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a745c-130">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a745c-130">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



