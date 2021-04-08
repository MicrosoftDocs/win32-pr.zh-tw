---
description: 網路封包提供者 (NPPs) 是網路監視器系統元件，可從網路收集網路流量 (框架) ，然後將這些流量傳遞至網路監視器 UI，以及 NPP 應用程式。
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: 網路封包提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852708"
---
# <a name="network-packet-providers"></a><span data-ttu-id="7bde6-103">網路封包提供者</span><span class="sxs-lookup"><span data-stu-id="7bde6-103">Network Packet Providers</span></span>

<span data-ttu-id="7bde6-104">網路封包提供者 (NPPs) 是網路監視器系統元件，可從網路收集網路流量 (框架) ，然後將這些流量傳遞至網路監視器 UI，以及 [*NPP 應用程式*](n.md)。</span><span class="sxs-lookup"><span data-stu-id="7bde6-104">Network packet providers (NPPs) are Network Monitor system components that collect network traffic (frames) from the network and pass them on to the Network Monitor UI, and [*NPP applications*](n.md).</span></span>

<span data-ttu-id="7bde6-105">下圖顯示兩個 NPPs：網路監視器提供的 NDIS NPP 和自訂 NPP。</span><span class="sxs-lookup"><span data-stu-id="7bde6-105">The following illustration shows two NPPs: the NDIS NPP provided by Network Monitor and a custom NPP.</span></span>

![網路監視器和自訂 npp 所提供的 ndis npp](images/npp.png)

<span data-ttu-id="7bde6-107">網路監視器所提供的 NDIS NPP 是 Ndisnpp.dll。</span><span class="sxs-lookup"><span data-stu-id="7bde6-107">The NDIS NPP provided by Network Monitor is Ndisnpp.dll.</span></span> <span data-ttu-id="7bde6-108">此 NPP 使用網路監視器系統驅動程式 (Nmnt.sys) 來取得從網路收集的畫面格，以及數個 COM 介面 (稱為 NPP 介面) 將框架傳遞至網路監視器 UI，以及 NPP 應用程式，可在其中顯示和分析這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="7bde6-108">This NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network and several COM interfaces (referred to as the NPP interfaces) to pass the frames on to the Network Monitor UI, and NPP applications, where they can be displayed and analyzed.</span></span>

<span data-ttu-id="7bde6-109">Ndisnpp.dll 會連接到 [*NDIS*](n.md) 層以取得其網路流量。</span><span class="sxs-lookup"><span data-stu-id="7bde6-109">Ndisnpp.dll connects to the [*NDIS*](n.md) layer to obtain its network traffic.</span></span> <span data-ttu-id="7bde6-110"> (的自訂 NPPs 可以略過 NDIS 層，並直接與網路硬體通訊。 ) 請注意，不論 NPP 是否使用 NDIS，NPPs 都可以連線到任意數目的網路卡，而且所有 NPPs 都必須支援相同的 NPP 介面。</span><span class="sxs-lookup"><span data-stu-id="7bde6-110">(Custom NPPs can bypass the NDIS layer and communicate directly with the networking hardware.) Be aware that regardless of whether an NPP uses NDIS, NPPs can connect to any number of network cards and that all NPPs must support the same NPP interfaces.</span></span>

<span data-ttu-id="7bde6-111">在應用程式開始捕獲資料之前，必須先：</span><span class="sxs-lookup"><span data-stu-id="7bde6-111">Before an application can start to capture data, it must:</span></span>

-   <span data-ttu-id="7bde6-112">選取將 NPP 連接到網路的網路介面卡 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="7bde6-112">Select the network interface card (NIC) that will connect the NPP to the network.</span></span>
-   <span data-ttu-id="7bde6-113">選取將用來捕捉網路框架的 NPP 介面。</span><span class="sxs-lookup"><span data-stu-id="7bde6-113">Select the NPP interface that will be used to capture the network frames.</span></span>
-   <span data-ttu-id="7bde6-114">使用選取的介面連接至 NIC。</span><span class="sxs-lookup"><span data-stu-id="7bde6-114">Use the selected interface to connect to the NIC.</span></span>

<span data-ttu-id="7bde6-115">如需有關如何列舉和選取網路介面卡的詳細資訊，請參閱 [選取網路介面卡](selecting-a-network-interface-card.md)。</span><span class="sxs-lookup"><span data-stu-id="7bde6-115">For more information about how to enumerate and select a network interface card, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md).</span></span>

<span data-ttu-id="7bde6-116">如需 NPPs 所公開的 COM 介面的詳細資訊，請參閱 [選取 NPP 介面](selecting-an-npp-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="7bde6-116">For more information about COM interfaces exposed by NPPs, see [Selecting an NPP Interface](selecting-an-npp-interface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bde6-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bde6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bde6-118">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="7bde6-118">**IDelaydC**</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="7bde6-119">**IESP**</span><span class="sxs-lookup"><span data-stu-id="7bde6-119">**IESP**</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="7bde6-120">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="7bde6-120">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="7bde6-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="7bde6-121">**IStats**</span></span>](istats.md)
</dt> </dl>

 

 



