---
title: 架構支援層級
description: 本節涵蓋有關架構支援層級的詳細資料。
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- 適用于 Windows 的架構支援層級 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104553393"
---
# <a name="schema-support-level"></a><span data-ttu-id="11aaf-106">架構支援層級</span><span class="sxs-lookup"><span data-stu-id="11aaf-106">Schema support level</span></span>

<span data-ttu-id="11aaf-107">本節涵蓋有關架構支援層級的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11aaf-107">This section covers the details around the level of schema support.</span></span>


<span data-ttu-id="11aaf-108">架構直接支援下列各項：</span><span class="sxs-lookup"><span data-stu-id="11aaf-108">The schema directly supports the following:</span></span>

-   <span data-ttu-id="11aaf-109">元素的序列。</span><span class="sxs-lookup"><span data-stu-id="11aaf-109">Sequences of elements.</span></span>
-   <span data-ttu-id="11aaf-110">元素類型的衍生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-110">Derivation of element types.</span></span>
-   <span data-ttu-id="11aaf-111">專案的簡單選擇 (對應至加上標籤聯集) 的專案。</span><span class="sxs-lookup"><span data-stu-id="11aaf-111">Simple choices of elements (those that map to a tagged union).</span></span>
-   <span data-ttu-id="11aaf-112">XSD/.NET 二進位格式所定義的基本類型，包括範圍 (min/max) 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-112">Basic types defined by XSD / .NET binary format including ranges (min/max).</span></span>
-   <span data-ttu-id="11aaf-113">對任何專案的簡單支援 (專案) 的類型沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="11aaf-113">Simple support for any element (no restrictions on type of element).</span></span>
-   <span data-ttu-id="11aaf-114">具有預設值的選擇性元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="11aaf-114">Optional elements and attributes with default values.</span></span>
-   <span data-ttu-id="11aaf-115">範圍 (min/max) 的重複元素。</span><span class="sxs-lookup"><span data-stu-id="11aaf-115">Repeating elements with ranges (min/max).</span></span>
-   <span data-ttu-id="11aaf-116">Nillable 元素。</span><span class="sxs-lookup"><span data-stu-id="11aaf-116">Nillable elements.</span></span>

<span data-ttu-id="11aaf-117">架構不支援下列直接 (表示「回溯」行為) ：</span><span class="sxs-lookup"><span data-stu-id="11aaf-117">The schema does not support the following directly (which imply the "fallback" behavior):</span></span>

-   <span data-ttu-id="11aaf-118">使用者定義的基本類型。</span><span class="sxs-lookup"><span data-stu-id="11aaf-118">User defined basic types.</span></span>
-   <span data-ttu-id="11aaf-119">更複雜的選項。</span><span class="sxs-lookup"><span data-stu-id="11aaf-119">More complicated choices.</span></span>
-   <span data-ttu-id="11aaf-120">拒絕未知的屬性。</span><span class="sxs-lookup"><span data-stu-id="11aaf-120">Rejecting unknown attributes.</span></span>
-   <span data-ttu-id="11aaf-121">來回往返未知的屬性。</span><span class="sxs-lookup"><span data-stu-id="11aaf-121">Round tripping unknown attributes.</span></span>
-   <span data-ttu-id="11aaf-122">對任何專案更複雜的支援。</span><span class="sxs-lookup"><span data-stu-id="11aaf-122">More complicated support for any element.</span></span>
-   <span data-ttu-id="11aaf-123">All 結構。</span><span class="sxs-lookup"><span data-stu-id="11aaf-123">The all construct.</span></span>
-   <span data-ttu-id="11aaf-124">Key/keyref。</span><span class="sxs-lookup"><span data-stu-id="11aaf-124">Key/keyref.</span></span>

<span data-ttu-id="11aaf-125">以下是不同架構元件支援的詳細細目。</span><span class="sxs-lookup"><span data-stu-id="11aaf-125">Following is a detailed breakdown of different schema component support.</span></span> <span data-ttu-id="11aaf-126">它會與 WCF 中的資料合約比較，因為功能中的相似性。</span><span class="sxs-lookup"><span data-stu-id="11aaf-126">It is compared with data contract in WCF because the similarity in functionality.</span></span> <span data-ttu-id="11aaf-127">將會說明差異。</span><span class="sxs-lookup"><span data-stu-id="11aaf-127">The difference will be described.</span></span>

<span data-ttu-id="11aaf-128">通常，針對回溯行為：</span><span class="sxs-lookup"><span data-stu-id="11aaf-128">Generally, for fallback behaviors:</span></span>

-   <span data-ttu-id="11aaf-129">屬性會被備份到 WS \_ 字串;</span><span class="sxs-lookup"><span data-stu-id="11aaf-129">attributes are fall backed to WS\_STRING;</span></span>
-   <span data-ttu-id="11aaf-130">元素內容會被支援至 WS \_ XML \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11aaf-130">element content are fall backed to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="11aaf-131">complexType 的支援是包含 WS XML 緩衝區欄位的結構 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-131">complexType are fall backed to structure containing a field of WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="11aaf-132">簡單類型會支援到 WS \_ 字串。</span><span class="sxs-lookup"><span data-stu-id="11aaf-132">Simple types are fall backed to WS\_STRING.</span></span>

<span data-ttu-id="11aaf-133">wsutil 會針對目前未完全支援的架構元件產生警告。</span><span class="sxs-lookup"><span data-stu-id="11aaf-133">wsutil generates warnings for schema components that are not currently fully supported.</span></span> <span data-ttu-id="11aaf-134">應用程式可能需要針對這些元件進行額外的驗證。</span><span class="sxs-lookup"><span data-stu-id="11aaf-134">Application might need to do additional verification for those components are needed.</span></span> <span data-ttu-id="11aaf-135">您可以改進加班 wsutil 來處理執行時間目前支援的一些功能，例如預設值支援。</span><span class="sxs-lookup"><span data-stu-id="11aaf-135">Overtime wsutil can be improved to handle some of the features that are currently supported in runtime, like default value support.</span></span> <span data-ttu-id="11aaf-136">wsutil 也可與序列化一起改善，以支援其他功能，例如抽象。</span><span class="sxs-lookup"><span data-stu-id="11aaf-136">wsutil can also be improved together with serialization to support other features like abstract.</span></span> <span data-ttu-id="11aaf-137">不支援的架構元件數目可在一段時間後減少。</span><span class="sxs-lookup"><span data-stu-id="11aaf-137">The number of unsupported schema components can be reduced over time.</span></span>

## <a name="the-overall-schema-document"></a><span data-ttu-id="11aaf-138">整體架構檔</span><span class="sxs-lookup"><span data-stu-id="11aaf-138">The Overall Schema Document</span></span>

<span data-ttu-id="11aaf-139">全域定義，可能會影響架構中的內嵌定義。</span><span class="sxs-lookup"><span data-stu-id="11aaf-139">Global definition that might affect embedded definitions in the schema.</span></span> <span data-ttu-id="11aaf-140">這些是全域屬性，適用于架構中的所有定義。</span><span class="sxs-lookup"><span data-stu-id="11aaf-140">These are global attributes that are applicable to all definitions in the schema.</span></span>

<span data-ttu-id="11aaf-141"><xs： schema> 屬性</span><span class="sxs-lookup"><span data-stu-id="11aaf-141"><xs:schema> attributes</span></span>

-   <span data-ttu-id="11aaf-142">已忽略 attributeFromDefault。</span><span class="sxs-lookup"><span data-stu-id="11aaf-142">attributeFromDefault Ignored.</span></span>
-   <span data-ttu-id="11aaf-143">已忽略 blockDefault。</span><span class="sxs-lookup"><span data-stu-id="11aaf-143">blockDefault Ignored.</span></span>
-   <span data-ttu-id="11aaf-144">已忽略 elementFormDefault。</span><span class="sxs-lookup"><span data-stu-id="11aaf-144">elementFormDefault Ignored.</span></span> <span data-ttu-id="11aaf-145">這與 dataContract 不同，因為執行時間支援不合格的元素。</span><span class="sxs-lookup"><span data-stu-id="11aaf-145">This is different from dataContract as unqualified elements are supported in runtime.</span></span>
-   <span data-ttu-id="11aaf-146">已忽略 finalDefault。</span><span class="sxs-lookup"><span data-stu-id="11aaf-146">finalDefault Ignored.</span></span> <span data-ttu-id="11aaf-147">最終的概念不支援 C 語言。</span><span class="sxs-lookup"><span data-stu-id="11aaf-147">There is no C language support for the concept of final.</span></span>
-   <span data-ttu-id="11aaf-148">已忽略識別碼。</span><span class="sxs-lookup"><span data-stu-id="11aaf-148">id Ignored.</span></span>
-   <span data-ttu-id="11aaf-149">targetNamespace 支援並對應至服務命名空間。</span><span class="sxs-lookup"><span data-stu-id="11aaf-149">targetNamespace Supported and mapped to the service namespace.</span></span>
-   <span data-ttu-id="11aaf-150">已忽略版本。</span><span class="sxs-lookup"><span data-stu-id="11aaf-150">version Ignored.</span></span>

<span data-ttu-id="11aaf-151"><xs： schema> 內容</span><span class="sxs-lookup"><span data-stu-id="11aaf-151"><xs:schema> contents</span></span>

-   <span data-ttu-id="11aaf-152">包含支援的;wsutil 需要在編譯期間將所有必要的定義當作輸入檔來使用。</span><span class="sxs-lookup"><span data-stu-id="11aaf-152">include Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="11aaf-153">已忽略重新定義。</span><span class="sxs-lookup"><span data-stu-id="11aaf-153">redefine Ignored.</span></span> <span data-ttu-id="11aaf-154">wsutil 不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="11aaf-154">wsutil does not support this.</span></span>
-   <span data-ttu-id="11aaf-155">支援匯入;wsutil 需要在編譯期間將所有必要的定義當作輸入檔來使用。</span><span class="sxs-lookup"><span data-stu-id="11aaf-155">import Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="11aaf-156">支援 simpleType-請參閱下方的簡單類型區段。</span><span class="sxs-lookup"><span data-stu-id="11aaf-156">simpleType Supported- see simple type section below.</span></span>
-   <span data-ttu-id="11aaf-157">支援 complexType-請參閱 ' complexType ' 區段</span><span class="sxs-lookup"><span data-stu-id="11aaf-157">complexType Supported- see 'complexType' section</span></span>
-   <span data-ttu-id="11aaf-158">已忽略群組。</span><span class="sxs-lookup"><span data-stu-id="11aaf-158">group Ignored.</span></span>
-   <span data-ttu-id="11aaf-159">已忽略 attributeGroup。</span><span class="sxs-lookup"><span data-stu-id="11aaf-159">attributeGroup Ignored.</span></span>
-   <span data-ttu-id="11aaf-160">支援的元素;對應至全域元素定義。</span><span class="sxs-lookup"><span data-stu-id="11aaf-160">element Supported; maps to global element definitions.</span></span>
-   <span data-ttu-id="11aaf-161">支援的屬性;對應到全域屬性定義。</span><span class="sxs-lookup"><span data-stu-id="11aaf-161">attribute Supported; maps to global attribute definitions.</span></span>
-   <span data-ttu-id="11aaf-162">已忽略標記法</span><span class="sxs-lookup"><span data-stu-id="11aaf-162">notation Ignored</span></span>

## <a name="complex-type"></a><span data-ttu-id="11aaf-163">複雜類型</span><span class="sxs-lookup"><span data-stu-id="11aaf-163">Complex Type</span></span>

<span data-ttu-id="11aaf-164">以 <xs： complexType> 表示的複雜類型可能會限制簡單類型或複雜類型、簡單類型、陣列或結構的副檔名。</span><span class="sxs-lookup"><span data-stu-id="11aaf-164">Complex type, represented by <xs:complexType>, could be restriction of simple type or complex type, extension of simple type, arrays or structure.</span></span> <span data-ttu-id="11aaf-165">請注意，在簡單類型的延伸中，沒有任何繼承和 xsi： type 支援。</span><span class="sxs-lookup"><span data-stu-id="11aaf-165">Noticed that in extension of simple types, there is no inheritance and no xsi:type support.</span></span>

<span data-ttu-id="11aaf-166"><xs： complexType> 屬性</span><span class="sxs-lookup"><span data-stu-id="11aaf-166"><xs:complexType> attributes</span></span>

-   <span data-ttu-id="11aaf-167">abstract 會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-167">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-168">封鎖會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-168">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-169">最後會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-169">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-170">已忽略識別碼。</span><span class="sxs-lookup"><span data-stu-id="11aaf-170">id Ignored.</span></span>
-   <span data-ttu-id="11aaf-171">mixed 會產生關於不支援功能的警告， \_ 如果為 true，則會使用 WS XML 緩衝區來切換至結構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-171">mixed Generate warning about unsupported feature, fallback to structure with WS\_XML\_BUFFER if true.</span></span>
-   <span data-ttu-id="11aaf-172">名稱支援且對應至結構類型名稱。</span><span class="sxs-lookup"><span data-stu-id="11aaf-172">name Supported and mapped to structure type name.</span></span>

<span data-ttu-id="11aaf-173"><xs： complexType> 內容</span><span class="sxs-lookup"><span data-stu-id="11aaf-173"><xs:complexType> contents</span></span>

<span data-ttu-id="11aaf-174">這是結構的型別定義。</span><span class="sxs-lookup"><span data-stu-id="11aaf-174">This is type definition for structure.</span></span> <span data-ttu-id="11aaf-175">不支援 complexContent 限制。</span><span class="sxs-lookup"><span data-stu-id="11aaf-175">complexContent restriction is not supported.</span></span>

-   <span data-ttu-id="11aaf-176">complexContent 支援複雜內容延伸模組。</span><span class="sxs-lookup"><span data-stu-id="11aaf-176">complexContent Support complex content extension.</span></span> <span data-ttu-id="11aaf-177">對應至結構繼承。</span><span class="sxs-lookup"><span data-stu-id="11aaf-177">Maps to structure inheritance.</span></span>
-   <span data-ttu-id="11aaf-178">群組目前已與 WS \_ XML 緩衝區欄位回溯至結構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-178">group Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="11aaf-179">可以根據下一個物件來支援。</span><span class="sxs-lookup"><span data-stu-id="11aaf-179">Can be supported according to the underneath particle.</span></span>
-   <span data-ttu-id="11aaf-180">選擇支援做為聯集。</span><span class="sxs-lookup"><span data-stu-id="11aaf-180">choice supported as union.</span></span> <span data-ttu-id="11aaf-181">資料合約中不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="11aaf-181">This is not supported in data contract.</span></span>
-   <span data-ttu-id="11aaf-182">支援的序列-對應至結構的欄位</span><span class="sxs-lookup"><span data-stu-id="11aaf-182">sequence Supported - maps to fields of a structure</span></span>
-   <span data-ttu-id="11aaf-183">支援屬性，但有一個例外狀況「禁止」。</span><span class="sxs-lookup"><span data-stu-id="11aaf-183">attribute supported with one exception of 'prohibited'.</span></span> <span data-ttu-id="11aaf-184">如果「禁止」，則會使用 WS XML 緩衝區來切換至結構 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-184">fallback to structure with WS\_XML\_BUFFER if 'prohibited'.</span></span>
-   <span data-ttu-id="11aaf-185">attributeGroup 支援-對應至屬性的順序</span><span class="sxs-lookup"><span data-stu-id="11aaf-185">attributeGroup supported - maps to sequence of attributes</span></span>
-   <span data-ttu-id="11aaf-186">已忽略 anyAttribute</span><span class="sxs-lookup"><span data-stu-id="11aaf-186">anyAttribute Ignored</span></span>
-   <span data-ttu-id="11aaf-187">AttributeGroupRef 支援-對應至屬性的順序。</span><span class="sxs-lookup"><span data-stu-id="11aaf-187">AttributeGroupRef Supported - maps to sequence of attributes.</span></span>
-   <span data-ttu-id="11aaf-188">GroupRef 目前已使用 WS \_ XML 緩衝區欄位回溯至結構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-188">GroupRef Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="11aaf-189">可以根據下一個群組來支援。</span><span class="sxs-lookup"><span data-stu-id="11aaf-189">Can be supported according to the underneath group.</span></span>
-   <span data-ttu-id="11aaf-190">任何支援的，對應至 XML \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="11aaf-190">Any Supported, maps to XML\_BUFFER</span></span>
-   <span data-ttu-id="11aaf-191"> (空白) 支援的對應至空白結構描述，但未產生任何結構。</span><span class="sxs-lookup"><span data-stu-id="11aaf-191">(blank) supported map to empty struct description with no struct generated.</span></span>

<span data-ttu-id="11aaf-192">複雜型別中的 <xs:sequence>：內容</span><span class="sxs-lookup"><span data-stu-id="11aaf-192"><xs:sequence> in a complex type: contents</span></span>

<span data-ttu-id="11aaf-193">wsutil 僅支援 minOccurs = 1 和 maxOccurs = 1 的完整支援順序;否則，複雜型別目前會支援到 WS \_ XML \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11aaf-193">wsutil only fully support sequence of minOccurs = 1 and maxOccurs = 1; otherwise the complex type is currently fall backed to WS\_XML\_BUFFER.</span></span> <span data-ttu-id="11aaf-194">它可支援為結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="11aaf-194">It can be supported as array of structures.</span></span>

-   <span data-ttu-id="11aaf-195">支援的元素;每個實例都會對應至結構中的欄位。</span><span class="sxs-lookup"><span data-stu-id="11aaf-195">element Supported; each instance maps to a field in the structure.</span></span>
-   <span data-ttu-id="11aaf-196">群組退回;complexType 會回到 WS \_ XML \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11aaf-196">Group fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="11aaf-197">所有回復;complexType 會回到 WS \_ XML \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11aaf-197">All fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="11aaf-198">支援的選擇;對應至聯集欄位。</span><span class="sxs-lookup"><span data-stu-id="11aaf-198">choice supported; map to union field.</span></span>
-   <span data-ttu-id="11aaf-199">順序回復;complexType 會回到 WS \_ XML \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11aaf-199">sequence fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="11aaf-200">任何支援的;對應至 XML \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11aaf-200">any Supported; mapped to XML\_BUFFER.</span></span>
-   <span data-ttu-id="11aaf-201"> (空白) 支援;如果沒有任何屬性，則 complexType 可以是空的結構。</span><span class="sxs-lookup"><span data-stu-id="11aaf-201">(blank) supported; complexType can be an empty structure if there is no attributes.</span></span>

## <a name="elements"></a><span data-ttu-id="11aaf-202">元素</span><span class="sxs-lookup"><span data-stu-id="11aaf-202">Elements</span></span>

<span data-ttu-id="11aaf-203"><xs： element>可能發生在三個內容中。</span><span class="sxs-lookup"><span data-stu-id="11aaf-203"><xs:element>may occur in three contexts.</span></span>

-   <span data-ttu-id="11aaf-204">它可能會出現在 <xs： sequence> 中，描述一般結構的欄位。</span><span class="sxs-lookup"><span data-stu-id="11aaf-204">It may occur within an <xs:sequence>, describing a field of a regular struct.</span></span> <span data-ttu-id="11aaf-205">在此情況下，maxOccurs 屬性必須是1。</span><span class="sxs-lookup"><span data-stu-id="11aaf-205">In this case, the maxOccurs attribute must be 1.</span></span> <span data-ttu-id="11aaf-206">如果 minOccurs 為0，則此欄位是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="11aaf-206">The field is optional if minOccurs is 0.</span></span>
-   <span data-ttu-id="11aaf-207">它可能會出現在 <xs： sequence> 中，描述陣列的欄位。</span><span class="sxs-lookup"><span data-stu-id="11aaf-207">It may occur within an <xs:sequence>, describing a field of an array.</span></span> <span data-ttu-id="11aaf-208">在此情況下，maxOccurs 屬性必須大於1或「未系結」。</span><span class="sxs-lookup"><span data-stu-id="11aaf-208">In this case, the maxOccurs attribute must be greater than 1 or 'unbounded'.</span></span>
-   <span data-ttu-id="11aaf-209">它可能會在 <xs： schema> 內，做為全域專案描述。</span><span class="sxs-lookup"><span data-stu-id="11aaf-209">It may occur within an <xs:schema> as a global element description.</span></span>

<span data-ttu-id="11aaf-210"><xs： element> 在 <xs： sequence> 或 <xs： choice> 作為結構中的欄位</span><span class="sxs-lookup"><span data-stu-id="11aaf-210"><xs:element> within an <xs:sequence> or <xs:choice> as a field in a structure</span></span>

-   <span data-ttu-id="11aaf-211">支援 ref;解析為全域元素的參考。</span><span class="sxs-lookup"><span data-stu-id="11aaf-211">ref Supported; resolved to reference to global element.</span></span>
-   <span data-ttu-id="11aaf-212">名稱支援，對應至功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="11aaf-212">name Supported, maps to field name.</span></span>
-   <span data-ttu-id="11aaf-213">支援的類型，對應至欄位類型。</span><span class="sxs-lookup"><span data-stu-id="11aaf-213">type Supported, maps to field type.</span></span> <span data-ttu-id="11aaf-214">如需詳細資訊，請參閱「類型對應」。</span><span class="sxs-lookup"><span data-stu-id="11aaf-214">For more information, see 'Type Mapping'.</span></span> <span data-ttu-id="11aaf-215">如果未指定 (且元素未包含匿名型別) ，則會假設為 xs： anyType。</span><span class="sxs-lookup"><span data-stu-id="11aaf-215">If not specified (and the element does not contain an anonymous type), xs:anyType is assumed.</span></span>
-   <span data-ttu-id="11aaf-216">封鎖會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-216">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-217">預設會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-217">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-218">已修正產生不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-218">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-219">忽略的表單。</span><span class="sxs-lookup"><span data-stu-id="11aaf-219">form Ignored.</span></span> <span data-ttu-id="11aaf-220">我們的序列化層同時支援合格和不合格的表單。</span><span class="sxs-lookup"><span data-stu-id="11aaf-220">Our serialization layer supports both qualified and unqualified forms.</span></span>
-   <span data-ttu-id="11aaf-221">已忽略識別碼。</span><span class="sxs-lookup"><span data-stu-id="11aaf-221">id Ignored.</span></span>
-   <span data-ttu-id="11aaf-222">如果等於1，則 maxOccurs 對應至單一資料欄位。</span><span class="sxs-lookup"><span data-stu-id="11aaf-222">maxOccurs maps to a single data field if equals 1.</span></span> <span data-ttu-id="11aaf-223">如果 maxOccurs 大於1，它會對應至陣列欄位， (重複元素) 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-223">it is mapped to an array field (repeating element) if maxOccurs is larger than 1.</span></span>
-   <span data-ttu-id="11aaf-224">如果為0，則欄位選項設定為 [欄位 \_ 選擇性] （如果未設定 nillable）。</span><span class="sxs-lookup"><span data-stu-id="11aaf-224">minOccurs if 0, the field options is set to FIELD\_OPTIONAL, if nillable is not set.</span></span>
-   <span data-ttu-id="11aaf-225">nillable 欄位是 nillable。</span><span class="sxs-lookup"><span data-stu-id="11aaf-225">nillable The field is nillable.</span></span> <span data-ttu-id="11aaf-226">如需詳細資訊，請參閱 [序列化](serialization.md) 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-226">See [Serialization](serialization.md) for more detail.</span></span>

<span data-ttu-id="11aaf-227"><xs： element> 為 global element： attributes</span><span class="sxs-lookup"><span data-stu-id="11aaf-227"><xs:element> as global element: attributes</span></span>

<span data-ttu-id="11aaf-228">minOccurs 和 maxOccurs 屬性是不正確全域元素描述。</span><span class="sxs-lookup"><span data-stu-id="11aaf-228">minOccurs and maxOccurs attributes are invalid as global element description.</span></span> <span data-ttu-id="11aaf-229">應用程式可以直接在序列化層或通道層級中使用產生的元素描述。</span><span class="sxs-lookup"><span data-stu-id="11aaf-229">Application can use generated element description in serialization layer or channel layers directly.</span></span>

-   <span data-ttu-id="11aaf-230">abstract 會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-230">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-231">封鎖會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-231">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-232">預設會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-232">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-233">最後會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-233">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-234">已修正產生不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-234">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-235">已忽略識別碼。</span><span class="sxs-lookup"><span data-stu-id="11aaf-235">id Ignored.</span></span>
-   <span data-ttu-id="11aaf-236">支援的名稱-對應至全域元素描述的名稱，而這是指定時匿名型別的基底。</span><span class="sxs-lookup"><span data-stu-id="11aaf-236">name Supported- map to name of the global element description, and it is the base for the anonymous type when specified.</span></span>
-   <span data-ttu-id="11aaf-237">nillable 已忽略-應用程式需要以 right 旗標呼叫。</span><span class="sxs-lookup"><span data-stu-id="11aaf-237">nillable Ignored-application needs to call with right flag.</span></span>
-   <span data-ttu-id="11aaf-238">如果已設定，substitutionGroup 會使用 WS XML 緩衝區回復為結構 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="11aaf-238">substitutionGroup fallback to structure with WS\_XML\_BUFFER if set.</span></span> <span data-ttu-id="11aaf-239">wsutil 不支援 substitutionGroup。</span><span class="sxs-lookup"><span data-stu-id="11aaf-239">wsutil does not support substitutionGroup.</span></span>
-   <span data-ttu-id="11aaf-240">輸入支援的類型，並將其對應至元素的類型。</span><span class="sxs-lookup"><span data-stu-id="11aaf-240">type Supported and map to the type of the element.</span></span>

<span data-ttu-id="11aaf-241"><xs： element> 為 global element：內容</span><span class="sxs-lookup"><span data-stu-id="11aaf-241"><xs:element> as global element: contents</span></span>

-   <span data-ttu-id="11aaf-242">支援 simpleType;對應至類型定義。</span><span class="sxs-lookup"><span data-stu-id="11aaf-242">simpleType Supported; maps to type definition.</span></span>
-   <span data-ttu-id="11aaf-243">支援 complexType;對應至複雜型別。</span><span class="sxs-lookup"><span data-stu-id="11aaf-243">complexType supported; maps to a complex type.</span></span>
-   <span data-ttu-id="11aaf-244">unique 會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-244">unique Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="11aaf-245">wsutil 不支援元素條件約束。</span><span class="sxs-lookup"><span data-stu-id="11aaf-245">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="11aaf-246">金鑰會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-246">key Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="11aaf-247">wsutil 不支援元素條件約束。</span><span class="sxs-lookup"><span data-stu-id="11aaf-247">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="11aaf-248">keyref 會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-248">keyref Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="11aaf-249">wsutil 不支援元素條件約束。</span><span class="sxs-lookup"><span data-stu-id="11aaf-249">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="11aaf-250"> (空白) 支援;沒有類型規格的元素會被視為 xs： anyType。</span><span class="sxs-lookup"><span data-stu-id="11aaf-250">(blank) Supported; element with no type specification is treated as xs:anyType.</span></span>

## <a name="simple-types"></a><span data-ttu-id="11aaf-251">簡單型別</span><span class="sxs-lookup"><span data-stu-id="11aaf-251">Simple Types</span></span>

<span data-ttu-id="11aaf-252"><xs： simpleType> 屬性</span><span class="sxs-lookup"><span data-stu-id="11aaf-252"><xs:simpleType> attributes</span></span>

-   <span data-ttu-id="11aaf-253">最後會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-253">Final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-254">已忽略識別碼</span><span class="sxs-lookup"><span data-stu-id="11aaf-254">Id Ignored</span></span>
-   <span data-ttu-id="11aaf-255">名稱支援，對應至類型名稱。</span><span class="sxs-lookup"><span data-stu-id="11aaf-255">Name Supported, maps to type name.</span></span>

<span data-ttu-id="11aaf-256"><xs： simpleType> 內容</span><span class="sxs-lookup"><span data-stu-id="11aaf-256"><xs:simpleType> contents</span></span>

-   <span data-ttu-id="11aaf-257">支援的限制，對應至列舉類型或範圍。</span><span class="sxs-lookup"><span data-stu-id="11aaf-257">Restriction Supported, maps to enum type or range.</span></span> <span data-ttu-id="11aaf-258">請參閱「xs： simpleType 限制」一節。</span><span class="sxs-lookup"><span data-stu-id="11aaf-258">See "xs:simpleType restrictions" section.</span></span>
-   <span data-ttu-id="11aaf-259">清單會產生有關不支援功能的警告，並回到 XML \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11aaf-259">List Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>
-   <span data-ttu-id="11aaf-260">Union 會產生有關不支援之功能的警告，並回到 XML \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11aaf-260">Union Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>

## <a name="simple-type-restriction"></a><span data-ttu-id="11aaf-261">簡單類型限制</span><span class="sxs-lookup"><span data-stu-id="11aaf-261">Simple Type restriction</span></span>

<span data-ttu-id="11aaf-262">整數類型和字串類型允許某些 facet，以允許範圍和列舉支援。</span><span class="sxs-lookup"><span data-stu-id="11aaf-262">Certain facets are allowed in integral types and strings type to allow range and enum support.</span></span>

<span data-ttu-id="11aaf-263">列舉支援</span><span class="sxs-lookup"><span data-stu-id="11aaf-263">enumeration support</span></span>

<span data-ttu-id="11aaf-264"><xs：列舉> 字串基底類型的簡單類型限制會視為列舉類型。</span><span class="sxs-lookup"><span data-stu-id="11aaf-264"><xs:enumeration> simple type restriction for base type of string is treated as enum type.</span></span> <span data-ttu-id="11aaf-265">在此情況下，基底屬性必須是字串類型。</span><span class="sxs-lookup"><span data-stu-id="11aaf-265">In this case, the Base attribute MUST be string type.</span></span> <span data-ttu-id="11aaf-266">在列舉案例中，會忽略所有其他 facet。</span><span class="sxs-lookup"><span data-stu-id="11aaf-266">In enumeration case, all other facets are ignored.</span></span>

<span data-ttu-id="11aaf-267">簡單類型支援的範圍</span><span class="sxs-lookup"><span data-stu-id="11aaf-267">range on simple type support</span></span>

<span data-ttu-id="11aaf-268">某些 facet 支援簡單類型，可有效地支援類型上允許的範圍。</span><span class="sxs-lookup"><span data-stu-id="11aaf-268">Some facets are support in simple types support effectively range allowed on the type.</span></span> <span data-ttu-id="11aaf-269">以下是整數類型和 float/double 類型的限制。</span><span class="sxs-lookup"><span data-stu-id="11aaf-269">Following are restriction for integral types and float/double types.</span></span> <span data-ttu-id="11aaf-270">具有其他 facet 的簡單類型會支援至 WS \_ 字串類型</span><span class="sxs-lookup"><span data-stu-id="11aaf-270">Simple types with other facets are fall backed to WS\_STRING type</span></span>

-   <span data-ttu-id="11aaf-271">支援的 minExclusive</span><span class="sxs-lookup"><span data-stu-id="11aaf-271">minExclusive Supported</span></span>
-   <span data-ttu-id="11aaf-272">支援 minInclusive</span><span class="sxs-lookup"><span data-stu-id="11aaf-272">minInclusive Supported</span></span>
-   <span data-ttu-id="11aaf-273">支援 maxExclusive</span><span class="sxs-lookup"><span data-stu-id="11aaf-273">maxExclusive Supported</span></span>
-   <span data-ttu-id="11aaf-274">支援 maxInclusive</span><span class="sxs-lookup"><span data-stu-id="11aaf-274">maxInclusive Supported</span></span>
-   <span data-ttu-id="11aaf-275">totalDigits 會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-275">totalDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-276">fractionDigits 會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-276">fractionDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-277">長度會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-277">length Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-278">minLength 會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-278">minLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-279">maxLength 會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-279">maxLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-280">列舉會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-280">enumeration Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-281">空白字元會產生關於不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-281">whiteSpace Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-282">模式會產生有關不支援功能的警告，而不會變更程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-282">pattern Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="11aaf-283"> (空白) 支援。</span><span class="sxs-lookup"><span data-stu-id="11aaf-283">(blank) Supported.</span></span>

<span data-ttu-id="11aaf-284">目前不支援字串上的 minLength 和 maxLength，但這是要支援的必要功能。</span><span class="sxs-lookup"><span data-stu-id="11aaf-284">minLength and maxLength on string is not supported currently but is a desirable feature to support.</span></span>

## <a name="inheritance"></a><span data-ttu-id="11aaf-285">繼承</span><span class="sxs-lookup"><span data-stu-id="11aaf-285">Inheritance</span></span>

<span data-ttu-id="11aaf-286">Wsutil 支援繼承複雜類型，也就是說，結構可以繼承自另一個結構，類似于 c + + 中的介面繼承。</span><span class="sxs-lookup"><span data-stu-id="11aaf-286">Wsutil supports inheritance of complex types, that is, a structure can inherit from another structure, similar to interface inheritance in C++.</span></span> <span data-ttu-id="11aaf-287">這是透過 <xs： complexContentExtension> 來完成。</span><span class="sxs-lookup"><span data-stu-id="11aaf-287">This is done through <xs:complexContentExtension>.</span></span> <span data-ttu-id="11aaf-288">支援 <xs： simpleContentExtension>，但會以基底類型為第一個欄位而非類型繼承的一般結構來產生。</span><span class="sxs-lookup"><span data-stu-id="11aaf-288"><xs:simpleContentExtension> is supported but is generated as plain structure with base type as first field instead of type inheritance.</span></span>

## <a name="typeprimitive-mapping"></a><span data-ttu-id="11aaf-289">型別/基本對應</span><span class="sxs-lookup"><span data-stu-id="11aaf-289">Type/primitive mapping</span></span>

<span data-ttu-id="11aaf-290">從 XML 中的 Ncname 轉譯時，必須將識別碼正規化。</span><span class="sxs-lookup"><span data-stu-id="11aaf-290">Identifiers needs to be normalized when translating from NCNames in XML.</span></span> <span data-ttu-id="11aaf-291">字串為 nillable;指標類型為 nillable;整數類資料類型和 float/double 是 nillable，而 defaultValue 則設定為0。</span><span class="sxs-lookup"><span data-stu-id="11aaf-291">Strings are nillable; pointer types are nillable; integral types and float/double are nillable and defaultValue is set to 0.</span></span>

![顯示 XSD 類型與 Sapphire 資料類型之間對應的資料表。](images/schematypemap.png)

 

 




