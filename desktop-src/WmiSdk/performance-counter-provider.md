---
description: 效能計數器提供者是一個高效能的提供者，可提供原始效能計數器資料給從 Win32 PerfRawData 衍生的 WMI 效能計數器類別 \_ 。 \_ \_ Win32Provider 實例名稱是 &\# 0034;NT5 \_ GenericPerfProvider \_ V1&\# 0034;。
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: 效能計數器提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027437"
---
# <a name="performance-counter-provider"></a><span data-ttu-id="d0744-104">效能計數器提供者</span><span class="sxs-lookup"><span data-stu-id="d0744-104">Performance Counter Provider</span></span>

<span data-ttu-id="d0744-105">\[效能計數器提供者不再可供使用。</span><span class="sxs-lookup"><span data-stu-id="d0744-105">\[The Performance Counter Provider is no longer available for use.</span></span> <span data-ttu-id="d0744-106">相反地，請使用 [WMIPerfInst](wmiperfinst-provider.md) 提供者。\]</span><span class="sxs-lookup"><span data-stu-id="d0744-106">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="d0744-107">效能計數器提供者是一個高效能的提供者，可提供原始效能計數器資料給從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)衍生的 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。</span><span class="sxs-lookup"><span data-stu-id="d0744-107">The Performance Counter provider is a high-performance provider that provides raw performance counter data to the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="d0744-108">[**\_ \_ Win32Provider**](--win32provider.md)實例名稱為 "NT5 \_ GenericPerfProvider \_ V1"。</span><span class="sxs-lookup"><span data-stu-id="d0744-108">The [**\_\_Win32Provider**](--win32provider.md) instance name is "NT5\_GenericPerfProvider\_V1".</span></span>

<span data-ttu-id="d0744-109">[**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別位於 WMI "Root \\ CIMv2" 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="d0744-109">The [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes are located in the WMI "Root\\CIMv2" namespace.</span></span> <span data-ttu-id="d0744-110">每個 WMI 效能類別都會對應到效能程式庫中的效能物件。</span><span class="sxs-lookup"><span data-stu-id="d0744-110">Each WMI performance class corresponds to a performance object in a performance library.</span></span> <span data-ttu-id="d0744-111">這些類別的屬性代表物件的計數器。</span><span class="sxs-lookup"><span data-stu-id="d0744-111">The properties of these classes represent the counters for the object.</span></span> <span data-ttu-id="d0744-112">原始計數器物件的 WMI 類別名稱的格式為 \**Win32 \_ \_ \_ PerfRawData* 服務 \_ 名稱 *\_* 物件 \_ 名稱 \* \* \*。</span><span class="sxs-lookup"><span data-stu-id="d0744-112">The WMI class name for a raw counter object is of the form \**Win32\_PerfRawData\_\_* service\_name *\_* object\_name\*\*\*.</span></span> <span data-ttu-id="d0744-113">例如，包含邏輯磁片計數器的 WMI 類別名稱是 [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="d0744-113">For example, the WMI class name that contains the logical disk counters is [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="d0744-114">您可以使用對應的 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 類別，來取得 [*系統監視器*](gloss-s.md)中顯示的預先計算效能資料。</span><span class="sxs-lookup"><span data-stu-id="d0744-114">You can use the corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class to get the pre-calculated performance data shown in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="d0744-115">例如，使用 [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) 類別取得預先計算的磁片資料。</span><span class="sxs-lookup"><span data-stu-id="d0744-115">For example, use the [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class to get pre-calculated disk data.</span></span>

<span data-ttu-id="d0744-116">如需如何撰寫可存取原始效能資料之用戶端的詳細資訊，請參閱使用 [c + + 存取效能資料](accessing-performance-data-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="d0744-116">For more information about how to write a client that can access raw performance data, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

<span data-ttu-id="d0744-117">效能計數器提供者是一個高效能的提供者，它會實作為標準 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 方法和下列 [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) 方法：</span><span class="sxs-lookup"><span data-stu-id="d0744-117">As a high-performance provider, the Performance Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="d0744-118">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="d0744-118">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="d0744-119">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="d0744-119">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="d0744-120">**CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="d0744-120">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="d0744-121">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="d0744-121">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="d0744-122">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="d0744-122">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="d0744-123">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="d0744-123">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="d0744-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0744-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0744-125">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="d0744-125">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
