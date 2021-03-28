---
description: <property>元素指定程式庫所使用的屬性。 這些是程式庫特有的屬性，因此沒有預先定義的屬性名稱組可供使用。 這個元素是選擇性的，且沒有任何子項目。
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: 'property 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991106"
---
# <a name="property-element-library-schema"></a><span data-ttu-id="b9e20-105">property 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="b9e20-105">property Element (Library Schema)</span></span>

<span data-ttu-id="b9e20-106"><property>元素指定程式庫所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="b9e20-106">The <property> element specifies a property used by the library.</span></span> <span data-ttu-id="b9e20-107">這些是程式庫特有的屬性，因此沒有預先定義的屬性名稱組可供使用。</span><span class="sxs-lookup"><span data-stu-id="b9e20-107">These properties are specific to the library, so there is no predefined set of property names to use.</span></span> <span data-ttu-id="b9e20-108">這個元素是選擇性的，且沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="b9e20-108">This element is optional and has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e20-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9e20-109">Syntax</span></span>

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="b9e20-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b9e20-110">Element Information</span></span>



| <span data-ttu-id="b9e20-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="b9e20-111">Parent Element</span></span>                                                             | <span data-ttu-id="b9e20-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b9e20-112">Child Elements</span></span> |
|----------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="b9e20-113">propertyStore 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="b9e20-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) | <span data-ttu-id="b9e20-114">無</span><span class="sxs-lookup"><span data-stu-id="b9e20-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="b9e20-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b9e20-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9e20-116">屬性</span><span class="sxs-lookup"><span data-stu-id="b9e20-116">Attribute</span></span></th>
<th><span data-ttu-id="b9e20-117">描述</span><span class="sxs-lookup"><span data-stu-id="b9e20-117">Description</span></span></th>
<th><span data-ttu-id="b9e20-118">值</span><span class="sxs-lookup"><span data-stu-id="b9e20-118">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9e20-119">NAME</span><span class="sxs-lookup"><span data-stu-id="b9e20-119">name</span></span></td>
<td><span data-ttu-id="b9e20-120">公用。</span><span class="sxs-lookup"><span data-stu-id="b9e20-120">Public.</span></span> <span data-ttu-id="b9e20-121">必要。</span><span class="sxs-lookup"><span data-stu-id="b9e20-121">Required.</span></span> <span data-ttu-id="b9e20-122">屬性的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b9e20-122">The display name of the property.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b9e20-123">類型</span><span class="sxs-lookup"><span data-stu-id="b9e20-123">type</span></span></td>
<td><span data-ttu-id="b9e20-124">公用。</span><span class="sxs-lookup"><span data-stu-id="b9e20-124">Public.</span></span> <span data-ttu-id="b9e20-125">必要。</span><span class="sxs-lookup"><span data-stu-id="b9e20-125">Required.</span></span> <span data-ttu-id="b9e20-126">屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="b9e20-126">The type of property.</span></span></td>
<td><ul>
<li><span data-ttu-id="b9e20-127">任何：預設值。</span><span class="sxs-lookup"><span data-stu-id="b9e20-127">Any: Default.</span></span> <span data-ttu-id="b9e20-128">此值將不會被屬性子系統強制轉型。</span><span class="sxs-lookup"><span data-stu-id="b9e20-128">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="b9e20-129">GetPropertyType 會傳回 VT_Null。</span><span class="sxs-lookup"><span data-stu-id="b9e20-129">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="b9e20-130">Null：沒有這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="b9e20-130">Null: There is no value for this property.</span></span> <span data-ttu-id="b9e20-131">GetPropertyType 會傳回 VT_Null。</span><span class="sxs-lookup"><span data-stu-id="b9e20-131">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="b9e20-132">字串：值必須是 VT_LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="b9e20-132">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="b9e20-133">布林值：此值必須是 VT_BOOL。</span><span class="sxs-lookup"><span data-stu-id="b9e20-133">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="b9e20-134">Byte：此值必須是 VT_UI1。</span><span class="sxs-lookup"><span data-stu-id="b9e20-134">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="b9e20-135">緩衝區：此值必須是 VT_UI1 |VT_VECTOR 位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b9e20-135">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="b9e20-136">Int16：此值必須是 VT_I2。</span><span class="sxs-lookup"><span data-stu-id="b9e20-136">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="b9e20-137">UInt16：此值必須是 VT_UI2。</span><span class="sxs-lookup"><span data-stu-id="b9e20-137">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="b9e20-138">Int32：此值必須是 VT_I4。</span><span class="sxs-lookup"><span data-stu-id="b9e20-138">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="b9e20-139">UInt32：此值必須是 VT_UI4。</span><span class="sxs-lookup"><span data-stu-id="b9e20-139">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="b9e20-140">Int64：此值必須是 VT_I8。</span><span class="sxs-lookup"><span data-stu-id="b9e20-140">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="b9e20-141">UInt64：此值必須是 VT_UI8。</span><span class="sxs-lookup"><span data-stu-id="b9e20-141">UInt64: The value must be a VT_UI8.</span></span></li>
<li><span data-ttu-id="b9e20-142">Double：此值必須是 VT_R8。</span><span class="sxs-lookup"><span data-stu-id="b9e20-142">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="b9e20-143">DateTime：此值必須是 VT_FILETIME。</span><span class="sxs-lookup"><span data-stu-id="b9e20-143">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="b9e20-144">Guid：此值必須是 VT_CLSID。</span><span class="sxs-lookup"><span data-stu-id="b9e20-144">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="b9e20-145">Blob：此值必須是 VT_BLOB。</span><span class="sxs-lookup"><span data-stu-id="b9e20-145">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="b9e20-146">物件：此值必須是 VT_UNKNOWN。</span><span class="sxs-lookup"><span data-stu-id="b9e20-146">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="b9e20-147">Stream：此值必須是 VT_STREAM。</span><span class="sxs-lookup"><span data-stu-id="b9e20-147">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="b9e20-148">剪貼簿：此值必須是 VT_CF。</span><span class="sxs-lookup"><span data-stu-id="b9e20-148">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b9e20-149">備註</span><span class="sxs-lookup"><span data-stu-id="b9e20-149">Remarks</span></span>

<span data-ttu-id="b9e20-150"><標準名稱> 元素的需求符合 Windows Search 和 Windows 屬性系統的需求。</span><span class="sxs-lookup"><span data-stu-id="b9e20-150">The requirements for the <canonical-name> element match the requirements for Windows Search and the Windows property system.</span></span> <span data-ttu-id="b9e20-151">字串的型別必須是標準型別。</span><span class="sxs-lookup"><span data-stu-id="b9e20-151">The string must be of type canonical-type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9e20-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9e20-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9e20-153">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="b9e20-153">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="b9e20-154">屬性結構描述</span><span class="sxs-lookup"><span data-stu-id="b9e20-154">Property Schemas</span></span>](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="b9e20-155">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="b9e20-155">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
