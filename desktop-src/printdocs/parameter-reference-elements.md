---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: ParameterRef 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c0e145e99b1ee705d63449cf693c6fc87f6463
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104035228"
---
# <a name="parameterref-elements"></a><span data-ttu-id="344f5-104">ParameterRef 元素</span><span class="sxs-lookup"><span data-stu-id="344f5-104">ParameterRef Elements</span></span>

<span data-ttu-id="344f5-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="344f5-105">This topic is not current.</span></span> <span data-ttu-id="344f5-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="344f5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="344f5-107">ParameterRef 專案特別適用于 Option 元素，可讓該選項專案參考特定的 ParameterDef 元素。</span><span class="sxs-lookup"><span data-stu-id="344f5-107">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="344f5-108">針對這些選項元素，ScoredProperty 專案會將此選項的特性標示為不會以值的形式在 PrintCapabilities 檔中進行硬式編碼，但改為變數。</span><span class="sxs-lookup"><span data-stu-id="344f5-108">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="344f5-109">為了啟用此變異，這些 ScoredProperty 元素包含 ParameterRef 元素。</span><span class="sxs-lookup"><span data-stu-id="344f5-109">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="344f5-110">ScoredProperty 元素不可同時包含 Value 元素和 ParameterRef 元素。</span><span class="sxs-lookup"><span data-stu-id="344f5-110">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="344f5-111">包含一或多個 ParameterRef 元素的 Option 元素稱為參數化 Option 元素。</span><span class="sxs-lookup"><span data-stu-id="344f5-111">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="344f5-112">Print Schema Framework 可讓 Option 元素包含任意數目的 ScoredProperty 專案，這些專案會參考參數專案，以及包含值專案的任何數目的 ScoredProperty 元素。</span><span class="sxs-lookup"><span data-stu-id="344f5-112">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="344f5-113">此架構也可讓任意數目的功能元素包含參數化選項專案，而且每個功能元素都允許任何數目的參數化選項元素。</span><span class="sxs-lookup"><span data-stu-id="344f5-113">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="344f5-114">此外，相同的參數結構可由數個不同的選項專案所參考，也就是可以屬於相同或不同功能專案的選項元素。</span><span class="sxs-lookup"><span data-stu-id="344f5-114">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="344f5-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="344f5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="344f5-116">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="344f5-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



