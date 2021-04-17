---
description: 選擇性 <property> 元素會指定搜尋連接器所使用的屬性。 這些是此搜尋連接器特有的屬性，因此沒有預先定義的名稱組可供使用。 這個元素沒有任何子項目。
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: propertyStore (搜尋連接器架構) 的 property 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511079"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a><span data-ttu-id="e8fb4-105">propertyStore (搜尋連接器架構) 的 property 元素</span><span class="sxs-lookup"><span data-stu-id="e8fb4-105">property Element of propertyStore (Search Connector Schema)</span></span>

<span data-ttu-id="e8fb4-106">選擇性 <property> 元素會指定搜尋連接器所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-106">The optional <property> element specifies a property used by the search connector.</span></span> <span data-ttu-id="e8fb4-107">這些是此搜尋連接器特有的屬性，因此沒有預先定義的名稱組可供使用。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-107">These properties are specific to this search connector, so there is no predefined set of names to use.</span></span> <span data-ttu-id="e8fb4-108">這個元素沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-108">This element has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fb4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8fb4-109">Syntax</span></span>


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e8fb4-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e8fb4-110">Element Information</span></span>



| <span data-ttu-id="e8fb4-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="e8fb4-111">Parent Element</span></span>                                                                           | <span data-ttu-id="e8fb4-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e8fb4-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="e8fb4-113">propertyStore 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="e8fb4-113">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a><span data-ttu-id="e8fb4-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e8fb4-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8fb4-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e8fb4-115">Attribute</span></span></th>
<th><span data-ttu-id="e8fb4-116">描述</span><span class="sxs-lookup"><span data-stu-id="e8fb4-116">Description</span></span></th>
<th><span data-ttu-id="e8fb4-117">值</span><span class="sxs-lookup"><span data-stu-id="e8fb4-117">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8fb4-118">NAME</span><span class="sxs-lookup"><span data-stu-id="e8fb4-118">name</span></span></td>
<td><span data-ttu-id="e8fb4-119">公用。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-119">Public.</span></span> <span data-ttu-id="e8fb4-120">必要。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-120">Required.</span></span> <span data-ttu-id="e8fb4-121">屬性的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-121">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8fb4-122">類型</span><span class="sxs-lookup"><span data-stu-id="e8fb4-122">type</span></span></td>
<td><span data-ttu-id="e8fb4-123">公用。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-123">Public.</span></span> <span data-ttu-id="e8fb4-124">必要。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-124">Required.</span></span> <span data-ttu-id="e8fb4-125">屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-125">The type of property.</span></span></td>
<td><span data-ttu-id="e8fb4-126">任何：預設值。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-126">Any: Default.</span></span> <span data-ttu-id="e8fb4-127">此值將不會被屬性子系統強制轉型。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-127">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="e8fb4-128">GetPropertyType 會傳回 VT_Null。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-128">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="e8fb4-129">Null：沒有這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-129">Null: There is no value for this property.</span></span> <span data-ttu-id="e8fb4-130">GetPropertyType 會傳回 VT_Null。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-130">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="e8fb4-131">字串：值必須是 VT_LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-131">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="e8fb4-132">布林值：此值必須是 VT_BOOL。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-132">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="e8fb4-133">Byte：此值必須是 VT_UI1。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-133">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="e8fb4-134">緩衝區：此值必須是 VT_UI1 |VT_VECTOR 位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-134">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="e8fb4-135">Int16：此值必須是 VT_I2。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-135">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="e8fb4-136">UInt16：此值必須是 VT_UI2。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-136">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="e8fb4-137">Int32：此值必須是 VT_I4。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-137">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="e8fb4-138">UInt32：此值必須是 VT_UI4。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-138">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="e8fb4-139">Int64：此值必須是 VT_I8。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-139">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="e8fb4-140">UInt64：此值必須是 VT_UI8</span><span class="sxs-lookup"><span data-stu-id="e8fb4-140">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="e8fb4-141">Double：此值必須是 VT_R8。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-141">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="e8fb4-142">DateTime：此值必須是 VT_FILETIME。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-142">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="e8fb4-143">Guid：此值必須是 VT_CLSID。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-143">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="e8fb4-144">Blob：此值必須是 VT_BLOB。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-144">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="e8fb4-145">物件：此值必須是 VT_UNKNOWN。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-145">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="e8fb4-146">Stream：此值必須是 VT_STREAM。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-146">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="e8fb4-147">剪貼簿：此值必須是 VT_CF。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-147">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8fb4-148">結構描述</span><span class="sxs-lookup"><span data-stu-id="e8fb4-148">schema</span></span></td>
<td><span data-ttu-id="e8fb4-149">公用。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-149">Public.</span></span> <span data-ttu-id="e8fb4-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-150">Optional.</span></span> <span data-ttu-id="e8fb4-151">定義屬性的架構。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-151">The schema where the property is defined.</span></span></td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e8fb4-152">備註</span><span class="sxs-lookup"><span data-stu-id="e8fb4-152">Remarks</span></span>

<span data-ttu-id="e8fb4-153">OpenSearch 搜尋連接器可以使用 OpenSearchHTMLRolloverTemplate 屬性。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-153">OpenSearch search connectors can use the OpenSearchHTMLRolloverTemplate property.</span></span> <span data-ttu-id="e8fb4-154">這個屬性會識別依照 OpenSearch 範本慣例格式化的範本。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-154">This property identifies a template that is formatted following the OpenSearch template convention.</span></span> <span data-ttu-id="e8fb4-155">當使用者按一下命令列中的 [在網站上搜尋] 按鈕時，會使用 OpenSearchHTMLRolloverTemplate 範本。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-155">The OpenSearchHTMLRolloverTemplate template is used when the user clicks on the "Search on website" button in the command bar.</span></span>

## <a name="example"></a><span data-ttu-id="e8fb4-156">範例</span><span class="sxs-lookup"><span data-stu-id="e8fb4-156">Example</span></span>

<span data-ttu-id="e8fb4-157">下列範例顯示 <propertyStore> 具有兩個元素的元素 <property> 。</span><span class="sxs-lookup"><span data-stu-id="e8fb4-157">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



