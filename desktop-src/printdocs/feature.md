---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "107000212"
---
# <a name="feature"></a><span data-ttu-id="e10df-104">功能</span><span class="sxs-lookup"><span data-stu-id="e10df-104">Feature</span></span>

<span data-ttu-id="e10df-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e10df-105">This topic is not current.</span></span> <span data-ttu-id="e10df-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e10df-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e10df-107">Feature 元素包含選項和屬性專案的完整清單，可完整描述裝置屬性、作業格式設定或其他相關特性。</span><span class="sxs-lookup"><span data-stu-id="e10df-107">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="e10df-108">元素標記</span><span class="sxs-lookup"><span data-stu-id="e10df-108">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="e10df-109">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="e10df-109">XML Attributes</span></span>

<span data-ttu-id="e10df-110">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="e10df-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="e10df-111">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="e10df-111">XML Attribute</span></span>   | <span data-ttu-id="e10df-112">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e10df-112">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10df-113">NAME</span><span class="sxs-lookup"><span data-stu-id="e10df-113">name</span></span><br/> | <span data-ttu-id="e10df-114">保存功能的名稱，也就是標準功能或私下定義的功能。</span><span class="sxs-lookup"><span data-stu-id="e10df-114">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="e10df-115">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="e10df-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="e10df-116">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e10df-116">Element Information</span></span>

<span data-ttu-id="e10df-117">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="e10df-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e10df-118">類別</span><span class="sxs-lookup"><span data-stu-id="e10df-118">Category</span></span></th>
<th><span data-ttu-id="e10df-119">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e10df-119">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e10df-120">父元素</span><span class="sxs-lookup"><span data-stu-id="e10df-120">Parent elements</span></span><br/></td>
<td><span data-ttu-id="e10df-121">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="e10df-121">PrintCapabilities</span></span> <br/> <span data-ttu-id="e10df-122">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="e10df-122">PrintTicket</span></span> <br/> <span data-ttu-id="e10df-123">功能</span><span class="sxs-lookup"><span data-stu-id="e10df-123">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e10df-124">子元素</span><span class="sxs-lookup"><span data-stu-id="e10df-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="e10df-125">下列其中一個群組：</span><span class="sxs-lookup"><span data-stu-id="e10df-125">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="e10df-126"><em>功能</em> (零或多個) </span><span class="sxs-lookup"><span data-stu-id="e10df-126"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="e10df-127"><em>選項</em> (一或多個) </span><span class="sxs-lookup"><span data-stu-id="e10df-127"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="e10df-128"><em>屬性</em> (零或多個) </span><span class="sxs-lookup"><span data-stu-id="e10df-128"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="e10df-129">或</span><span class="sxs-lookup"><span data-stu-id="e10df-129">or</span></span> <br/>
<ul>
<li><span data-ttu-id="e10df-130"><em>功能</em> (一或多個) </span><span class="sxs-lookup"><span data-stu-id="e10df-130"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="e10df-131"><em>選項</em> (零或多個) </span><span class="sxs-lookup"><span data-stu-id="e10df-131"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="e10df-132"><em>屬性</em> (零或多個) </span><span class="sxs-lookup"><span data-stu-id="e10df-132"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e10df-133">這個元素</span><span class="sxs-lookup"><span data-stu-id="e10df-133">This element</span></span><br/></td>
<td><span data-ttu-id="e10df-134">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="e10df-134">No character data is permitted.</span></span><br/> <span data-ttu-id="e10df-135">允許有同級的重複子選項元素。</span><span class="sxs-lookup"><span data-stu-id="e10df-135">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="e10df-136">允許重複的名稱屬性快捷方式。</span><span class="sxs-lookup"><span data-stu-id="e10df-136">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="e10df-137">設定相依性</span><span class="sxs-lookup"><span data-stu-id="e10df-137">Configuration Dependencies</span></span>

<span data-ttu-id="e10df-138">功能元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="e10df-138">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="e10df-139">專案使用方式</span><span class="sxs-lookup"><span data-stu-id="e10df-139">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="e10df-140">與 XML 屬性的關聯性</span><span class="sxs-lookup"><span data-stu-id="e10df-140">Relationship to XML Attributes</span></span>

<span data-ttu-id="e10df-141">在功能/選項標記法中，裝置屬性是由 Feature 元素表示。</span><span class="sxs-lookup"><span data-stu-id="e10df-141">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="e10df-142">裝置屬性是由裝置屬性的 Feature 元素中的 name 屬性唯一識別，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="e10df-142">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="e10df-143">在此範例中，裝置屬性為「解析」。</span><span class="sxs-lookup"><span data-stu-id="e10df-143">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="e10df-144">列印架構會定義特定功能實例的一組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="e10df-144">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="e10df-145">這些名稱屬性會用來識別一組與特定可設定裝置屬性相關聯的預先定義功能實例。</span><span class="sxs-lookup"><span data-stu-id="e10df-145">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="e10df-146">您應該在適當的情況下使用這些功能實例名稱，因為它們會增加 PrintCapabilities 檔的可攜性，以及從中衍生的 PrintTickets。</span><span class="sxs-lookup"><span data-stu-id="e10df-146">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="e10df-147">如果某些裝置屬性未對應到任何架構定義的功能實例，可能會引進私用定義的功能實例。</span><span class="sxs-lookup"><span data-stu-id="e10df-147">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="e10df-148">如需名稱屬性語法的詳細資訊，以及適用于架構定義和私人定義名稱的慣例，請參閱 [XML 屬性](xml-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="e10df-148">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="e10df-149">Option 元素的關聯性</span><span class="sxs-lookup"><span data-stu-id="e10df-149">Relationship to Option Element</span></span>

<span data-ttu-id="e10df-150">每個可能的狀態都會以 Option 元素表示。</span><span class="sxs-lookup"><span data-stu-id="e10df-150">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="e10df-151">每個選項定義都包含一或多個 ScoredProperty 元素，這些元素會以獨特的方式來描述或描述所表示的狀態。</span><span class="sxs-lookup"><span data-stu-id="e10df-151">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="e10df-152">[選項定義](option-definitions.md)中說明用來建立選項定義的技巧。</span><span class="sxs-lookup"><span data-stu-id="e10df-152">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="e10df-153">所有與特定功能專案相關聯的選項元素都會作為 Feature 專案的子專案。</span><span class="sxs-lookup"><span data-stu-id="e10df-153">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="e10df-154">釋放</span><span class="sxs-lookup"><span data-stu-id="e10df-154">Subfeatures</span></span>

<span data-ttu-id="e10df-155">Print Schema Framework 也可讓您以階層方式將功能專案群組在一起。</span><span class="sxs-lookup"><span data-stu-id="e10df-155">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="e10df-156">也就是說，Feature 元素本身可以包含一或多個子功能元素， (子功能) 。</span><span class="sxs-lookup"><span data-stu-id="e10df-156">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="e10df-157">這有助於組織相關的功能專案，或用於控制裝置功能各個層面的功能元素。</span><span class="sxs-lookup"><span data-stu-id="e10df-157">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="e10df-158">其中一個範例是支援裝訂的裝置。</span><span class="sxs-lookup"><span data-stu-id="e10df-158">One example is a device that supports stapling.</span></span> <span data-ttu-id="e10df-159">這類裝置可讓使用者選擇要在哪裡找到裝訂，例如左上角或右上角，或是沿著上邊緣，或是沿著左邊緣。</span><span class="sxs-lookup"><span data-stu-id="e10df-159">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="e10df-160">此裝置 (UI) 的使用者介面應該能夠先顯示最高層級選項的使用者，在此案例中是要使用裝訂。</span><span class="sxs-lookup"><span data-stu-id="e10df-160">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="e10df-161">只有在使用者決定使用裝訂之後，使用者才會看到第二層選擇：裝訂位置。</span><span class="sxs-lookup"><span data-stu-id="e10df-161">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="e10df-162">功能階層會新增可讓這類使用者介面成為可能的額外結構。</span><span class="sxs-lookup"><span data-stu-id="e10df-162">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="e10df-163">Print Schema Framework 可讓子功能擁有自己的子功能，因此允許無限制的嵌套層級。</span><span class="sxs-lookup"><span data-stu-id="e10df-163">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="e10df-164">Print Schema Framework 也可讓選項元素出現在與子功能相同的層級;亦即相同父項功能專案內的同級。</span><span class="sxs-lookup"><span data-stu-id="e10df-164">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="e10df-165">這可讓使用者進行高階決策 (是否要在進行 subfeature 選擇之前使用裝訂) 。</span><span class="sxs-lookup"><span data-stu-id="e10df-165">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="e10df-166">在此範例中，根功能元素 "裝訂" 可能包含兩個選項元素： "On" 和 "Off"，以及名為 "StapleLocation" 的 subfeature。</span><span class="sxs-lookup"><span data-stu-id="e10df-166">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="e10df-167">範例</span><span class="sxs-lookup"><span data-stu-id="e10df-167">Example</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="e10df-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="e10df-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e10df-169">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e10df-169">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




