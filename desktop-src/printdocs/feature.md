---
description: 檢查功能元素，其中包含描述裝置屬性、作業格式設定或其他相關特性的選項和屬性專案清單。
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28ab7e8cc69ecc9ba3956fbae3c5278baace8cf
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120633"
---
# <a name="feature"></a><span data-ttu-id="f8d31-103">功能</span><span class="sxs-lookup"><span data-stu-id="f8d31-103">Feature</span></span>

<span data-ttu-id="f8d31-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="f8d31-104">This topic is not current.</span></span> <span data-ttu-id="f8d31-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="f8d31-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f8d31-106">Feature 元素包含選項和屬性專案的完整清單，可完整描述裝置屬性、作業格式設定或其他相關特性。</span><span class="sxs-lookup"><span data-stu-id="f8d31-106">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="f8d31-107">元素標記</span><span class="sxs-lookup"><span data-stu-id="f8d31-107">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="f8d31-108">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="f8d31-108">XML Attributes</span></span>

<span data-ttu-id="f8d31-109">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="f8d31-109">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="f8d31-110">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="f8d31-110">XML Attribute</span></span>   | <span data-ttu-id="f8d31-111">詳細資料</span><span class="sxs-lookup"><span data-stu-id="f8d31-111">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d31-112">NAME</span><span class="sxs-lookup"><span data-stu-id="f8d31-112">name</span></span><br/> | <span data-ttu-id="f8d31-113">保存功能的名稱，也就是標準功能或私下定義的功能。</span><span class="sxs-lookup"><span data-stu-id="f8d31-113">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="f8d31-114">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="f8d31-114">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="f8d31-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f8d31-115">Element Information</span></span>

<span data-ttu-id="f8d31-116">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="f8d31-116">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8d31-117">類別</span><span class="sxs-lookup"><span data-stu-id="f8d31-117">Category</span></span></th>
<th><span data-ttu-id="f8d31-118">詳細資料</span><span class="sxs-lookup"><span data-stu-id="f8d31-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8d31-119">父元素</span><span class="sxs-lookup"><span data-stu-id="f8d31-119">Parent elements</span></span><br/></td>
<td><span data-ttu-id="f8d31-120">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="f8d31-120">PrintCapabilities</span></span> <br/> <span data-ttu-id="f8d31-121">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="f8d31-121">PrintTicket</span></span> <br/> <span data-ttu-id="f8d31-122">功能</span><span class="sxs-lookup"><span data-stu-id="f8d31-122">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8d31-123">子元素</span><span class="sxs-lookup"><span data-stu-id="f8d31-123">Child elements</span></span><br/></td>
<td><span data-ttu-id="f8d31-124">下列其中一個群組：</span><span class="sxs-lookup"><span data-stu-id="f8d31-124">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="f8d31-125"><em>功能</em> (零或多個) </span><span class="sxs-lookup"><span data-stu-id="f8d31-125"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="f8d31-126"><em>選項</em> (一或多個) </span><span class="sxs-lookup"><span data-stu-id="f8d31-126"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="f8d31-127"><em>屬性</em> (零或多個) </span><span class="sxs-lookup"><span data-stu-id="f8d31-127"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="f8d31-128">或</span><span class="sxs-lookup"><span data-stu-id="f8d31-128">or</span></span> <br/>
<ul>
<li><span data-ttu-id="f8d31-129"><em>功能</em> (一或多個) </span><span class="sxs-lookup"><span data-stu-id="f8d31-129"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="f8d31-130"><em>選項</em> (零或多個) </span><span class="sxs-lookup"><span data-stu-id="f8d31-130"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="f8d31-131"><em>屬性</em> (零或多個) </span><span class="sxs-lookup"><span data-stu-id="f8d31-131"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8d31-132">這個元素</span><span class="sxs-lookup"><span data-stu-id="f8d31-132">This element</span></span><br/></td>
<td><span data-ttu-id="f8d31-133">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="f8d31-133">No character data is permitted.</span></span><br/> <span data-ttu-id="f8d31-134">允許有同級的重複子選項元素。</span><span class="sxs-lookup"><span data-stu-id="f8d31-134">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="f8d31-135">允許重複的名稱屬性快捷方式。</span><span class="sxs-lookup"><span data-stu-id="f8d31-135">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="f8d31-136">設定相依性</span><span class="sxs-lookup"><span data-stu-id="f8d31-136">Configuration Dependencies</span></span>

<span data-ttu-id="f8d31-137">功能元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="f8d31-137">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="f8d31-138">專案使用方式</span><span class="sxs-lookup"><span data-stu-id="f8d31-138">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="f8d31-139">與 XML 屬性的關聯性</span><span class="sxs-lookup"><span data-stu-id="f8d31-139">Relationship to XML Attributes</span></span>

<span data-ttu-id="f8d31-140">在功能/選項標記法中，裝置屬性是由 Feature 元素表示。</span><span class="sxs-lookup"><span data-stu-id="f8d31-140">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="f8d31-141">裝置屬性是由裝置屬性的 Feature 元素中的 name 屬性唯一識別，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="f8d31-141">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="f8d31-142">在此範例中，裝置屬性為「解析」。</span><span class="sxs-lookup"><span data-stu-id="f8d31-142">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="f8d31-143">列印架構會定義特定功能實例的一組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="f8d31-143">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="f8d31-144">這些名稱屬性會用來識別一組與特定可設定裝置屬性相關聯的預先定義功能實例。</span><span class="sxs-lookup"><span data-stu-id="f8d31-144">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="f8d31-145">您應該在適當的情況下使用這些功能實例名稱，因為它們會增加 PrintCapabilities 檔的可攜性，以及從中衍生的 PrintTickets。</span><span class="sxs-lookup"><span data-stu-id="f8d31-145">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="f8d31-146">如果某些裝置屬性未對應到任何架構定義的功能實例，可能會引進私用定義的功能實例。</span><span class="sxs-lookup"><span data-stu-id="f8d31-146">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="f8d31-147">如需名稱屬性語法的詳細資訊，以及適用于架構定義和私人定義名稱的慣例，請參閱 [XML 屬性](xml-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="f8d31-147">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="f8d31-148">Option 元素的關聯性</span><span class="sxs-lookup"><span data-stu-id="f8d31-148">Relationship to Option Element</span></span>

<span data-ttu-id="f8d31-149">每個可能的狀態都會以 Option 元素表示。</span><span class="sxs-lookup"><span data-stu-id="f8d31-149">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="f8d31-150">每個選項定義都包含一或多個 ScoredProperty 元素，這些元素會以獨特的方式來描述或描述所表示的狀態。</span><span class="sxs-lookup"><span data-stu-id="f8d31-150">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="f8d31-151">[選項定義](option-definitions.md)中說明用來建立選項定義的技巧。</span><span class="sxs-lookup"><span data-stu-id="f8d31-151">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="f8d31-152">所有與特定功能專案相關聯的選項元素都會作為 Feature 專案的子專案。</span><span class="sxs-lookup"><span data-stu-id="f8d31-152">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="f8d31-153">釋放</span><span class="sxs-lookup"><span data-stu-id="f8d31-153">Subfeatures</span></span>

<span data-ttu-id="f8d31-154">Print Schema Framework 也可讓您以階層方式將功能專案群組在一起。</span><span class="sxs-lookup"><span data-stu-id="f8d31-154">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="f8d31-155">也就是說，Feature 元素本身可以包含一或多個子功能元素， (子功能) 。</span><span class="sxs-lookup"><span data-stu-id="f8d31-155">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="f8d31-156">這有助於組織相關的功能專案，或用於控制裝置功能各個層面的功能元素。</span><span class="sxs-lookup"><span data-stu-id="f8d31-156">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="f8d31-157">其中一個範例是支援裝訂的裝置。</span><span class="sxs-lookup"><span data-stu-id="f8d31-157">One example is a device that supports stapling.</span></span> <span data-ttu-id="f8d31-158">這類裝置可讓使用者選擇要在哪裡找到裝訂，例如左上角或右上角，或是沿著上邊緣，或是沿著左邊緣。</span><span class="sxs-lookup"><span data-stu-id="f8d31-158">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="f8d31-159">此裝置 (UI) 的使用者介面應該能夠先顯示最高層級選項的使用者，在此案例中是要使用裝訂。</span><span class="sxs-lookup"><span data-stu-id="f8d31-159">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="f8d31-160">只有在使用者決定使用裝訂之後，使用者才會看到第二層選擇：裝訂位置。</span><span class="sxs-lookup"><span data-stu-id="f8d31-160">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="f8d31-161">功能階層會新增可讓這類使用者介面成為可能的額外結構。</span><span class="sxs-lookup"><span data-stu-id="f8d31-161">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="f8d31-162">Print Schema Framework 可讓子功能擁有自己的子功能，因此允許無限制的嵌套層級。</span><span class="sxs-lookup"><span data-stu-id="f8d31-162">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="f8d31-163">Print Schema Framework 也可讓選項元素出現在與子功能相同的層級;亦即相同父項功能專案內的同級。</span><span class="sxs-lookup"><span data-stu-id="f8d31-163">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="f8d31-164">這可讓使用者進行高階決策 (是否要在進行 subfeature 選擇之前使用裝訂) 。</span><span class="sxs-lookup"><span data-stu-id="f8d31-164">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="f8d31-165">在此範例中，根功能元素 "裝訂" 可能包含兩個選項元素： "On" 和 "Off"，以及名為 "StapleLocation" 的 subfeature。</span><span class="sxs-lookup"><span data-stu-id="f8d31-165">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="f8d31-166">範例</span><span class="sxs-lookup"><span data-stu-id="f8d31-166">Example</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f8d31-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8d31-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8d31-168">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="f8d31-168">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




