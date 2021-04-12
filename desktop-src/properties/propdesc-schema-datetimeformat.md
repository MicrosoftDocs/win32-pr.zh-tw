---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType=&\#0034;DateTime&\#0034;> 。
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192143"
---
# <a name="datetimeformat"></a><span data-ttu-id="81808-104">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="81808-104">dateTimeFormat</span></span>

<span data-ttu-id="81808-105">指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。</span><span class="sxs-lookup"><span data-stu-id="81808-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="81808-106">這僅適用于 <displayInfo displayType="DateTime"> 。</span><span class="sxs-lookup"><span data-stu-id="81808-106">This is applicable only if <displayInfo displayType="DateTime">.</span></span> <span data-ttu-id="81808-107">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[dateTimeFormat]()元素。</span><span class="sxs-lookup"><span data-stu-id="81808-107">There should be only one [dateTimeFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="81808-108">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="81808-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="81808-109">如果未提供任何 [dateTimeFormat]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="81808-109">If no [dateTimeFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="81808-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="81808-110">Syntax</span></span>


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
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
```



## <a name="element-information"></a><span data-ttu-id="81808-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="81808-111">Element Information</span></span>



| <span data-ttu-id="81808-112">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="81808-112">Parent Element</span></span>                                   | <span data-ttu-id="81808-113">子元素</span><span class="sxs-lookup"><span data-stu-id="81808-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="81808-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="81808-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="81808-115">無</span><span class="sxs-lookup"><span data-stu-id="81808-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="81808-116">屬性</span><span class="sxs-lookup"><span data-stu-id="81808-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81808-117">屬性</span><span class="sxs-lookup"><span data-stu-id="81808-117">Attribute</span></span></th>
<th><span data-ttu-id="81808-118">描述</span><span class="sxs-lookup"><span data-stu-id="81808-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81808-119">formatAs</span><span class="sxs-lookup"><span data-stu-id="81808-119">formatAs</span></span></td>
<td><span data-ttu-id="81808-120">公用。</span><span class="sxs-lookup"><span data-stu-id="81808-120">Public.</span></span> <span data-ttu-id="81808-121">選擇性。</span><span class="sxs-lookup"><span data-stu-id="81808-121">Optional.</span></span> <span data-ttu-id="81808-122">預設值為 &quot; [一般] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="81808-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="81808-123">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="81808-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="81808-124">值</span><span class="sxs-lookup"><span data-stu-id="81808-124">Value</span></span></th>
<th><span data-ttu-id="81808-125">意義</span><span class="sxs-lookup"><span data-stu-id="81808-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81808-126">一般</span><span class="sxs-lookup"><span data-stu-id="81808-126">General</span></span></td>
<td><span data-ttu-id="81808-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="81808-127">Default.</span></span> <span data-ttu-id="81808-128">使用 <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>格式化日期時間值。</span><span class="sxs-lookup"><span data-stu-id="81808-128">Formats the date-time value using <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span></span> <span data-ttu-id="81808-129">您可以使用 <em>formatTimeAs</em> 和 <em>formatDateAs</em> 屬性來指定時間和日期的格式。</span><span class="sxs-lookup"><span data-stu-id="81808-129">Use the <em>formatTimeAs</em> and <em>formatDateAs</em> attributes to specify how the time and date are formatted.</span></span> <span data-ttu-id="81808-130">需要屬性類型為 DateTime。</span><span class="sxs-lookup"><span data-stu-id="81808-130">Requires the property type to be DateTime.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81808-131">Month</span><span class="sxs-lookup"><span data-stu-id="81808-131">Month</span></span></td>
<td><span data-ttu-id="81808-132">將值格式化為年份的其中一個月份。</span><span class="sxs-lookup"><span data-stu-id="81808-132">Formats the value as one of the months of the year.</span></span> <span data-ttu-id="81808-133">要求屬性類型必須是 Int32。</span><span class="sxs-lookup"><span data-stu-id="81808-133">Requires the property type to be Int32.</span></span> <span data-ttu-id="81808-134">值必須儲存為數值，1代表當年的第一個月。</span><span class="sxs-lookup"><span data-stu-id="81808-134">The value must be stored as a numeric value with 1 representing the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81808-135">YearMonth</span><span class="sxs-lookup"><span data-stu-id="81808-135">YearMonth</span></span></td>
<td><span data-ttu-id="81808-136">將值格式化為 &quot; 年月 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="81808-136">Formats the value as &quot;Year - Month&quot;.</span></span> <span data-ttu-id="81808-137">要求屬性類型必須是 Int32。</span><span class="sxs-lookup"><span data-stu-id="81808-137">Requires the property type to be Int32.</span></span> <span data-ttu-id="81808-138">您必須儲存此值，讓兩個最高的位元組指定年份，而較低的兩個位元組指定月份。</span><span class="sxs-lookup"><span data-stu-id="81808-138">The value must be stored such that the two highest bytes specify the year and the lower two bytes specify the month.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81808-139">Year</span><span class="sxs-lookup"><span data-stu-id="81808-139">Year</span></span></td>
<td><span data-ttu-id="81808-140">將值格式化為簡單字串。</span><span class="sxs-lookup"><span data-stu-id="81808-140">Formats the value as a simple string.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81808-141">formatTimeAs</span><span class="sxs-lookup"><span data-stu-id="81808-141">formatTimeAs</span></span></td>
<td><span data-ttu-id="81808-142">公用。</span><span class="sxs-lookup"><span data-stu-id="81808-142">Public.</span></span> <span data-ttu-id="81808-143">選擇性。</span><span class="sxs-lookup"><span data-stu-id="81808-143">Optional.</span></span> <span data-ttu-id="81808-144">預設值為 &quot; ShortTime &quot; 。</span><span class="sxs-lookup"><span data-stu-id="81808-144">Default is &quot;ShortTime&quot;.</span></span> <span data-ttu-id="81808-145">指定要在其中顯示時間的格式。</span><span class="sxs-lookup"><span data-stu-id="81808-145">Specifies the format in which to display time.</span></span> <span data-ttu-id="81808-146">適用于<strong>formatAs = &quot; General &quot; </strong>。</span><span class="sxs-lookup"><span data-stu-id="81808-146">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="81808-147">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="81808-147">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="81808-148">值</span><span class="sxs-lookup"><span data-stu-id="81808-148">Value</span></span></th>
<th><span data-ttu-id="81808-149">意義</span><span class="sxs-lookup"><span data-stu-id="81808-149">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81808-150">ShortTime</span><span class="sxs-lookup"><span data-stu-id="81808-150">ShortTime</span></span></td>
<td><span data-ttu-id="81808-151">預設值。</span><span class="sxs-lookup"><span data-stu-id="81808-151">Default.</span></span> <span data-ttu-id="81808-152">顯示如下的時間 &quot; ：下午 7:48 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="81808-152">Show the time like &quot;7:48 PM&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81808-153">長期</span><span class="sxs-lookup"><span data-stu-id="81808-153">LongTime</span></span></td>
<td><span data-ttu-id="81808-154">顯示如下的時間 &quot; ：下午 7:48:33 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="81808-154">Show the time like &quot;7:48:33 PM&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81808-155">HideTime</span><span class="sxs-lookup"><span data-stu-id="81808-155">HideTime</span></span></td>
<td><span data-ttu-id="81808-156">不要顯示日期的時間部分。</span><span class="sxs-lookup"><span data-stu-id="81808-156">Do not display the time portion of the date.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81808-157">formatDateAs</span><span class="sxs-lookup"><span data-stu-id="81808-157">formatDateAs</span></span></td>
<td><span data-ttu-id="81808-158">公用。</span><span class="sxs-lookup"><span data-stu-id="81808-158">Public.</span></span> <span data-ttu-id="81808-159">選擇性。</span><span class="sxs-lookup"><span data-stu-id="81808-159">Optional.</span></span> <span data-ttu-id="81808-160">預設值為 &quot; >shortdate &quot; 。</span><span class="sxs-lookup"><span data-stu-id="81808-160">Default is &quot;ShortDate&quot;.</span></span> <span data-ttu-id="81808-161">指定要在其中顯示日期的格式。</span><span class="sxs-lookup"><span data-stu-id="81808-161">Specifies the format in which to display the date.</span></span> <span data-ttu-id="81808-162">適用于<strong>formatAs = &quot; General &quot; </strong>。</span><span class="sxs-lookup"><span data-stu-id="81808-162">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="81808-163">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="81808-163">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="81808-164">值</span><span class="sxs-lookup"><span data-stu-id="81808-164">Value</span></span></th>
<th><span data-ttu-id="81808-165">範例</span><span class="sxs-lookup"><span data-stu-id="81808-165">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81808-166">>shortdate</span><span class="sxs-lookup"><span data-stu-id="81808-166">ShortDate</span></span></td>
<td><span data-ttu-id="81808-167">預設值。</span><span class="sxs-lookup"><span data-stu-id="81808-167">Default.</span></span> <span data-ttu-id="81808-168">顯示日期，例如 &quot; 5/13/59 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="81808-168">Show the date like &quot;5/13/59&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81808-169">>longdate</span><span class="sxs-lookup"><span data-stu-id="81808-169">LongDate</span></span></td>
<td><span data-ttu-id="81808-170">顯示日期，例如 &quot; 星期三、5月13日、1959 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="81808-170">Show the date like &quot;Wednesday, May 13, 1959&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81808-171">HideDate</span><span class="sxs-lookup"><span data-stu-id="81808-171">HideDate</span></span></td>
<td><span data-ttu-id="81808-172">不要顯示日期部分。</span><span class="sxs-lookup"><span data-stu-id="81808-172">Do not display the date portion.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81808-173">RelativeShortDate</span><span class="sxs-lookup"><span data-stu-id="81808-173">RelativeShortDate</span></span></td>
<td><span data-ttu-id="81808-174">顯示日期（如 &quot; >shortdate &quot; ），但盡可能使用相對描述（例如 &quot; 昨天 &quot; ）。</span><span class="sxs-lookup"><span data-stu-id="81808-174">Show the date like &quot;ShortDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81808-175">RelativeLongDate</span><span class="sxs-lookup"><span data-stu-id="81808-175">RelativeLongDate</span></span></td>
<td><span data-ttu-id="81808-176">顯示日期（如 &quot; >longdate &quot; ），但盡可能使用相對描述（例如 &quot; 昨天 &quot; ）。</span><span class="sxs-lookup"><span data-stu-id="81808-176">Show the date like &quot;LongDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
