---
description: WMIPerfClass 提供者和 WMIPerfInst 提供者會動態提供 WMI 效能計數器類別的效能計數器資料。
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: 效能程式庫和 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979032"
---
# <a name="performance-libraries-and-wmi"></a><span data-ttu-id="19f16-103">效能程式庫和 WMI</span><span class="sxs-lookup"><span data-stu-id="19f16-103">Performance Libraries and WMI</span></span>

<span data-ttu-id="19f16-104">[WMIPerfClass 提供者](wmiperfclass-provider.md)和[WMIPerfInst 提供者](wmiperfinst-provider.md)會動態提供 WMI[效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)的效能計數器資料。</span><span class="sxs-lookup"><span data-stu-id="19f16-104">The [WMIPerfClass Provider](wmiperfclass-provider.md) and the [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provide performance counter data for the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span>

## <a name="wmiperfclass-and-wmiperfinst-providers"></a><span data-ttu-id="19f16-105">WMIPerfClass 和 WMIPerfInst 提供者</span><span class="sxs-lookup"><span data-stu-id="19f16-105">WMIPerfClass and WMIPerfInst Providers</span></span>

<span data-ttu-id="19f16-106">[WMIPerfClass 提供者](wmiperfclass-provider.md) 會在系統初始化時建立 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 。</span><span class="sxs-lookup"><span data-stu-id="19f16-106">[WMIPerfClass Provider](wmiperfclass-provider.md) creates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) at system initialization.</span></span> <span data-ttu-id="19f16-107">[WMIPerfInst 提供者](wmiperfinst-provider.md)會動態提供這些類別的效能計數器資料。</span><span class="sxs-lookup"><span data-stu-id="19f16-107">The [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provides performance counter data for these classes.</span></span> <span data-ttu-id="19f16-108">WMIPerfClass 提供者提供者會提供第1版和第2版 [效能計數器](/windows/desktop/PerfCtrs/performance-counters-portal)的類別。</span><span class="sxs-lookup"><span data-stu-id="19f16-108">The WMIPerfClass Provider provider supplies classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="19f16-109">第1版計數器可在登錄的 **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services** 下找到。</span><span class="sxs-lookup"><span data-stu-id="19f16-109">Version 1 counters are found in the registry under **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services**.</span></span> <span data-ttu-id="19f16-110">提供效能資料的服務具有 **效能** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="19f16-110">Services that provide performance data have a **Performance** subkey.</span></span> <span data-ttu-id="19f16-111">從第1版計數器建立的 WMI 效能類別沒有「計數器」作為其名稱的一部分。</span><span class="sxs-lookup"><span data-stu-id="19f16-111">WMI performance classes created from version 1 counters do not have "Counters" as part of their name.</span></span>

<span data-ttu-id="19f16-112">在登錄中的 [ **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**] 下找到識別第2版效能計數器提供者的 **GUID**。</span><span class="sxs-lookup"><span data-stu-id="19f16-112">The **GUID** s identifying a version 2 performance counter provider are found in the registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib\\\_V2Providers**.</span></span>

<span data-ttu-id="19f16-113">WMIPerfClass 會註冊為一般 WMI 類別提供者。</span><span class="sxs-lookup"><span data-stu-id="19f16-113">WMIPerfClass is registered as a normal WMI class provider.</span></span> <span data-ttu-id="19f16-114">WMIPerfInst 是一種 WMI 執行個體提供者，可為第1版和第2版計數器的效能資料協助程式 (PDH) 提供資料。</span><span class="sxs-lookup"><span data-stu-id="19f16-114">WMIPerfInst is a WMI instance provider that supplies data from Performance Data Helper (PDH) for both version 1 and version 2 counters.</span></span> <span data-ttu-id="19f16-115">如需詳細資訊，請參閱 [使用 PDH 函數來使用計數器資料](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)。</span><span class="sxs-lookup"><span data-stu-id="19f16-115">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19f16-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="19f16-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19f16-117">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="19f16-117">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="19f16-118">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="19f16-118">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
