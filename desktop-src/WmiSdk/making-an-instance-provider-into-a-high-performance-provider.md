---
description: 不建議寫入 WMI 高效能提供者來建立效能計數器。
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: 讓執行個體提供者成為 High-Performance 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985659"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a><span data-ttu-id="eb67c-103">讓執行個體提供者成為 High-Performance 提供者</span><span class="sxs-lookup"><span data-stu-id="eb67c-103">Making an Instance Provider into a High-Performance Provider</span></span>

<span data-ttu-id="eb67c-104">不建議寫入 WMI 高效能提供者來建立效能計數器。</span><span class="sxs-lookup"><span data-stu-id="eb67c-104">Writing a WMI high-performance provider to create performance counters is not recommended.</span></span> <span data-ttu-id="eb67c-105">從 Windows Vista 開始，自動探索/AutoPurge (ADAP) 反向介面卡，不再將 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 遷移至 Windows 效能程式庫中。</span><span class="sxs-lookup"><span data-stu-id="eb67c-105">Starting with Windows Vista, the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) are no longer migrated into the Windows performance libraries by the AutoDiscovery/AutoPurge (ADAP) reverse adapter.</span></span> <span data-ttu-id="eb67c-106">若要建立效能計數器提供者，請使用 [效能計數器2.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="eb67c-106">To create a performance counter provider, use [Performance Counters Version 2.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="eb67c-107">建立效能程式庫物件之後， [WMIPerfClass 提供者](wmiperfclass-provider.md) 會剖析物件，並為每個效能物件建立或重新整理衍生自 [**WIN32 \_ performance 的**](/windows/desktop/CIMWin32Prov/win32-perf) WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="eb67c-107">After performance library objects are created, the [WMIPerfClass Provider](wmiperfclass-provider.md) parses the objects and creates or refreshes a WMI class derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) for each performance object.</span></span> <span data-ttu-id="eb67c-108">然後， [WMIPerfInst 提供者](wmiperfinst-provider.md) 會動態地將原始和格式化的效能計數器資料提供給 WMI 效能類別。</span><span class="sxs-lookup"><span data-stu-id="eb67c-108">The [WMIPerfInst Provider](wmiperfinst-provider.md) then dynamically provides raw and formatted performance counter data to the WMI performance classes.</span></span>

<span data-ttu-id="eb67c-109">下列高階程式提供建立高效能提供者所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="eb67c-109">The following high-level procedure provides the steps required to create a high-performance provider.</span></span>

<span data-ttu-id="eb67c-110">**若要建立高效能提供者**</span><span class="sxs-lookup"><span data-stu-id="eb67c-110">**To create a high-performance provider**</span></span>

1.  <span data-ttu-id="eb67c-111">向 WMI 註冊您的提供者。</span><span class="sxs-lookup"><span data-stu-id="eb67c-111">Register your provider with WMI.</span></span> <span data-ttu-id="eb67c-112">如需詳細資訊，請參閱 [註冊 High-Performance 提供者](registering-a-high-performance-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="eb67c-112">For more information, see [Registering a High-Performance Provider](registering-a-high-performance-provider.md).</span></span>
2.  <span data-ttu-id="eb67c-113">執行您的提供者。</span><span class="sxs-lookup"><span data-stu-id="eb67c-113">Implement your provider.</span></span> <span data-ttu-id="eb67c-114">如需詳細資訊，請參閱 [撰寫執行個體提供者](writing-an-instance-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="eb67c-114">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>
3.  <span data-ttu-id="eb67c-115">執行高效能介面。</span><span class="sxs-lookup"><span data-stu-id="eb67c-115">Implement the high-performance interface.</span></span> <span data-ttu-id="eb67c-116">如需詳細資訊，請參閱 [執行 High-Performance 介面](implementing-the-high-performance-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="eb67c-116">For more information, see [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).</span></span>
4.  <span data-ttu-id="eb67c-117">受控物件格式 (MOF) 架構中衍生並撰寫您的，以取得原始效能資料。</span><span class="sxs-lookup"><span data-stu-id="eb67c-117">Derive and write your Managed Object Format (MOF) schema to obtain raw performance data.</span></span> <span data-ttu-id="eb67c-118">如需詳細資訊，請參閱 [支援 Win32 \_ PerfRawData 類別](supporting-the-win32-perfrawdata-class.md)。</span><span class="sxs-lookup"><span data-stu-id="eb67c-118">For more information, see [Supporting the Win32\_PerfRawData Class](supporting-the-win32-perfrawdata-class.md).</span></span>
5.  <span data-ttu-id="eb67c-119">衍生並撰寫您的 MOF 架構，以取得預先計算的資料。</span><span class="sxs-lookup"><span data-stu-id="eb67c-119">Derive and write your MOF schema to obtain precalculated data.</span></span> <span data-ttu-id="eb67c-120">藉由支援這個類別，就不需要提供者來執行計算。</span><span class="sxs-lookup"><span data-stu-id="eb67c-120">By supporting this class, the provider is not required to perform the calculations.</span></span> <span data-ttu-id="eb67c-121">這項資料會與在 Perfmon 中的系統監視器中顯示的資料相同。</span><span class="sxs-lookup"><span data-stu-id="eb67c-121">This data will be the same that appears in the System Monitor in Perfmon.</span></span> <span data-ttu-id="eb67c-122">如需詳細資訊，請參閱 [支援 Win32 \_ PerfFormattedData 類別](supporting-the-win32-perfformatteddata-class.md)。</span><span class="sxs-lookup"><span data-stu-id="eb67c-122">For more information, see [Supporting the Win32\_PerfFormattedData Class](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb67c-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb67c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb67c-124">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="eb67c-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="eb67c-125">效能程式庫和 WMI</span><span class="sxs-lookup"><span data-stu-id="eb67c-125">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
