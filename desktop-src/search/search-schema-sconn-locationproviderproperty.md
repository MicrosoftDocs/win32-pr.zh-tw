---
description: 選擇性 <property> 元素會指定位置提供者所使用的屬性。
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: locationProvider (搜尋連接器架構) 的 property 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106975645"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a><span data-ttu-id="d772c-103">locationProvider (搜尋連接器架構) 的 property 元素</span><span class="sxs-lookup"><span data-stu-id="d772c-103">property Element of locationProvider (Search Connector Schema)</span></span>

<span data-ttu-id="d772c-104">選擇性 <property> 元素會指定位置提供者所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="d772c-104">The optional <property> element specifies the properties used by the location provider.</span></span> <span data-ttu-id="d772c-105">這些屬性是此位置提供者特有的屬性，因此沒有預先定義的名稱組可供使用。</span><span class="sxs-lookup"><span data-stu-id="d772c-105">These properties are specific to this location provider, so there is no predefined set of names to use.</span></span> <span data-ttu-id="d772c-106"><property>此元素有兩個屬性，如本主題中所述。</span><span class="sxs-lookup"><span data-stu-id="d772c-106">The <property> element has two attributes, as described in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="d772c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d772c-107">Syntax</span></span>


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><span data-ttu-id="d772c-108"><property> 元素資訊</span><span class="sxs-lookup"><span data-stu-id="d772c-108"><property> Element Information</span></span>



| <span data-ttu-id="d772c-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="d772c-109">Parent Element</span></span>                                                                                 | <span data-ttu-id="d772c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d772c-110">Child Elements</span></span>                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="d772c-111">locationProvider 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="d772c-111">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | <span data-ttu-id="d772c-112">屬性，如本主題中所述。</span><span class="sxs-lookup"><span data-stu-id="d772c-112">property, described in this topic.</span></span> |



 


## <a name="property-attributes"></a><span data-ttu-id="d772c-113"><property> 屬性</span><span class="sxs-lookup"><span data-stu-id="d772c-113"><property> Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d772c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d772c-114">Attribute</span></span></th>
<th><span data-ttu-id="d772c-115">描述</span><span class="sxs-lookup"><span data-stu-id="d772c-115">Description</span></span></th>
<th><span data-ttu-id="d772c-116">值</span><span class="sxs-lookup"><span data-stu-id="d772c-116">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d772c-117">NAME</span><span class="sxs-lookup"><span data-stu-id="d772c-117">name</span></span></td>
<td><span data-ttu-id="d772c-118">必要。</span><span class="sxs-lookup"><span data-stu-id="d772c-118">Required.</span></span> <span data-ttu-id="d772c-119">屬性的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d772c-119">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="d772c-120">類型</span><span class="sxs-lookup"><span data-stu-id="d772c-120">type</span></span></td>
<td><span data-ttu-id="d772c-121">必要。</span><span class="sxs-lookup"><span data-stu-id="d772c-121">Required.</span></span> <span data-ttu-id="d772c-122">屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="d772c-122">The type of property.</span></span></td>
<td><span data-ttu-id="d772c-123">任何：預設值。</span><span class="sxs-lookup"><span data-stu-id="d772c-123">Any: Default.</span></span> <span data-ttu-id="d772c-124">此值將不會被屬性子系統強制轉型。</span><span class="sxs-lookup"><span data-stu-id="d772c-124">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="d772c-125">GetPropertyType 會傳回 VT_Null。</span><span class="sxs-lookup"><span data-stu-id="d772c-125">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="d772c-126">Null：沒有這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d772c-126">Null: There is no value for this property.</span></span> <span data-ttu-id="d772c-127">GetPropertyType 會傳回 VT_Null。</span><span class="sxs-lookup"><span data-stu-id="d772c-127">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="d772c-128">字串：值必須是 VT_LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="d772c-128">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="d772c-129">布林值：此值必須是 VT_BOOL。</span><span class="sxs-lookup"><span data-stu-id="d772c-129">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="d772c-130">Byte：此值必須是 VT_UI1。</span><span class="sxs-lookup"><span data-stu-id="d772c-130">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="d772c-131">緩衝區：此值必須是 VT_UI1 |VT_VECTOR 位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d772c-131">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="d772c-132">Int16：此值必須是 VT_I2。</span><span class="sxs-lookup"><span data-stu-id="d772c-132">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="d772c-133">UInt16：此值必須是 VT_UI2。</span><span class="sxs-lookup"><span data-stu-id="d772c-133">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="d772c-134">Int32：此值必須是 VT_I4。</span><span class="sxs-lookup"><span data-stu-id="d772c-134">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="d772c-135">UInt32：此值必須是 VT_UI4。</span><span class="sxs-lookup"><span data-stu-id="d772c-135">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="d772c-136">Int64：此值必須是 VT_I8。</span><span class="sxs-lookup"><span data-stu-id="d772c-136">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="d772c-137">UInt64：此值必須是 VT_UI8</span><span class="sxs-lookup"><span data-stu-id="d772c-137">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="d772c-138">Double：此值必須是 VT_R8。</span><span class="sxs-lookup"><span data-stu-id="d772c-138">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="d772c-139">DateTime：此值必須是 VT_FILETIME。</span><span class="sxs-lookup"><span data-stu-id="d772c-139">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="d772c-140">Guid：此值必須是 VT_CLSID。</span><span class="sxs-lookup"><span data-stu-id="d772c-140">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="d772c-141">Blob：此值必須是 VT_BLOB。</span><span class="sxs-lookup"><span data-stu-id="d772c-141">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="d772c-142">物件：此值必須是 VT_UNKNOWN。</span><span class="sxs-lookup"><span data-stu-id="d772c-142">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="d772c-143">Stream：此值必須是 VT_STREAM。</span><span class="sxs-lookup"><span data-stu-id="d772c-143">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="d772c-144">剪貼簿：此值必須是 VT_CF。</span><span class="sxs-lookup"><span data-stu-id="d772c-144">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d772c-145">備註</span><span class="sxs-lookup"><span data-stu-id="d772c-145">Remarks</span></span>

<span data-ttu-id="d772c-146">若為 [OpenSearch 提供者]，則會使用下列屬性：</span><span class="sxs-lookup"><span data-stu-id="d772c-146">For the OpenSearch provider, the following properties are used:</span></span>

-   <span data-ttu-id="d772c-147">OpenSearchShortName：搜尋服務的簡短名稱</span><span class="sxs-lookup"><span data-stu-id="d772c-147">OpenSearchShortName: Short name of the search service</span></span>
-   <span data-ttu-id="d772c-148">OpenSearchQueryTemplate：在查詢服務中依照 OpenSearch 範本慣例格式化的範本</span><span class="sxs-lookup"><span data-stu-id="d772c-148">OpenSearchQueryTemplate: Template, formatted following the OpenSearch template convention, for the query service</span></span>
-   <span data-ttu-id="d772c-149">MaximumResultCount： (number) 搜尋服務所傳回的結果數目上限</span><span class="sxs-lookup"><span data-stu-id="d772c-149">MaximumResultCount: (number) Maximum number of results returned by the search service</span></span>
-   <span data-ttu-id="d772c-150">LinkIsFilePath： (布林值) 如果為 true，則提供者會嘗試將傳回的專案解讀為檔案，並使用其擴充功能在視圖中建立適當的 ShellItem。</span><span class="sxs-lookup"><span data-stu-id="d772c-150">LinkIsFilePath: (Boolean) If true, the provider tries to interpret returned items as files, using their extensions to create the proper ShellItem in the view.</span></span> <span data-ttu-id="d772c-151">如果為 false，則會將專案視為 URL 快捷方式。</span><span class="sxs-lookup"><span data-stu-id="d772c-151">If false, items are treated as URL shortcuts.</span></span>

 

 



