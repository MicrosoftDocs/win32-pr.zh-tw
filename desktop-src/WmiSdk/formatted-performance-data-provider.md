---
description: 提供計算 (&\# 0034; 處理後&\# 0034; ) 效能計數器資料。 提供動態資料給衍生自 Win32 PerfFormattedData 的 WMI 類別 \_ 。 也稱為處理後計數器提供者。
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: 格式化效能 Data Provider
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985635"
---
# <a name="formatted-performance-data-provider"></a><span data-ttu-id="3535a-105">格式化效能 Data Provider</span><span class="sxs-lookup"><span data-stu-id="3535a-105">Formatted Performance Data Provider</span></span>

<span data-ttu-id="3535a-106">\[格式化的效能 Data Provider （也稱為「處理後計數器提供者」）不再適用于使用。</span><span class="sxs-lookup"><span data-stu-id="3535a-106">\[The Formatted Performance Data Provider, also known as the "Cooked Counter Provider," is no longer available for use.</span></span> <span data-ttu-id="3535a-107">相反地，請使用 [WMIPerfInst](wmiperfinst-provider.md) 提供者。\]</span><span class="sxs-lookup"><span data-stu-id="3535a-107">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="3535a-108">高效能格式化的效能資料提供者提供計算 ( "處理後" ) 效能計數器資料，例如磁片花在寫入資料的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="3535a-108">The high-performance Formatted Performance Data provider supplies calculated ("cooked") performance counter data, such as the percentage of time a disk spends writing data.</span></span> <span data-ttu-id="3535a-109">此提供者會將動態資料提供給衍生自 [**Win32 \_ PERFFORMATTEDDATA**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="3535a-109">This provider supplies dynamic data to the WMI classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="3535a-110">此提供者和 [效能計數器提供者](performance-counter-provider.md) 之間的差異在於效能計數器提供者會提供原始資料，而處理後計數器提供者會提供與 [*系統監視器*](gloss-s.md)完全一樣的效能資料。</span><span class="sxs-lookup"><span data-stu-id="3535a-110">The difference between this provider and the [Performance Counter provider](performance-counter-provider.md) is that the Performance Counter provider supplies raw data and the Cooked Counter provider supplies performance data that appears exactly as in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="3535a-111">[**\_ \_ Win32Provider**](--win32provider.md)實例名稱為 "HiPerfCooker \_ v1"。</span><span class="sxs-lookup"><span data-stu-id="3535a-111">The [**\_\_Win32Provider**](--win32provider.md) instance name is "HiPerfCooker\_v1".</span></span>

<span data-ttu-id="3535a-112">計數器物件的 WMI 格式化類別名稱的格式為「Win32 \_ PerfFormattedData \_ *服務 \_ 名稱* \_ *物件 \_ 名稱*」。</span><span class="sxs-lookup"><span data-stu-id="3535a-112">The WMI formatted class name for a counter object is of the form "Win32\_PerfFormattedData\_*service\_name*\_*object\_name*".</span></span> <span data-ttu-id="3535a-113">例如，包含邏輯磁片計數器的 WMI 類別名稱是 **Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**。</span><span class="sxs-lookup"><span data-stu-id="3535a-113">For example, the WMI class name that contains the logical disk counters is **Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**.</span></span> <span data-ttu-id="3535a-114">這些類別位於「根 \\ CIMv2」命名空間中。</span><span class="sxs-lookup"><span data-stu-id="3535a-114">These classes are located in the "Root\\CIMv2" namespace.</span></span>

<span data-ttu-id="3535a-115">因為效能資料類別是在指定的系統上動態新增和修改，所以無法正式記錄所有已知效能物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="3535a-115">Because performance data classes are added and modified dynamically on a given system, it is not possible to formally document the properties of all known performance objects.</span></span> <span data-ttu-id="3535a-116">若要判斷哪些類別可供您使用，以及識別這些類別具有哪些成員，請參閱抓取 [原始和格式化效能資料物件的檔](retrieving-raw-and-formatted-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="3535a-116">To determine what classes are available to you, and to identify what members those classes have, see [Retrieving Documentation for Raw and Formatted Performance Data Objects](retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="3535a-117">[**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別會使用 [WMI 效能計數器類型](wmi-performance-counter-types.md)中的 **CookingType** 辨識符號來指定計算效能資料的公式。</span><span class="sxs-lookup"><span data-stu-id="3535a-117">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes use the **CookingType** qualifier in [WMI Performance Counter Types](wmi-performance-counter-types.md) to specify the formula for calculating performance data.</span></span> <span data-ttu-id="3535a-118">此辨識符號與 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中的 **CounterType** 限定詞相同。</span><span class="sxs-lookup"><span data-stu-id="3535a-118">This qualifier is the same as the **CounterType** qualifier in the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span>

<span data-ttu-id="3535a-119">作為高效能的提供者，處理後計數器提供者會實作為標準 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 方法和下列 [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) 方法：</span><span class="sxs-lookup"><span data-stu-id="3535a-119">As a high-performance provider, the Cooked Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="3535a-120">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="3535a-120">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="3535a-121">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="3535a-121">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="3535a-122">**CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="3535a-122">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="3535a-123">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="3535a-123">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="3535a-124">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="3535a-124">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="3535a-125">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="3535a-125">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="3535a-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="3535a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3535a-127">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="3535a-127">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
