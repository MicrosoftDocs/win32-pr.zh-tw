---
title: PrintCapabilities 架構和檔
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1b8e2827e451fd8b1df477c33fe18d6203d10c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106974775"
---
# <a name="printcapabilities-schema-and-document-construction"></a><span data-ttu-id="1a394-104">PrintCapabilities 架構和檔結構</span><span class="sxs-lookup"><span data-stu-id="1a394-104">PrintCapabilities Schema and Document Construction</span></span>

<span data-ttu-id="1a394-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1a394-105">This topic is not current.</span></span> <span data-ttu-id="1a394-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1a394-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1a394-107">目前的 Win32 DevCaps 函式 (例如 GetDeviceCaps 或 DeviceCapabilities，在 Microsoft 平臺軟體發展工具組 (SDK) 檔中所述，) 嚴格地限制非驅動程式元件可取得的資訊類型，與列印裝置的功能和屬性有關。</span><span class="sxs-lookup"><span data-stu-id="1a394-107">The current Win32 DevCaps functions (such as GetDeviceCaps or DeviceCapabilities, both described in the Microsoft Platform Software Development Kit (SDK) documentation) severely limit the type of information non-driver components can obtain, with regard to the capabilities and properties of printing devices.</span></span> <span data-ttu-id="1a394-108">不支援發行列印處理器的功能，也不會有列舉非標準功能的方法。</span><span class="sxs-lookup"><span data-stu-id="1a394-108">There is no support for publishing the capabilities of print processors, nor is there a method to enumerate nonstandard features.</span></span> <span data-ttu-id="1a394-109">因此，驅動程式以外的元件無法用來建立完整的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="1a394-109">Thus there is no way for a component other than a driver to construct a complete user interface.</span></span> <span data-ttu-id="1a394-110">此外，用戶端或應用程式無法完全判斷裝置的功能，或除了 Win32 DevCaps 函式所提供的列印佇列以外的其他功能。</span><span class="sxs-lookup"><span data-stu-id="1a394-110">Furthermore, the client or application cannot completely determine the capabilities of devices or print queues beyond those provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="1a394-111">目前的函式無法擴充，因此裝置無法發佈新的屬性或功能。</span><span class="sxs-lookup"><span data-stu-id="1a394-111">The current functions are not extensible, so devices cannot publish new properties or features.</span></span>

<span data-ttu-id="1a394-112">PrintCapabilities 架構的目的是要藉由提供這些函式所提供功能的超集合，來消除 Win32 DevCaps 函數的許多限制。</span><span class="sxs-lookup"><span data-stu-id="1a394-112">The PrintCapabilities Schema is intended to eliminate many of the limitations of the Win32 DevCaps functions by providing a superset of the functionality afforded by these functions.</span></span> <span data-ttu-id="1a394-113">如果需要更多的功能，PrintCapabilities 檔的提供者可以藉由新增私用定義的元素實例，來擴充 print schema Framework 的條件約束中的列印架構關鍵字。</span><span class="sxs-lookup"><span data-stu-id="1a394-113">If more functionality is needed, a provider of the PrintCapabilities document can extend the Print Schema Keywords, within the constraints of the Print Schema Framework, by adding privately-defined element instances.</span></span> <span data-ttu-id="1a394-114">由於它依賴 XML 做為交換的媒體，因此 PrintCapabilities 檔的任何取用者都可以存取檔中的所有資料，而不受限制，也不會考慮與不同作業系統版本的相容性。</span><span class="sxs-lookup"><span data-stu-id="1a394-114">Because of its reliance on XML as the medium of interchange, any consumer of a PrintCapabilities document can access all of the data in the document without restriction, and without concern for compatibility with different operating system versions.</span></span> <span data-ttu-id="1a394-115">本節說明 PrintCapabilities 架構，並詳細說明其用法。</span><span class="sxs-lookup"><span data-stu-id="1a394-115">This section describes the PrintCapabilities Schema and details its use.</span></span>

<span data-ttu-id="1a394-116">本章節的目標物件包括下列群組：</span><span class="sxs-lookup"><span data-stu-id="1a394-116">The intended audience for this section includes the following groups:</span></span>

-   <span data-ttu-id="1a394-117">PrintTicket/PrintCapabilities 提供者介面的實作者</span><span class="sxs-lookup"><span data-stu-id="1a394-117">Implementers of the PrintTicket/PrintCapabilities Provider interface</span></span>

-   <span data-ttu-id="1a394-118">PrintCapabilities 的取用者</span><span class="sxs-lookup"><span data-stu-id="1a394-118">Consumers of PrintCapabilities</span></span>

-   <span data-ttu-id="1a394-119">PrintTicket/PrintCapabilities 提供者介面的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a394-119">Clients of the PrintTicket/PrintCapabilities Provider interface</span></span>

<span data-ttu-id="1a394-120">上述清單中的第一個類別在本節的其餘部分稱為 PrintCapabilities 提供者。</span><span class="sxs-lookup"><span data-stu-id="1a394-120">The first category in the preceding list is referred to as PrintCapabilities providers in the remainder of this section.</span></span> <span data-ttu-id="1a394-121">第二和第三個類別稱為 PrintCapabilities 取用者。</span><span class="sxs-lookup"><span data-stu-id="1a394-121">The second and third categories are referred to as PrintCapabilities consumers.</span></span>

## <a name="relationship-to-print-schema-and-printticket-schema"></a><span data-ttu-id="1a394-122">與列印架構和 PrintTicket 架構的關聯性</span><span class="sxs-lookup"><span data-stu-id="1a394-122">Relationship to Print Schema and PrintTicket Schema</span></span>

<span data-ttu-id="1a394-123">PrintCapabilities 和 PrintTicket 架構都是列印架構的特殊部分。</span><span class="sxs-lookup"><span data-stu-id="1a394-123">The PrintCapabilities and PrintTicket Schemas are both specialized parts of the Print Schema.</span></span> <span data-ttu-id="1a394-124">這兩個列印架構子集之間的主要結構差異在於，PrintCapabilities 架構包含了不包含在 PrintTicket 架構中的屬性和 ParameterDef 實例，而 PrintTicket 架構則包含不包含在 PrintCapabilities 架構中的屬性和 ParameterInit 實例。</span><span class="sxs-lookup"><span data-stu-id="1a394-124">The main structural differences between these subsets of the Print Schema is that the PrintCapabilities Schema includes Property and ParameterDef instances that are not contained in the PrintTicket Schema, while the PrintTicket Schema contains Property and ParameterInit instances that are not contained in the PrintCapabilities Schema.</span></span> <span data-ttu-id="1a394-125">除了這些差異之外，PrintCapabilities 和 PrintTicket 架構通常會在內容、共用功能、選項、ScoredProperty 和值實例中彼此進行鏡像。</span><span class="sxs-lookup"><span data-stu-id="1a394-125">Except for these differences, the PrintCapabilities and PrintTicket Schemas generally mirror each other in content, sharing Feature, Option, ScoredProperty, and Value instances.</span></span> <span data-ttu-id="1a394-126">任何這類共用內容都必須保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="1a394-126">Any such shared content must be kept up-to-date.</span></span> <span data-ttu-id="1a394-127">例如，如果在 PrintCapabilities 架構的 PageMediaSize 功能中進行了變更，則必須在 PrintTicket 架構中進行相同的變更。</span><span class="sxs-lookup"><span data-stu-id="1a394-127">For example, if a change is made in the PageMediaSize Feature in the PrintCapabilities Schema, the same change must be made in the PrintTicket Schema.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a394-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a394-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a394-129">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1a394-129">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



