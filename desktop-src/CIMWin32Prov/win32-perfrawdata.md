---
description: 所有具體原始效能計數器類別的抽象基類。
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Win32_PerfRawData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510729"
---
# <a name="win32_perfrawdata-class"></a><span data-ttu-id="fd502-103">Win32 \_ PerfRawData 類別</span><span class="sxs-lookup"><span data-stu-id="fd502-103">Win32\_PerfRawData class</span></span>

<span data-ttu-id="fd502-104">所有具體原始效能計數器類別的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="fd502-104">The abstract base class for all concrete raw performance counter classes.</span></span>

<span data-ttu-id="fd502-105">若要顯示在 [系統監視器] 中，效能計數器類別必須新增至根 \\ cimv2 命名空間，並衍生自 **Win32 \_ PerfRawData**。</span><span class="sxs-lookup"><span data-stu-id="fd502-105">To appear in System Monitor, performance counter classes must be added to the root\\cimv2 namespace and derived from **Win32\_PerfRawData**.</span></span> <span data-ttu-id="fd502-106">這些類別中的資料是由高效能 [效能計數器提供者](../wmisdk/performance-counter-provider.md)所提供。</span><span class="sxs-lookup"><span data-stu-id="fd502-106">Data in these classes are provided by the high-performance [Performance Counter Provider](../wmisdk/performance-counter-provider.md).</span></span>

<span data-ttu-id="fd502-107">從 **Win32 \_ PerfRawData** 衍生類別時，會繼承下列屬性：</span><span class="sxs-lookup"><span data-stu-id="fd502-107">The following properties are inherited when a class is derived from **Win32\_PerfRawData**:</span></span>

-   <span data-ttu-id="fd502-108">**時間戳記 \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="fd502-108">**Timestamp\_PerfTime**</span></span>
-   <span data-ttu-id="fd502-109">**時間戳記 \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="fd502-109">**Timestamp\_Sys100NS**</span></span>
-   <span data-ttu-id="fd502-110">**Timestamp \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="fd502-110">**Timestamp\_Object**</span></span>
-   <span data-ttu-id="fd502-111">**頻率 \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="fd502-111">**Frequency\_PerfTime**</span></span>
-   <span data-ttu-id="fd502-112">**頻率 \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="fd502-112">**Frequency\_Sys100NS**</span></span>
-   <span data-ttu-id="fd502-113">**Frequency \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="fd502-113">**Frequency\_Object**</span></span>

<span data-ttu-id="fd502-114">在每個案例中，屬性都必須由提供者填寫，否則無法在系統監視器中顯示該類別。</span><span class="sxs-lookup"><span data-stu-id="fd502-114">In each case, the properties must be filled out by the provider or the class cannot be displayed in System Monitor.</span></span> <span data-ttu-id="fd502-115">這些屬性是用來計算效能資料取用者的計數器類型公式。</span><span class="sxs-lookup"><span data-stu-id="fd502-115">These properties are used to compute counter type formulas by consumers of performance data.</span></span>

<span data-ttu-id="fd502-116">下列語法簡化自 MOF 程式碼，並顯示所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd502-116">The following syntax is simplified from MOF code and shows all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd502-117">語法</span><span class="sxs-lookup"><span data-stu-id="fd502-117">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

## <a name="members"></a><span data-ttu-id="fd502-118">成員</span><span class="sxs-lookup"><span data-stu-id="fd502-118">Members</span></span>

<span data-ttu-id="fd502-119">**Win32 \_ PerfRawData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fd502-119">The **Win32\_PerfRawData** class has these types of members:</span></span>

-   [<span data-ttu-id="fd502-120">屬性</span><span class="sxs-lookup"><span data-stu-id="fd502-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd502-121">屬性</span><span class="sxs-lookup"><span data-stu-id="fd502-121">Properties</span></span>

<span data-ttu-id="fd502-122">**Win32 \_ PerfRawData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fd502-122">The **Win32\_PerfRawData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd502-123">**標題**</span><span class="sxs-lookup"><span data-stu-id="fd502-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd502-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd502-126">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="fd502-126">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fd502-127">統計資料或度量的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="fd502-127">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="fd502-128">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-128">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd502-129">**說明**</span><span class="sxs-lookup"><span data-stu-id="fd502-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd502-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd502-132">統計資料或度量的文字描述。</span><span class="sxs-lookup"><span data-stu-id="fd502-132">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="fd502-133">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-133">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd502-134">**Frequency \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="fd502-134">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-135">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fd502-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd502-137">**Timestamp \_ 物件** 屬性之每秒刻度的頻率。</span><span class="sxs-lookup"><span data-stu-id="fd502-137">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="fd502-138">當子歸類時，提供者會定義這個屬性。</span><span class="sxs-lookup"><span data-stu-id="fd502-138">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="fd502-139">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fd502-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fd502-140">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-140">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd502-141">**頻率 \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="fd502-141">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-142">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fd502-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd502-144">**Frequency \_ PerfTime** 屬性每秒的頻率（以刻度為單位）。</span><span class="sxs-lookup"><span data-stu-id="fd502-144">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="fd502-145">您可以藉由呼叫 Windows 函式 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。</span><span class="sxs-lookup"><span data-stu-id="fd502-145">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="fd502-146">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fd502-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fd502-147">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-147">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd502-148">**頻率 \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="fd502-148">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-149">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fd502-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd502-151">**時間戳記 \_ Sys100NS** 屬性 (10000000) 的每秒刻度頻率。</span><span class="sxs-lookup"><span data-stu-id="fd502-151">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="fd502-152">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fd502-152">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fd502-153">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-153">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd502-154">**名稱**</span><span class="sxs-lookup"><span data-stu-id="fd502-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd502-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd502-157">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="fd502-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fd502-158">統計資料或度量已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="fd502-158">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="fd502-159">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="fd502-159">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fd502-160">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-160">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd502-161">**Timestamp \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="fd502-161">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-162">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fd502-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd502-164">物件定義的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fd502-164">Object-defined timestamp.</span></span> <span data-ttu-id="fd502-165">提供者會定義他的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd502-165">The provider defines his property.</span></span>

<span data-ttu-id="fd502-166">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fd502-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fd502-167">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-167">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd502-168">**時間戳記 \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="fd502-168">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-169">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fd502-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd502-171">High 效能計數器時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fd502-171">High Performance counter timestamp.</span></span> <span data-ttu-id="fd502-172">您可以藉由呼叫 Windows 函式 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。</span><span class="sxs-lookup"><span data-stu-id="fd502-172">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="fd502-173">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fd502-173">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fd502-174">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-174">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd502-175">**時間戳記 \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="fd502-175">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd502-176">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fd502-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fd502-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd502-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd502-178">100毫微秒單位的時間戳記值。</span><span class="sxs-lookup"><span data-stu-id="fd502-178">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="fd502-179">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fd502-179">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fd502-180">這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-180">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd502-181">備註</span><span class="sxs-lookup"><span data-stu-id="fd502-181">Remarks</span></span>

<span data-ttu-id="fd502-182">**Win32 \_ PerfRawData** 類別是衍生自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)的 [**win32 \_ Perf**](win32-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-182">The **Win32\_PerfRawData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

<span data-ttu-id="fd502-183">所有衍生自 Win32 效能的類別都是設計來搭配 [*複習*](../wmisdk/gloss-r.md)物件使用。 [**\_**](win32-perf.md)</span><span class="sxs-lookup"><span data-stu-id="fd502-183">All classes derived from [**Win32\_Perf**](win32-perf.md) are designed to be used with a [*refresher*](../wmisdk/gloss-r.md) object.</span></span> <span data-ttu-id="fd502-184">如需如何以 c + + 程式設計語言建立及使用重新整理程式物件的詳細資訊，請參閱使用 [c + + 存取效能資料](../wmisdk/accessing-performance-data-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-184">For more information about how to create and use a refresher object in the C++ programming language, see [Accessing Performance Data in C++](../wmisdk/accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="fd502-185">如需如何在腳本程式設計語言中建立及使用重新整理程式物件的詳細資訊，請參閱 [在腳本中重新整理 WMI 資料](../wmisdk/refreshing-wmi-data-in-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="fd502-185">For more information about how to create and use a refresher object in a script programming language, see [Refreshing WMI Data in Scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd502-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd502-186">Requirements</span></span>



| <span data-ttu-id="fd502-187">需求</span><span class="sxs-lookup"><span data-stu-id="fd502-187">Requirement</span></span> | <span data-ttu-id="fd502-188">值</span><span class="sxs-lookup"><span data-stu-id="fd502-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd502-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd502-189">Minimum supported client</span></span><br/> | <span data-ttu-id="fd502-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd502-190">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="fd502-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd502-191">Minimum supported server</span></span><br/> | <span data-ttu-id="fd502-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd502-192">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="fd502-193">命名空間</span><span class="sxs-lookup"><span data-stu-id="fd502-193">Namespace</span></span><br/>                | <span data-ttu-id="fd502-194">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fd502-194">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="fd502-195">MOF</span><span class="sxs-lookup"><span data-stu-id="fd502-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd502-196"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd502-196"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="fd502-197">DLL</span><span class="sxs-lookup"><span data-stu-id="fd502-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd502-198"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd502-198"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd502-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd502-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd502-200">**Win32 \_ 效能**</span><span class="sxs-lookup"><span data-stu-id="fd502-200">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="fd502-201">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="fd502-201">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="fd502-202">存取 WMI 預先安裝的效能類別</span><span class="sxs-lookup"><span data-stu-id="fd502-202">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="fd502-203">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="fd502-203">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="fd502-204">存取腳本中的效能資料</span><span class="sxs-lookup"><span data-stu-id="fd502-204">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
