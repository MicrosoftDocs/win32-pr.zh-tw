---
description: 瞭解 ParameterRef 元素，它會定義 ParameterInit 專案的參考，以及它如何與 ScoredProperty 搭配使用。
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407181"
---
# <a name="parameterref"></a><span data-ttu-id="e3652-103">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="e3652-103">ParameterRef</span></span>

<span data-ttu-id="e3652-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e3652-104">This topic is not current.</span></span> <span data-ttu-id="e3652-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e3652-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3652-106">ParameterRef 元素會定義 ParameterInit 元素的參考。</span><span class="sxs-lookup"><span data-stu-id="e3652-106">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="e3652-107">包含 ParameterRef 元素的 ScoredProperty 元素沒有明確設定的 Value 元素。</span><span class="sxs-lookup"><span data-stu-id="e3652-107">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="e3652-108">相反地，ScoredProperty 專案會從 ParameterRef 元素所參考的 ParameterInit 元素接收其值。</span><span class="sxs-lookup"><span data-stu-id="e3652-108">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="e3652-109">元素標記</span><span class="sxs-lookup"><span data-stu-id="e3652-109">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="e3652-110">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="e3652-110">XML Attributes</span></span>

<span data-ttu-id="e3652-111">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="e3652-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="e3652-112">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="e3652-112">XML Attribute</span></span>   | <span data-ttu-id="e3652-113">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e3652-113">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3652-114">NAME</span><span class="sxs-lookup"><span data-stu-id="e3652-114">name</span></span><br/> | <span data-ttu-id="e3652-115">保留目前檔內容中所參考之 ParameterDef 元素的 name 屬性。</span><span class="sxs-lookup"><span data-stu-id="e3652-115">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="e3652-116">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="e3652-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="e3652-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e3652-117">Element Information</span></span>

<span data-ttu-id="e3652-118">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="e3652-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="e3652-119">類別</span><span class="sxs-lookup"><span data-stu-id="e3652-119">Category</span></span>                   | <span data-ttu-id="e3652-120">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e3652-120">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3652-121">父元素</span><span class="sxs-lookup"><span data-stu-id="e3652-121">Parent elements</span></span><br/> | <span data-ttu-id="e3652-122">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="e3652-122">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="e3652-123">子元素</span><span class="sxs-lookup"><span data-stu-id="e3652-123">Child elements</span></span><br/>  | <span data-ttu-id="e3652-124">無允許。</span><span class="sxs-lookup"><span data-stu-id="e3652-124">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="e3652-125">這個元素</span><span class="sxs-lookup"><span data-stu-id="e3652-125">This element</span></span><br/>    | <span data-ttu-id="e3652-126">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="e3652-126">No character data is permitted.</span></span><br/> <span data-ttu-id="e3652-127">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="e3652-127">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="e3652-128">設定相依性</span><span class="sxs-lookup"><span data-stu-id="e3652-128">Configuration Dependencies</span></span>

<span data-ttu-id="e3652-129">ParameterRef 元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="e3652-129">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="e3652-130">範例</span><span class="sxs-lookup"><span data-stu-id="e3652-130">Example</span></span>

<span data-ttu-id="e3652-131">下列範例說明如何使用 ParameterRef 元素，讓使用者輸入自訂媒體大小參數。</span><span class="sxs-lookup"><span data-stu-id="e3652-131">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e3652-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3652-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3652-133">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e3652-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




