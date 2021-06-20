---
description: Print Schema Framework 會定義命名空間，其中包含在 Print Schema 關鍵字中定義的元素和 XML 屬性。
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: 在 Print Schema 關鍵字中定義的物件和名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408551"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="e6656-103">在 Print Schema 關鍵字中定義的物件和名稱</span><span class="sxs-lookup"><span data-stu-id="e6656-103">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="e6656-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e6656-104">This topic is not current.</span></span> <span data-ttu-id="e6656-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e6656-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e6656-106">Print Schema Framework 會定義命名空間，其中包含在 Print Schema 關鍵字中定義的元素和 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6656-106">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="e6656-107">這包括功能、選項和 ScoredProperty 之類的元素。屬性名稱，例如名稱和傳播;和 XML 屬性的值，例如受限的。</span><span class="sxs-lookup"><span data-stu-id="e6656-107">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="e6656-108">換句話說，在 Print Schema 關鍵字中定義的每個名稱都應使用這個命名空間來明確限定，或應該透過使用預設的 xmlns 屬性，以隱含方式與這個命名空間相關聯。</span><span class="sxs-lookup"><span data-stu-id="e6656-108">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="e6656-109">Print Schema 關鍵字檔會定義可能出現在任何給定內容或位置的公用元素實例。</span><span class="sxs-lookup"><span data-stu-id="e6656-109">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="e6656-110">元素實例必須只出現在 Print Schema Framework 所指定的內容或位置中。</span><span class="sxs-lookup"><span data-stu-id="e6656-110">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="e6656-111">例如，在列印架構關鍵字中定義的 <.psf： Option name = "psk： Letter" > 實例必須出現在 <.psf： Feature name = "psk： PageMediaSize" > 實例 (也定義在列印架構關鍵字) 中。</span><span class="sxs-lookup"><span data-stu-id="e6656-111">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="e6656-112">您無法在其指定的內容之外自由使用指定的選項實例。</span><span class="sxs-lookup"><span data-stu-id="e6656-112">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="e6656-113">私用定義的元素實例可能會出現在任何位置，只要專案類型出現在 Print Schema Framework 所允許的內容中即可。</span><span class="sxs-lookup"><span data-stu-id="e6656-113">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6656-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6656-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6656-115">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e6656-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



