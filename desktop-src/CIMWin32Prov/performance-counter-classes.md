---
description: 效能計數器類別可讓腳本和程式存取由現有高效能提供者計算的系統效能資料。
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: 效能計數器類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847605"
---
# <a name="performance-counter-classes"></a><span data-ttu-id="d4ba9-103">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="d4ba9-103">Performance Counter Classes</span></span>

<span data-ttu-id="d4ba9-104">效能計數器類別可讓腳本和程式存取由現有高效能提供者計算的系統效能資料。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-104">Performance Counter classes allow script and program access to system performance data calculated by existing high-performance providers.</span></span> <span data-ttu-id="d4ba9-105">這些類別是由原始效能計數器類別和格式化效能計數器類別所組成。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-105">These classes consist of raw performance counter classes and formatted performance counter classes.</span></span>

<span data-ttu-id="d4ba9-106">不同的提供者會透過 WMI 提供效能程式庫資料。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-106">Different providers supply performance library data through WMI.</span></span> <span data-ttu-id="d4ba9-107">[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)和[WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)提供者會提供第1版和第2版[效能計數器](/windows/desktop/PerfCtrs/performance-counters-portal)的類別。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-107">The [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) and [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) providers supply classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="d4ba9-108">這些提供者會維持與舊版作業系統中可用類別的相容性。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-108">These providers maintain compatibility with the classes available in earlier operating systems.</span></span>

<span data-ttu-id="d4ba9-109">此區段中的類別是用來建立效能計數器類別的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-109">The classes in this section are the abstract base classes used to create performance counter classes.</span></span> <span data-ttu-id="d4ba9-110">這不是您在作業系統上可能會發現的完整類別清單。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-110">This is not a complete list of classes that you may find on your operating system.</span></span> <span data-ttu-id="d4ba9-111">如需詳細資訊，請參閱 [效能程式庫和 WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-111">For more information, see [Performance Libraries and WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4ba9-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="d4ba9-112">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="d4ba9-113">**Win32 \_ 效能**</span><span class="sxs-lookup"><span data-stu-id="d4ba9-113">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dd>

<span data-ttu-id="d4ba9-114">效能計數器類別 [**Win32 \_ PerfRawData**](win32-perfrawdata.md) 和 [**win32 \_ PerfFormattedData**](win32-perfformatteddata.md)的基類。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-114">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

</dd> <dt>

[<span data-ttu-id="d4ba9-115">**Win32 \_ PerfFormattedData**</span><span class="sxs-lookup"><span data-stu-id="d4ba9-115">**Win32\_PerfFormattedData**</span></span>](win32-perfformatteddata.md)
</dt> <dd>

<span data-ttu-id="d4ba9-116">預先安裝的計算資料類別的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-116">an abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

[<span data-ttu-id="d4ba9-117">**Win32 \_ PerfRawData**</span><span class="sxs-lookup"><span data-stu-id="d4ba9-117">**Win32\_PerfRawData**</span></span>](win32-perfrawdata.md)
</dt> <dd>

<span data-ttu-id="d4ba9-118">所有具體原始效能計數器類別的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="d4ba9-118">The abstract base class for all concrete raw performance counter classes.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d4ba9-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4ba9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4ba9-120">Win32 類別</span><span class="sxs-lookup"><span data-stu-id="d4ba9-120">Win32 Classes</span></span>](win32-provider.md)
</dt> </dl>

 

 
