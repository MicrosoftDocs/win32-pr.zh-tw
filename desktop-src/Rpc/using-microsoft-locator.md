---
title: 使用 Microsoft 定位器
description: Microsoft 定位器是預設的名稱服務。 RPC 執行時間程式庫會使用它來尋找伺服器主機系統上的伺服器程式。
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- 使用 Microsoft 定位器的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840020"
---
# <a name="using-microsoft-locator"></a><span data-ttu-id="bbd6b-105">使用 Microsoft 定位器</span><span class="sxs-lookup"><span data-stu-id="bbd6b-105">Using Microsoft Locator</span></span>

<span data-ttu-id="bbd6b-106">Microsoft 定位器是預設的名稱服務。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-106">Microsoft Locator is the default name service.</span></span> <span data-ttu-id="bbd6b-107">RPC 執行時間程式庫會使用它來尋找伺服器主機系統上的伺服器程式。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-107">The RPC run-time library uses it to find server programs on server host systems.</span></span>

<span data-ttu-id="bbd6b-108">**注意**   Windows Vista 和更新版本的作業系統不支援 Microsoft RPC 定位器。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-108">**Note**  Microsoft RPC locator is not supported in Windows Vista and later operating systems.</span></span>

<span data-ttu-id="bbd6b-109">在 Windows 2000 之前，Microsoft 定位器未提供持續性的名稱服務專案。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-109">Prior to Windows 2000, Microsoft Locator did not provide persistent name service entries.</span></span> <span data-ttu-id="bbd6b-110">名稱服務中的所有專案都儲存在伺服器程式的主機電腦上的記憶體快取中。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-110">All entries in the name service were stored in a memory cache on the server program's host computer.</span></span> <span data-ttu-id="bbd6b-111">定位器使用廣播機制來探索用戶端所要求的伺服器位置。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-111">The locator used a broadcast mechanism to discover the location of servers as requested by clients.</span></span> <span data-ttu-id="bbd6b-112">當主機系統關機時，所有名稱服務專案都會遺失。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-112">Whenever the host system shut down, all name service entries were lost.</span></span>

<span data-ttu-id="bbd6b-113">從 Windows 2000 版開始，Microsoft 定位器現在支援持續性名稱服務專案。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-113">Beginning with the release of Windows 2000, Microsoft Locator now supports persistent name service entries.</span></span> <span data-ttu-id="bbd6b-114">為了達成此目的，系統採用分散式目錄服務來儲存名稱服務專案。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-114">To accomplish this, the system employs a distributed directory service to store name service entries.</span></span> <span data-ttu-id="bbd6b-115">這項機制有幾個優點：</span><span class="sxs-lookup"><span data-stu-id="bbd6b-115">This mechanism has several advantages:</span></span>

-   <span data-ttu-id="bbd6b-116">**堅持。**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-116">**Persistence.**</span></span> <span data-ttu-id="bbd6b-117">伺服器程式在每次啟動時，都不再需要將其系結資訊匯出至名稱服務。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-117">Server programs are no longer required to export their binding information to the name service each time they start up.</span></span> <span data-ttu-id="bbd6b-118">名稱服務現在會儲存資訊，直到網路系統管理員上的伺服器程式明確移除該資訊為止。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-118">The name service now stores the information until the server program on the network administrator explicitly removes it.</span></span>
-   <span data-ttu-id="bbd6b-119">**效率。**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-119">**Efficiency.**</span></span> <span data-ttu-id="bbd6b-120">藉由排除名稱服務專案的大部分廣播，定位器可減少網路流量。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-120">By eliminating the majority of broadcasting for name service entries, the locator reduces network traffic.</span></span> <span data-ttu-id="bbd6b-121">它也能更快速地找到名稱服務專案。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-121">It also finds name service entries more rapidly.</span></span>
-   <span data-ttu-id="bbd6b-122">**跨網域互通性。**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-122">**Cross-Domain Interoperability.**</span></span> <span data-ttu-id="bbd6b-123">用戶端現在可以跨多個網域提出名稱服務要求。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-123">Clients are now able to make name service requests across multiple domains.</span></span>

<span data-ttu-id="bbd6b-124">Microsoft 定位器的目前版本具有回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-124">Current versions of Microsoft Locator are backward compatible.</span></span> <span data-ttu-id="bbd6b-125">比方說，執行隨附于 Windows 2000 之定位器的伺服器主機系統可以在包含執行 Windows NT 4.0 隨附之定位器的伺服器主機系統的網路上正確運作。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-125">For instance, a server host system running the locator that ships with Windows 2000 can operate correctly on a network that contains server host systems running the locator that ships with Windows NT 4.0.</span></span>

<span data-ttu-id="bbd6b-126">在 Windows 2000 版中，Microsoft 定位程式現在支援使用者群組的名稱服務專案。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-126">With the release of Windows 2000, Microsoft Locator now supports name service entries for groups of users.</span></span> <span data-ttu-id="bbd6b-127">它也能讓您建立使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-127">It also provides the ability for you to create user profiles.</span></span>

<span data-ttu-id="bbd6b-128">此外，目前版本的 Microsoft 定位器支援在名稱服務專案中使用存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-128">In addition, the current version of Microsoft Locator supports the use of Access Control Lists in name service entries.</span></span> <span data-ttu-id="bbd6b-129">這項功能可增強網路的安全性。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-129">This ability enhances the security of the network.</span></span>

<span data-ttu-id="bbd6b-130">Microsoft 定位器現在已包含隨插即用支援。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-130">Plug and Play support is now included in Microsoft Locator.</span></span> <span data-ttu-id="bbd6b-131">因此，它可以透明地處理隨插即用事件，例如網域變更。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-131">Therefore, it can transparently handle Plug and Play events such as domain changes.</span></span> <span data-ttu-id="bbd6b-132">如需詳細資訊，請參閱 [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) 和 [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa)。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-132">For more information, see [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) and [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span></span>

 

 




