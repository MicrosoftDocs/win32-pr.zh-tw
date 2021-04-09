---
description: 以字母 N 開頭網路監視器詞彙的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: 'N (網路監視器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850903"
---
# <a name="n-network-monitor"></a><span data-ttu-id="57a8e-103">N (網路監視器) </span><span class="sxs-lookup"><span data-stu-id="57a8e-103">N (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="57a8e-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**Ndis**</span><span class="sxs-lookup"><span data-stu-id="57a8e-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span></span>
</dt> <dd>

<span data-ttu-id="57a8e-105">請參閱網路驅動程式介面規格。</span><span class="sxs-lookup"><span data-stu-id="57a8e-105">See network driver interface specification.</span></span>

</dd> <dt>

<span data-ttu-id="57a8e-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**(NDIS) 的網路驅動程式介面規格**</span><span class="sxs-lookup"><span data-stu-id="57a8e-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**network driver interface specification (NDIS)**</span></span>
</dt> <dd>

<span data-ttu-id="57a8e-107">設備磁碟機和網路之間介面的規格。</span><span class="sxs-lookup"><span data-stu-id="57a8e-107">The specification for the interface between device drivers and a network.</span></span> <span data-ttu-id="57a8e-108">所有傳輸都會呼叫 NDIS 介面來存取和使用網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="57a8e-108">All transports call the NDIS interface to access and work with network interface cards.</span></span>

</dd> <dt>

<span data-ttu-id="57a8e-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**網路監視器代理程式**</span><span class="sxs-lookup"><span data-stu-id="57a8e-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Network Monitor agent**</span></span>
</dt> <dd>

<span data-ttu-id="57a8e-110">網路監視器元件。</span><span class="sxs-lookup"><span data-stu-id="57a8e-110">A Network Monitor component.</span></span> <span data-ttu-id="57a8e-111">代理程式可讓遠端電腦從網路中捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="57a8e-111">The agent enables a remote computer to capture data from the network.</span></span> <span data-ttu-id="57a8e-112">當網路監視器安裝從遠端連線到網路監視器代理程式並起始捕獲時，來自 capture 的統計資料會透過網路傳送到管理的電腦。</span><span class="sxs-lookup"><span data-stu-id="57a8e-112">When a Network Monitor installation connects remotely to the Network Monitor agent and initiates a capture, statistics from the capture are transferred over the network to the managing computer.</span></span> <span data-ttu-id="57a8e-113">傳輸會依建立連接時所指定的間隔進行。</span><span class="sxs-lookup"><span data-stu-id="57a8e-113">The transfer proceeds at intervals specified when the connection is made.</span></span>

</dd> <dt>

<span data-ttu-id="57a8e-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**網路封包提供者 (NPP)**</span><span class="sxs-lookup"><span data-stu-id="57a8e-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**network packet provider (NPP)**</span></span>
</dt> <dd>

<span data-ttu-id="57a8e-115">網路監視器元件會收集畫面中的網路流量，然後將框架傳遞給專家，並 NPP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="57a8e-115">The Network Monitor component that collects network traffic in frames, and then passes the frames to an expert, and NPP application.</span></span> <span data-ttu-id="57a8e-116">NPP 使用網路監視器系統驅動程式 (Nmnt.sys) 來取得從網路收集的畫面格，並提供數個 COM 介面，可將框架傳遞給專家、監視器和網路封包提供者， (NPP) 應用程式可以顯示和分析。</span><span class="sxs-lookup"><span data-stu-id="57a8e-116">An NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network, and provides several COM interfaces that pass the frames to an expert, monitor, and network packet provider (NPP) application where they can be displayed and analyzed.</span></span>

</dd> <dt>

<span data-ttu-id="57a8e-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**核電站**</span><span class="sxs-lookup"><span data-stu-id="57a8e-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span></span>
</dt> <dd>

<span data-ttu-id="57a8e-118">請參閱網路封包提供者。</span><span class="sxs-lookup"><span data-stu-id="57a8e-118">See network packet provider.</span></span>

</dd> <dt>

<span data-ttu-id="57a8e-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP 應用程式**</span><span class="sxs-lookup"><span data-stu-id="57a8e-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP application**</span></span>
</dt> <dd>

<span data-ttu-id="57a8e-120">一種應用程式，它會略過網路監視器 UI 和監視器控制工具，並直接連接到網路封包提供者 (NPP) 。</span><span class="sxs-lookup"><span data-stu-id="57a8e-120">An application that bypasses both the Network Monitor UI and Monitor Control Tool, and connects directly to the network packet provider (NPP).</span></span> <span data-ttu-id="57a8e-121">NPP 應用程式可以使用五個 NPP COM 介面的任一個連接到 NPP 元件。</span><span class="sxs-lookup"><span data-stu-id="57a8e-121">An NPP application can connect to the NPP component with any of the five NPP COM interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="57a8e-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**</span><span class="sxs-lookup"><span data-stu-id="57a8e-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**</span></span>
</dt> <dd>

<span data-ttu-id="57a8e-123">與 NPPs 通訊的網路監視器元件。</span><span class="sxs-lookup"><span data-stu-id="57a8e-123">The Network Monitor component that communicates with NPPs.</span></span>

</dd> </dl>

 

 



