---
description: Hyper-v 的 WMI 提供者可讓開發人員和腳本撰寫人員快速建立虛擬化平臺的自訂工具、公用程式和增強功能。 WMI 介面可以管理 Hyper-v 服務的所有層面。
ms.assetid: 773BB141-7B9C-4015-81A0-BD17B8233CCD
title: 關於 Hyper-v WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c30b329f7e8a3fd3ae65b49f8467a8f712707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974456"
---
# <a name="about-the-hyper-v-wmi-provider"></a><span data-ttu-id="a7551-104">關於 Hyper-v WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="a7551-104">About the Hyper-V WMI provider</span></span>

<span data-ttu-id="a7551-105">Hyper-v 的 WMI 提供者可讓開發人員和腳本撰寫人員快速建立虛擬化平臺的自訂工具、公用程式和增強功能。</span><span class="sxs-lookup"><span data-stu-id="a7551-105">The WMI provider for Hyper-V enable developers, and scripters, to quickly build custom tools, utilities, and enhancements for the virtualization platform.</span></span> <span data-ttu-id="a7551-106">WMI 介面可以管理 Hyper-v 服務的所有層面。</span><span class="sxs-lookup"><span data-stu-id="a7551-106">The WMI interfaces can manage all aspects of the Hyper-V services.</span></span>

## <a name="about-microsoft-windows-server-2008-r2-hyper-v"></a><span data-ttu-id="a7551-107">關於 Microsoft Windows Server 2008 R2 Hyper-v</span><span class="sxs-lookup"><span data-stu-id="a7551-107">About Microsoft Windows Server 2008 R2 Hyper-V</span></span>

<span data-ttu-id="a7551-108">Microsoft Windows Server 2008 R2 Hyper-v 可讓系統管理員將個別的硬體伺服器合併到執行 Microsoft Windows Server 2008 R2 作為主機作業系統的單一伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a7551-108">Microsoft Windows Server 2008 R2 Hyper-V allows system administrators to consolidate separate hardware servers on to a single server running Microsoft Windows Server 2008 R2 as the host operating system.</span></span>

<span data-ttu-id="a7551-109">每個裝載的虛擬機器都會在其各自獨立且獨立的虛擬環境中執行。</span><span class="sxs-lookup"><span data-stu-id="a7551-109">Each of the hosted virtual machines runs in its own separate and isolated virtual environment.</span></span> <span data-ttu-id="a7551-110">這可讓系統管理員輕鬆地管理、提供及維護大量的虛擬機器，同時減少執行多個硬體解決方案以使用各種產品和作業系統的需求。</span><span class="sxs-lookup"><span data-stu-id="a7551-110">This allows the administrator to easily manage, provide for, and maintain large numbers of virtual machines while reducing the need to run multiple hardware solutions to use various products and operating systems.</span></span>

<span data-ttu-id="a7551-111">虛擬機器環境的另一個優點是測試和支援。</span><span class="sxs-lookup"><span data-stu-id="a7551-111">Another advantage of the virtual machine environment is in test and support.</span></span> <span data-ttu-id="a7551-112">新的伺服器和系統設定可以與現有的系統平行部署及測試，而不需要在首度發行階段產生昂貴的停機時間。</span><span class="sxs-lookup"><span data-stu-id="a7551-112">New server and system configurations can be deployed and tested in parallel with the existing system without requiring costly downtime during the rollout phase.</span></span> <span data-ttu-id="a7551-113">每部虛擬機器都可以設定成在標準平臺上執行時使用不同的設定，以產生更好的測試結果。</span><span class="sxs-lookup"><span data-stu-id="a7551-113">Each virtual machine can be setup to use varying configurations while running on a standard platform to produce better test results.</span></span> <span data-ttu-id="a7551-114">支援舊版的作業系統，可支援和測試舊版硬體、系統和應用程式。</span><span class="sxs-lookup"><span data-stu-id="a7551-114">With support for earlier operating systems, one can support and test legacy hardware, systems and applications.</span></span> <span data-ttu-id="a7551-115">快照集支援可讓您建立虛擬機器狀態的快照，讓您可以視需要返回先前的事件。</span><span class="sxs-lookup"><span data-stu-id="a7551-115">Snapshot support allows you to take a snapshot of a virtual machine's state so you can return to a prior event if needed.</span></span>

<span data-ttu-id="a7551-116">Hyper-v 公開豐富的介面，可讓使用者監視及控制虛擬機器環境。</span><span class="sxs-lookup"><span data-stu-id="a7551-116">Hyper-V exposes a rich interface which permits the user to monitor and control the virtual machine environment.</span></span> <span data-ttu-id="a7551-117">大部分的 Hyper-v 都可以使用 WMI 提供者來控制，而這種方式可讓您輕鬆又強大地自訂虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a7551-117">Most of Hyper-V can be controlled by using the WMI provider, which allows easy, yet powerful customization of the virtual machines.</span></span> <span data-ttu-id="a7551-118">如需可使用 WMI 提供者控制哪些內容的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="a7551-118">For more information about what can be controlled with the WMI provider, see the following topics:</span></span>

-   [<span data-ttu-id="a7551-119">虛擬系統管理服務</span><span class="sxs-lookup"><span data-stu-id="a7551-119">Virtual system management service</span></span>](virtual-system-management-service.md)
-   [<span data-ttu-id="a7551-120">網路服務</span><span class="sxs-lookup"><span data-stu-id="a7551-120">Networking service</span></span>](networking-service.md)
-   [<span data-ttu-id="a7551-121">資源管理服務</span><span class="sxs-lookup"><span data-stu-id="a7551-121">Resource management service</span></span>](resource-management-service.md)
-   [<span data-ttu-id="a7551-122">Hyper-v WMI 提供者的新功能</span><span class="sxs-lookup"><span data-stu-id="a7551-122">What's new in Hyper-V WMI provider</span></span>](what-s-new-in-hyper-v.md)

 

 



