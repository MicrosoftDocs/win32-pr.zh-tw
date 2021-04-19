---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997603"
---
# <a name="parameterref"></a><span data-ttu-id="20d45-104">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="20d45-104">ParameterRef</span></span>

<span data-ttu-id="20d45-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="20d45-105">This topic is not current.</span></span> <span data-ttu-id="20d45-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="20d45-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="20d45-107">ParameterRef 元素會定義 ParameterInit 元素的參考。</span><span class="sxs-lookup"><span data-stu-id="20d45-107">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="20d45-108">包含 ParameterRef 元素的 ScoredProperty 元素沒有明確設定的 Value 元素。</span><span class="sxs-lookup"><span data-stu-id="20d45-108">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="20d45-109">相反地，ScoredProperty 專案會從 ParameterRef 元素所參考的 ParameterInit 元素接收其值。</span><span class="sxs-lookup"><span data-stu-id="20d45-109">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="20d45-110">元素標記</span><span class="sxs-lookup"><span data-stu-id="20d45-110">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="20d45-111">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="20d45-111">XML Attributes</span></span>

<span data-ttu-id="20d45-112">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="20d45-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="20d45-113">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="20d45-113">XML Attribute</span></span>   | <span data-ttu-id="20d45-114">詳細資料</span><span class="sxs-lookup"><span data-stu-id="20d45-114">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d45-115">NAME</span><span class="sxs-lookup"><span data-stu-id="20d45-115">name</span></span><br/> | <span data-ttu-id="20d45-116">保留目前檔內容中所參考之 ParameterDef 元素的 name 屬性。</span><span class="sxs-lookup"><span data-stu-id="20d45-116">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="20d45-117">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="20d45-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="20d45-118">項目資訊</span><span class="sxs-lookup"><span data-stu-id="20d45-118">Element Information</span></span>

<span data-ttu-id="20d45-119">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="20d45-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="20d45-120">類別</span><span class="sxs-lookup"><span data-stu-id="20d45-120">Category</span></span>                   | <span data-ttu-id="20d45-121">詳細資料</span><span class="sxs-lookup"><span data-stu-id="20d45-121">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d45-122">父元素</span><span class="sxs-lookup"><span data-stu-id="20d45-122">Parent elements</span></span><br/> | <span data-ttu-id="20d45-123">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="20d45-123">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="20d45-124">子元素</span><span class="sxs-lookup"><span data-stu-id="20d45-124">Child elements</span></span><br/>  | <span data-ttu-id="20d45-125">無允許。</span><span class="sxs-lookup"><span data-stu-id="20d45-125">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="20d45-126">這個元素</span><span class="sxs-lookup"><span data-stu-id="20d45-126">This element</span></span><br/>    | <span data-ttu-id="20d45-127">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="20d45-127">No character data is permitted.</span></span><br/> <span data-ttu-id="20d45-128">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="20d45-128">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="20d45-129">設定相依性</span><span class="sxs-lookup"><span data-stu-id="20d45-129">Configuration Dependencies</span></span>

<span data-ttu-id="20d45-130">ParameterRef 元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="20d45-130">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="20d45-131">範例</span><span class="sxs-lookup"><span data-stu-id="20d45-131">Example</span></span>

<span data-ttu-id="20d45-132">下列範例說明如何使用 ParameterRef 元素，讓使用者輸入自訂媒體大小參數。</span><span class="sxs-lookup"><span data-stu-id="20d45-132">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a><span data-ttu-id="20d45-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="20d45-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20d45-134">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="20d45-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




