---
title: 開發與網路中的部署
description: 大部分的開發人員都是在快速可靠的 LAN 上撰寫和測試軟體。
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021324"
---
# <a name="development-vs-deployment-in-the-network"></a><span data-ttu-id="5c03d-103">開發與網路中的部署</span><span class="sxs-lookup"><span data-stu-id="5c03d-103">Development vs. Deployment in the Network</span></span>

<span data-ttu-id="5c03d-104">大部分的開發人員都是在快速可靠的 LAN 上撰寫和測試軟體。</span><span class="sxs-lookup"><span data-stu-id="5c03d-104">Most developers write and test their software on a fast reliable LAN.</span></span> <span data-ttu-id="5c03d-105">他們的用戶端和伺服器通常位於相同的網路區段。</span><span class="sxs-lookup"><span data-stu-id="5c03d-105">Their client and server are often on the same network segment.</span></span> <span data-ttu-id="5c03d-106">在這種情況下，網路幾乎沒有回應，而且連線很少會遺失。</span><span class="sxs-lookup"><span data-stu-id="5c03d-106">In such circumstances the network is rarely unresponsive, and connectivity rarely lost.</span></span> <span data-ttu-id="5c03d-107">不過，當部署在客戶環境中時，用戶端和伺服器通常位於不同的網路區段，可能位於遠端，而且伺服器會與其他用戶端高度載入。</span><span class="sxs-lookup"><span data-stu-id="5c03d-107">When deployed in a customer environment however, client and server are often on different network segments, possibly geographically remote, and the server is heavily loaded with other clients.</span></span> <span data-ttu-id="5c03d-108">換句話說：無法假設網路回應性。</span><span class="sxs-lookup"><span data-stu-id="5c03d-108">In other words: network responsiveness cannot be assumed.</span></span>

<span data-ttu-id="5c03d-109">本文說明如何在本質上不可靠的網路和可能無法使用的伺服器所引進的不確定性情況下，建立穩固的用戶端/伺服器架構。</span><span class="sxs-lookup"><span data-stu-id="5c03d-109">This article explains how to construct robust client/server architectures in the face of uncertainty introduced by an intrinsically unreliable network and potentially unavailable servers.</span></span>

 

 




