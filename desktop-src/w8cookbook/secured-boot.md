---
title: 早期啟動反惡意程式碼
description: 早期啟動反惡意程式碼
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104027618"
---
# <a name="early-launch-antimalware"></a><span data-ttu-id="b0067-103">早期啟動反惡意程式碼</span><span class="sxs-lookup"><span data-stu-id="b0067-103">Early launch antimalware</span></span>

## <a name="platforms"></a><span data-ttu-id="b0067-104">平台</span><span class="sxs-lookup"><span data-stu-id="b0067-104">Platforms</span></span>

 <span data-ttu-id="b0067-105">**客戶** 端-Windows 8</span><span class="sxs-lookup"><span data-stu-id="b0067-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="b0067-106">**伺服器** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0067-106">**Servers** - Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="b0067-107">Description</span><span class="sxs-lookup"><span data-stu-id="b0067-107">Description</span></span>

<span data-ttu-id="b0067-108">由於反惡意程式碼 (AM) 軟體在偵測到執行時間惡意程式碼時變得更好且更好，攻擊者也會在建立可隱藏偵測的 rootkit 時變得更好。</span><span class="sxs-lookup"><span data-stu-id="b0067-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="b0067-109">偵測開機週期初期啟動的惡意程式碼，是大部分的廠商都能處理的挑戰。</span><span class="sxs-lookup"><span data-stu-id="b0067-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="b0067-110">一般情況下，它們會建立主機作業系統不支援的系統駭客，而且實際上會導致電腦處於不穩定的狀態。</span><span class="sxs-lookup"><span data-stu-id="b0067-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="b0067-111">到目前為止，Windows 尚未提供良好的方式來偵測並解決這些早期開機的威脅。</span><span class="sxs-lookup"><span data-stu-id="b0067-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span>

<span data-ttu-id="b0067-112">Windows 8 引進稱為「安全開機」的新功能，可保護 Windows 開機設定和元件，並載入早期啟動的反惡意程式碼 (ELAM) 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b0067-112">Windows 8 introduces a new feature called Secure Boot, which protects the Windows boot configuration and components, and loads an Early Launch Anti-malware (ELAM) driver.</span></span> <span data-ttu-id="b0067-113">此驅動程式會在其他開機啟動驅動程式之前啟動，並可讓您評估這些驅動程式，並協助 Windows 核心決定是否應該將它們初始化。</span><span class="sxs-lookup"><span data-stu-id="b0067-113">This driver starts before other boot-start drivers and enables the evaluation of those drivers and helps the Windows kernel decide whether they should be initialized.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b0067-114">表現</span><span class="sxs-lookup"><span data-stu-id="b0067-114">Manifestation</span></span>

<span data-ttu-id="b0067-115">藉由核心先啟動，ELAM 可確保在任何協力廠商軟體之前啟動，因此能夠偵測開機程式中的惡意程式碼，並防止它初始化。</span><span class="sxs-lookup"><span data-stu-id="b0067-115">By being launched first by the kernel, ELAM is ensured to be launched before any third-party software, and is therefore able to detect malware in the boot process and prevent it from initializing.</span></span>

## <a name="mitigation"></a><span data-ttu-id="b0067-116">降低</span><span class="sxs-lookup"><span data-stu-id="b0067-116">Mitigation</span></span>

<span data-ttu-id="b0067-117">開機驅動程式會根據根據初始化原則從 ELAM 驅動程式傳回的分類進行初始化。</span><span class="sxs-lookup"><span data-stu-id="b0067-117">Boot drivers are initialized based on the classification that is returned from the ELAM driver according to an initialization policy.</span></span> <span data-ttu-id="b0067-118">依預設，此原則會初始化已知的良好和未知驅動程式，但不會初始化已知的不良驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b0067-118">By default, the policy initializes known good and unknown drivers, but will not initialize known bad drivers.</span></span> <span data-ttu-id="b0067-119">系統管理員可以透過群組原則來指定自訂原則，以防止未知的驅動程式初始化，或可啟用開機程式不可或缺的驅動程式，但已遭篡改、開機以進行初始化。</span><span class="sxs-lookup"><span data-stu-id="b0067-119">A system administrator can specify a custom policy through Group Policy that can prevent unknown drivers from initializing or can enable drivers that are critical to the boot process, but have been tampered with, boot to be initialized.</span></span>

## <a name="solution"></a><span data-ttu-id="b0067-120">解決方法</span><span class="sxs-lookup"><span data-stu-id="b0067-120">Solution</span></span>

<span data-ttu-id="b0067-121">ELAM 驅動程式必須註冊核心回呼，以取得每個開機啟動驅動程式初始化時的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b0067-121">An ELAM driver must register for kernel callbacks to get info about each boot-start driver as it is initializing.</span></span> <span data-ttu-id="b0067-122">然後，ELAM 驅動程式就可以針對每個驅動程式傳回分類。</span><span class="sxs-lookup"><span data-stu-id="b0067-122">The ELAM driver can then return a classification for each driver.</span></span> <span data-ttu-id="b0067-123">這些是必要的功能：</span><span class="sxs-lookup"><span data-stu-id="b0067-123">These functions are required:</span></span>

-   [<span data-ttu-id="b0067-124">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="b0067-124">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="b0067-125">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="b0067-125">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

<span data-ttu-id="b0067-126">ELAM 驅動程式也可以註冊登錄回呼。</span><span class="sxs-lookup"><span data-stu-id="b0067-126">An ELAM driver can also register for registry callbacks.</span></span> <span data-ttu-id="b0067-127">這麼做可讓 ELAM 驅動程式檢查每個開機啟動驅動程式所使用的設定資料。</span><span class="sxs-lookup"><span data-stu-id="b0067-127">Doing so enables the ELAM driver to inspect the configuration data that is used by each boot-start driver.</span></span> <span data-ttu-id="b0067-128">然後，ELAM 驅動程式就可以在開機啟動驅動程式使用之前，先封鎖或修改資料（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="b0067-128">The ELAM driver can then block or modify the data before it is used by the boot-start drivers, if necessary.</span></span> <span data-ttu-id="b0067-129">這些是必要的功能：</span><span class="sxs-lookup"><span data-stu-id="b0067-129">These functions are required:</span></span>

-   [<span data-ttu-id="b0067-130">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="b0067-130">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="b0067-131">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="b0067-131">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

<span data-ttu-id="b0067-132">如需 ELAM 驅動程式需求和 API 使用方式的詳細資訊，請參閱 [早期啟動反惡意](/windows-hardware/drivers/install/early-launch-antimalware)代碼。</span><span class="sxs-lookup"><span data-stu-id="b0067-132">For more details about ELAM driver requirements and API usage, see [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).</span></span>

## <a name="tests"></a><span data-ttu-id="b0067-133">測試</span><span class="sxs-lookup"><span data-stu-id="b0067-133">Tests</span></span>

<span data-ttu-id="b0067-134">ELAM 驅動程式必須由 Microsoft 特別簽署，以確保在開機過程中，Windows 核心會儘早啟動這些驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b0067-134">ELAM drivers must be specially signed by Microsoft to ensure they are started by the Windows kernel early in the boot process.</span></span> <span data-ttu-id="b0067-135">若要取得簽章，ELAM 驅動程式必須通過一組認證測試，以驗證效能和其他行為。</span><span class="sxs-lookup"><span data-stu-id="b0067-135">To get the signature, ELAM drivers must pass a set of certification tests to verify performance and other behavior.</span></span> <span data-ttu-id="b0067-136">這些測試都包含在 Windows 硬體認證套件中。</span><span class="sxs-lookup"><span data-stu-id="b0067-136">These tests are included in the Windows Hardware Certification Kit.</span></span>

## <a name="resources"></a><span data-ttu-id="b0067-137">資源</span><span class="sxs-lookup"><span data-stu-id="b0067-137">Resources</span></span>

-   [<span data-ttu-id="b0067-138">早期啟動反惡意程式碼</span><span class="sxs-lookup"><span data-stu-id="b0067-138">Early Launch Antimalware</span></span>](/windows-hardware/drivers/install/early-launch-antimalware)
-   [<span data-ttu-id="b0067-139">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="b0067-139">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="b0067-140">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="b0067-140">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [<span data-ttu-id="b0067-141">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="b0067-141">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="b0067-142">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="b0067-142">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [<span data-ttu-id="b0067-143">使用 Windows 硬體認證套件組建會議簡報來認證硬體</span><span class="sxs-lookup"><span data-stu-id="b0067-143">Certifying hardware with the Windows Hardware Certification Kit Build Conference presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [<span data-ttu-id="b0067-144">下載套件和工具</span><span class="sxs-lookup"><span data-stu-id="b0067-144">Download Kits and Tools</span></span>](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
