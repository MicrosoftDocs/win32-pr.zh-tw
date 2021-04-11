---
description: 接收封裝 (通道) 封包，並將它們 demultiplexes 到特定介面的程式碼有一項限制。
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: IPv6 轉送通道封包
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848016"
---
# <a name="ipv6-forwarding-tunneled-packets"></a><span data-ttu-id="e7973-103">IPv6 轉送通道封包</span><span class="sxs-lookup"><span data-stu-id="e7973-103">IPv6 Forwarding Tunneled Packets</span></span>

<span data-ttu-id="e7973-104">接收封裝 (通道) 封包，並將它們 demultiplexes 到特定介面的程式碼有一項限制。</span><span class="sxs-lookup"><span data-stu-id="e7973-104">There is a limitation in the code that receives encapsulated (tunneled) packets and demultiplexes them to a specific interface.</span></span> <span data-ttu-id="e7973-105">如果您想要轉送透過已設定通道接收的通道封包，則必須在任何6個以上的介面和介面2上啟用轉送 \# 。</span><span class="sxs-lookup"><span data-stu-id="e7973-105">If you want to forward tunneled packets received through a configured tunnel, then it is necessary to enable forwarding on any 6-over-4 interfaces as well as interface \#2.</span></span> <span data-ttu-id="e7973-106">只在介面2上啟用轉送 \# 將無法運作。</span><span class="sxs-lookup"><span data-stu-id="e7973-106">Just enabling forwarding on interface \#2 will not work.</span></span> <span data-ttu-id="e7973-107">通常在設定路由器時，您會在回送以外的所有介面上啟用轉送。</span><span class="sxs-lookup"><span data-stu-id="e7973-107">Typically when configuring a router, you would enable forwarding on all interfaces except loopback.</span></span>

 

 



