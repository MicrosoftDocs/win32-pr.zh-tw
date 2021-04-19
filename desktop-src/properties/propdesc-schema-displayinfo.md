---
description: 指定屬性的顯示資訊。
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff0bb441b4535c0b6c6f3183671fbe8ade09183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983656"
---
# <a name="displayinfo"></a><span data-ttu-id="06061-103">displayInfo</span><span class="sxs-lookup"><span data-stu-id="06061-103">displayInfo</span></span>

<span data-ttu-id="06061-104">指定屬性的顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="06061-104">Specifies a property's display information.</span></span> <span data-ttu-id="06061-105">每個[propertyDescription](./propdesc-schema-propertydescription.md)只能有一個[displayInfo]()元素。</span><span class="sxs-lookup"><span data-stu-id="06061-105">There should be only one [displayInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span>

<span data-ttu-id="06061-106">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="06061-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="06061-107">如果未提供任何 [displayInfo]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="06061-107">If no [displayInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="06061-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06061-108">Syntax</span></span>


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="FileName"/>
                                <xs:enumeration value="FilePath"/>
                                <xs:enumeration value="Hyperlink"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="YesNo"/>
                                <xs:enumeration value="OnOff"/>
                                <xs:enumeration value="TrueFalse"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="Percentage"/>
                                <xs:enumeration value="ByteSize"/>
                                <xs:enumeration value="KBSize"/>
                                <xs:enumeration value="SampleSize"/>
                                <xs:enumeration value="Bitrate"/>
                                <xs:enumeration value="SampleRate"/>
                                <xs:enumeration value="FrameRate"/>
                                <xs:enumeration value="Pixels"/>
                                <xs:enumeration value="DPI"/>
                                <xs:enumeration value="Duration"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatDurationAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="Month"/>
                                <xs:enumeration value="YearMonth"/>
                                <xs:enumeration value="Year"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatTimeAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="ShortTime"/>
                                <xs:enumeration value="LongTime"/>
                                <xs:enumeration value="HideTime"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatDateAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="ShortDate"/>
                                <xs:enumeration value="LongDate"/>
                                <xs:enumeration value="HideDate"/>
                                <xs:enumeration value="RelativeShortDate"/>
                                <xs:enumeration value="RelativeLongDate"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="value" type="xs:string" use="required"/>
                                <xs:attribute name="text" type="xs:string" use="required"/>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="PercentBar"/>
                                <xs:enumeration value="ProgressBar"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="StaticText"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Boolean"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="NumericText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="06061-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="06061-109">Element Information</span></span>



| <span data-ttu-id="06061-110">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="06061-110">Parent Element</span></span>                                                   | <span data-ttu-id="06061-111">子元素</span><span class="sxs-lookup"><span data-stu-id="06061-111">Child Elements</span></span>                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06061-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="06061-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="06061-113">stringFormat</span><span class="sxs-lookup"><span data-stu-id="06061-113">stringFormat</span></span>](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [<span data-ttu-id="06061-114">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="06061-114">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [<span data-ttu-id="06061-115">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="06061-115">numberFormat</span></span>](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [<span data-ttu-id="06061-116">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="06061-116">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [<span data-ttu-id="06061-117">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="06061-117">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [<span data-ttu-id="06061-118">drawControl</span><span class="sxs-lookup"><span data-stu-id="06061-118">drawControl</span></span>](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="06061-119">editControl</span><span class="sxs-lookup"><span data-stu-id="06061-119">editControl</span></span>](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="06061-120">filterControl</span><span class="sxs-lookup"><span data-stu-id="06061-120">filterControl</span></span>](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | <span data-ttu-id="06061-121">[queryControl](./propdesc-schema-querycontrol.md) (的 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="06061-121">[queryControl](./propdesc-schema-querycontrol.md) (Windows Vista only.</span></span> <span data-ttu-id="06061-122">在 Windows 7 及更新版本中不支援。 ) </span><span class="sxs-lookup"><span data-stu-id="06061-122">Not supported in Windows 7 and later.)</span></span> |



 

## <a name="attributes"></a><span data-ttu-id="06061-123">屬性</span><span class="sxs-lookup"><span data-stu-id="06061-123">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06061-124">屬性</span><span class="sxs-lookup"><span data-stu-id="06061-124">Attribute</span></span></th>
<th><span data-ttu-id="06061-125">描述</span><span class="sxs-lookup"><span data-stu-id="06061-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06061-126">defaultColumnWidth</span><span class="sxs-lookup"><span data-stu-id="06061-126">defaultColumnWidth</span></span></td>
<td><span data-ttu-id="06061-127">公用。</span><span class="sxs-lookup"><span data-stu-id="06061-127">Public.</span></span> <span data-ttu-id="06061-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="06061-128">Optional.</span></span> <span data-ttu-id="06061-129">預設值為 &quot; 20 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="06061-129">Default is &quot;20&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-130">displayType</span><span class="sxs-lookup"><span data-stu-id="06061-130">displayType</span></span></td>
<td><span data-ttu-id="06061-131">公用。</span><span class="sxs-lookup"><span data-stu-id="06061-131">Public.</span></span> <span data-ttu-id="06061-132">選擇性。</span><span class="sxs-lookup"><span data-stu-id="06061-132">Optional.</span></span> <span data-ttu-id="06061-133">預設值是 &quot; String &quot; 。</span><span class="sxs-lookup"><span data-stu-id="06061-133">Default is &quot;String&quot;.</span></span> <span data-ttu-id="06061-134">指定顯示字串的類型。</span><span class="sxs-lookup"><span data-stu-id="06061-134">Specifies the type of the display string.</span></span> <span data-ttu-id="06061-135">在這裡設定之後， <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription：： GetDisplayType</strong></a>會取出相關聯的<strong>PROPDESC_DISPLAYTYPE</strong>值。</span><span class="sxs-lookup"><span data-stu-id="06061-135">Once set here, the associated <strong>PROPDESC_DISPLAYTYPE</strong> values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>.</span></span> <span data-ttu-id="06061-136">以下是有效的類型。</span><span class="sxs-lookup"><span data-stu-id="06061-136">The following are valid types.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="06061-137">值</span><span class="sxs-lookup"><span data-stu-id="06061-137">Value</span></span></th>
<th><span data-ttu-id="06061-138">意義</span><span class="sxs-lookup"><span data-stu-id="06061-138">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06061-139">String</span><span class="sxs-lookup"><span data-stu-id="06061-139">String</span></span></td>
<td><span data-ttu-id="06061-140">預設值。</span><span class="sxs-lookup"><span data-stu-id="06061-140">Default.</span></span> <span data-ttu-id="06061-141">值會顯示為字串。</span><span class="sxs-lookup"><span data-stu-id="06061-141">Value is displayed as a string.</span></span> <span data-ttu-id="06061-142">使用 &quot; stringFormat &quot; 來格式化。</span><span class="sxs-lookup"><span data-stu-id="06061-142">Use &quot;stringFormat&quot; to format.</span></span> <span data-ttu-id="06061-143">方法會傳回 PDDT_STRING。</span><span class="sxs-lookup"><span data-stu-id="06061-143">Method returns PDDT_STRING.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-144">Number</span><span class="sxs-lookup"><span data-stu-id="06061-144">Number</span></span></td>
<td><span data-ttu-id="06061-145">數值屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="06061-145">Default for numeric properties.</span></span> <span data-ttu-id="06061-146">值會顯示為數字。</span><span class="sxs-lookup"><span data-stu-id="06061-146">Value is displayed as a number.</span></span> <span data-ttu-id="06061-147">使用 &quot; >cultureinfo.numberformat &quot; 來格式化。</span><span class="sxs-lookup"><span data-stu-id="06061-147">Use &quot;numberFormat&quot; to format.</span></span> <span data-ttu-id="06061-148">方法會傳回 PDDT_NUMBER。</span><span class="sxs-lookup"><span data-stu-id="06061-148">Method returns PDDT_NUMBER.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="06061-149">Boolean</span></span></td>
<td><span data-ttu-id="06061-150">預設值 <typeInfo type=&quot;Boolean&quot;> 。</span><span class="sxs-lookup"><span data-stu-id="06061-150">Default if <typeInfo type=&quot;Boolean&quot;>.</span></span> <span data-ttu-id="06061-151">值會顯示為布林值。</span><span class="sxs-lookup"><span data-stu-id="06061-151">Value is displayed as a boolean.</span></span> <span data-ttu-id="06061-152">使用 &quot; booleanFormat &quot; 來格式化。</span><span class="sxs-lookup"><span data-stu-id="06061-152">Use &quot;booleanFormat&quot; to format.</span></span> <span data-ttu-id="06061-153">方法會傳回 PDDT_BOOLEAN。</span><span class="sxs-lookup"><span data-stu-id="06061-153">Method returns PDDT_BOOLEAN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-154">Datetime</span><span class="sxs-lookup"><span data-stu-id="06061-154">DateTime</span></span></td>
<td><span data-ttu-id="06061-155">預設值 <typeInfo type=&quot;DateTime&quot;> 。</span><span class="sxs-lookup"><span data-stu-id="06061-155">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="06061-156">值會顯示為日期或時間。</span><span class="sxs-lookup"><span data-stu-id="06061-156">Value is displayed as a date or time.</span></span> <span data-ttu-id="06061-157">使用 &quot; dateTimeFormat &quot; 來格式化。</span><span class="sxs-lookup"><span data-stu-id="06061-157">Use &quot;dateTimeFormat&quot; to format.</span></span> <span data-ttu-id="06061-158">方法會傳回 PDDT_DATETIME。</span><span class="sxs-lookup"><span data-stu-id="06061-158">Method returns PDDT_DATETIME.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-159">列舉型別</span><span class="sxs-lookup"><span data-stu-id="06061-159">Enumeration</span></span></td>
<td><span data-ttu-id="06061-160">值會顯示為 enumeratedList 元素所提供的顯示字串 &quot; 對應 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="06061-160">Value is displayed as a display string mapping provided by the &quot;enumeratedList&quot; element.</span></span> <span data-ttu-id="06061-161">方法會傳回 PDDT_ENUMERATED。</span><span class="sxs-lookup"><span data-stu-id="06061-161">Method returns PDDT_ENUMERATED.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-162">對齊</span><span class="sxs-lookup"><span data-stu-id="06061-162">alignment</span></span></td>
<td><span data-ttu-id="06061-163">選擇性。</span><span class="sxs-lookup"><span data-stu-id="06061-163">Optional.</span></span> <span data-ttu-id="06061-164">預設值為 &quot; Left &quot; 。</span><span class="sxs-lookup"><span data-stu-id="06061-164">Default is &quot;Left&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="06061-165">值</span><span class="sxs-lookup"><span data-stu-id="06061-165">Value</span></span></th>
<th><span data-ttu-id="06061-166">意義</span><span class="sxs-lookup"><span data-stu-id="06061-166">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06061-167">Left</span><span class="sxs-lookup"><span data-stu-id="06061-167">Left</span></span></td>
<td><span data-ttu-id="06061-168">預設值。</span><span class="sxs-lookup"><span data-stu-id="06061-168">Default.</span></span> <span data-ttu-id="06061-169">靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="06061-169">Align left.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-170">Center</span><span class="sxs-lookup"><span data-stu-id="06061-170">Center</span></span></td>
<td><span data-ttu-id="06061-171">置中對齊。</span><span class="sxs-lookup"><span data-stu-id="06061-171">Align center.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-172">Right</span><span class="sxs-lookup"><span data-stu-id="06061-172">Right</span></span></td>
<td><span data-ttu-id="06061-173">靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="06061-173">Align right.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-174">relativeDescriptionType</span><span class="sxs-lookup"><span data-stu-id="06061-174">relativeDescriptionType</span></span></td>
<td><span data-ttu-id="06061-175">選擇性。</span><span class="sxs-lookup"><span data-stu-id="06061-175">Optional.</span></span> <span data-ttu-id="06061-176">預設值為 &quot; [一般] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="06061-176">Default is &quot;General&quot;.</span></span> <span data-ttu-id="06061-177">指定當您將此屬性與另一個值進行比較時，應如何描述這兩個值。</span><span class="sxs-lookup"><span data-stu-id="06061-177">Specifies how two values of this property should be described when they are compared with one another.</span></span> <span data-ttu-id="06061-178">在相等的情況下， &quot; &quot; 一律會使用相同的。</span><span class="sxs-lookup"><span data-stu-id="06061-178">In the case of equivalency, &quot;Same&quot; is always used.</span></span> <span data-ttu-id="06061-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription：： GetRelativeDescription</strong></a> 和 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription：： GetRelativeDescriptionType</strong></a> 使用此值來決定要使用的相對描述顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="06061-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> and <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> use this value to determine what relative description display names to use.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="06061-180">值</span><span class="sxs-lookup"><span data-stu-id="06061-180">Value</span></span></th>
<th><span data-ttu-id="06061-181">意義</span><span class="sxs-lookup"><span data-stu-id="06061-181">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06061-182">一般</span><span class="sxs-lookup"><span data-stu-id="06061-182">General</span></span></td>
<td><span data-ttu-id="06061-183">預設值。</span><span class="sxs-lookup"><span data-stu-id="06061-183">Default.</span></span> <span data-ttu-id="06061-184">使用 &quot; 不同 &quot;  /  &quot; &quot;  /  &quot; 的不同 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="06061-184">Uses &quot;Different&quot; / &quot;Same&quot; / &quot;Different&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-185">Date</span><span class="sxs-lookup"><span data-stu-id="06061-185">Date</span></span></td>
<td><span data-ttu-id="06061-186">預設值 <typeInfo type=&quot;DateTime&quot;> 。</span><span class="sxs-lookup"><span data-stu-id="06061-186">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="06061-187">稍後會使用較 &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; 舊的版本，或使用 &quot; 較舊的舊版本 &quot;  /  &quot; &quot;  /  &quot; &quot; ，或 &quot; 稍後使用 &quot;  /  &quot; &quot;  /  &quot; &quot; 較舊的版本。</span><span class="sxs-lookup"><span data-stu-id="06061-187">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;, or uses &quot;Older&quot; / &quot;Same&quot; / &quot;Newer&quot;, or uses &quot;Sooner&quot; / &quot;Same&quot; / &quot;Later&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-188">大小</span><span class="sxs-lookup"><span data-stu-id="06061-188">Size</span></span></td>
<td><span data-ttu-id="06061-189">使用 &quot; 較 &quot;  /  &quot; &quot;  /  &quot; 大的相同&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-189">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-190">Count</span><span class="sxs-lookup"><span data-stu-id="06061-190">Count</span></span></td>
<td><span data-ttu-id="06061-191">使用 &quot; 較 &quot;  /  &quot; &quot;  /  &quot; 大的相同&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-191">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-192">修訂版</span><span class="sxs-lookup"><span data-stu-id="06061-192">Revision</span></span></td>
<td><span data-ttu-id="06061-193">&quot;稍早 &quot;  /  &quot; &quot;  /  &quot; 使用&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-193">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-194">長度</span><span class="sxs-lookup"><span data-stu-id="06061-194">Length</span></span></td>
<td><span data-ttu-id="06061-195">使用 &quot; 較 &quot;  /  &quot; &quot;  /  &quot; 長的時間&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-195">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-196">持續時間</span><span class="sxs-lookup"><span data-stu-id="06061-196">Duration</span></span></td>
<td><span data-ttu-id="06061-197">使用 &quot; 較 &quot;  /  &quot; &quot;  /  &quot; 長的時間&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-197">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-198">速度</span><span class="sxs-lookup"><span data-stu-id="06061-198">Speed</span></span></td>
<td><span data-ttu-id="06061-199">使用 &quot; 速度 &quot;  /  &quot; &quot;  /  &quot; 愈慢&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-199">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-200">費率</span><span class="sxs-lookup"><span data-stu-id="06061-200">Rate</span></span></td>
<td><span data-ttu-id="06061-201">使用 &quot; 速度 &quot;  /  &quot; &quot;  /  &quot; 愈慢&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-201">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-202">分級</span><span class="sxs-lookup"><span data-stu-id="06061-202">Rating</span></span></td>
<td><span data-ttu-id="06061-203">使用 &quot; 較 &quot;  /  &quot; &quot;  /  &quot; 高的相同&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-203">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-204">優先順序</span><span class="sxs-lookup"><span data-stu-id="06061-204">Priority</span></span></td>
<td><span data-ttu-id="06061-205">使用 &quot; 較 &quot;  /  &quot; &quot;  /  &quot; 高的相同&quot;</span><span class="sxs-lookup"><span data-stu-id="06061-205">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06061-206">defaultSortDirection</span><span class="sxs-lookup"><span data-stu-id="06061-206">defaultSortDirection</span></span></td>
<td><span data-ttu-id="06061-207">指定排序方向。</span><span class="sxs-lookup"><span data-stu-id="06061-207">Specifies sort direction.</span></span> <span data-ttu-id="06061-208">預設值為 &quot; 遞增 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="06061-208">Default is &quot;Ascending&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="06061-209">值</span><span class="sxs-lookup"><span data-stu-id="06061-209">Value</span></span></th>
<th><span data-ttu-id="06061-210">意義</span><span class="sxs-lookup"><span data-stu-id="06061-210">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06061-211">遞增</span><span class="sxs-lookup"><span data-stu-id="06061-211">Ascending</span></span></td>
<td><span data-ttu-id="06061-212">遞增排序。</span><span class="sxs-lookup"><span data-stu-id="06061-212">Sorts ascending.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06061-213">遞減</span><span class="sxs-lookup"><span data-stu-id="06061-213">Descending</span></span></td>
<td><span data-ttu-id="06061-214">遞減排序。</span><span class="sxs-lookup"><span data-stu-id="06061-214">Sorts descending.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
