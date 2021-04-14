---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cb985e746b400b1c804f21b5996352ae590e3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195805"
---
# <a name="parameterinit"></a><span data-ttu-id="37113-104">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="37113-104">ParameterInit</span></span>

<span data-ttu-id="37113-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="37113-105">This topic is not current.</span></span> <span data-ttu-id="37113-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="37113-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="37113-107">定義 ParameterDef 元素之實例的值。</span><span class="sxs-lookup"><span data-stu-id="37113-107">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="37113-108">ParameterInit 元素是 ParameterRef 專案所做之參考的目標。</span><span class="sxs-lookup"><span data-stu-id="37113-108">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="37113-109">元素標記</span><span class="sxs-lookup"><span data-stu-id="37113-109">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="37113-110">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="37113-110">XML Attributes</span></span>

<span data-ttu-id="37113-111">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="37113-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="37113-112">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="37113-112">XML Attribute</span></span>   | <span data-ttu-id="37113-113">詳細資料</span><span class="sxs-lookup"><span data-stu-id="37113-113">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37113-114">NAME</span><span class="sxs-lookup"><span data-stu-id="37113-114">name</span></span><br/> | <span data-ttu-id="37113-115">保存 ParameterDef 專案的 name 屬性，該專案是要在目前檔的內容中初始化。</span><span class="sxs-lookup"><span data-stu-id="37113-115">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="37113-116">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="37113-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="37113-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="37113-117">Element Information</span></span>

<span data-ttu-id="37113-118">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="37113-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="37113-119">類別</span><span class="sxs-lookup"><span data-stu-id="37113-119">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37113-120">父元素</span><span class="sxs-lookup"><span data-stu-id="37113-120">Parent elements</span></span><br/> | <span data-ttu-id="37113-121">PrintTicket (PrintTicket 根) </span><span class="sxs-lookup"><span data-stu-id="37113-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="37113-122">子元素</span><span class="sxs-lookup"><span data-stu-id="37113-122">Child elements</span></span><br/>  | <span data-ttu-id="37113-123">值 (一) </span><span class="sxs-lookup"><span data-stu-id="37113-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="37113-124">這個元素</span><span class="sxs-lookup"><span data-stu-id="37113-124">This element</span></span><br/>    | <span data-ttu-id="37113-125">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="37113-125">No character data is permitted.</span></span><br/> <span data-ttu-id="37113-126">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="37113-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="37113-127">設定相依性</span><span class="sxs-lookup"><span data-stu-id="37113-127">Configuration Dependencies</span></span>

<span data-ttu-id="37113-128">None</span><span class="sxs-lookup"><span data-stu-id="37113-128">None</span></span>

## <a name="example"></a><span data-ttu-id="37113-129">範例</span><span class="sxs-lookup"><span data-stu-id="37113-129">Example</span></span>

<span data-ttu-id="37113-130">下列範例會將參數初始化為1。</span><span class="sxs-lookup"><span data-stu-id="37113-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="37113-131">[ParameterDef](parameterdef.md)中的範例示範如何為此參數設定所有必要的屬性元素。</span><span class="sxs-lookup"><span data-stu-id="37113-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="37113-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="37113-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37113-133">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="37113-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




