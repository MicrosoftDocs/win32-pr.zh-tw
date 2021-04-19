---
description: 指定與 WMI 效能計數器類別對應的效能物件相關資訊。
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: 效能計數器類別的類別限定詞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992487"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="e8880-103">效能計數器類別的類別限定詞</span><span class="sxs-lookup"><span data-stu-id="e8880-103">Class Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="e8880-104">類別限定詞指定與 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 對應的效能物件相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e8880-104">Class qualifiers specify information about the performance object to which the WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) is mapped.</span></span> <span data-ttu-id="e8880-105">如需詳細資訊，請參閱 [監視效能資料](monitoring-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="e8880-105">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

-   [<span data-ttu-id="e8880-106">原始和格式化 PerformanceClasses 的限定詞</span><span class="sxs-lookup"><span data-stu-id="e8880-106">Qualifiers for Raw and Formatted PerformanceClasses</span></span>](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [<span data-ttu-id="e8880-107">原始效能類別的限定詞</span><span class="sxs-lookup"><span data-stu-id="e8880-107">Qualifiers for Raw Performance Classes</span></span>](#)
-   [<span data-ttu-id="e8880-108">格式化效能類別的限定詞</span><span class="sxs-lookup"><span data-stu-id="e8880-108">Qualifiers for Formatted Performance Classes</span></span>](#)
-   [<span data-ttu-id="e8880-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8880-109">Related topics</span></span>](#related-topics)


<span data-ttu-id="e8880-110">「WbemPerfClass」提供者會自動將效能計數器特定的限定詞附加至根 CIMv2 中的 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別和屬性 \\ 。</span><span class="sxs-lookup"><span data-stu-id="e8880-110">Performance counter–specific qualifiers are automatically attached by the "WbemPerfClass" provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="e8880-111">這項資訊適用于類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="e8880-111">This information applies to all instances of the class.</span></span> <span data-ttu-id="e8880-112">具有永遠 **為 False** 的 **布林** 值的某些限定詞可能不會出現在特定類別上。</span><span class="sxs-lookup"><span data-stu-id="e8880-112">Some qualifiers with **Boolean** values that are always **False** may not be present on specific classes.</span></span>

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a><span data-ttu-id="e8880-113">原始和格式化 PerformanceClasses 的限定詞</span><span class="sxs-lookup"><span data-stu-id="e8880-113">Qualifiers for Raw and Formatted PerformanceClasses</span></span>

<span data-ttu-id="e8880-114">下列限定詞適用于所有衍生自 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的類別。</span><span class="sxs-lookup"><span data-stu-id="e8880-114">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="e8880-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**熟**</span><span class="sxs-lookup"><span data-stu-id="e8880-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-116">**boolean**</span><span class="sxs-lookup"><span data-stu-id="e8880-116">**boolean**</span></span>

<span data-ttu-id="e8880-117">指出類別是否包含處理後的資料。</span><span class="sxs-lookup"><span data-stu-id="e8880-117">Indicates whether the class contains cooked data.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="e8880-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-119">**string**</span><span class="sxs-lookup"><span data-stu-id="e8880-119">**string**</span></span>

<span data-ttu-id="e8880-120">效能物件名稱。</span><span class="sxs-lookup"><span data-stu-id="e8880-120">Performance object name.</span></span> <span data-ttu-id="e8880-121">如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="e8880-121">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="e8880-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="e8880-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="e8880-123">**sint32**</span></span>

<span data-ttu-id="e8880-124">不提供詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e8880-124">Does not provide detail data.</span></span> <span data-ttu-id="e8880-125">一律包含100的值。</span><span class="sxs-lookup"><span data-stu-id="e8880-125">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**動態**</span><span class="sxs-lookup"><span data-stu-id="e8880-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-127">**boolean**</span><span class="sxs-lookup"><span data-stu-id="e8880-127">**boolean**</span></span>

<span data-ttu-id="e8880-128">一律設定為 **True** ，因為實例一律為動態。</span><span class="sxs-lookup"><span data-stu-id="e8880-128">Always set to **True** because instances are always dynamic.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span><span class="sxs-lookup"><span data-stu-id="e8880-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-130">**boolean**</span><span class="sxs-lookup"><span data-stu-id="e8880-130">**boolean**</span></span>

<span data-ttu-id="e8880-131">指出類別是否來自舊版效能程式庫。</span><span class="sxs-lookup"><span data-stu-id="e8880-131">Indicates whether the class comes from a legacy performance library.</span></span> <span data-ttu-id="e8880-132">一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="e8880-132">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="e8880-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-134">**sint32**</span><span class="sxs-lookup"><span data-stu-id="e8880-134">**sint32**</span></span>

<span data-ttu-id="e8880-135">索引不再有效。</span><span class="sxs-lookup"><span data-stu-id="e8880-135">Indexes are no longer valid.</span></span> <span data-ttu-id="e8880-136">此辨識符號一律為零。</span><span class="sxs-lookup"><span data-stu-id="e8880-136">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="e8880-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span></span> 
</dt> <dd>

<span data-ttu-id="e8880-138">**boolean**</span><span class="sxs-lookup"><span data-stu-id="e8880-138">**boolean**</span></span>

<span data-ttu-id="e8880-139">指出類別是高效能類別。</span><span class="sxs-lookup"><span data-stu-id="e8880-139">Indicates that the class is a high-performance class.</span></span> <span data-ttu-id="e8880-140">一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="e8880-140">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**現場**</span><span class="sxs-lookup"><span data-stu-id="e8880-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="e8880-142">**sint32**</span></span>

<span data-ttu-id="e8880-143">地區設定識別項。</span><span class="sxs-lookup"><span data-stu-id="e8880-143">Locale identifier.</span></span> <span data-ttu-id="e8880-144">值一律為 1033 (美式英文) 。</span><span class="sxs-lookup"><span data-stu-id="e8880-144">Value is always 1033 (U.S. English).</span></span>

</dd> <dt>

<span data-ttu-id="e8880-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="e8880-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-146">**int32**</span><span class="sxs-lookup"><span data-stu-id="e8880-146">**int32**</span></span>

<span data-ttu-id="e8880-147">索引不再有效。</span><span class="sxs-lookup"><span data-stu-id="e8880-147">Indexes are no longer valid.</span></span> <span data-ttu-id="e8880-148">此辨識符號一律為零。</span><span class="sxs-lookup"><span data-stu-id="e8880-148">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**供應商**</span><span class="sxs-lookup"><span data-stu-id="e8880-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-150">**string**</span><span class="sxs-lookup"><span data-stu-id="e8880-150">**string**</span></span>

<span data-ttu-id="e8880-151">執行個體提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8880-151">Name of the instance provider.</span></span> <span data-ttu-id="e8880-152">值為 "WbemPerfV2"。</span><span class="sxs-lookup"><span data-stu-id="e8880-152">Value is "WbemPerfV2".</span></span>

</dd> <dt>

<span data-ttu-id="e8880-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span><span class="sxs-lookup"><span data-stu-id="e8880-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-154">**string**</span><span class="sxs-lookup"><span data-stu-id="e8880-154">**string**</span></span>

<span data-ttu-id="e8880-155">**HKEY \_ 本機 \_ 電腦 \\ CurrentControlSet \\ 服務** 機碼中的驅動程式名稱，可在此機碼中找到效能金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8880-155">Name of the driver in the **HKEY\_LOCAL\_MACHINE\\CurrentControlSet\\Services** key, under which the performance key can be located.</span></span> <span data-ttu-id="e8880-156">此名稱也是提供效能計數器之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8880-156">This name is also the name of the service that provides the performance counter.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**單身 人士**</span><span class="sxs-lookup"><span data-stu-id="e8880-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-158">**boolean**</span><span class="sxs-lookup"><span data-stu-id="e8880-158">**boolean**</span></span>

<span data-ttu-id="e8880-159">若 **為 True**，表示只有類別的單一實例存在。</span><span class="sxs-lookup"><span data-stu-id="e8880-159">If **True**, indicates that only a single instance of the class exists.</span></span>

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a><span data-ttu-id="e8880-160">原始效能類別的限定詞</span><span class="sxs-lookup"><span data-stu-id="e8880-160">Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="e8880-161">下列限定詞適用于所有衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)的類別。</span><span class="sxs-lookup"><span data-stu-id="e8880-161">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="e8880-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**昂貴**</span><span class="sxs-lookup"><span data-stu-id="e8880-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costly**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-163">**boolean**</span><span class="sxs-lookup"><span data-stu-id="e8880-163">**boolean**</span></span>

<span data-ttu-id="e8880-164">指出取得這個類別的實例是否為成本高昂的作業。</span><span class="sxs-lookup"><span data-stu-id="e8880-164">Indicates whether obtaining instances of this class is a costly operation.</span></span> <span data-ttu-id="e8880-165">對於在 \_ 類別名稱結尾附加「高成本」的類別，一律設定為 True。</span><span class="sxs-lookup"><span data-stu-id="e8880-165">Always set to **True** for classes with "\_Costly" appended to the end of the class name.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="e8880-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-167">**uint32**</span><span class="sxs-lookup"><span data-stu-id="e8880-167">**uint32**</span></span>

<span data-ttu-id="e8880-168">不提供詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e8880-168">Does not provide detail data.</span></span> <span data-ttu-id="e8880-169">一律包含100的值。</span><span class="sxs-lookup"><span data-stu-id="e8880-169">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="e8880-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-171">**boolean**</span><span class="sxs-lookup"><span data-stu-id="e8880-171">**boolean**</span></span>

<span data-ttu-id="e8880-172">值一律為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e8880-172">Value is always **False**.</span></span>

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="e8880-173">格式化效能類別的限定詞</span><span class="sxs-lookup"><span data-stu-id="e8880-173">Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="e8880-174">下列限定詞適用于所有衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的類別。</span><span class="sxs-lookup"><span data-stu-id="e8880-174">The following qualifiers apply to all classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="e8880-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**</span><span class="sxs-lookup"><span data-stu-id="e8880-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-176">**int32**</span><span class="sxs-lookup"><span data-stu-id="e8880-176">**int32**</span></span>

<span data-ttu-id="e8880-177">指出類別實例中的值會自動從對應的原始資料類別計算。</span><span class="sxs-lookup"><span data-stu-id="e8880-177">Indicates that the values in class instances are automatically calculated from the corresponding raw data class.</span></span> <span data-ttu-id="e8880-178">值一律為1。</span><span class="sxs-lookup"><span data-stu-id="e8880-178">Value is always 1.</span></span>

</dd> <dt>

<span data-ttu-id="e8880-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook \_ RawClass**</span><span class="sxs-lookup"><span data-stu-id="e8880-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook\_RawClass**</span></span>
</dt> <dd>

<span data-ttu-id="e8880-180">**string**</span><span class="sxs-lookup"><span data-stu-id="e8880-180">**string**</span></span>

<span data-ttu-id="e8880-181">用於計算格式化類別之原始類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8880-181">Name of the raw class to use for calculation for the formatted class.</span></span> <span data-ttu-id="e8880-182">這是必要的限定詞。</span><span class="sxs-lookup"><span data-stu-id="e8880-182">This qualifier is required.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="e8880-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8880-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8880-184">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="e8880-184">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="e8880-185">WMI 效能類別專用的限定詞</span><span class="sxs-lookup"><span data-stu-id="e8880-185">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="e8880-186">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="e8880-186">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="e8880-187">存取 WMI 預先安裝的效能類別</span><span class="sxs-lookup"><span data-stu-id="e8880-187">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="e8880-188">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="e8880-188">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
