---
description: 以下是使用 IP 協助程式開發介面 (API) 來開始進行程式設計的逐步指南。 它的設計目的是要讓您瞭解基本 IP Helper 函式和資料結構，以及它們如何一起運作。
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: 使用 IP Helper 的開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852952"
---
# <a name="getting-started-with-ip-helper"></a><span data-ttu-id="79644-104">使用 IP Helper 的開始使用</span><span class="sxs-lookup"><span data-stu-id="79644-104">Getting Started with IP Helper</span></span>

<span data-ttu-id="79644-105">以下是使用 IP 協助程式開發介面 (API) 來開始進行程式設計的逐步指南。</span><span class="sxs-lookup"><span data-stu-id="79644-105">The following is a step-by-step guide to getting started programming using the IP Helper application programming interface (API).</span></span> <span data-ttu-id="79644-106">它的設計目的是要讓您瞭解基本 IP Helper 函式和資料結構，以及它們如何一起運作。</span><span class="sxs-lookup"><span data-stu-id="79644-106">It is designed to provide an understanding of basic IP Helper functions and data structures, and how they work together.</span></span>

<span data-ttu-id="79644-107">用於說明的應用程式是非常基本的 IP Helper 應用程式。</span><span class="sxs-lookup"><span data-stu-id="79644-107">The application that is used for illustration is a very basic IP Helper application.</span></span> <span data-ttu-id="79644-108">Microsoft Windows 軟體開發套件 (SDK) 隨附的範例包含更先進的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="79644-108">More advanced code examples are included in the samples included with the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="79644-109">大部分 IP 協助程式應用程式的第一個步驟都是相同的。</span><span class="sxs-lookup"><span data-stu-id="79644-109">The first step is the same for most IP Helper applications.</span></span>

-   [<span data-ttu-id="79644-110">建立基本 IP 協助程式應用程式</span><span class="sxs-lookup"><span data-stu-id="79644-110">Creating a Basic IP Helper Application</span></span>](creating-a-basic-ip-helper-application.md)

<span data-ttu-id="79644-111">下列各節說明建立此基本 IP 協助程式應用程式的其餘步驟。</span><span class="sxs-lookup"><span data-stu-id="79644-111">The following sections describe the remaining steps for creating this basic IP Helper application.</span></span>

-   [<span data-ttu-id="79644-112">使用 GetNetworkParams 抓取資訊</span><span class="sxs-lookup"><span data-stu-id="79644-112">Retrieving Information Using GetNetworkParams</span></span>](retrieving-information-using-getnetworkparams.md)
-   [<span data-ttu-id="79644-113">使用 GetAdaptersInfo 管理網路介面卡</span><span class="sxs-lookup"><span data-stu-id="79644-113">Managing Network Adapters Using GetAdaptersInfo</span></span>](managing-network-adapters-using-getadaptersinfo.md)
-   [<span data-ttu-id="79644-114">使用 GetInterfaceInfo 管理介面</span><span class="sxs-lookup"><span data-stu-id="79644-114">Managing Interfaces Using GetInterfaceInfo</span></span>](managing-interfaces-using-getinterfaceinfo.md)
-   [<span data-ttu-id="79644-115">使用 GetIpAddrTable 管理 IP 位址</span><span class="sxs-lookup"><span data-stu-id="79644-115">Managing IP Addresses Using GetIpAddrTable</span></span>](managing-ip-addresses-using-getipaddrtable.md)
-   [<span data-ttu-id="79644-116">使用 IpReleaseAddress 和 IpRenewAddress 管理 DHCP 租用</span><span class="sxs-lookup"><span data-stu-id="79644-116">Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress</span></span>](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [<span data-ttu-id="79644-117">使用 AddIPAddress 和 DeleteIPAddress 管理 IP 位址</span><span class="sxs-lookup"><span data-stu-id="79644-117">Managing IP Addresses Using AddIPAddress and DeleteIPAddress</span></span>](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [<span data-ttu-id="79644-118">使用 GetIpStatistics 抓取資訊</span><span class="sxs-lookup"><span data-stu-id="79644-118">Retrieving Information Using GetIpStatistics</span></span>](retrieving-information-using-getipstatistics.md)
-   [<span data-ttu-id="79644-119">使用 GetTcpStatistics 抓取資訊</span><span class="sxs-lookup"><span data-stu-id="79644-119">Retrieving Information Using GetTcpStatistics</span></span>](retrieving-information-using-gettcpstatistics.md)

<span data-ttu-id="79644-120">此基本 IP Helper 範例的完整原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="79644-120">The complete source code for this basic IP Helper example.</span></span>

-   [<span data-ttu-id="79644-121">完整 IP 協助程式的原始程式碼</span><span class="sxs-lookup"><span data-stu-id="79644-121">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a><span data-ttu-id="79644-122">Advanced IP Helper 範例</span><span class="sxs-lookup"><span data-stu-id="79644-122">Advanced IP Helper Samples</span></span>

<span data-ttu-id="79644-123">Microsoft Windows 軟體開發套件 (SDK) 包含數個更先進的 IP 協助程式範例。</span><span class="sxs-lookup"><span data-stu-id="79644-123">Several more advanced IP Helper samples are included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="79644-124">根據預設，IP 協助程式範例原始程式碼是由下列目錄中針對 Windows 7 發行的 Windows SDK 所安裝：</span><span class="sxs-lookup"><span data-stu-id="79644-124">By default, the IP Helper sample source code is installed by the Windows SDK released for Windows 7 in the following directory:</span></span>

<span data-ttu-id="79644-125">*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ NetDs \\ IPHelp*</span><span class="sxs-lookup"><span data-stu-id="79644-125">*C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\IPHelp*</span></span>

<span data-ttu-id="79644-126">以下是在下列目錄中找到的更先進範例：</span><span class="sxs-lookup"><span data-stu-id="79644-126">The more advanced samples listed below are found in the following directories:</span></span>

-   <span data-ttu-id="79644-127">EnableRouter</span><span class="sxs-lookup"><span data-stu-id="79644-127">EnableRouter</span></span>

    <span data-ttu-id="79644-128">此目錄包含的範例會示範如何使用 [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) 和 [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP 協助程式功能，在本機電腦上啟用和停用 IPv4 轉送。</span><span class="sxs-lookup"><span data-stu-id="79644-128">This directory contains a sample that demonstrates how to use the [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) and [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP Helper functions to enable and disable IPv4 forwarding on the local computer.</span></span>

-   <span data-ttu-id="79644-129">iparp</span><span class="sxs-lookup"><span data-stu-id="79644-129">iparp</span></span>

    <span data-ttu-id="79644-130">此目錄包含一個範例程式，示範如何使用 IP 協助程式函式，在本機電腦上顯示和操作 IPv4 ARP 資料表中的專案。</span><span class="sxs-lookup"><span data-stu-id="79644-130">This directory contains a sample program that demonstrates how to use the IP Helper functions to display and manipulate entries in the IPv4 ARP table on the local computer.</span></span>

-   <span data-ttu-id="79644-131">ipchange</span><span class="sxs-lookup"><span data-stu-id="79644-131">ipchange</span></span>

    <span data-ttu-id="79644-132">此目錄包含一個範例程式，示範如何使用 IP Helper 函式，以程式設計方式變更您電腦上特定網路介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="79644-132">This directory contains a sample program that demonstrates how to use IP Helper functions to programmatically change an IP address for a specific network adapter on your machine.</span></span> <span data-ttu-id="79644-133">此程式也會示範如何取出現有的網路介面卡 IP 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="79644-133">This program also demonstrates how to retrieve existing network adapter IP configuration information.</span></span>

-   <span data-ttu-id="79644-134">IPConfig</span><span class="sxs-lookup"><span data-stu-id="79644-134">IPConfig</span></span>

    <span data-ttu-id="79644-135">此目錄包含一個範例程式，示範如何以程式設計方式抓取類似 IPCONFIG.EXE 公用程式的 IPv4 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="79644-135">This directory contains a sample program that demonstrates how to programmatically retrieve IPv4 configuration information similar to the IPCONFIG.EXE utility.</span></span> <span data-ttu-id="79644-136">它會示範如何使用 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 和 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="79644-136">It demonstrates how to use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) and [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) functions.</span></span> <span data-ttu-id="79644-137">請注意， **GetAdaptersInfo** 函數只會取出 IPv4 資訊。</span><span class="sxs-lookup"><span data-stu-id="79644-137">Note that the **GetAdaptersInfo** function only retrieves IPv4 information.</span></span>

-   <span data-ttu-id="79644-138">IPRenew</span><span class="sxs-lookup"><span data-stu-id="79644-138">IPRenew</span></span>

    <span data-ttu-id="79644-139">此目錄包含一個範例程式，示範如何以程式設計方式釋放和更新透過 DHCP 取得的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="79644-139">This directory contains a sample program that demonstrates how to programmatically release and renew IPv4 addresses obtained through DHCP.</span></span> <span data-ttu-id="79644-140">此程式也會示範如何取出現有的網路介面卡設定資訊。</span><span class="sxs-lookup"><span data-stu-id="79644-140">This program also demonstrates how to retrieve existing network adapter configuration information.</span></span>

-   <span data-ttu-id="79644-141">IPRoute</span><span class="sxs-lookup"><span data-stu-id="79644-141">IPRoute</span></span>

    <span data-ttu-id="79644-142">此目錄包含一個範例程式，示範如何使用 IP Helper 函式來操作 IPv4 路由表。</span><span class="sxs-lookup"><span data-stu-id="79644-142">This directory contains a sample program that demonstrates how to use the IP Helper functions to manipulate the IPv4 routing table.</span></span>

-   <span data-ttu-id="79644-143">ipstat</span><span class="sxs-lookup"><span data-stu-id="79644-143">ipstat</span></span>

    <span data-ttu-id="79644-144">此目錄包含一個範例程式，示範如何使用 IP Helper 函式來顯示通訊協定的 IPv4 連線。</span><span class="sxs-lookup"><span data-stu-id="79644-144">This directory contains a sample program that demonstrates how to use the IP Helper functions to show IPv4 connections for a protocol.</span></span> <span data-ttu-id="79644-145">根據預設，會顯示 IP、ICMP、TCP 和 UDP 的統計資料。</span><span class="sxs-lookup"><span data-stu-id="79644-145">By default, statistics are shown for IP, ICMP, TCP and UDP.</span></span>

-   <span data-ttu-id="79644-146">Netinfo</span><span class="sxs-lookup"><span data-stu-id="79644-146">Netinfo</span></span>

    <span data-ttu-id="79644-147">此目錄包含一個範例程式，示範如何使用 Windows Vista 和更新版本上引進的新 IP 協助程式 Api 來顯示/變更 IPv4 和 IPv6 的位址和介面資訊。</span><span class="sxs-lookup"><span data-stu-id="79644-147">This directory contains a sample program that demonstrates how to the use the new IP Helper APIs introduced on Windows Vista and later to display/change address and interface information for IPv4 and IPv6.</span></span>

 

 



