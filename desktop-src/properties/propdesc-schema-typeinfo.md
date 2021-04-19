---
description: 指定屬性的類型資訊。
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987459"
---
# <a name="typeinfo"></a><span data-ttu-id="affd8-103">typeInfo</span><span class="sxs-lookup"><span data-stu-id="affd8-103">typeInfo</span></span>

<span data-ttu-id="affd8-104">指定屬性的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="affd8-104">Specifies a property's type information.</span></span> <span data-ttu-id="affd8-105">每個[propertyDescription](./propdesc-schema-propertydescription.md)只能有一個[typeInfo]()元素。</span><span class="sxs-lookup"><span data-stu-id="affd8-105">There should be only one [typeInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span> <span data-ttu-id="affd8-106">此元素已針對 Windows 7 變更。</span><span class="sxs-lookup"><span data-stu-id="affd8-106">This element has changed for Windows 7.</span></span>

<span data-ttu-id="affd8-107">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="affd8-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="affd8-108">如果未提供任何 [typeInfo]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="affd8-108">If no [typeInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="affd8-109">Windows 7 的語法</span><span class="sxs-lookup"><span data-stu-id="affd8-109">Syntax for Windows 7</span></span>


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="affd8-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="affd8-110">Element Information</span></span>



| <span data-ttu-id="affd8-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="affd8-111">Parent Element</span></span>                                                   | <span data-ttu-id="affd8-112">子元素</span><span class="sxs-lookup"><span data-stu-id="affd8-112">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="affd8-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="affd8-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="affd8-114">無</span><span class="sxs-lookup"><span data-stu-id="affd8-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="affd8-115">屬性</span><span class="sxs-lookup"><span data-stu-id="affd8-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="affd8-116">屬性</span><span class="sxs-lookup"><span data-stu-id="affd8-116">Attribute</span></span></th>
<th><span data-ttu-id="affd8-117">描述</span><span class="sxs-lookup"><span data-stu-id="affd8-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="affd8-118">type</span><span class="sxs-lookup"><span data-stu-id="affd8-118">type</span></span></td>
<td><span data-ttu-id="affd8-119">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-119">Public.</span></span> <span data-ttu-id="affd8-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-120">Optional.</span></span> <span data-ttu-id="affd8-121">預設值為 &quot; Any &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-121">Default is &quot;Any&quot;.</span></span> <span data-ttu-id="affd8-122">指出屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="affd8-122">Indicates the type of the property.</span></span> <span data-ttu-id="affd8-123">下列是有效的類型，且其相關聯的 variant 類型會由 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription：： GetPropertyType</strong></a>抓取。</span><span class="sxs-lookup"><span data-stu-id="affd8-123">The following are valid types and their associated variant types are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="affd8-124">值</span><span class="sxs-lookup"><span data-stu-id="affd8-124">Value</span></span></th>
<th><span data-ttu-id="affd8-125">意義</span><span class="sxs-lookup"><span data-stu-id="affd8-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="affd8-126">任意</span><span class="sxs-lookup"><span data-stu-id="affd8-126">Any</span></span></td>
<td><span data-ttu-id="affd8-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-127">Default.</span></span> <span data-ttu-id="affd8-128">屬性子系統不會強制執行或強制轉換屬性值。</span><span class="sxs-lookup"><span data-stu-id="affd8-128">The property subsystem will not enforce or coerce the property value.</span></span> <span data-ttu-id="affd8-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription：： GetPropertyType</strong></a> 會傳回 VT_Null。</span><span class="sxs-lookup"><span data-stu-id="affd8-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span> <span data-ttu-id="affd8-130">強烈建議 (Isv) 的獨立軟體廠商提供類型，而不是改回此預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-130">Independent software vendors (ISVs) are strongly encouraged to provide a type rather than fall back on this default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-131">Null</span><span class="sxs-lookup"><span data-stu-id="affd8-131">Null</span></span></td>
<td><span data-ttu-id="affd8-132">這個屬性沒有值。</span><span class="sxs-lookup"><span data-stu-id="affd8-132">There is no value for this property.</span></span> <span data-ttu-id="affd8-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription：： GetPropertyType</strong></a> 會傳回 VT_Null。</span><span class="sxs-lookup"><span data-stu-id="affd8-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-134">String</span><span class="sxs-lookup"><span data-stu-id="affd8-134">String</span></span></td>
<td><span data-ttu-id="affd8-135">值必須是 VT_LPWSTR，也就是以 null 參考結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="affd8-135">The value must be a VT_LPWSTR, which is a Unicode string terminated by a null reference.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="affd8-136">Boolean</span></span></td>
<td><span data-ttu-id="affd8-137">值必須是 VT_BOOL，也就是布林值。</span><span class="sxs-lookup"><span data-stu-id="affd8-137">The value must be a VT_BOOL, which is a boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-138">Byte</span><span class="sxs-lookup"><span data-stu-id="affd8-138">Byte</span></span></td>
<td><span data-ttu-id="affd8-139">值必須是 VT_UI1，也就是位元組。</span><span class="sxs-lookup"><span data-stu-id="affd8-139">The value must be a VT_UI1, which is a byte.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-140">Buffer</span><span class="sxs-lookup"><span data-stu-id="affd8-140">Buffer</span></span></td>
<td><span data-ttu-id="affd8-141">值必須是 VT_UI1 |VT_VECTOR 位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="affd8-141">The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-142">Int16</span><span class="sxs-lookup"><span data-stu-id="affd8-142">Int16</span></span></td>
<td><span data-ttu-id="affd8-143">值必須是 VT_I2，也就是16位整數。</span><span class="sxs-lookup"><span data-stu-id="affd8-143">The value must be a VT_I2, which is a 16-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-144">UInt16</span><span class="sxs-lookup"><span data-stu-id="affd8-144">UInt16</span></span></td>
<td><span data-ttu-id="affd8-145">值必須是 VT_UI2，也就是16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="affd8-145">The value must be a VT_UI2, which is a 16-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-146">Int32</span><span class="sxs-lookup"><span data-stu-id="affd8-146">Int32</span></span></td>
<td><span data-ttu-id="affd8-147">值必須是 VT_I4，也就是32位的整數。</span><span class="sxs-lookup"><span data-stu-id="affd8-147">The value must be a VT_I4, which is a 32-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-148">UInt32</span><span class="sxs-lookup"><span data-stu-id="affd8-148">UInt32</span></span></td>
<td><span data-ttu-id="affd8-149">值必須是 VT_UI4，也就是32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="affd8-149">The value must be a VT_UI4, which is a 32-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-150">Int64</span><span class="sxs-lookup"><span data-stu-id="affd8-150">Int64</span></span></td>
<td><span data-ttu-id="affd8-151">值必須是 VT_I8，也就是64位的整數。</span><span class="sxs-lookup"><span data-stu-id="affd8-151">The value must be a VT_I8, which is a 64-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-152">UInt64</span><span class="sxs-lookup"><span data-stu-id="affd8-152">UInt64</span></span></td>
<td><span data-ttu-id="affd8-153">值必須是 VT_UI8，也就是64位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="affd8-153">The value must be a VT_UI8, which is a 64-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-154">Double</span><span class="sxs-lookup"><span data-stu-id="affd8-154">Double</span></span></td>
<td><span data-ttu-id="affd8-155">值必須是 VT_R8，也就是雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="affd8-155">The value must be a VT_R8, which is a double.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-156">Datetime</span><span class="sxs-lookup"><span data-stu-id="affd8-156">DateTime</span></span></td>
<td><span data-ttu-id="affd8-157">值必須是 VT_FILETIME，也就是 <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="affd8-157">The value must be a VT_FILETIME, which is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-158">Guid</span><span class="sxs-lookup"><span data-stu-id="affd8-158">Guid</span></span></td>
<td><span data-ttu-id="affd8-159">值必須是 VT_CLSID，也就是 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="affd8-159">The value must be a VT_CLSID, which is a class identifier (CLSID).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-160">Blob</span><span class="sxs-lookup"><span data-stu-id="affd8-160">Blob</span></span></td>
<td><span data-ttu-id="affd8-161">值必須是長度為首碼位元組的 VT_BLOB。</span><span class="sxs-lookup"><span data-stu-id="affd8-161">The value must be a VT_BLOB, which are length-prefixed bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-162">串流</span><span class="sxs-lookup"><span data-stu-id="affd8-162">Stream</span></span></td>
<td><span data-ttu-id="affd8-163">值必須是 VT_STREAM，也就是執行 <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>的物件。</span><span class="sxs-lookup"><span data-stu-id="affd8-163">The value must be a VT_STREAM, which is an object that implements <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-164">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="affd8-164">Clipboard</span></span></td>
<td><span data-ttu-id="affd8-165">值必須是 VT_CF，也就是剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="affd8-165">The value must be a VT_CF, which is a clipboard format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-166">Object</span><span class="sxs-lookup"><span data-stu-id="affd8-166">Object</span></span></td>
<td><span data-ttu-id="affd8-167">值必須是 VT_UNKNOWN，也就是執行 <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>的物件。</span><span class="sxs-lookup"><span data-stu-id="affd8-167">The value must be a VT_UNKNOWN, which is an object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-168">groupingRange</span><span class="sxs-lookup"><span data-stu-id="affd8-168">groupingRange</span></span></td>
<td><span data-ttu-id="affd8-169">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-169">Optional.</span></span> <span data-ttu-id="affd8-170">預設值是 &quot; 離散的 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-170">Default is &quot;Discrete&quot;.</span></span> <span data-ttu-id="affd8-171">指定當視圖依此屬性分組時，顯示內容的方式。</span><span class="sxs-lookup"><span data-stu-id="affd8-171">Specifies how the property is displayed when a view is grouped by this property.</span></span> <span data-ttu-id="affd8-172">在這裡設定之後，這些值就會由 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription：： GetGroupingRange</strong></a>取出。</span><span class="sxs-lookup"><span data-stu-id="affd8-172">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>.</span></span> <span data-ttu-id="affd8-173">以下是有效的類型。</span><span class="sxs-lookup"><span data-stu-id="affd8-173">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="affd8-174">值</span><span class="sxs-lookup"><span data-stu-id="affd8-174">Value</span></span></th>
<th><span data-ttu-id="affd8-175">意義</span><span class="sxs-lookup"><span data-stu-id="affd8-175">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="affd8-176">Discrete</span><span class="sxs-lookup"><span data-stu-id="affd8-176">Discrete</span></span></td>
<td><span data-ttu-id="affd8-177">預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-177">Default.</span></span> <span data-ttu-id="affd8-178">顯示個別的值。</span><span class="sxs-lookup"><span data-stu-id="affd8-178">Displays individual values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-179">英數字元</span><span class="sxs-lookup"><span data-stu-id="affd8-179">Alphanumeric</span></span></td>
<td><span data-ttu-id="affd8-180">顯示值的靜態英數位元範圍。</span><span class="sxs-lookup"><span data-stu-id="affd8-180">Displays static alphanumeric ranges for values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-181">大小</span><span class="sxs-lookup"><span data-stu-id="affd8-181">Size</span></span></td>
<td><span data-ttu-id="affd8-182">顯示值的靜態大小範圍。</span><span class="sxs-lookup"><span data-stu-id="affd8-182">Displays static size ranges for values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-183">Date</span><span class="sxs-lookup"><span data-stu-id="affd8-183">Date</span></span></td>
<td><span data-ttu-id="affd8-184">顯示月份/年度群組。</span><span class="sxs-lookup"><span data-stu-id="affd8-184">Displays month/year groups.</span></span> <span data-ttu-id="affd8-185">Type = DateTime 之屬性的預設值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-185">Default for properties of type=&quot;DateTime&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-186">TimeRelative</span><span class="sxs-lookup"><span data-stu-id="affd8-186">TimeRelative</span></span></td>
<td><span data-ttu-id="affd8-187">以時間相對的群組顯示。</span><span class="sxs-lookup"><span data-stu-id="affd8-187">Displays in time-relative groups.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-188">動態</span><span class="sxs-lookup"><span data-stu-id="affd8-188">Dynamic</span></span></td>
<td><span data-ttu-id="affd8-189">顯示動態建立的值範圍。</span><span class="sxs-lookup"><span data-stu-id="affd8-189">Displays dynamically created ranges for the values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-190">百分比</span><span class="sxs-lookup"><span data-stu-id="affd8-190">Percent</span></span></td>
<td><span data-ttu-id="affd8-191">顯示百分比值區。</span><span class="sxs-lookup"><span data-stu-id="affd8-191">Displays percent buckets.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-192">isInnate</span><span class="sxs-lookup"><span data-stu-id="affd8-192">isInnate</span></span></td>
<td><span data-ttu-id="affd8-193">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-193">Public.</span></span> <span data-ttu-id="affd8-194">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-194">Optional.</span></span> <span data-ttu-id="affd8-195">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="affd8-195">Default is &quot;false&quot;.</span></span> <span data-ttu-id="affd8-196">指定屬性是否視為固有。</span><span class="sxs-lookup"><span data-stu-id="affd8-196">Specifies whether the property is considered innate.</span></span> <span data-ttu-id="affd8-197">固有屬性是從檔案內容或從其他資源或系統進行計算的屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-197">An innate property is one which is either calculated from the content of a file, or from other resources or systems.</span></span> <span data-ttu-id="affd8-198">例如，System.object 是檔案系統提供的固有屬性;變更和本身的屬性值不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="affd8-198">For example, System.Size is an innate property provided by the file system; changing the value of the property in and of itself does nothing.</span></span> <span data-ttu-id="affd8-199">其他範例為 system.string 和 System.Doc>ument。PageCount，根據檔案內容的程式來計算，而不是根據使用者變更的設定。</span><span class="sxs-lookup"><span data-stu-id="affd8-199">Other examples are System.Image.Dimensions and System.Document.PageCount, which are calculated by programs based upon the content of the file, not based upon a user-changeable setting.</span></span> <span data-ttu-id="affd8-200">設定 isInnate = &quot; true &quot; 表示使用者無法直接透過屬性控制項來編輯此屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-200">Setting isInnate=&quot;true&quot; means the user cannot edit this property directly via a property control.</span></span> <span data-ttu-id="affd8-201">此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_ISINNATE 旗標。</span><span class="sxs-lookup"><span data-stu-id="affd8-201">This value maps to the PDTF_ISINNATE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-202">canBePurged</span><span class="sxs-lookup"><span data-stu-id="affd8-202">canBePurged</span></span></td>
<td><span data-ttu-id="affd8-203"><strong>Windows Vista Service Pack 1 (SP1) 和更新版本</strong>。</span><span class="sxs-lookup"><span data-stu-id="affd8-203"><strong>Windows Vista with Service Pack 1 (SP1) and later only</strong>.</span></span> <span data-ttu-id="affd8-204">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-204">Public.</span></span> <span data-ttu-id="affd8-205">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-205">Optional.</span></span> <span data-ttu-id="affd8-206">當設為 &quot; true 時 &quot; ，允許刪除固有屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-206">When set to &quot;true&quot;, allows an innate property to be deleted.</span></span> <span data-ttu-id="affd8-207">固有屬性（從其他屬性計算而來）是以唯讀方式定義的。</span><span class="sxs-lookup"><span data-stu-id="affd8-207">Innate properties, which are calculated from other properties, are read-only by definition.</span></span> <span data-ttu-id="affd8-208">這個屬性的預設值取決於 <em>isInnate</em> 值。</span><span class="sxs-lookup"><span data-stu-id="affd8-208">The default value for this attribute depends on the <em>isInnate</em> value.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="affd8-209">isInnate</span><span class="sxs-lookup"><span data-stu-id="affd8-209">isInnate</span></span></th>
<th><span data-ttu-id="affd8-210">canBePurged 預設值</span><span class="sxs-lookup"><span data-stu-id="affd8-210">canBePurged Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="affd8-211">true</span><span class="sxs-lookup"><span data-stu-id="affd8-211">true</span></span></td>
<td><span data-ttu-id="affd8-212">false</span><span class="sxs-lookup"><span data-stu-id="affd8-212">false</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-213">false</span><span class="sxs-lookup"><span data-stu-id="affd8-213">false</span></span></td>
<td><span data-ttu-id="affd8-214">true</span><span class="sxs-lookup"><span data-stu-id="affd8-214">true</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="affd8-215">屬性，其 <em>isInnate</em> 值為 &quot; false &quot; (表示屬性是讀取/寫入) 也無法將 <em>canBePurged</em> 值設定為 &quot; false &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-215">A property whose <em>isInnate</em> value is &quot;false&quot; (meaning that the property is read/write) cannot also set the <em>canBePurged</em> value to &quot;false&quot;.</span></span> <span data-ttu-id="affd8-216">這項限制是由作業系統強制執行。</span><span class="sxs-lookup"><span data-stu-id="affd8-216">This restriction is enforced by the operating system.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="affd8-217">雖然這個屬性是在 Windows Vista Service Pack 1 (SP1) 引進的，但包含這個屬性的 propdesc 檔案與 Windows Vista SP1 之前的 Windows Vista 相容。</span><span class="sxs-lookup"><span data-stu-id="affd8-217">Although this attribute was introduced in Windows Vista with Service Pack 1 (SP1), a .propdesc file that includes this attribute is compatible with Windows Vista prior to Windows Vista with SP1.</span></span> <span data-ttu-id="affd8-218">在這種情況下，只會忽略 <em>canBePurged</em> 屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-218">The <em>canBePurged</em> attribute is simply ignored in that situation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-219">multipleValues</span><span class="sxs-lookup"><span data-stu-id="affd8-219">multipleValues</span></span></td>
<td><span data-ttu-id="affd8-220">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-220">Public.</span></span> <span data-ttu-id="affd8-221">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-221">Optional.</span></span> <span data-ttu-id="affd8-222">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="affd8-222">Default is &quot;false&quot;.</span></span> <span data-ttu-id="affd8-223">指定這個屬性是否可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="affd8-223">Specifies whether this property can have multiple values.</span></span> <span data-ttu-id="affd8-224">此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_MULTIPLEVALUES 旗標。</span><span class="sxs-lookup"><span data-stu-id="affd8-224">This value maps to the PDTF_MULTIPLEVALUES flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span> <span data-ttu-id="affd8-225">這也會影響 VT_VECTOR 是否為屬性值的 VARTYPE 或。</span><span class="sxs-lookup"><span data-stu-id="affd8-225">This also influences whether VT_VECTOR is OR'd to the VARTYPE of the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-226">isGroup</span><span class="sxs-lookup"><span data-stu-id="affd8-226">isGroup</span></span></td>
<td><span data-ttu-id="affd8-227">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-227">Public.</span></span> <span data-ttu-id="affd8-228">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-228">Optional.</span></span> <span data-ttu-id="affd8-229">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="affd8-229">Default is &quot;false&quot;.</span></span> <span data-ttu-id="affd8-230">指定屬性是否為群組標題。</span><span class="sxs-lookup"><span data-stu-id="affd8-230">Specifies whether the property is a group heading.</span></span> <span data-ttu-id="affd8-231">群組標題會嚴格用於 proplists 中，沒有任何值，絕對不會儲存在檔案中，也應該具有 <typeInfo type=&quot;Null&quot;> 。</span><span class="sxs-lookup"><span data-stu-id="affd8-231">A group heading is strictly used in proplists, has no value, is never stored in a file, and should also have <typeInfo type=&quot;Null&quot;>.</span></span> <span data-ttu-id="affd8-232">系統中的某些 UI 會使用 proplists 來指出要顯示的屬性順序。</span><span class="sxs-lookup"><span data-stu-id="affd8-232">Some UI in the system use proplists to indicate the sequence of the properties to display.</span></span> <span data-ttu-id="affd8-233">這些 proplists 可能包含群組標題的參考 (例如 PropGroup) ，它會告訴 UI 啟動新的群組區段 (例如 &quot; 相機設定 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="affd8-233">These proplists may include references to group headings (eg, System.PropGroup.Camera), which tell the UI to start a new group section (eg, &quot;Camera Settings&quot;).</span></span> <span data-ttu-id="affd8-234">具有 isGroup = true 的屬性 &quot; 描述 &quot; 應該指定 <labelInfo label=&quot;Some localized label&quot;> ，否則它不是有用的屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-234">A property description with isGroup=&quot;true&quot; should specify a <labelInfo label=&quot;Some localized label&quot;>, otherwise it isn't a useful property.</span></span> <span data-ttu-id="affd8-235">此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_ISGROUP 旗標。</span><span class="sxs-lookup"><span data-stu-id="affd8-235">This value maps to the PDTF_ISGROUP flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-236">aggregationType</span><span class="sxs-lookup"><span data-stu-id="affd8-236">aggregationType</span></span></td>
<td><span data-ttu-id="affd8-237">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-237">Public.</span></span> <span data-ttu-id="affd8-238">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-238">Optional.</span></span> <span data-ttu-id="affd8-239">預設值為預設值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-239">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="affd8-240">指定當選取多個專案時，如何顯示匯總屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-240">Specifies how aggregate properties are displayed when multiple items are selected.</span></span> <span data-ttu-id="affd8-241">在這裡設定之後， <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription：： GetAggregationType</strong></a> 會以 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>的形式取出這些值。</span><span class="sxs-lookup"><span data-stu-id="affd8-241">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> as an <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span></span> <span data-ttu-id="affd8-242">以下是有效的類型。</span><span class="sxs-lookup"><span data-stu-id="affd8-242">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="affd8-243">值</span><span class="sxs-lookup"><span data-stu-id="affd8-243">Value</span></span></th>
<th><span data-ttu-id="affd8-244">意義</span><span class="sxs-lookup"><span data-stu-id="affd8-244">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="affd8-245">預設</span><span class="sxs-lookup"><span data-stu-id="affd8-245">Default</span></span></td>
<td><span data-ttu-id="affd8-246">預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-246">Default.</span></span> <span data-ttu-id="affd8-247">在 UI 中顯示 <strong>多個值</strong> 預留位置。</span><span class="sxs-lookup"><span data-stu-id="affd8-247">Displays a <strong>Multiple Values</strong> placeholder in the UI.</span></span> <span data-ttu-id="affd8-248">如果 <em>類型</em> 與指定的 <em>aggregationType</em>不相容，這就是預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-248">This is the default if the <em>type</em> is incompatible with the specified <em>aggregationType</em>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-249">First</span><span class="sxs-lookup"><span data-stu-id="affd8-249">First</span></span></td>
<td><span data-ttu-id="affd8-250">顯示選取專案或集合中第一個專案的屬性值。</span><span class="sxs-lookup"><span data-stu-id="affd8-250">Displays the property value of the first item in the selection or collection.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-251">Sum</span><span class="sxs-lookup"><span data-stu-id="affd8-251">Sum</span></span></td>
<td><span data-ttu-id="affd8-252">顯示數值的總和。</span><span class="sxs-lookup"><span data-stu-id="affd8-252">Displays the sum of the numerical values.</span></span> <span data-ttu-id="affd8-253">適用于如 system.string 或 System. 大小等屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-253">Useful for properties such as System.Media.Duration or System.Size.</span></span> <span data-ttu-id="affd8-254">此值與非數數值型別不相容。</span><span class="sxs-lookup"><span data-stu-id="affd8-254">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-255">平均</span><span class="sxs-lookup"><span data-stu-id="affd8-255">Average</span></span></td>
<td><span data-ttu-id="affd8-256">顯示數值的平均值。</span><span class="sxs-lookup"><span data-stu-id="affd8-256">Displays the average of the numerical values.</span></span> <span data-ttu-id="affd8-257">適用于如 System. 評等的屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-257">Useful for properties such as System.Rating.</span></span> <span data-ttu-id="affd8-258">此值與非數數值型別不相容。</span><span class="sxs-lookup"><span data-stu-id="affd8-258">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-259">DateRange</span><span class="sxs-lookup"><span data-stu-id="affd8-259">DateRange</span></span></td>
<td><span data-ttu-id="affd8-260">顯示日期的範圍。</span><span class="sxs-lookup"><span data-stu-id="affd8-260">Displays a range of dates.</span></span> <span data-ttu-id="affd8-261">適用于 DateTaken 等屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-261">Useful for properties like System.Photo.DateTaken.</span></span> <span data-ttu-id="affd8-262">這個值與 type = DateTime 以外的任何值都不相容 &quot; &quot; ，而且是該類型屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-262">This value is not compatible with anything except type=&quot;DateTime&quot; and is the default for properties of that type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-263">Union</span><span class="sxs-lookup"><span data-stu-id="affd8-263">Union</span></span></td>
<td><span data-ttu-id="affd8-264">顯示選取範圍或集合中所有值的聯集。</span><span class="sxs-lookup"><span data-stu-id="affd8-264">Displays a union of all the values in the selection or collection.</span></span> <span data-ttu-id="affd8-265">值的顯示順序未定義。</span><span class="sxs-lookup"><span data-stu-id="affd8-265">The order in which the values are shown is undefined.</span></span> <span data-ttu-id="affd8-266">此值是 type = &quot; String &quot; 和 multipleValues = true 的屬性預設值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-266">This value is the default for properties of type=&quot;String&quot; and multipleValues=&quot;true&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-267">最大值</span><span class="sxs-lookup"><span data-stu-id="affd8-267">Maximum</span></span></td>
<td><span data-ttu-id="affd8-268">顯示集合中的最大值。</span><span class="sxs-lookup"><span data-stu-id="affd8-268">Displays the maximum value in the collection.</span></span> <span data-ttu-id="affd8-269">適用于 DateModified 之類的屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-269">Useful for properties like System.DateModified.</span></span> <span data-ttu-id="affd8-270">與非數值或非日期類型不相容。</span><span class="sxs-lookup"><span data-stu-id="affd8-270">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-271">最小值</span><span class="sxs-lookup"><span data-stu-id="affd8-271">Minimum</span></span></td>
<td><span data-ttu-id="affd8-272">顯示集合中的最小值。</span><span class="sxs-lookup"><span data-stu-id="affd8-272">Displays the minimum value in the collection.</span></span> <span data-ttu-id="affd8-273">與非數值或非日期類型不相容。</span><span class="sxs-lookup"><span data-stu-id="affd8-273">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-274">isTreeProperty</span><span class="sxs-lookup"><span data-stu-id="affd8-274">isTreeProperty</span></span></td>
<td><span data-ttu-id="affd8-275">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-275">Public.</span></span> <span data-ttu-id="affd8-276">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-276">Optional.</span></span> <span data-ttu-id="affd8-277">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="affd8-277">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-278">isViewable</span><span class="sxs-lookup"><span data-stu-id="affd8-278">isViewable</span></span></td>
<td><span data-ttu-id="affd8-279">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-279">Public.</span></span> <span data-ttu-id="affd8-280">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-280">Optional.</span></span> <span data-ttu-id="affd8-281">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="affd8-281">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="affd8-282">指定是否要向使用者查看此屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-282">Specifies whether this property is intended to be viewable to the user.</span></span> <span data-ttu-id="affd8-283">例如，資料行選擇器 UI 只會顯示具有 isViewable = true 的 &quot; 屬性 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-283">For example, the Column Chooser UI only shows the properties that have isViewable=&quot;true&quot;.</span></span> <span data-ttu-id="affd8-284">例外狀況是由 proplist 驅動的 UI，一律會顯示內容。</span><span class="sxs-lookup"><span data-stu-id="affd8-284">The exception is UI that is driven by a proplist, which will always show the property.</span></span> <span data-ttu-id="affd8-285">如果您的屬性只是要在兩個物件之間快速流覽資料，而不想讓使用者看到，則這個屬性應該是 false。</span><span class="sxs-lookup"><span data-stu-id="affd8-285">If you have a property that is only meant to shuttle data between two objects, and never intended to be viewed by the user, this attribute should be false.</span></span> <span data-ttu-id="affd8-286">此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_ISVIEWABLE 旗標。</span><span class="sxs-lookup"><span data-stu-id="affd8-286">This value maps to the PDTF_ISVIEWABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-287">isQueryable</span><span class="sxs-lookup"><span data-stu-id="affd8-287">isQueryable</span></span></td>
<td><span data-ttu-id="affd8-288">僅限 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="affd8-288">Windows Vista only.</span></span> <span data-ttu-id="affd8-289">在 Windows 7 和更新版本中不支援。</span><span class="sxs-lookup"><span data-stu-id="affd8-289">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="affd8-290">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-290">Public.</span></span> <span data-ttu-id="affd8-291">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-291">Optional.</span></span> <span data-ttu-id="affd8-292">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="affd8-292">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="affd8-293">指定是否要在搜尋查詢產生器 UI 中提供這個屬性。</span><span class="sxs-lookup"><span data-stu-id="affd8-293">Specifies whether this property is intended to be available in the Search Query Builder UI.</span></span> <span data-ttu-id="affd8-294">在 &quot; &quot; 遵守 isQueryable = true 之前，屬性必須有 isViewable = true &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-294">A property must have isViewable=&quot;true&quot; before isQueryable=&quot;true&quot; is respected.</span></span> <span data-ttu-id="affd8-295">此值會對應到 <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> 中所定義並在 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription：： GetTypeFlags</strong></a>中使用的 PDTF_ISQUERYABLE 旗標。</span><span class="sxs-lookup"><span data-stu-id="affd8-295">This value maps to the PDTF_ISQUERYABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-296">searchRawValue</span><span class="sxs-lookup"><span data-stu-id="affd8-296">searchRawValue</span></span></td>
<td><span data-ttu-id="affd8-297"><strong>Windows 7 和更新版本。</strong></span><span class="sxs-lookup"><span data-stu-id="affd8-297"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="affd8-298">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-298">Public.</span></span> <span data-ttu-id="affd8-299">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-299">Optional.</span></span> <span data-ttu-id="affd8-300">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="affd8-300">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-301">includeInFullTextQuery</span><span class="sxs-lookup"><span data-stu-id="affd8-301">includeInFullTextQuery</span></span></td>
<td><span data-ttu-id="affd8-302">僅限 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="affd8-302">Windows Vista only.</span></span> <span data-ttu-id="affd8-303">在 Windows 7 和更新版本中不支援。</span><span class="sxs-lookup"><span data-stu-id="affd8-303">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="affd8-304">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-304">Public.</span></span> <span data-ttu-id="affd8-305">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-305">Optional.</span></span> <span data-ttu-id="affd8-306">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="affd8-306">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-307">conditionType</span><span class="sxs-lookup"><span data-stu-id="affd8-307">conditionType</span></span></td>
<td><span data-ttu-id="affd8-308">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-308">Public.</span></span> <span data-ttu-id="affd8-309">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-309">Optional.</span></span> <span data-ttu-id="affd8-310">預設值是 &quot; String &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-310">Default is &quot;String&quot;.</span></span> <span data-ttu-id="affd8-311">指定搜尋查詢產生器 UI 的提示，讓它可以判斷述詞內可能條件運算子的清單。</span><span class="sxs-lookup"><span data-stu-id="affd8-311">Specifies a hint to the Search Query Builder UI so that it can determine the list of possible condition operators inside a predicate.</span></span> <span data-ttu-id="affd8-312">以下是可辨識的值。</span><span class="sxs-lookup"><span data-stu-id="affd8-312">The following are recognized values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="affd8-313">值</span><span class="sxs-lookup"><span data-stu-id="affd8-313">Value</span></span></th>
<th><span data-ttu-id="affd8-314">意義</span><span class="sxs-lookup"><span data-stu-id="affd8-314">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="affd8-315">String</span><span class="sxs-lookup"><span data-stu-id="affd8-315">String</span></span></td>
<td><span data-ttu-id="affd8-316">預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-316">Default.</span></span> <span data-ttu-id="affd8-317">將會使用下列運算子：是，不是，，，，， &quot; &quot; &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; &quot; 開頭為 &quot; ， &quot; 結尾為 &quot; ， &quot; 包含 &quot; ， &quot; 不包含 &quot; ， &quot; 則類似 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-317">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;&lt;&quot;, &quot;&gt;&quot;, &quot;<=&quot;, &quot;>=&quot;, &quot;starts with&quot;, &quot;ends with&quot;, &quot;contains&quot;, &quot;doesn't contain&quot;, &quot;is like&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-318">Number</span><span class="sxs-lookup"><span data-stu-id="affd8-318">Number</span></span></td>
<td><span data-ttu-id="affd8-319">數值屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-319">Default for numeric properties.</span></span> <span data-ttu-id="affd8-320">將會使用下列運算子： &quot; equals &quot; 、 &quot; 不等於、小於、大於 &quot; &quot; &quot; &quot; &quot; 、 &quot; 小於或等於 &quot; 、 &quot; 大於或等於 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-320">The following operators will be used: &quot;equals&quot;, &quot;doesn't equal&quot;, &quot;is less than&quot;, &quot;is greater than&quot;, &quot;is less than or equal to&quot;, &quot;is greater than or equal to&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-321">Datetime</span><span class="sxs-lookup"><span data-stu-id="affd8-321">DateTime</span></span></td>
<td><span data-ttu-id="affd8-322">Type = DateTime 之屬性的預設值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-322">Default for properties of type=&quot;DateTime&quot;.</span></span> <span data-ttu-id="affd8-323">將會使用下列運算子： &quot; 是，不是 &quot; &quot; &quot; ， &quot; 之前是 &quot; &quot; &quot; &quot; &quot; &quot; &quot; ，在之後，但在中，但包含。</span><span class="sxs-lookup"><span data-stu-id="affd8-323">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;is before&quot;, &quot;is after&quot;, &quot;is before but includes&quot;, &quot;is after but includes&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-324">Boolean</span><span class="sxs-lookup"><span data-stu-id="affd8-324">Boolean</span></span></td>
<td><span data-ttu-id="affd8-325">Type = Boolean 的屬性預設 &quot; 值 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-325">Default for properties of type=&quot;Boolean&quot;.</span></span> <span data-ttu-id="affd8-326">與數位相同。</span><span class="sxs-lookup"><span data-stu-id="affd8-326">Same as Number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-327">大小</span><span class="sxs-lookup"><span data-stu-id="affd8-327">Size</span></span></td>
<td><span data-ttu-id="affd8-328">與數位相同。</span><span class="sxs-lookup"><span data-stu-id="affd8-328">Same as Number.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-329">defaultOperation</span><span class="sxs-lookup"><span data-stu-id="affd8-329">defaultOperation</span></span></td>
<td><span data-ttu-id="affd8-330">公用。</span><span class="sxs-lookup"><span data-stu-id="affd8-330">Public.</span></span> <span data-ttu-id="affd8-331">選擇性。</span><span class="sxs-lookup"><span data-stu-id="affd8-331">Optional.</span></span> <span data-ttu-id="affd8-332">預設值為 [ &quot; 等於] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-332">Default is &quot;Equal&quot;.</span></span> <span data-ttu-id="affd8-333">指定搜尋查詢產生器工具的提示，讓它可以判斷預設運算子。</span><span class="sxs-lookup"><span data-stu-id="affd8-333">Specifies a hint to the Search Query Builder tool so that it can determine the default operator.</span></span> <span data-ttu-id="affd8-334">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="affd8-334">The possible values are as follows:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="affd8-335">值</span><span class="sxs-lookup"><span data-stu-id="affd8-335">Value</span></span></th>
<th><span data-ttu-id="affd8-336">意義</span><span class="sxs-lookup"><span data-stu-id="affd8-336">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="affd8-337">等於</span><span class="sxs-lookup"><span data-stu-id="affd8-337">Equal</span></span></td>
<td><span data-ttu-id="affd8-338">預設值。</span><span class="sxs-lookup"><span data-stu-id="affd8-338">Default.</span></span> <span data-ttu-id="affd8-339">表示對等專案。</span><span class="sxs-lookup"><span data-stu-id="affd8-339">Indicates equivalent.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-340">NotEqual</span><span class="sxs-lookup"><span data-stu-id="affd8-340">NotEqual</span></span></td>
<td><span data-ttu-id="affd8-341">表示不相等。</span><span class="sxs-lookup"><span data-stu-id="affd8-341">Indicates not equivalent.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-342">LessThan</span><span class="sxs-lookup"><span data-stu-id="affd8-342">LessThan</span></span></td>
<td><span data-ttu-id="affd8-343">表示小於。</span><span class="sxs-lookup"><span data-stu-id="affd8-343">Indicates less than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="affd8-344">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="affd8-344">GreaterThan</span></span></td>
<td><span data-ttu-id="affd8-345">ConditionType = Size 的屬性預設 &quot; 值 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-345">Default for properties of conditionType=&quot;Size&quot;.</span></span> <span data-ttu-id="affd8-346">表示大於。</span><span class="sxs-lookup"><span data-stu-id="affd8-346">Indicates greater than.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="affd8-347">包含</span><span class="sxs-lookup"><span data-stu-id="affd8-347">Contains</span></span></td>
<td><span data-ttu-id="affd8-348">ConditionType = String 的屬性預設 &quot; 值 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="affd8-348">Default for properties of conditionType=&quot;String&quot;.</span></span> <span data-ttu-id="affd8-349">表示包含。</span><span class="sxs-lookup"><span data-stu-id="affd8-349">Indicates inclusion.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
