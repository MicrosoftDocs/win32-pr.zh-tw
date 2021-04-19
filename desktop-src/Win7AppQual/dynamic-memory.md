---
description: .
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: 動態記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1e868a89714a7f6f1d77f9416515897876c150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988441"
---
# <a name="dynamic-memory"></a><span data-ttu-id="4574b-103">動態記憶體</span><span class="sxs-lookup"><span data-stu-id="4574b-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4574b-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="4574b-104">Affected Platforms</span></span>

<span data-ttu-id="4574b-105">**用戶端 () 的虛擬機器** 執行-windows Vista \| windows 7</span><span class="sxs-lookup"><span data-stu-id="4574b-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="4574b-106">**伺服器** -Windows Server 2008 R2 hyper-v SP1</span><span class="sxs-lookup"><span data-stu-id="4574b-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="4574b-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="4574b-107">Feature Impact</span></span>

 <span data-ttu-id="4574b-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="4574b-108">**Severity** - Low</span></span>  
<span data-ttu-id="4574b-109">**頻率** -高</span><span class="sxs-lookup"><span data-stu-id="4574b-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="4574b-110">Description</span><span class="sxs-lookup"><span data-stu-id="4574b-110">Description</span></span>

<span data-ttu-id="4574b-111">概括而言，Hyper-v 動態記憶體是 Windows Server 2008 R2 SP1 內含之 Hyper-v 角色的記憶體管理增強功能。</span><span class="sxs-lookup"><span data-stu-id="4574b-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="4574b-112">它是專為生產環境使用而設計，可讓客戶達到更高的匯總/虛擬機器 (VM) 密度比例，同時優化實體機器中的記憶體使用率。</span><span class="sxs-lookup"><span data-stu-id="4574b-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="4574b-113">系統會減少靜態記憶體配置，並視需要配置額外的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4574b-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="4574b-114">動態記憶體會影響需要確保其軟體在虛擬機器環境中正常運作的軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="4574b-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="4574b-115">使用案例</span><span class="sxs-lookup"><span data-stu-id="4574b-115">Usage Scenario</span></span>

<span data-ttu-id="4574b-116">有兩個主要的使用案例，其中動態記憶體進入 play、主機端應用程式和來賓端應用程式。</span><span class="sxs-lookup"><span data-stu-id="4574b-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="4574b-117">**主機端應用程式 (管理工具)**</span><span class="sxs-lookup"><span data-stu-id="4574b-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="4574b-118">管理新的 Windows Server 2008 R2 SP1 伺服器的舊版工具將無法存取新的動態記憶體設定。</span><span class="sxs-lookup"><span data-stu-id="4574b-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="4574b-119">已開發新的 WMI Api 和效能計數器，以管理 Hyper-v 虛擬機器的新動態記憶體設定。</span><span class="sxs-lookup"><span data-stu-id="4574b-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="4574b-120">處理管理工具的軟體發展人員應該利用這些 Api 和計數器，以搭配已安裝 Hyper-v 角色的 Windows Server 2008 R2 SP1 使用。</span><span class="sxs-lookup"><span data-stu-id="4574b-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="4574b-121">有關這些新 Api 的詳細資料，可透過 [MSDN 上的 HYPER-V WMI 提供者檔](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)取得。</span><span class="sxs-lookup"><span data-stu-id="4574b-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="4574b-122">**來賓端應用程式**</span><span class="sxs-lookup"><span data-stu-id="4574b-122">**Guest-side applications**</span></span>

<span data-ttu-id="4574b-123">撰寫要在設定為使用動態記憶體的虛擬機器中使用的軟體的開發人員必須記住，VM 系統記憶體不再是固定的。</span><span class="sxs-lookup"><span data-stu-id="4574b-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="4574b-124">因此，其應用程式應該在不再需要時釋放記憶體，讓其他應用程式能夠利用資源。</span><span class="sxs-lookup"><span data-stu-id="4574b-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="4574b-125">在使用者應用程式中，記憶體配置和取消配置仍會持續正常運作。</span><span class="sxs-lookup"><span data-stu-id="4574b-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="4574b-126">動態記憶體對大部分的終端使用者應用程式而言都是完全透明的。</span><span class="sxs-lookup"><span data-stu-id="4574b-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="4574b-127">但是，如果所開發的軟體會使用虛擬機器中的記憶體效能計數器，則應該在啟用動態記憶體的環境中執行測試，以確保軟體會將對客體作業系統記憶體配置所做的變更納入考慮。</span><span class="sxs-lookup"><span data-stu-id="4574b-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="4574b-128">從虛擬機器的觀點來看，可用記憶體不再是「靜態」。</span><span class="sxs-lookup"><span data-stu-id="4574b-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="4574b-129">方案</span><span class="sxs-lookup"><span data-stu-id="4574b-129">Solutions</span></span>

<span data-ttu-id="4574b-130">虛擬機器必須安裝更新的 integration services (SP1) ，才能利用動態記憶體。</span><span class="sxs-lookup"><span data-stu-id="4574b-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="4574b-131">確定 Hyper-v 虛擬機器管理中使用的所有電腦都使用最新的 Windows Server 2008 R2 SP1 位。</span><span class="sxs-lookup"><span data-stu-id="4574b-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="4574b-132">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="4574b-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="4574b-133">動態記憶體進入 Hyper-v 的 blog</span><span class="sxs-lookup"><span data-stu-id="4574b-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="4574b-134">使用 Hyper-v WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="4574b-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="4574b-135">免責聲明</span><span class="sxs-lookup"><span data-stu-id="4574b-135">Disclaimer</span></span>

<span data-ttu-id="4574b-136">本檔中包含的資訊與搶鮮版軟體產品相關，該產品可能會在其第一個商業發行之前經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="4574b-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="4574b-137">因此，在第一次正式發行時，資訊可能無法正確描述或反映軟體產品。</span><span class="sxs-lookup"><span data-stu-id="4574b-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="4574b-138">此文件僅供參考之用。</span><span class="sxs-lookup"><span data-stu-id="4574b-138">This document is for informational purposes only.</span></span> <span data-ttu-id="4574b-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="4574b-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 
