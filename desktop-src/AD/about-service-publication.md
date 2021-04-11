---
title: 關於服務發行
description: 服務是讓網路用戶端可以使用資料或作業的應用程式。 服務通常會實作為正式的 Microsoft Win32 型服務，但這不是必要的。
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34c1f0955f45f1bd4c689455ac03e79d987480
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931794"
---
# <a name="about-service-publication"></a><span data-ttu-id="869cf-104">關於服務發行</span><span class="sxs-lookup"><span data-stu-id="869cf-104">About Service Publication</span></span>

<span data-ttu-id="869cf-105">服務是讓網路用戶端可以使用資料或作業的應用程式。</span><span class="sxs-lookup"><span data-stu-id="869cf-105">A service is an application that makes data or operations available to network clients.</span></span> <span data-ttu-id="869cf-106">服務通常會實作為正式的 Microsoft Win32 型服務，但這不是必要的。</span><span class="sxs-lookup"><span data-stu-id="869cf-106">Often, a service is implemented as a formal Microsoft Win32-based service, but this is not required.</span></span>

<span data-ttu-id="869cf-107">服務發行集是建立和維護指定服務的一或多個實例之相關資料的動作，讓網路用戶端可以尋找及使用服務。</span><span class="sxs-lookup"><span data-stu-id="869cf-107">Service publication is the act of creating and maintaining data about one or more instances of a given service so that network clients can find and use the service.</span></span> <span data-ttu-id="869cf-108">在 Active Directory Domain Services 中發佈服務，可讓用戶端和系統管理員從以電腦為中心的分散式系統觀點移至以服務為中心的觀點。</span><span class="sxs-lookup"><span data-stu-id="869cf-108">Publishing a service in Active Directory Domain Services enables clients and administrators to move from a computer-centric view of the distributed system to a service-centric view.</span></span>

<span data-ttu-id="869cf-109">**Microsoft Windows NT 3.51 和更新版本的作業系統：** 分散式系統是一組執行各種服務的電腦。</span><span class="sxs-lookup"><span data-stu-id="869cf-109">**Microsoft Windows NT 3.51 and later operating systems:** A distributed system was a group of computers running various services.</span></span> <span data-ttu-id="869cf-110">若要存取服務，應用程式需要有哪些電腦提供服務的相關資料。</span><span class="sxs-lookup"><span data-stu-id="869cf-110">To access a service, an application required data about which computers offered the service.</span></span>

<span data-ttu-id="869cf-111">**Windows 2000 Server、windows 2000 Advanced Server 和 Windows 2000 Datacenter Server：** 服務會使用 Active Directory Domain Services 物件來發佈其存在。</span><span class="sxs-lookup"><span data-stu-id="869cf-111">**Windows 2000 Server, Windows 2000 Advanced Server and Windows 2000 Datacenter Server:** Services publish their existence using Active Directory Domain Services objects.</span></span> <span data-ttu-id="869cf-112">這些物件包含用戶端應用程式用來連接到服務實例的系結資訊。</span><span class="sxs-lookup"><span data-stu-id="869cf-112">The objects contain binding information that client applications use to connect to instances of the service.</span></span> <span data-ttu-id="869cf-113">若要存取服務，用戶端不需要知道特定電腦： Active Directory 伺服器中的物件包含這項資訊。</span><span class="sxs-lookup"><span data-stu-id="869cf-113">To access a service, a client does not need to know about specific computers: the objects in an Active Directory server include this information.</span></span> <span data-ttu-id="869cf-114">用戶端會向 Active Directory 伺服器查詢代表服務的物件 (稱為連接點物件) 並使用來自物件的系結資料來連接至服務。</span><span class="sxs-lookup"><span data-stu-id="869cf-114">A client queries the Active Directory server for an object representing a service (called a connection point object) and uses the binding data from the object to connect to the service.</span></span>

<span data-ttu-id="869cf-115">下表顯示系結的範例。</span><span class="sxs-lookup"><span data-stu-id="869cf-115">The following table shows examples of bindings.</span></span>



| <span data-ttu-id="869cf-116">服務</span><span class="sxs-lookup"><span data-stu-id="869cf-116">Service</span></span>      | <span data-ttu-id="869cf-117">繫結</span><span class="sxs-lookup"><span data-stu-id="869cf-117">Binding</span></span>                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="869cf-118">檔案服務</span><span class="sxs-lookup"><span data-stu-id="869cf-118">File Service</span></span> | <span data-ttu-id="869cf-119">共用的 UNC 名稱。</span><span class="sxs-lookup"><span data-stu-id="869cf-119">UNC Name for a share.</span></span> <span data-ttu-id="869cf-120">例如 " \\ \\ MyServer \\ MyshareName"。</span><span class="sxs-lookup"><span data-stu-id="869cf-120">For example "\\\\MyServer\\MyshareName".</span></span>                                                                                                                                                              |
| <span data-ttu-id="869cf-121">Web 服務</span><span class="sxs-lookup"><span data-stu-id="869cf-121">Web Service</span></span>  | <span data-ttu-id="869cf-122">Url。</span><span class="sxs-lookup"><span data-stu-id="869cf-122">URL.</span></span> <span data-ttu-id="869cf-123">例如 " https://www.fabrikam.com "。</span><span class="sxs-lookup"><span data-stu-id="869cf-123">For example "https://www.fabrikam.com".</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="869cf-124">RPC 服務</span><span class="sxs-lookup"><span data-stu-id="869cf-124">RPC Service</span></span>  | <span data-ttu-id="869cf-125">遠端程序呼叫 (RPC) 系結：用來連接到 RPC 伺服器的特殊編碼資訊。</span><span class="sxs-lookup"><span data-stu-id="869cf-125">Remote procedure call (RPC) binding: special encoded information used to connect to the RPC server.</span></span> <span data-ttu-id="869cf-126">RPC 系結可以使用 RPC Api 在字串之間來回轉換。</span><span class="sxs-lookup"><span data-stu-id="869cf-126">RPC bindings can be converted to and from strings with the RPC APIs.</span></span> <span data-ttu-id="869cf-127">例如： "ncacn \_ ip \_ tcp:server]。</span><span class="sxs-lookup"><span data-stu-id="869cf-127">For example: "ncacn\_ip\_tcp:server.fabrikam.com".</span></span> |



 

<span data-ttu-id="869cf-128">在分散式系統中，電腦是引擎，而有趣的實體就是可用的服務。</span><span class="sxs-lookup"><span data-stu-id="869cf-128">In a distributed system, the computers are engines, and the interesting entities are the services that are available.</span></span> <span data-ttu-id="869cf-129">從使用者的觀點來看，提供特定服務的電腦身分識別並不重要。</span><span class="sxs-lookup"><span data-stu-id="869cf-129">From the user perspective, the identity of the computer that provides a particular service is not important.</span></span> <span data-ttu-id="869cf-130">存取服務本身是很重要的。</span><span class="sxs-lookup"><span data-stu-id="869cf-130">What is important is accessing the service itself.</span></span>

<span data-ttu-id="869cf-131">這也是服務管理的情況。</span><span class="sxs-lookup"><span data-stu-id="869cf-131">This is also the case with service management.</span></span> <span data-ttu-id="869cf-132">指定 DNS 區域的系統管理員對執行 DNS 服務的電腦不感興趣;系統管理員想要管理 DNS。</span><span class="sxs-lookup"><span data-stu-id="869cf-132">The administrator of a given DNS zone is not interested in the computers running the DNS service; the administrator wants to administer DNS.</span></span> <span data-ttu-id="869cf-133">DNS 服務可能會有多個實例，其中一個是授權的。</span><span class="sxs-lookup"><span data-stu-id="869cf-133">There will likely be multiple instances of the DNS service, one of which is authoritative.</span></span> <span data-ttu-id="869cf-134">支援 DNS 服務的電腦對 DNS 系統管理員而言並不重要。</span><span class="sxs-lookup"><span data-stu-id="869cf-134">The computers that support DNS service are not important to the DNS administrator.</span></span> <span data-ttu-id="869cf-135">重要的是如何將服務當作單一分散式資源來管理，而不是在不同電腦上執行的個別進程。</span><span class="sxs-lookup"><span data-stu-id="869cf-135">What is important is how to manage the service as a single distributed resource—not as individual processes running on different computers.</span></span>

 

 




