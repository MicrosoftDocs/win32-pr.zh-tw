---
description: 屬性限定詞會指定屬性所對應之效能計數器的相關資訊。
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: 效能計數器類別的屬性限定詞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e060d072c34d248f9faf634aec7710f5638721b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194916"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="62542-103">效能計數器類別的屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-103">Property Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="62542-104">屬性限定詞會指定屬性所對應之效能計數器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="62542-104">Property qualifiers specify information about the performance counter to which the property maps.</span></span>

-   [<span data-ttu-id="62542-105">原始和格式化效能類別的屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-105">Property Qualifiers for Raw and Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="62542-106">原始效能類別的屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-106">Property Qualifiers for Raw Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="62542-107">格式化效能類別的屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-107">Property Qualifiers for Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="62542-108">如何解讀屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-108">How to Interpret Property Qualifiers</span></span>](#how-to-interpret-property-qualifiers)
-   [<span data-ttu-id="62542-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="62542-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="62542-110">效能計數器是由 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 效能計數器所代表之效能物件的一部分，而 WbemPerfClass 提供者會自動將這些限定詞附加至根 CIMv2 中的 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別和屬性 \\ 。</span><span class="sxs-lookup"><span data-stu-id="62542-110">The performance counter is part of a performance object represented by a WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) Performance counter–specific qualifiers are automatically attached by the WbemPerfClass provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="62542-111">這項資訊適用于 performance 類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="62542-111">This information applies to all instances of the performance class.</span></span> <span data-ttu-id="62542-112">具有永遠為 false 的 **布林** 值的某些限定詞可能不會出現在特定類別上。</span><span class="sxs-lookup"><span data-stu-id="62542-112">Some qualifiers with **Boolean** values that are always false may not be present on specific classes.</span></span>

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a><span data-ttu-id="62542-113">原始和格式化效能類別的屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-113">Property Qualifiers for Raw and Formatted Performance Classes</span></span>

<span data-ttu-id="62542-114">下列清單會列出套用至類別中的屬性（從 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 或 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)衍生）的限定詞。</span><span class="sxs-lookup"><span data-stu-id="62542-114">The following list lists qualifiers that apply to properties in classes that are derived either from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) or [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="62542-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="62542-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="62542-116">**sint32**</span><span class="sxs-lookup"><span data-stu-id="62542-116">**sint32**</span></span>

<span data-ttu-id="62542-117">計數器類型列舉中的整數值，如 Winperf .h 或 Perflib 中所定義。</span><span class="sxs-lookup"><span data-stu-id="62542-117">Integer value in the counter type enumeration, as defined in Winperf.h or Perflib.h.</span></span> <span data-ttu-id="62542-118">[**CounterType**](countertype-qualifier.md)限定詞表示用來計算屬性所代表計數器之系統監視器中所顯示值的公式或演算法。</span><span class="sxs-lookup"><span data-stu-id="62542-118">The [**CounterType**](countertype-qualifier.md)qualifier indicates the formula or algorithm used to calculate the value shown in System Monitor for the counter which the property represents.</span></span>

</dd> <dt>

<span data-ttu-id="62542-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="62542-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="62542-120">**string**</span><span class="sxs-lookup"><span data-stu-id="62542-120">**string**</span></span>

<span data-ttu-id="62542-121">效能計數器名稱，如效能資料協助程式 (PDH) 所指定。</span><span class="sxs-lookup"><span data-stu-id="62542-121">The performance Counter name, as specified by Performance Data Helper (PDH).</span></span>

</dd> <dt>

<span data-ttu-id="62542-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="62542-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="62542-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="62542-123">**sint32**</span></span>

<span data-ttu-id="62542-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="62542-124">Not used.</span></span> <span data-ttu-id="62542-125">一律包含0。</span><span class="sxs-lookup"><span data-stu-id="62542-125">Always contains 0.</span></span>

</dd> <dt>

<span data-ttu-id="62542-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="62542-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="62542-127">**sint32**</span><span class="sxs-lookup"><span data-stu-id="62542-127">**sint32**</span></span>

<span data-ttu-id="62542-128">未使用。</span><span class="sxs-lookup"><span data-stu-id="62542-128">Not used.</span></span> <span data-ttu-id="62542-129">一律包含0。</span><span class="sxs-lookup"><span data-stu-id="62542-129">Always contains 0.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a><span data-ttu-id="62542-130">原始效能類別的屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-130">Property Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="62542-131">下列清單會列出套用至衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)之類別的所有屬性的限定詞。</span><span class="sxs-lookup"><span data-stu-id="62542-131">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="62542-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="62542-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="62542-133">**boolean**</span><span class="sxs-lookup"><span data-stu-id="62542-133">**boolean**</span></span>

<span data-ttu-id="62542-134">指出此屬性是否為要在清單方塊中使用的預設計數器。</span><span class="sxs-lookup"><span data-stu-id="62542-134">Indicates whether this property is the default counter to use in list boxes.</span></span> <span data-ttu-id="62542-135">效能計數器版本6.0 的此限定詞預設為 **False** ，因為它們不會提供資料給它。</span><span class="sxs-lookup"><span data-stu-id="62542-135">This qualifier defaults to **False** for Performance Counters Version 6.0 because they do not supply data for it.</span></span> <span data-ttu-id="62542-136">如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="62542-136">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="62542-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="62542-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span></span>
</dt> <dd>

<span data-ttu-id="62542-138">**sint32**</span><span class="sxs-lookup"><span data-stu-id="62542-138">**sint32**</span></span>

<span data-ttu-id="62542-139">要用於顯示計數器的10乘冪。</span><span class="sxs-lookup"><span data-stu-id="62542-139">Power of 10 to use for display of the counter.</span></span> <span data-ttu-id="62542-140">若為零，估計的最大值為 10 ^ 0 或1。</span><span class="sxs-lookup"><span data-stu-id="62542-140">For zero, the estimated maximum is 10^0, or 1.</span></span>

</dd> <dt>

<span data-ttu-id="62542-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="62542-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="62542-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="62542-142">**sint32**</span></span>

<span data-ttu-id="62542-143">物件層級的知識。</span><span class="sxs-lookup"><span data-stu-id="62542-143">Audience level of knowledge.</span></span> <span data-ttu-id="62542-144">未使用。</span><span class="sxs-lookup"><span data-stu-id="62542-144">Not used.</span></span> <span data-ttu-id="62542-145">此值一律為100。</span><span class="sxs-lookup"><span data-stu-id="62542-145">The value is always 100.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="62542-146">格式化效能類別的屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-146">Property Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="62542-147">下列清單會列出套用至衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)之類別的所有屬性的限定詞。</span><span class="sxs-lookup"><span data-stu-id="62542-147">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="62542-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span><span class="sxs-lookup"><span data-stu-id="62542-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span></span>
</dt> <dd>

<span data-ttu-id="62542-149">**string**</span><span class="sxs-lookup"><span data-stu-id="62542-149">**string**</span></span>

<span data-ttu-id="62542-150">用來產生結果的公式類型。</span><span class="sxs-lookup"><span data-stu-id="62542-150">Formula type used to produce the result.</span></span> <span data-ttu-id="62542-151">每個計數器類型都會使用其他屬性限定詞來計算顯示為目前屬性值的結果。</span><span class="sxs-lookup"><span data-stu-id="62542-151">Each counter type uses the other property qualifiers to calculate the result shown as the value of the current property.</span></span> <span data-ttu-id="62542-152">**Counter**、 **PerfTimeStamp** 和 **PerfTimeFreq** 限定詞會對應到提供資料的原始類別中的屬性。</span><span class="sxs-lookup"><span data-stu-id="62542-152">The **Counter**, **PerfTimeStamp**, and **PerfTimeFreq** qualifiers map to properties in a raw class which supply the data.</span></span>

<span data-ttu-id="62542-153">如需詳細資訊，請參閱 [CounterType 限定詞](countertype-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="62542-153">For more information, see [CounterType Qualifier](countertype-qualifier.md).</span></span>

</dd> <dt>

<span data-ttu-id="62542-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**計數器**</span><span class="sxs-lookup"><span data-stu-id="62542-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter**</span></span>
</dt> <dd>

<span data-ttu-id="62542-155">**string**</span><span class="sxs-lookup"><span data-stu-id="62542-155">**string**</span></span>

<span data-ttu-id="62542-156">在對應的原始類別中，用來做為烹飪公式中之計數器值的必要屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="62542-156">Name of a required property in the corresponding raw class to use as the counter value in the cooking formula.</span></span> <span data-ttu-id="62542-157">此值必須是對應原始類別中資料來源屬性的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="62542-157">The value must be the property name of the data source property in the corresponding raw class.</span></span>

</dd> <dt>

<span data-ttu-id="62542-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="62542-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="62542-159">**string**</span><span class="sxs-lookup"><span data-stu-id="62542-159">**string**</span></span>

<span data-ttu-id="62542-160">原始類別中的屬性名稱，用來做為烹飪公式中的頻率。</span><span class="sxs-lookup"><span data-stu-id="62542-160">Name of a property in a raw class to use as a frequency in the cooking formula.</span></span> <span data-ttu-id="62542-161">如果屬性沒有此限定詞，則會使用類別層級上適當的預設值。</span><span class="sxs-lookup"><span data-stu-id="62542-161">The appropriate default value at the class level will be used if this qualifier is not present for the property.</span></span> <span data-ttu-id="62542-162">頻率代表時間戳記的每秒刻度。</span><span class="sxs-lookup"><span data-stu-id="62542-162">The frequency represents the ticks per second of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="62542-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="62542-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span></span>
</dt> <dd>

<span data-ttu-id="62542-164">**string**</span><span class="sxs-lookup"><span data-stu-id="62542-164">**string**</span></span>

<span data-ttu-id="62542-165">原始類別中用來做為烹飪公式中之時間戳記的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="62542-165">Name of a property in a raw class to use as a timestamp in the cooking formula.</span></span> <span data-ttu-id="62542-166">如果屬性沒有此限定詞，則會使用類別層級上適當的預設值。</span><span class="sxs-lookup"><span data-stu-id="62542-166">The appropriate default value at the class level is used if this qualifier is not present for the property.</span></span> <span data-ttu-id="62542-167">自動產生的時間戳記可能會在計算中造成錯誤，因為時間戳記是近似值，並且不會考慮封送處理和實際資料收集所產生的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="62542-167">An automatically generated time stamp may introduce error in a calculation because the timestamp is an approximation and does not account for overhead incurred by marshaling and actual data collection.</span></span>

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a><span data-ttu-id="62542-168">如何解讀屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-168">How to Interpret Property Qualifiers</span></span>

<span data-ttu-id="62542-169">[**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別中的屬性包含 [格式化效能 Data Provider](formatted-performance-data-provider.md)所提供的計算資料。</span><span class="sxs-lookup"><span data-stu-id="62542-169">Properties in the [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data supplied by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span> <span data-ttu-id="62542-170">屬性值是最後計算的結果。</span><span class="sxs-lookup"><span data-stu-id="62542-170">The property value is the final calculated result.</span></span> <span data-ttu-id="62542-171">限定詞提供配方。</span><span class="sxs-lookup"><span data-stu-id="62542-171">The qualifiers supply a recipe.</span></span>

<span data-ttu-id="62542-172">**計數器** 和 **基底** 限定詞指向資料來源， **CookingType** 會指定用來產生結果的公式。</span><span class="sxs-lookup"><span data-stu-id="62542-172">The **Counter** and **Base** qualifiers point to the sources of data and **CookingType** specifies the formula used to produce the result.</span></span> <span data-ttu-id="62542-173">時間戳記和取樣頻率也來自對應的原始類別，並在 **PerfTimeStamp** 和 **PerfTimeFreq** 中命名。</span><span class="sxs-lookup"><span data-stu-id="62542-173">The timestamp and sample frequency also come from the corresponding raw class and are named in **PerfTimeStamp** and **PerfTimeFreq**.</span></span>

<span data-ttu-id="62542-174">例如，WMI 提供的其中一個格式化類別（ [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)）包含名為 **AvgDiskBytesPerRead** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="62542-174">For example, one of the formatted classes supplied by WMI, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contains a property named **AvgDiskBytesPerRead**.</span></span> <span data-ttu-id="62542-175">格式化類別中的屬性名稱必須與原始類別中的屬性相同。</span><span class="sxs-lookup"><span data-stu-id="62542-175">The name of the property in the formatted class must be the same as the property in the raw class.</span></span> <span data-ttu-id="62542-176">**AvgDiskBytesPerRead** 屬性具有下列限定詞。</span><span class="sxs-lookup"><span data-stu-id="62542-176">The **AvgDiskBytesPerRead** property has the following qualifiers.</span></span>

<span data-ttu-id="62542-177">下列清單列出所有衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)之類別的屬性可用的屬性限定詞。</span><span class="sxs-lookup"><span data-stu-id="62542-177">The following list lists the available property qualifiers for properties of all classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>



| <span data-ttu-id="62542-178">Qualifier</span><span class="sxs-lookup"><span data-stu-id="62542-178">Qualifier</span></span>         | <span data-ttu-id="62542-179">值</span><span class="sxs-lookup"><span data-stu-id="62542-179">Value</span></span>                     |
|-------------------|---------------------------|
| <span data-ttu-id="62542-180">**CookingType**</span><span class="sxs-lookup"><span data-stu-id="62542-180">**CookingType**</span></span>   | <span data-ttu-id="62542-181">效能 \_ 平均 \_ 大量</span><span class="sxs-lookup"><span data-stu-id="62542-181">PERF\_AVERAGE\_BULK</span></span>       |
| <span data-ttu-id="62542-182">**計數器**</span><span class="sxs-lookup"><span data-stu-id="62542-182">**Counter**</span></span>       | <span data-ttu-id="62542-183">AvgDiskBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="62542-183">AvgDiskBytesPerRead</span></span>       |
| <span data-ttu-id="62542-184">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="62542-184">**PerfTimeStamp**</span></span> | <span data-ttu-id="62542-185">時間戳記 \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="62542-185">Timestamp\_PerfTime</span></span>       |
| <span data-ttu-id="62542-186">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="62542-186">**PerfTimeFreq**</span></span>  | <span data-ttu-id="62542-187">頻率 \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="62542-187">Frequency\_PerfTime</span></span>       |
| <span data-ttu-id="62542-188">**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="62542-188">**PerfIndex**</span></span>     | <span data-ttu-id="62542-189">408</span><span class="sxs-lookup"><span data-stu-id="62542-189">408</span></span>                       |
| <span data-ttu-id="62542-190">**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="62542-190">**HelpIndex**</span></span>     | <span data-ttu-id="62542-191">409</span><span class="sxs-lookup"><span data-stu-id="62542-191">409</span></span>                       |
| <span data-ttu-id="62542-192">**基本**</span><span class="sxs-lookup"><span data-stu-id="62542-192">**Base**</span></span>          | <span data-ttu-id="62542-193">AvgDiskBytesPerRead \_ 基底</span><span class="sxs-lookup"><span data-stu-id="62542-193">AvgDiskBytesPerRead\_Base</span></span> |



 

<span data-ttu-id="62542-194">**AvgDiskBytesPerRead** 屬性會報告讀取作業期間從磁片傳輸的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="62542-194">The **AvgDiskBytesPerRead** property reports the average number of bytes transferred from the disk during read operations.</span></span> <span data-ttu-id="62542-195">效能 \_ 平均大量的公式 \_ 是：</span><span class="sxs-lookup"><span data-stu-id="62542-195">The formula for PERF\_AVERAGE\_BULK is:</span></span>

<span data-ttu-id="62542-196"> (Sample2.xml-Sample1) / (Base Sample2.xml-Base Sample1) </span><span class="sxs-lookup"><span data-stu-id="62542-196">(Sample2 - Sample1) / (Base Sample2 - Base Sample1)</span></span>

<span data-ttu-id="62542-197">讀取作業會以 **PerfTimeFreq** 指定的頻率進行取樣，並以 **PerfTimeStamp** 值表示最新的範例。</span><span class="sxs-lookup"><span data-stu-id="62542-197">The read operation is sampled at the frequency specified by **PerfTimeFreq** with the **PerfTimeStamp** value indicating the most recent sample.</span></span> <span data-ttu-id="62542-198">原始計數器資料（以位元組為單位）取自 [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)類別中的 **AvgDiskBytesPerRead** 屬性。</span><span class="sxs-lookup"><span data-stu-id="62542-198">The raw counter data in bytes is taken from the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class.</span></span> <span data-ttu-id="62542-199">作業資料的基礎數目取自相同類別中的 **AvgDiskBytesPerRead \_ 基底** 屬性。</span><span class="sxs-lookup"><span data-stu-id="62542-199">The base number of operations data is taken from the **AvgDiskBytesPerRead\_Base** property in that same class.</span></span>

<span data-ttu-id="62542-200">如需詳細資訊，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md) 和 [監視效能資料](monitoring-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="62542-200">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62542-201">相關主題</span><span class="sxs-lookup"><span data-stu-id="62542-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62542-202">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="62542-202">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="62542-203">WMI 效能類別專用的限定詞</span><span class="sxs-lookup"><span data-stu-id="62542-203">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="62542-204">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="62542-204">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="62542-205">存取 WMI 預先安裝的效能類別</span><span class="sxs-lookup"><span data-stu-id="62542-205">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="62542-206">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="62542-206">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
