---
description: 預先安裝的計算資料類別的抽象基類。
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Win32_PerfFormattedData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936446"
---
# <a name="win32_perfformatteddata-class"></a><span data-ttu-id="e1caf-103">Win32 \_ PerfFormattedData 類別</span><span class="sxs-lookup"><span data-stu-id="e1caf-103">Win32\_PerfFormattedData class</span></span>

<span data-ttu-id="e1caf-104">預先安裝的計算資料類別的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="e1caf-104">An abstract base class for the preinstalled, calculated data classes.</span></span> <span data-ttu-id="e1caf-105">這類類別的範例為 [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-105">An example of such a class is [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="e1caf-106">這些類別包含高效能 [格式化效能 Data Provider](../wmisdk/formatted-performance-data-provider.md)所提供的計算值。</span><span class="sxs-lookup"><span data-stu-id="e1caf-106">These classes contain calculated values provided by the high-performance [Formatted Performance Data Provider](../wmisdk/formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="e1caf-107">下列語法簡化自 MOF 程式碼，並顯示所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e1caf-107">The following syntax is simplified from MOF code and shows all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1caf-108">語法</span><span class="sxs-lookup"><span data-stu-id="e1caf-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a><span data-ttu-id="e1caf-109">成員</span><span class="sxs-lookup"><span data-stu-id="e1caf-109">Members</span></span>

<span data-ttu-id="e1caf-110">**Win32 \_ PerfFormattedData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e1caf-110">The **Win32\_PerfFormattedData** class has these types of members:</span></span>

-   [<span data-ttu-id="e1caf-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e1caf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1caf-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e1caf-112">Properties</span></span>

<span data-ttu-id="e1caf-113">**Win32 \_ PerfFormattedData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e1caf-113">The **Win32\_PerfFormattedData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1caf-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="e1caf-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e1caf-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-117">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="e1caf-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-118">統計資料或度量的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e1caf-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="e1caf-119">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1caf-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="e1caf-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e1caf-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-123">統計資料或度量的文字描述。</span><span class="sxs-lookup"><span data-stu-id="e1caf-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="e1caf-124">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1caf-125">**Frequency \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="e1caf-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e1caf-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-128">**Timestamp \_ 物件** 屬性之每秒刻度的頻率。</span><span class="sxs-lookup"><span data-stu-id="e1caf-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="e1caf-129">當子歸類時，提供者會定義這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e1caf-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="e1caf-130">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e1caf-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="e1caf-131">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-131">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1caf-132">**頻率 \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="e1caf-132">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-133">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e1caf-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-135">**Frequency \_ PerfTime** 屬性每秒的頻率（以刻度為單位）。</span><span class="sxs-lookup"><span data-stu-id="e1caf-135">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="e1caf-136">您可以藉由呼叫 Windows 函式 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。</span><span class="sxs-lookup"><span data-stu-id="e1caf-136">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="e1caf-137">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e1caf-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="e1caf-138">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-138">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1caf-139">**頻率 \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="e1caf-139">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-140">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e1caf-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-142">**時間戳記 \_ Sys100NS** 屬性 (10000000) 的每秒刻度頻率。</span><span class="sxs-lookup"><span data-stu-id="e1caf-142">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="e1caf-143">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e1caf-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="e1caf-144">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-144">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1caf-145">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e1caf-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e1caf-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-148">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e1caf-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-149">統計資料或度量已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="e1caf-149">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="e1caf-150">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="e1caf-150">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e1caf-151">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-151">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1caf-152">**Timestamp \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="e1caf-152">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-153">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e1caf-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-155">物件定義的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e1caf-155">Object-defined timestamp.</span></span> <span data-ttu-id="e1caf-156">提供者會定義他的屬性。</span><span class="sxs-lookup"><span data-stu-id="e1caf-156">The provider defines his property.</span></span>

<span data-ttu-id="e1caf-157">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e1caf-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="e1caf-158">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-158">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1caf-159">**時間戳記 \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="e1caf-159">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-160">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e1caf-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-162">High 效能計數器時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e1caf-162">High Performance counter timestamp.</span></span> <span data-ttu-id="e1caf-163">您可以藉由呼叫 Windows 函式 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。</span><span class="sxs-lookup"><span data-stu-id="e1caf-163">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="e1caf-164">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e1caf-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="e1caf-165">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-165">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1caf-166">**時間戳記 \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="e1caf-166">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1caf-167">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e1caf-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1caf-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1caf-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1caf-169">100毫微秒單位的時間戳記值。</span><span class="sxs-lookup"><span data-stu-id="e1caf-169">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="e1caf-170">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e1caf-170">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="e1caf-171">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-171">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1caf-172">備註</span><span class="sxs-lookup"><span data-stu-id="e1caf-172">Remarks</span></span>

<span data-ttu-id="e1caf-173">**Win32 \_ PerfFormattedData** 類別是衍生自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)的 [**win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="e1caf-173">The **Win32\_PerfFormattedData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span> <span data-ttu-id="e1caf-174">類別可在 **根 \\ cimv2** 命名空間中找到。</span><span class="sxs-lookup"><span data-stu-id="e1caf-174">The class is found in the **root\\cimv2** namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1caf-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1caf-175">Requirements</span></span>



| <span data-ttu-id="e1caf-176">需求</span><span class="sxs-lookup"><span data-stu-id="e1caf-176">Requirement</span></span> | <span data-ttu-id="e1caf-177">值</span><span class="sxs-lookup"><span data-stu-id="e1caf-177">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1caf-178">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1caf-178">Minimum supported client</span></span><br/> | <span data-ttu-id="e1caf-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1caf-179">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="e1caf-180">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1caf-180">Minimum supported server</span></span><br/> | <span data-ttu-id="e1caf-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1caf-181">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="e1caf-182">命名空間</span><span class="sxs-lookup"><span data-stu-id="e1caf-182">Namespace</span></span><br/>                | <span data-ttu-id="e1caf-183">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e1caf-183">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="e1caf-184">MOF</span><span class="sxs-lookup"><span data-stu-id="e1caf-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1caf-185"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1caf-185"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="e1caf-186">DLL</span><span class="sxs-lookup"><span data-stu-id="e1caf-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1caf-187"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1caf-187"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1caf-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1caf-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1caf-189">**Win32 \_ 效能**</span><span class="sxs-lookup"><span data-stu-id="e1caf-189">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="e1caf-190">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="e1caf-190">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="e1caf-191">存取 WMI 預先安裝的效能類別</span><span class="sxs-lookup"><span data-stu-id="e1caf-191">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="e1caf-192">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="e1caf-192">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="e1caf-193">存取腳本中的效能資料</span><span class="sxs-lookup"><span data-stu-id="e1caf-193">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
