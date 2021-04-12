---
description: 數個網路環境會影響應用程式的網路行為。
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: 不同的網路環境
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104195695"
---
# <a name="different-network-environments"></a><span data-ttu-id="dc87c-103">不同的網路環境</span><span class="sxs-lookup"><span data-stu-id="dc87c-103">Different Network Environments</span></span>

<span data-ttu-id="dc87c-104">數個網路環境會影響應用程式的網路行為。</span><span class="sxs-lookup"><span data-stu-id="dc87c-104">Several network environments affect the networked behavior of an application.</span></span> <span data-ttu-id="dc87c-105">區分網路環境的屬性包括低和高頻寬，以及低和高 RTT。</span><span class="sxs-lookup"><span data-stu-id="dc87c-105">Properties that differentiate network environments include low versus high bandwidth, and low versus high RTT.</span></span> <span data-ttu-id="dc87c-106">網路環境會以不同的方式影響交易式和串流處理應用程式。</span><span class="sxs-lookup"><span data-stu-id="dc87c-106">Network environments affect transactional and streaming applications in different ways.</span></span> <span data-ttu-id="dc87c-107">交易式應用程式對 RTT 而言更為敏感;串流應用程式對頻寬延遲產品而言更加敏感。</span><span class="sxs-lookup"><span data-stu-id="dc87c-107">Transactional applications are more sensitive to RTT; streaming applications are more sensitive to bandwidth-delay products.</span></span>

![此圖顯示不同的網路環境如何影響應用程式的網路行為。](images/hperf-1.png)

<span data-ttu-id="dc87c-109">撥號網路和某些無線網路具有變數 RTT。</span><span class="sxs-lookup"><span data-stu-id="dc87c-109">Dial-up networks and some wireless networks have a variable RTT.</span></span> <span data-ttu-id="dc87c-110">衛星網路的上游和下游之間通常會有非對稱的頻寬。</span><span class="sxs-lookup"><span data-stu-id="dc87c-110">Satellite networks generally have an asymmetric bandwidth between upstream and downstream.</span></span> <span data-ttu-id="dc87c-111">無線區域網路和 xDSL 是一個很好的網路範例，其頻寬延遲產品類似于快速乙太網路。</span><span class="sxs-lookup"><span data-stu-id="dc87c-111">Wireless LAN and xDSL are good examples of networks with bandwidth-delay products similar to that of Fast Ethernet.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc87c-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc87c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc87c-113">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="dc87c-113">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="dc87c-114">效能維度</span><span class="sxs-lookup"><span data-stu-id="dc87c-114">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



