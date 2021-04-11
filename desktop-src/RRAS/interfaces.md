---
title: RAS 介面
description: 介面代表可透過 LAN 或 WAN 介面卡連線的網路。
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841720"
---
# <a name="ras-interfaces"></a><span data-ttu-id="eb9c9-103">RAS 介面</span><span class="sxs-lookup"><span data-stu-id="eb9c9-103">RAS interfaces</span></span>

<span data-ttu-id="eb9c9-104">介面代表可透過 LAN 或 WAN 介面卡連線的網路。</span><span class="sxs-lookup"><span data-stu-id="eb9c9-104">An interface represents a network that can be reached over a LAN or WAN adapter.</span></span> <span data-ttu-id="eb9c9-105">每個介面在路由器上都有唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb9c9-105">Each interface has a unique identifier on the router.</span></span> <span data-ttu-id="eb9c9-106">作用中的介面有一個介面卡，可提供其所代表網路的連線能力。</span><span class="sxs-lookup"><span data-stu-id="eb9c9-106">Interfaces that are active have an adapter that is providing connectivity to the network they represent.</span></span> <span data-ttu-id="eb9c9-107">非使用中的介面沒有提供連線能力的介面卡，除非系統管理員在介面已經有介面卡之後停用該介面。</span><span class="sxs-lookup"><span data-stu-id="eb9c9-107">Interfaces that are inactive do not have an adapter providing connectivity, unless an administrator disabled the interface after it already had an adapter.</span></span>

<span data-ttu-id="eb9c9-108">將封包路由傳送至由介面表示的網路時，會導致路由器配置該介面的介面卡，並建立與遠端網路的 WAN 連線。</span><span class="sxs-lookup"><span data-stu-id="eb9c9-108">Routing a packet to a network represented by an interface will cause the router to allocate an adapter for that interface, and establish a WAN connection to the remote network.</span></span> <span data-ttu-id="eb9c9-109">將介面卡配置給介面，稱為「系結」（ *binding*）。</span><span class="sxs-lookup"><span data-stu-id="eb9c9-109">Allocating an adapter to an interface is referred to as *binding*.</span></span>

<span data-ttu-id="eb9c9-110">介面是可管理的物件。</span><span class="sxs-lookup"><span data-stu-id="eb9c9-110">Interfaces are manageable objects.</span></span> <span data-ttu-id="eb9c9-111">每個介面在適當 SNMP MIB 的介面表中會顯示為數據列。</span><span class="sxs-lookup"><span data-stu-id="eb9c9-111">Each interface appears as a row in the Interface Table of the appropriate SNMP MIB.</span></span>