---
description: 效能計數器類別 Win32 \_ PerfRawData 和 win32 PerfFormattedData 的基類 \_ 。
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Win32_Perf 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 13b339e95e175e4d2dff50c0a9674f8002933c1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970736"
---
# <a name="win32_perf-class"></a><span data-ttu-id="4926b-103">Win32 效能 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="4926b-103">Win32\_Perf class</span></span>

<span data-ttu-id="4926b-104">效能計數器類別 [**Win32 \_ PerfRawData**](win32-perfrawdata.md) 和 [**win32 \_ PerfFormattedData**](win32-perfformatteddata.md)的基類。</span><span class="sxs-lookup"><span data-stu-id="4926b-104">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

<span data-ttu-id="4926b-105">**Win32 \_Performance 會定義性能** 計數器類別的 [**CounterType**](../wmisdk/countertype-qualifier.md) 演算法中所使用的時間戳記和頻率屬性。</span><span class="sxs-lookup"><span data-stu-id="4926b-105">**Win32\_Perf** defines the required timestamp and frequency properties used in the [**CounterType**](../wmisdk/countertype-qualifier.md) algorithms for the performance counter classes.</span></span>

<span data-ttu-id="4926b-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4926b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4926b-107">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="4926b-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4926b-108">語法</span><span class="sxs-lookup"><span data-stu-id="4926b-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

## <a name="members"></a><span data-ttu-id="4926b-109">成員</span><span class="sxs-lookup"><span data-stu-id="4926b-109">Members</span></span>

<span data-ttu-id="4926b-110">**Win32 效能 \_** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4926b-110">The **Win32\_Perf** class has these types of members:</span></span>

-   [<span data-ttu-id="4926b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4926b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4926b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4926b-112">Properties</span></span>

<span data-ttu-id="4926b-113">**Win32 效能 \_** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4926b-113">The **Win32\_Perf** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4926b-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="4926b-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4926b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4926b-117">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="4926b-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4926b-118">統計資料或度量的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="4926b-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="4926b-119">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="4926b-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="4926b-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="4926b-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4926b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4926b-123">統計資料或度量的文字描述。</span><span class="sxs-lookup"><span data-stu-id="4926b-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="4926b-124">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="4926b-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="4926b-125">**Frequency \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="4926b-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4926b-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4926b-128">**Timestamp \_ 物件** 屬性之每秒刻度的頻率。</span><span class="sxs-lookup"><span data-stu-id="4926b-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="4926b-129">當子歸類時，提供者會定義這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4926b-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="4926b-130">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4926b-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4926b-131">**頻率 \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="4926b-131">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-132">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4926b-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4926b-134">**Frequency \_ PerfTime** 屬性每秒的頻率（以刻度為單位）。</span><span class="sxs-lookup"><span data-stu-id="4926b-134">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="4926b-135">您可以藉由呼叫 Windows 函式 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。</span><span class="sxs-lookup"><span data-stu-id="4926b-135">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="4926b-136">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4926b-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4926b-137">**頻率 \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="4926b-137">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-138">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4926b-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4926b-140">**時間戳記 \_ Sys100NS** 屬性 (10000000) 的每秒刻度頻率。</span><span class="sxs-lookup"><span data-stu-id="4926b-140">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="4926b-141">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4926b-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4926b-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4926b-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4926b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4926b-145">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="4926b-145">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4926b-146">統計資料或度量已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="4926b-146">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="4926b-147">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4926b-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4926b-148">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="4926b-148">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="4926b-149">**Timestamp \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="4926b-149">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-150">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4926b-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4926b-152">物件定義的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4926b-152">Object-defined timestamp.</span></span> <span data-ttu-id="4926b-153">提供者會定義他的屬性。</span><span class="sxs-lookup"><span data-stu-id="4926b-153">The provider defines his property.</span></span>

<span data-ttu-id="4926b-154">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4926b-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4926b-155">**時間戳記 \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="4926b-155">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-156">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4926b-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4926b-158">High 效能計數器時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4926b-158">High Performance counter timestamp.</span></span> <span data-ttu-id="4926b-159">您可以藉由呼叫 Windows 函式 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。</span><span class="sxs-lookup"><span data-stu-id="4926b-159">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="4926b-160">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4926b-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4926b-161">**時間戳記 \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="4926b-161">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4926b-162">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4926b-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4926b-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4926b-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4926b-164">100毫微秒單位的時間戳記值。</span><span class="sxs-lookup"><span data-stu-id="4926b-164">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="4926b-165">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4926b-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4926b-166">備註</span><span class="sxs-lookup"><span data-stu-id="4926b-166">Remarks</span></span>

<span data-ttu-id="4926b-167">**Win32 效能 \_** 類別衍生自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="4926b-167">The **Win32\_Perf** class derives from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4926b-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="4926b-168">Requirements</span></span>



| <span data-ttu-id="4926b-169">需求</span><span class="sxs-lookup"><span data-stu-id="4926b-169">Requirement</span></span> | <span data-ttu-id="4926b-170">值</span><span class="sxs-lookup"><span data-stu-id="4926b-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4926b-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4926b-171">Minimum supported client</span></span><br/> | <span data-ttu-id="4926b-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4926b-172">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="4926b-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4926b-173">Minimum supported server</span></span><br/> | <span data-ttu-id="4926b-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4926b-174">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="4926b-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="4926b-175">Namespace</span></span><br/>                | <span data-ttu-id="4926b-176">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4926b-176">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="4926b-177">DLL</span><span class="sxs-lookup"><span data-stu-id="4926b-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4926b-178"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4926b-178"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4926b-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4926b-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4926b-180">**CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="4926b-180">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dt>

[<span data-ttu-id="4926b-181">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="4926b-181">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="4926b-182">存取 WMI 預先安裝的效能類別</span><span class="sxs-lookup"><span data-stu-id="4926b-182">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="4926b-183">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="4926b-183">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="4926b-184">存取腳本中的效能資料</span><span class="sxs-lookup"><span data-stu-id="4926b-184">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
