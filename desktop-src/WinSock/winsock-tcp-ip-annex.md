---
description: 本節說明傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 函數、資料結構和控制項。
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Winsock TCP/IP 附錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191729"
---
# <a name="winsock-tcpip-annex"></a><span data-ttu-id="a60b0-103">Winsock TCP/IP 附錄</span><span class="sxs-lookup"><span data-stu-id="a60b0-103">Winsock TCP/IP Annex</span></span>

<span data-ttu-id="a60b0-104">本節說明傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 函數、資料結構和控制項。</span><span class="sxs-lookup"><span data-stu-id="a60b0-104">This section describes Transmission Control Protocol/Internet Protocol (TCP/IP) functions, data structures, and controls.</span></span>



| <span data-ttu-id="a60b0-105">元素</span><span class="sxs-lookup"><span data-stu-id="a60b0-105">Element</span></span>          | <span data-ttu-id="a60b0-106">描述</span><span class="sxs-lookup"><span data-stu-id="a60b0-106">Description</span></span>                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a60b0-107">通訊協定名稱 (s) </span><span class="sxs-lookup"><span data-stu-id="a60b0-107">Protocol name(s)</span></span> | <span data-ttu-id="a60b0-108">TCP、UDP</span><span class="sxs-lookup"><span data-stu-id="a60b0-108">TCP, UDP</span></span>                                                                                                                                    |
| <span data-ttu-id="a60b0-109">Description</span><span class="sxs-lookup"><span data-stu-id="a60b0-109">Description</span></span>      | <span data-ttu-id="a60b0-110">透過 IP 網路層提供傳輸服務： UDP 適用于不可靠的資料包、TCP （適用于可靠的連接導向位元組串流）。</span><span class="sxs-lookup"><span data-stu-id="a60b0-110">Provides transport services over the IP networking layer: UDP for unreliable datagrams, TCP for reliable, connection-oriented byte streams.</span></span> |
| <span data-ttu-id="a60b0-111">位址系列</span><span class="sxs-lookup"><span data-stu-id="a60b0-111">Address family</span></span>   | <span data-ttu-id="a60b0-112">**AF \_INET**， **AF \_ INET6**</span><span class="sxs-lookup"><span data-stu-id="a60b0-112">**AF\_INET**, **AF\_INET6**</span></span>                                                                                                                 |
| <span data-ttu-id="a60b0-113">標頭檔</span><span class="sxs-lookup"><span data-stu-id="a60b0-113">Header file</span></span>      | <span data-ttu-id="a60b0-114">*Ws2tcpip。h*</span><span class="sxs-lookup"><span data-stu-id="a60b0-114">*Ws2tcpip.h*</span></span>                                                                                                                                |



 

<span data-ttu-id="a60b0-115">提供兩種基本類型的傳輸服務：不可靠的資料包 (UDP) ，以及可靠的連接導向-位元組串流 (的 TCP) 。</span><span class="sxs-lookup"><span data-stu-id="a60b0-115">Two basic types of transport services are offered: unreliable datagrams (UDP), and reliable connection oriented–byte streams (TCP).</span></span> <span data-ttu-id="a60b0-116">此外，也可以選擇性地支援原始通訊端。</span><span class="sxs-lookup"><span data-stu-id="a60b0-116">In addition, a raw socket is optionally supported.</span></span> <span data-ttu-id="a60b0-117">原始通訊端可讓應用程式透過 TCP 和 UDP （例如 ICMP）以外的通訊協定進行通訊。</span><span class="sxs-lookup"><span data-stu-id="a60b0-117">Raw sockets allow an application to communicate through protocols other than TCP and UDP such as ICMP.</span></span> <span data-ttu-id="a60b0-118">**Af \_ INET** 和 **af \_ INET6** 位址系列支援原始通訊端，但有一些限制。</span><span class="sxs-lookup"><span data-stu-id="a60b0-118">Raw sockets are supported on the **AF\_INET** and **AF\_INET6** address families with some limitations.</span></span>

<span data-ttu-id="a60b0-119">本節涵蓋 TCP/IP 通訊協定專用的 Winsock 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="a60b0-119">This section covers extensions to Winsock that are specific to TCP/IP protocols.</span></span> <span data-ttu-id="a60b0-120">它也會描述需要特殊考慮的基底 Winsock 函式，或使用 TCP/IP 時可能出現的獨特行為的層面。</span><span class="sxs-lookup"><span data-stu-id="a60b0-120">It also describes aspects of base Winsock functions that require special consideration or that may exhibit unique behavior when using TCP/IP.</span></span>

 

 



