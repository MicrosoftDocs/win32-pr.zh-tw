---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: 列印架構的語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2503b3f44ff8b4bdda41f0feefe374c27d78bd41
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "107000532"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="0611f-104">列印架構的語法</span><span class="sxs-lookup"><span data-stu-id="0611f-104">Syntax of the Print Schema</span></span>

<span data-ttu-id="0611f-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="0611f-105">This topic is not current.</span></span> <span data-ttu-id="0611f-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="0611f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0611f-107">列印架構是以 XML 語法表示。</span><span class="sxs-lookup"><span data-stu-id="0611f-107">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="0611f-108">因此讀者應該熟悉 XML 語法和詞彙，例如專案、專案標記、元素內容、屬性和命名空間。</span><span class="sxs-lookup"><span data-stu-id="0611f-108">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="0611f-109">Print Schema Framework 是由少量的元素類型所組成;每個元素類型都可在以列印架構為基礎的技術中提供特定用途。</span><span class="sxs-lookup"><span data-stu-id="0611f-109">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="0611f-110">專案類型是由其 XML 元素標記所區分。</span><span class="sxs-lookup"><span data-stu-id="0611f-110">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="0611f-111">Print Schema Framework 會藉由為每個專案類型表示允許做為子專案的元素類型，來定義相依技術的整體結構和組織。</span><span class="sxs-lookup"><span data-stu-id="0611f-111">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="0611f-112">許多專案類型都與名稱屬性的相同類型的其他專案不同，這在架構中扮演著重要的角色。</span><span class="sxs-lookup"><span data-stu-id="0611f-112">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="0611f-113">Name 屬性可用來識別每個元素類型的實例。</span><span class="sxs-lookup"><span data-stu-id="0611f-113">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="0611f-114">Print Schema 關鍵字會為許多專案類型的名稱屬性定義一組值。</span><span class="sxs-lookup"><span data-stu-id="0611f-114">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="0611f-115">在大多數情況下，提供者可以將自己的值指派給 name 屬性。</span><span class="sxs-lookup"><span data-stu-id="0611f-115">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="0611f-116">它們只需要確保值是以提供者唯一的命名空間限定的 XML QNames。</span><span class="sxs-lookup"><span data-stu-id="0611f-116">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0611f-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="0611f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0611f-118">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="0611f-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



