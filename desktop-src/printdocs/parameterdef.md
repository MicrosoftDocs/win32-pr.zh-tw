---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981944"
---
# <a name="parameterdef"></a><span data-ttu-id="ea7b2-104">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ea7b2-104">ParameterDef</span></span>

<span data-ttu-id="ea7b2-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-105">This topic is not current.</span></span> <span data-ttu-id="ea7b2-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ea7b2-107">ParameterDef 元素會定義參數輸入的有效特性。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-107">A ParameterDef element defines the valid characteristics of parameter input.</span></span> <span data-ttu-id="ea7b2-108">藉由 ParameterInit 元素來輸入值。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-108">The value is entered by means of a ParameterInit element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="ea7b2-109">元素標記</span><span class="sxs-lookup"><span data-stu-id="ea7b2-109">Element Tag</span></span>

<ParameterDef>

## <a name="xml-attributes"></a><span data-ttu-id="ea7b2-110">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="ea7b2-110">XML Attributes</span></span>

<span data-ttu-id="ea7b2-111">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="ea7b2-112">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="ea7b2-112">XML Attribute</span></span>   | <span data-ttu-id="ea7b2-113">詳細資料</span><span class="sxs-lookup"><span data-stu-id="ea7b2-113">Details</span></span>                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea7b2-114">NAME</span><span class="sxs-lookup"><span data-stu-id="ea7b2-114">name</span></span><br/> | <span data-ttu-id="ea7b2-115">在目前檔的內容中定義參數的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-115">Defines a unique name for the parameter in the context of the current document.</span></span> <span data-ttu-id="ea7b2-116">重複的 ParameterDef 名稱屬性轉譯 PrintCapabilities 檔無效。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-116">Duplicate ParameterDef name attributes render the PrintCapabilities document invalid.</span></span><br/> |



 

<span data-ttu-id="ea7b2-117">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="ea7b2-118">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ea7b2-118">Element Information</span></span>

<span data-ttu-id="ea7b2-119">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea7b2-120">類別</span><span class="sxs-lookup"><span data-stu-id="ea7b2-120">Category</span></span></th>
<th><span data-ttu-id="ea7b2-121">詳細資料</span><span class="sxs-lookup"><span data-stu-id="ea7b2-121">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea7b2-122">父元素</span><span class="sxs-lookup"><span data-stu-id="ea7b2-122">Parent elements</span></span><br/></td>
<td><span data-ttu-id="ea7b2-123">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="ea7b2-123">PrintCapabilities</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea7b2-124">子元素</span><span class="sxs-lookup"><span data-stu-id="ea7b2-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="ea7b2-125">屬性 (一個或多個)</span><span class="sxs-lookup"><span data-stu-id="ea7b2-125">Property (one or more)</span></span><br/> <span data-ttu-id="ea7b2-126">下列標準屬性元素必須顯示為 ParameterDef 元素的內容。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-126">The following standard Property elements must appear as the content of a ParameterDef element.</span></span> <br/>
<ul>
<li><span data-ttu-id="ea7b2-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ea7b2-127">DataType</span></span> <br/></li>
<li><span data-ttu-id="ea7b2-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ea7b2-128">DefaultValue</span></span> <br/></li>
<li><span data-ttu-id="ea7b2-129">強制性</span><span class="sxs-lookup"><span data-stu-id="ea7b2-129">Mandatory</span></span> <br/></li>
<li><span data-ttu-id="ea7b2-130">MaxLength 或 Timespan.maxvalue</span><span class="sxs-lookup"><span data-stu-id="ea7b2-130">MaxLength or MaxValue</span></span><br/></li>
<li><span data-ttu-id="ea7b2-131">MinLength 或 MinValue</span><span class="sxs-lookup"><span data-stu-id="ea7b2-131">MinLength or MinValue</span></span><br/></li>
<li><span data-ttu-id="ea7b2-132">名</span><span class="sxs-lookup"><span data-stu-id="ea7b2-132">Multiple\*</span></span> <br/></li>
<li><span data-ttu-id="ea7b2-133">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="ea7b2-133">UnitType</span></span> <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea7b2-134">這個元素</span><span class="sxs-lookup"><span data-stu-id="ea7b2-134">This element</span></span><br/></td>
<td><span data-ttu-id="ea7b2-135">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-135">No character data is permitted.</span></span><br/> <span data-ttu-id="ea7b2-136">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-136">Duplicate child siblings are not permitted.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ea7b2-137">\*當資料類型是整數或十進位時，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-137">\*Required when DataType is integer or decimal.</span></span> <span data-ttu-id="ea7b2-138">當 DataType 為 string 時為選擇性。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-138">Optional when DataType is string.</span></span>

## <a name="configuration-dependencies"></a><span data-ttu-id="ea7b2-139">設定相依性</span><span class="sxs-lookup"><span data-stu-id="ea7b2-139">Configuration Dependencies</span></span>

<span data-ttu-id="ea7b2-140">ParameterDef 及其內容到任何嵌套層級都可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-140">A ParameterDef and its content to any nesting level may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="ea7b2-141">範例</span><span class="sxs-lookup"><span data-stu-id="ea7b2-141">Example</span></span>

<span data-ttu-id="ea7b2-142">下列範例會為此參數設定所有必要的屬性元素。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-142">The following example sets all of the required Property elements for this parameter.</span></span> <span data-ttu-id="ea7b2-143">[ParameterInit](parameterinit.md)中的範例會示範如何初始化此參數。</span><span class="sxs-lookup"><span data-stu-id="ea7b2-143">The example in [ParameterInit](parameterinit.md) demonstrates how to initialize this parameter.</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a><span data-ttu-id="ea7b2-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea7b2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea7b2-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ea7b2-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




