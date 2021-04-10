---
title: 轉寄站
description: 轉寄站是路由器的核心模式元件，負責將資料從一個路由器介面轉送到其他路由器介面。
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021496"
---
# <a name="forwarder"></a><span data-ttu-id="0ae43-103">轉寄站</span><span class="sxs-lookup"><span data-stu-id="0ae43-103">Forwarder</span></span>

<span data-ttu-id="0ae43-104">轉寄站是路由器的核心模式元件，負責將資料從一個路由器介面轉送到其他路由器介面。</span><span class="sxs-lookup"><span data-stu-id="0ae43-104">The forwarder is the kernel-mode component of the router that is responsible for forwarding data from one router interface to the others.</span></span> <span data-ttu-id="0ae43-105">轉寄站也會決定封包是否以本機傳遞為目的地，無論是要將它從另一個介面（或兩者）轉寄。</span><span class="sxs-lookup"><span data-stu-id="0ae43-105">The forwarder also decides whether a packet is destined for local delivery, whether it is destined to be forwarded out of another interface, or both.</span></span>

<span data-ttu-id="0ae43-106">有兩個核心模式轉寄站：單點傳送和多播。</span><span class="sxs-lookup"><span data-stu-id="0ae43-106">There are two kernel-mode forwarders: unicast and multicast.</span></span>

<span data-ttu-id="0ae43-107">路由器管理員會從路由表管理員取得所有目的地的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="0ae43-107">The router manager obtains the best routes to all destinations from the routing table manager.</span></span> <span data-ttu-id="0ae43-108">這些路由會傳遞至單播轉寄站。</span><span class="sxs-lookup"><span data-stu-id="0ae43-108">These routes are passed to the unicast forwarder.</span></span> <span data-ttu-id="0ae43-109">單播轉寄站會使用這些路由來執行單播資料的實際轉送。</span><span class="sxs-lookup"><span data-stu-id="0ae43-109">The unicast forwarder uses these routes to perform the actual forwarding of unicast data.</span></span> <span data-ttu-id="0ae43-110">如此一來，單播轉寄站會在路由表的單點傳送視圖中維護最佳路由的快取。</span><span class="sxs-lookup"><span data-stu-id="0ae43-110">In this manner, the unicast forwarder maintains a cache of the best routes in the unicast view of the routing table.</span></span>

<span data-ttu-id="0ae43-111">多播群組管理員會使用路由表的多播視圖中的資訊，將多播轉送專案新增至多播轉寄站。</span><span class="sxs-lookup"><span data-stu-id="0ae43-111">The multicast group manager uses information from the multicast view of the routing table to add multicast forwarding entries to the multicast forwarder.</span></span>

 

 




