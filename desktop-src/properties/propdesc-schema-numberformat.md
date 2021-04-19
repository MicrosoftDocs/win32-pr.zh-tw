---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType=&\#0034;Number&\#0034;> 。
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: '>cultureinfo.numberformat'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988730"
---
# <a name="numberformat"></a><span data-ttu-id="0c984-104">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="0c984-104">numberFormat</span></span>

<span data-ttu-id="0c984-105">指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。</span><span class="sxs-lookup"><span data-stu-id="0c984-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="0c984-106">這僅適用于 <displayInfo displayType="Number"> 。</span><span class="sxs-lookup"><span data-stu-id="0c984-106">This is applicable only if <displayInfo displayType="Number">.</span></span> <span data-ttu-id="0c984-107">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[>cultureinfo.numberformat]()元素。</span><span class="sxs-lookup"><span data-stu-id="0c984-107">There should be only one [numberFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="0c984-108">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="0c984-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="0c984-109">如果未提供任何 [>cultureinfo.numberformat]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="0c984-109">If no [numberFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c984-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c984-110">Syntax</span></span>


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
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
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="0c984-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0c984-111">Element Information</span></span>



| <span data-ttu-id="0c984-112">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="0c984-112">Parent Element</span></span>                                   | <span data-ttu-id="0c984-113">子元素</span><span class="sxs-lookup"><span data-stu-id="0c984-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="0c984-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0c984-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="0c984-115">無</span><span class="sxs-lookup"><span data-stu-id="0c984-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0c984-116">屬性</span><span class="sxs-lookup"><span data-stu-id="0c984-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c984-117">屬性</span><span class="sxs-lookup"><span data-stu-id="0c984-117">Attribute</span></span></th>
<th><span data-ttu-id="0c984-118">描述</span><span class="sxs-lookup"><span data-stu-id="0c984-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c984-119">formatAs</span><span class="sxs-lookup"><span data-stu-id="0c984-119">formatAs</span></span></td>
<td><span data-ttu-id="0c984-120">公用。</span><span class="sxs-lookup"><span data-stu-id="0c984-120">Public.</span></span> <span data-ttu-id="0c984-121">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0c984-121">Optional.</span></span> <span data-ttu-id="0c984-122">預設值為 &quot; [一般] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="0c984-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="0c984-123">指定顯示格式。</span><span class="sxs-lookup"><span data-stu-id="0c984-123">Specifies the display format.</span></span> <span data-ttu-id="0c984-124">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="0c984-124">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0c984-125">值</span><span class="sxs-lookup"><span data-stu-id="0c984-125">Value</span></span></th>
<th><span data-ttu-id="0c984-126">意義</span><span class="sxs-lookup"><span data-stu-id="0c984-126">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c984-127">一般</span><span class="sxs-lookup"><span data-stu-id="0c984-127">General</span></span></td>
<td><span data-ttu-id="0c984-128">預設值。</span><span class="sxs-lookup"><span data-stu-id="0c984-128">Default.</span></span> <span data-ttu-id="0c984-129">將值顯示為未格式化的數位。</span><span class="sxs-lookup"><span data-stu-id="0c984-129">Displays the value as an unformatted number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c984-130">百分比</span><span class="sxs-lookup"><span data-stu-id="0c984-130">Percentage</span></span></td>
<td><span data-ttu-id="0c984-131">將值格式化為百分比。</span><span class="sxs-lookup"><span data-stu-id="0c984-131">Formats the value as a percentage.</span></span> <span data-ttu-id="0c984-132">需要屬性為 UInt32。</span><span class="sxs-lookup"><span data-stu-id="0c984-132">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c984-133">ByteSize</span><span class="sxs-lookup"><span data-stu-id="0c984-133">ByteSize</span></span></td>
<td><span data-ttu-id="0c984-134">適當地將值格式化為位元組、 &quot; KB &quot; 、 &quot; MB &quot; 或 &quot; GB &quot; 。</span><span class="sxs-lookup"><span data-stu-id="0c984-134">Formats the value as a byte, &quot;KB&quot;, &quot;MB&quot;, or &quot;GB&quot; as appropriate.</span></span> <span data-ttu-id="0c984-135">要求屬性必須是 UInt64。</span><span class="sxs-lookup"><span data-stu-id="0c984-135">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c984-136">KBSize</span><span class="sxs-lookup"><span data-stu-id="0c984-136">KBSize</span></span></td>
<td><span data-ttu-id="0c984-137">&quot; &quot; 不論值為何，都會將值格式化為 KB。</span><span class="sxs-lookup"><span data-stu-id="0c984-137">Formats the value as a &quot;KB&quot;, no matter what the value is.</span></span> <span data-ttu-id="0c984-138">要求屬性必須是 UInt64。</span><span class="sxs-lookup"><span data-stu-id="0c984-138">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c984-139">SampleSize</span><span class="sxs-lookup"><span data-stu-id="0c984-139">SampleSize</span></span></td>
<td><span data-ttu-id="0c984-140">將值格式化為位數。</span><span class="sxs-lookup"><span data-stu-id="0c984-140">Formats the value as a number of bits.</span></span> <span data-ttu-id="0c984-141">需要屬性為 UInt32。</span><span class="sxs-lookup"><span data-stu-id="0c984-141">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c984-142">位元速率</span><span class="sxs-lookup"><span data-stu-id="0c984-142">BitRate</span></span></td>
<td><span data-ttu-id="0c984-143">以 Kbps 為單位格式化值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="0c984-143">Formats the value in &quot;Kbps&quot;.</span></span> <span data-ttu-id="0c984-144">需要屬性為 UInt32。</span><span class="sxs-lookup"><span data-stu-id="0c984-144">Requires the property to be UInt32.</span></span> <span data-ttu-id="0c984-145">此值必須以 &quot; 每秒位數的 &quot; 單位儲存。</span><span class="sxs-lookup"><span data-stu-id="0c984-145">The value must be stored in &quot;bits-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c984-146">SampleRate</span><span class="sxs-lookup"><span data-stu-id="0c984-146">SampleRate</span></span></td>
<td><span data-ttu-id="0c984-147">將值格式化為 &quot; KHz &quot; 。</span><span class="sxs-lookup"><span data-stu-id="0c984-147">Formats the value in &quot;KHz&quot;.</span></span> <span data-ttu-id="0c984-148">需要屬性為 UInt32。</span><span class="sxs-lookup"><span data-stu-id="0c984-148">Requires the property to be UInt32.</span></span> <span data-ttu-id="0c984-149">此值必須以 &quot; 赫茲單位儲存 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="0c984-149">The value must be stored in &quot;Hertz&quot; units.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c984-150">FrameRate</span><span class="sxs-lookup"><span data-stu-id="0c984-150">FrameRate</span></span></td>
<td><span data-ttu-id="0c984-151">將畫面格/秒的值格式化。</span><span class="sxs-lookup"><span data-stu-id="0c984-151">Formats the value in frames/second.</span></span> <span data-ttu-id="0c984-152">需要屬性為 UInt32。</span><span class="sxs-lookup"><span data-stu-id="0c984-152">Requires the property to be UInt32.</span></span> <span data-ttu-id="0c984-153">此值必須以 &quot; 每秒 kb 的 &quot; 單位儲存。</span><span class="sxs-lookup"><span data-stu-id="0c984-153">The value must be stored in &quot;kilo-frames-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c984-154">阻擋的</span><span class="sxs-lookup"><span data-stu-id="0c984-154">Pixels</span></span></td>
<td><span data-ttu-id="0c984-155">以圖元單位格式化值。</span><span class="sxs-lookup"><span data-stu-id="0c984-155">Formats the value in pixel units.</span></span> <span data-ttu-id="0c984-156">需要屬性為 UInt32。</span><span class="sxs-lookup"><span data-stu-id="0c984-156">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c984-157">DPI</span><span class="sxs-lookup"><span data-stu-id="0c984-157">DPI</span></span></td>
<td><span data-ttu-id="0c984-158">將值格式化為每英寸點。</span><span class="sxs-lookup"><span data-stu-id="0c984-158">Formats the value in dots-per-inch.</span></span> <span data-ttu-id="0c984-159">需要屬性為 UInt32。</span><span class="sxs-lookup"><span data-stu-id="0c984-159">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c984-160">持續時間</span><span class="sxs-lookup"><span data-stu-id="0c984-160">Duration</span></span></td>
<td><span data-ttu-id="0c984-161">將值格式化為持續時間。</span><span class="sxs-lookup"><span data-stu-id="0c984-161">Formats the value as a duration.</span></span> <span data-ttu-id="0c984-162">使用 <formatDurationAs> 指定持續時間格式。</span><span class="sxs-lookup"><span data-stu-id="0c984-162">Use <formatDurationAs> to specify the duration format.</span></span> <span data-ttu-id="0c984-163">要求屬性必須是 UInt64。</span><span class="sxs-lookup"><span data-stu-id="0c984-163">Requires the property to be UInt64.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c984-164">formatDurationAs</span><span class="sxs-lookup"><span data-stu-id="0c984-164">formatDurationAs</span></span></td>
<td><span data-ttu-id="0c984-165">公用。</span><span class="sxs-lookup"><span data-stu-id="0c984-165">Public.</span></span> <span data-ttu-id="0c984-166">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0c984-166">Optional.</span></span> <span data-ttu-id="0c984-167">預設值為 &quot; hh： mm： ss &quot; 。</span><span class="sxs-lookup"><span data-stu-id="0c984-167">Default is &quot;hh:mm:ss&quot;.</span></span> <span data-ttu-id="0c984-168">只有在<em>formatAs = &quot; Duration &quot; </em>時才適用。</span><span class="sxs-lookup"><span data-stu-id="0c984-168">Only applies if <em>formatAs=&quot;Duration&quot;</em>.</span></span> <span data-ttu-id="0c984-169">要求屬性必須是 UInt64。</span><span class="sxs-lookup"><span data-stu-id="0c984-169">Requires the property to be UInt64.</span></span> <span data-ttu-id="0c984-170">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="0c984-170">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0c984-171">值</span><span class="sxs-lookup"><span data-stu-id="0c984-171">Value</span></span></th>
<th><span data-ttu-id="0c984-172">意義</span><span class="sxs-lookup"><span data-stu-id="0c984-172">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c984-173">hh:mm</span><span class="sxs-lookup"><span data-stu-id="0c984-173">hh:mm</span></span></td>
<td><span data-ttu-id="0c984-174">將值格式化，以小時和分鐘為單位。</span><span class="sxs-lookup"><span data-stu-id="0c984-174">Formats the value in hours and minutes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c984-175">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="0c984-175">hh:mm:ss</span></span></td>
<td><span data-ttu-id="0c984-176">預設值。</span><span class="sxs-lookup"><span data-stu-id="0c984-176">Default.</span></span> <span data-ttu-id="0c984-177">以小時、分鐘和秒為單位來格式化值。</span><span class="sxs-lookup"><span data-stu-id="0c984-177">Formats the value in hours, minutes, and seconds.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c984-178">hh： mm： ss. fff</span><span class="sxs-lookup"><span data-stu-id="0c984-178">hh:mm:ss.fff</span></span></td>
<td><span data-ttu-id="0c984-179">以小時、分鐘、秒和毫秒為值格式化。</span><span class="sxs-lookup"><span data-stu-id="0c984-179">Formats the value in hours, minutes, seconds, and milliseconds.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
