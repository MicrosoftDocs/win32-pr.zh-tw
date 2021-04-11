---
description: 從 Windows Vista 開始，這個提供者會建立 WMI 效能計數器類別。
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: WmiPerfClass 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026850"
---
# <a name="wmiperfclass-provider"></a><span data-ttu-id="43867-103">WmiPerfClass 提供者</span><span class="sxs-lookup"><span data-stu-id="43867-103">WmiPerfClass Provider</span></span>

<span data-ttu-id="43867-104">從 Windows Vista 開始，這個提供者會建立 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。</span><span class="sxs-lookup"><span data-stu-id="43867-104">Starting with Windows Vista, this provider creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="43867-105">[WMIPerfInst](wmiperfinst-provider.md)提供者會動態提供這些 WMI 效能類別的資料。</span><span class="sxs-lookup"><span data-stu-id="43867-105">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst](wmiperfinst-provider.md) provider.</span></span> <span data-ttu-id="43867-106">自動探索/AutoPurge (ADAP) 進程不再將效能計數器物件傳輸至 WMI 儲存機制中的 WMI 效能類別。</span><span class="sxs-lookup"><span data-stu-id="43867-106">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="43867-107">如需詳細資訊，請參閱 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="43867-107">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="43867-108">如需詳細資訊，請參閱 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="43867-108">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="43867-109">雖然不建議您藉由建立 WMI 高效能提供者來開發新的效能物件，並相依于 [*ADAP 反向介面卡*](gloss-r.md) 程式以將資料傳輸至效能程式庫，但例外狀況是提供效能資料的 Windows Driver Model 驅動程式的開發。</span><span class="sxs-lookup"><span data-stu-id="43867-109">While it is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries, the exception is development of a Windows Driver Model driver that supplies performance data.</span></span> <span data-ttu-id="43867-110">雖然反向介面卡程式會繼續運作以提供回溯相容性，但建議的方法是使用 [效能計數器6.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="43867-110">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="43867-111">此提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例名稱為 "WmiPerfClass"。</span><span class="sxs-lookup"><span data-stu-id="43867-111">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfClass".</span></span>

## <a name="related-topics"></a><span data-ttu-id="43867-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="43867-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43867-113">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="43867-113">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="43867-114">效能程式庫和 WMI</span><span class="sxs-lookup"><span data-stu-id="43867-114">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="43867-115">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="43867-115">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
