---
title: PrintCapabilities 設定相依性
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7f376d8bd0dab823adb3a2e0665db27508b1d7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853524"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a><span data-ttu-id="07194-104">PrintCapabilities 架構中的設定相依性</span><span class="sxs-lookup"><span data-stu-id="07194-104">Configuration Dependency in the PrintCapabilities Schema</span></span>

<span data-ttu-id="07194-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="07194-105">This topic is not current.</span></span> <span data-ttu-id="07194-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="07194-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="07194-107">PrintCapabilities 架構會根據所使用的專案，以及由父元素和子項目表示的一般結構，而緊密地平行使用 Print Schema Framework。</span><span class="sxs-lookup"><span data-stu-id="07194-107">The PrintCapabilities Schema closely parallels the Print Schema Framework, in terms of the elements used and the general structure expressed by parent and child elements.</span></span> <span data-ttu-id="07194-108">專屬於 PrintCapabilities 的設定相依性會在此列為一般架構的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="07194-108">Configuration dependencies, which pertain specifically to the PrintCapabilities, are listed here as an extension to the general framework.</span></span> <span data-ttu-id="07194-109">設定相依性是指某些專案（包括其內容）可以改變或甚至從一個 PrintCapabilities 檔刪除到下一個，因為設定相依性的結果。</span><span class="sxs-lookup"><span data-stu-id="07194-109">Configuration dependencies refer to the fact that some elements, including their contents, can be altered or even deleted from one PrintCapabilities document to the next, as a result of dependencies on the configuration.</span></span> <span data-ttu-id="07194-110">即使父項目必須與設定無關，其子項目還是可能具有相依性。</span><span class="sxs-lookup"><span data-stu-id="07194-110">Even if a parent element is required to be independent of the configuration, its child elements might have dependencies.</span></span> <span data-ttu-id="07194-111">這類相依性是使用 \* \* GPD 檔中的 Switch/Case 結構來表示。</span><span class="sxs-lookup"><span data-stu-id="07194-111">Such dependencies are expressed using \*Switch/\*Case constructs in GPD files.</span></span>

<span data-ttu-id="07194-112">作為設定相依性的範例，請考慮與 PrintCapabilities 檔中每個屬性相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="07194-112">As an example of a configuration dependency, consider the values associated with each Property in the PrintCapabilities document.</span></span> <span data-ttu-id="07194-113">每個 PrintCapabilities 檔在定義的屬性實例和指派給這些屬性實例的值實例中可能不同。</span><span class="sxs-lookup"><span data-stu-id="07194-113">Each PrintCapabilities document can differ in the Property instances that are defined and in the Value instances assigned to those Property instances.</span></span>



| <span data-ttu-id="07194-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="07194-114">Element Type</span></span>                                                                                                                                                                             | <span data-ttu-id="07194-115">設定相依性</span><span class="sxs-lookup"><span data-stu-id="07194-115">Configuration Dependency</span></span>                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07194-116">功能</span><span class="sxs-lookup"><span data-stu-id="07194-116">Feature</span></span> <br/> <span data-ttu-id="07194-117">選項</span><span class="sxs-lookup"><span data-stu-id="07194-117">Option</span></span><br/> <span data-ttu-id="07194-118">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="07194-118">ParameterInit</span></span><br/> <span data-ttu-id="07194-119">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="07194-119">ParameterRef</span></span><br/> <span data-ttu-id="07194-120">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="07194-120">PrintCapabilities</span></span><br/> <span data-ttu-id="07194-121">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="07194-121">PrintTicket</span></span><br/> <span data-ttu-id="07194-122">屬性</span><span class="sxs-lookup"><span data-stu-id="07194-122">Property</span></span><br/> <span data-ttu-id="07194-123">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="07194-123">ScoredProperty</span></span><br/> | <span data-ttu-id="07194-124">這些元素不能有設定相依性。</span><span class="sxs-lookup"><span data-stu-id="07194-124">These elements must not have configuration dependencies.</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="07194-125">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="07194-125">ParameterDef</span></span> <br/>                                                                                                                                                                 | <span data-ttu-id="07194-126">ParameterDef 元素和其中包含的元素，都不能有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="07194-126">ParameterDef elements and elements contained within them to any nesting level must not have any configuration dependencies.</span></span><br/>                                                                                        |
| <span data-ttu-id="07194-127">屬性</span><span class="sxs-lookup"><span data-stu-id="07194-127">Property</span></span> <br/>                                                                                                                                                                     | <span data-ttu-id="07194-128">屬性元素可能具有設定相依性，除非它們出現在 ParameterDef 元素中。</span><span class="sxs-lookup"><span data-stu-id="07194-128">Property elements may have configuration dependencies, except when they appear within ParameterDef elements.</span></span><br/>                                                                                                       |
| <span data-ttu-id="07194-129">值</span><span class="sxs-lookup"><span data-stu-id="07194-129">Value</span></span> <br/>                                                                                                                                                                        | <span data-ttu-id="07194-130">出現在 ScoredProperty 元素內的值元素不能有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="07194-130">Value elements that appear within ScoredProperty elements must not have any configuration dependencies.</span></span> <span data-ttu-id="07194-131">出現在 Property 元素內的值元素可能會對設定有任意的相依性。</span><span class="sxs-lookup"><span data-stu-id="07194-131">Value elements that appear within a Property element may have arbitrary dependencies on the configuration.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="07194-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="07194-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07194-133">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="07194-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




