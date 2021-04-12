---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: 在 Print Schema 關鍵字中定義的物件和名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195797"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="5195b-104">在 Print Schema 關鍵字中定義的物件和名稱</span><span class="sxs-lookup"><span data-stu-id="5195b-104">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="5195b-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5195b-105">This topic is not current.</span></span> <span data-ttu-id="5195b-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5195b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5195b-107">Print Schema Framework 會定義命名空間，其中包含在 Print Schema 關鍵字中定義的元素和 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="5195b-107">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="5195b-108">這包括功能、選項和 ScoredProperty 之類的元素。屬性名稱，例如名稱和傳播;和 XML 屬性的值，例如受限的。</span><span class="sxs-lookup"><span data-stu-id="5195b-108">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="5195b-109">換句話說，在 Print Schema 關鍵字中定義的每個名稱都應使用這個命名空間來明確限定，或應該透過使用預設的 xmlns 屬性，以隱含方式與這個命名空間相關聯。</span><span class="sxs-lookup"><span data-stu-id="5195b-109">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="5195b-110">Print Schema 關鍵字檔會定義可能出現在任何給定內容或位置的公用元素實例。</span><span class="sxs-lookup"><span data-stu-id="5195b-110">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="5195b-111">元素實例必須只出現在 Print Schema Framework 所指定的內容或位置中。</span><span class="sxs-lookup"><span data-stu-id="5195b-111">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="5195b-112">例如，在列印架構關鍵字中定義的 <.psf： Option name = "psk： Letter" > 實例必須出現在 <.psf： Feature name = "psk： PageMediaSize" > 實例 (也定義在列印架構關鍵字) 中。</span><span class="sxs-lookup"><span data-stu-id="5195b-112">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="5195b-113">您無法在其指定的內容之外自由使用指定的選項實例。</span><span class="sxs-lookup"><span data-stu-id="5195b-113">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="5195b-114">私用定義的元素實例可能會出現在任何位置，只要專案類型出現在 Print Schema Framework 所允許的內容中即可。</span><span class="sxs-lookup"><span data-stu-id="5195b-114">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5195b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="5195b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5195b-116">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5195b-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



