---
description: 瞭解 Print Schema Framework 中的 XML 屬性。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: XML 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410dcb1476d90568bee10c7c1e41ee7a9bee2e7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548816"
---
# <a name="xml-attributes"></a><span data-ttu-id="c0f7e-105">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="c0f7e-105">XML Attributes</span></span>

<span data-ttu-id="c0f7e-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-106">This topic is not current.</span></span> <span data-ttu-id="c0f7e-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c0f7e-108">在列印架構架構中定義的數個元素類型中，會出現一些 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-108">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="c0f7e-109">具有相同名稱的 XML 屬性通常具有相同的意義，並遵循相同的規則，而不論其所在的元素類型為何。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-109">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="c0f7e-110">因此，XML 屬性會依名稱（而不是其主控制項類型）列在這裡。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-110">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="c0f7e-111">不允許私下定義的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-111">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="c0f7e-112">只有在此處定義的 XML 屬性可用於 PrintCapabilities 檔或 PrintTicket，然後才可用於定義的內容中。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-112">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="c0f7e-113">雖然私用的合作物件不允許將新的定義引入另一個合作物件的命名空間，但它們可以利用另一個私人命名空間的現有名稱，只要其使用方式與其他合作物件建立的使用量一致即可。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-113">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="c0f7e-114">因此，選項可能包含由數個不同的合作物件所定義的 ScoredProperty 元素，每個都位於不同的命名空間中。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-114">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0f7e-115">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="c0f7e-115">Attribute Name</span></span></th>
<th><span data-ttu-id="c0f7e-116">資料類型和值</span><span class="sxs-lookup"><span data-stu-id="c0f7e-116">Data Types and Values</span></span></th>
<th><span data-ttu-id="c0f7e-117">目的</span><span class="sxs-lookup"><span data-stu-id="c0f7e-117">Purpose</span></span></th>
<th><span data-ttu-id="c0f7e-118">注意</span><span class="sxs-lookup"><span data-stu-id="c0f7e-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0f7e-119">NAME</span><span class="sxs-lookup"><span data-stu-id="c0f7e-119">name</span></span> <br/></td>
<td><span data-ttu-id="c0f7e-120">XML QName</span><span class="sxs-lookup"><span data-stu-id="c0f7e-120">XML QName</span></span><br/></td>
<td><span data-ttu-id="c0f7e-121">這個 XML 屬性會識別元素實例。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-121">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="c0f7e-122">它會區分一個專案與相同元素類型的另一個專案。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-122">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="c0f7e-123">這個 XML 屬性很廣泛地使用，稱為 name 屬性。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-123">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="c0f7e-124">下列限制與 name 屬性相關。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-124">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="c0f7e-125">Name 屬性的格式必須是有效的 XML 定義 QName。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-125">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="c0f7e-126">也就是說，它必須由有效的 XML 命名空間限定。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-126">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="c0f7e-127">QNames 顯示為 name 屬性的值，即使已定義預設命名空間，也必須明確限定命名空間。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-127">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="c0f7e-128">字元內容必須是有效的 XML 定義 QName 的字元內容。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-128">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="c0f7e-129">私用定義的名稱必須以命名空間限定的命名空間，此命名空間與引進 name 屬性的合作物件具有唯一關聯性。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-129">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="c0f7e-130">同輩唯一性需求：兩個屬於相同元素類型的同一個同級元素可能具有相同的名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-130">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="c0f7e-131">唯一的例外是 Option 元素，其中 name 屬性可以用來定義選項。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-131">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="c0f7e-132">因此，多個同級的選項元素可能具有相同的名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-132">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="c0f7e-133">下列元素類型可能包含 name 屬性： Property、ScoredProperty、ParameterDef、Option 和 Feature。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-133">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="c0f7e-134">名稱屬性必須出現在包含它們的每個元素類型中，但某些先前定義的公用列印架構選項元素（例如 DocumentNUp）的情況除外。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-134">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="c0f7e-135">下列範例顯示如何使用 ' name ' 屬性來識別選項實例。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-135">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="c0f7e-136">這是定義 Option 元素的正確方式。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-136">This is the correct way to define Option elements.</span></span> <span data-ttu-id="c0f7e-137">提供者不應具有未命名的選項，除非它們是在列印架構中公開定義的，例如 DocumentNUp。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-137">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0f7e-138">傳播</span><span class="sxs-lookup"><span data-stu-id="c0f7e-138">propagate</span></span> <br/></td>
<td><span data-ttu-id="c0f7e-139">列舉型別</span><span class="sxs-lookup"><span data-stu-id="c0f7e-139">Enumeration</span></span><br/> <span data-ttu-id="c0f7e-140">目前未定義任何值。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-140">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="c0f7e-141">「傳播」屬性不會用於「列印架構」架構的初始版本。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-141">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="c0f7e-142">它記載于此處，讓針對 Print Schema Framework 初始版本所執行的 PrintCapabilities 或 PrintTicket 驗證程式代碼可以處理任何後續的架構版本，而不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-142">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c0f7e-143">約束</span><span class="sxs-lookup"><span data-stu-id="c0f7e-143">constrained</span></span> <br/></td>
<td><span data-ttu-id="c0f7e-144">列舉型別</span><span class="sxs-lookup"><span data-stu-id="c0f7e-144">Enumeration</span></span><br/> <span data-ttu-id="c0f7e-145">允許的值：</span><span class="sxs-lookup"><span data-stu-id="c0f7e-145">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="c0f7e-146">無</span><span class="sxs-lookup"><span data-stu-id="c0f7e-146">None</span></span> <br/></li>
<li><span data-ttu-id="c0f7e-147">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="c0f7e-147">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="c0f7e-148">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="c0f7e-148">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="c0f7e-149">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="c0f7e-149">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="c0f7e-150">指出選項是否可供選取或使用。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-150">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="c0f7e-151">受條件約束屬性的允許值具有下列意義。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-151">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="c0f7e-152">請注意，這些值依順序列出，從最嚴格的 (無) 到最嚴格的 (DeviceSettings) 。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-152">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="c0f7e-153">無</span><span class="sxs-lookup"><span data-stu-id="c0f7e-153">None</span></span> <br/>
<ul>
<li><span data-ttu-id="c0f7e-154">此選項不受限制。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-154">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="c0f7e-155">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="c0f7e-155">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="c0f7e-156">選項受限於 PrintTicket 設定。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-156">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="c0f7e-157">這表示變更設定可以移除條件約束。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-157">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="c0f7e-158">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="c0f7e-158">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="c0f7e-159">選項受限於系統管理員的設定;使用者無法啟用此選項。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-159">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="c0f7e-160">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="c0f7e-160">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="c0f7e-161">選項受限於裝置設定或實際安裝的裝置選項;使用者或系統管理員無法啟用此選項。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-161">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="c0f7e-162">當 PrintCapabilities 提供者報告條件約束屬性的值時，應該會報告最嚴格的限制條件約束。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-162">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="c0f7e-163">例如，如果某個選項受限於系統管理員設定和裝置設定，則 PrintCapabilities 提供者應該報告 DeviceSettings。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-163">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0f7e-164">xmlns</span><span class="sxs-lookup"><span data-stu-id="c0f7e-164">xmlns</span></span> <br/></td>
<td><span data-ttu-id="c0f7e-165">URI</span><span class="sxs-lookup"><span data-stu-id="c0f7e-165">URI</span></span><br/></td>
<td><span data-ttu-id="c0f7e-166">這個 XML 屬性會在命名空間統一資源識別項 (URI) 和出現在 XML QName 中的命名空間前置詞之間建立連結。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-166">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="c0f7e-167">您必須先建立針對 Print Schema Framework 所定義之命名空間 URI 的連結，才能使用任何架構定義的專案標記、屬性、名稱屬性等等。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-167">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="c0f7e-168">您可以將此命名空間宣告為預設值，以避免實際以命名空間前置詞來限定元素標記，不過所有其他 QNames 都必須明確限定。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-168">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="c0f7e-169">標準命名空間必須在適當的根項目中定義。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-169">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="c0f7e-170">觀察有關使用 xmlns 屬性的所有 XML 規則和慣例。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-170">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="c0f7e-171">Print Schema Framework 的 URI 為 http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework 。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-171">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="c0f7e-172">列印架構關鍵字的 URI 是 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 。</span><span class="sxs-lookup"><span data-stu-id="c0f7e-172">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c0f7e-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0f7e-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0f7e-174">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="c0f7e-174">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




