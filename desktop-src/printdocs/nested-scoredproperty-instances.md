---
description: ScoredProperty 實例也可以嵌套在其他 ScoredProperty 實例內或作為選項實例的子項目。
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: 嵌套 ScoredProperty 實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408601"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="7118a-103">嵌套 ScoredProperty 實例</span><span class="sxs-lookup"><span data-stu-id="7118a-103">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="7118a-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7118a-104">This topic is not current.</span></span> <span data-ttu-id="7118a-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7118a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7118a-106">請注意，您不會將 ScoredProperty 實例新增為選項實例的子項目。</span><span class="sxs-lookup"><span data-stu-id="7118a-106">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="7118a-107">ScoredProperty 實例也可以嵌套在其他 ScoredProperty 實例內。</span><span class="sxs-lookup"><span data-stu-id="7118a-107">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="7118a-108">當裝置屬性很複雜，且最適合由多個子屬性工作表示時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="7118a-108">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="7118a-109">將子屬性（Property）新增至現有的 (或公用) 屬性（Property）或 ScoredProperty 是增強選項的好方法，同時保留現有選項實例的可攜性。</span><span class="sxs-lookup"><span data-stu-id="7118a-109">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="7118a-110">例如，「媒體媒體」功能的標準選項實例包含 ScoredProperty，描述媒體的權數為淺色、中、大或 ExtraHeavy。</span><span class="sxs-lookup"><span data-stu-id="7118a-110">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="7118a-111">如果您想要更精確的權數描述，您可以在下列範例中新增子屬性 (GramsPer100Sheets) ，其中包含媒體的100工作表的實際權數)  (。</span><span class="sxs-lookup"><span data-stu-id="7118a-111">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="7118a-112">增強選項看起來可能如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="7118a-112">The enhanced Option might look like the following example.</span></span>

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

<span data-ttu-id="7118a-113">比較原始和增強的選項實例會產生近乎完美的比對，因為增強的選項是原始的超集合，而且會保留每個原始 ScoredProperty 實例的位置和值。</span><span class="sxs-lookup"><span data-stu-id="7118a-113">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7118a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="7118a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7118a-115">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7118a-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



