---
description: 深入瞭解 ParameterInit 元素，此元素會定義 ParameterDef 元素之實例的值。
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211fcad2c53824c7786850a7fc78c6825c219a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407261"
---
# <a name="parameterinit"></a><span data-ttu-id="a4d48-103">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="a4d48-103">ParameterInit</span></span>

<span data-ttu-id="a4d48-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a4d48-104">This topic is not current.</span></span> <span data-ttu-id="a4d48-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a4d48-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4d48-106">定義 ParameterDef 元素之實例的值。</span><span class="sxs-lookup"><span data-stu-id="a4d48-106">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="a4d48-107">ParameterInit 元素是 ParameterRef 專案所做之參考的目標。</span><span class="sxs-lookup"><span data-stu-id="a4d48-107">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="a4d48-108">元素標記</span><span class="sxs-lookup"><span data-stu-id="a4d48-108">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="a4d48-109">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="a4d48-109">XML Attributes</span></span>

<span data-ttu-id="a4d48-110">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="a4d48-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="a4d48-111">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="a4d48-111">XML Attribute</span></span>   | <span data-ttu-id="a4d48-112">詳細資料</span><span class="sxs-lookup"><span data-stu-id="a4d48-112">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d48-113">NAME</span><span class="sxs-lookup"><span data-stu-id="a4d48-113">name</span></span><br/> | <span data-ttu-id="a4d48-114">保存 ParameterDef 專案的 name 屬性，該專案是要在目前檔的內容中初始化。</span><span class="sxs-lookup"><span data-stu-id="a4d48-114">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="a4d48-115">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="a4d48-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="a4d48-116">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a4d48-116">Element Information</span></span>

<span data-ttu-id="a4d48-117">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="a4d48-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="a4d48-118">類別</span><span class="sxs-lookup"><span data-stu-id="a4d48-118">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d48-119">父元素</span><span class="sxs-lookup"><span data-stu-id="a4d48-119">Parent elements</span></span><br/> | <span data-ttu-id="a4d48-120">PrintTicket (PrintTicket 根) </span><span class="sxs-lookup"><span data-stu-id="a4d48-120">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="a4d48-121">子元素</span><span class="sxs-lookup"><span data-stu-id="a4d48-121">Child elements</span></span><br/>  | <span data-ttu-id="a4d48-122">值 (一) </span><span class="sxs-lookup"><span data-stu-id="a4d48-122">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="a4d48-123">這個元素</span><span class="sxs-lookup"><span data-stu-id="a4d48-123">This element</span></span><br/>    | <span data-ttu-id="a4d48-124">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="a4d48-124">No character data is permitted.</span></span><br/> <span data-ttu-id="a4d48-125">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="a4d48-125">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="a4d48-126">設定相依性</span><span class="sxs-lookup"><span data-stu-id="a4d48-126">Configuration Dependencies</span></span>

<span data-ttu-id="a4d48-127">None</span><span class="sxs-lookup"><span data-stu-id="a4d48-127">None</span></span>

## <a name="example"></a><span data-ttu-id="a4d48-128">範例</span><span class="sxs-lookup"><span data-stu-id="a4d48-128">Example</span></span>

<span data-ttu-id="a4d48-129">下列範例會將參數初始化為1。</span><span class="sxs-lookup"><span data-stu-id="a4d48-129">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="a4d48-130">[ParameterDef](parameterdef.md)中的範例示範如何為此參數設定所有必要的屬性元素。</span><span class="sxs-lookup"><span data-stu-id="a4d48-130">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="a4d48-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4d48-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4d48-132">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a4d48-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




