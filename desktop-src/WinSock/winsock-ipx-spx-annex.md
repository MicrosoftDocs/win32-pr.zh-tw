---
description: 本節說明網路封包交換/排序封包交換專用的 Winsock 延伸模組 (IPX/SPX) 。 它也會描述基底 Winsock 函式的各個層面，這些函式需要特殊考慮或可能展現獨特的行為。
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Winsock IPX/SPX 附錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973700"
---
# <a name="winsock-ipxspx-annex"></a><span data-ttu-id="a5fe1-104">Winsock IPX/SPX 附錄</span><span class="sxs-lookup"><span data-stu-id="a5fe1-104">Winsock IPX/SPX Annex</span></span>

<span data-ttu-id="a5fe1-105">本節說明網路封包交換/排序封包交換專用的 Winsock 延伸模組 (IPX/SPX) 。</span><span class="sxs-lookup"><span data-stu-id="a5fe1-105">This section describes Winsock extensions specific to Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX).</span></span> <span data-ttu-id="a5fe1-106">它也會描述基底 Winsock 函式的各個層面，這些函式需要特殊考慮或可能展現獨特的行為。</span><span class="sxs-lookup"><span data-stu-id="a5fe1-106">It also describes aspects of base Winsock functions that either require special consideration or may exhibit unique behavior.</span></span>



| <span data-ttu-id="a5fe1-107">元素</span><span class="sxs-lookup"><span data-stu-id="a5fe1-107">Element</span></span>          | <span data-ttu-id="a5fe1-108">描述</span><span class="sxs-lookup"><span data-stu-id="a5fe1-108">Description</span></span>                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fe1-109">通訊協定名稱 (s) </span><span class="sxs-lookup"><span data-stu-id="a5fe1-109">Protocol name(s)</span></span> | <span data-ttu-id="a5fe1-110">IPX、SPX</span><span class="sxs-lookup"><span data-stu-id="a5fe1-110">IPX, SPX</span></span>                                                                                                                                        |
| <span data-ttu-id="a5fe1-111">Description</span><span class="sxs-lookup"><span data-stu-id="a5fe1-111">Description</span></span>      | <span data-ttu-id="a5fe1-112">透過 IPX 網路層提供傳輸服務：適用于不可靠的資料包的 IPX、適用于可靠、以連接導向的訊息串流的 SPX。</span><span class="sxs-lookup"><span data-stu-id="a5fe1-112">Provides transport services over the IPX networking layer: IPX for unreliable datagrams, SPX for reliable, connection-oriented message streams.</span></span> |
| <span data-ttu-id="a5fe1-113">位址系列</span><span class="sxs-lookup"><span data-stu-id="a5fe1-113">Address family</span></span>   | <span data-ttu-id="a5fe1-114">AF \_ IPX</span><span class="sxs-lookup"><span data-stu-id="a5fe1-114">AF\_IPX</span></span>                                                                                                                                         |
| <span data-ttu-id="a5fe1-115">標頭檔</span><span class="sxs-lookup"><span data-stu-id="a5fe1-115">Header file</span></span>      | <span data-ttu-id="a5fe1-116">Wsipx。h</span><span class="sxs-lookup"><span data-stu-id="a5fe1-116">Wsipx.h</span></span>                                                                                                                                         |



 

<span data-ttu-id="a5fe1-117">本節討論如何使用 Winsock 搭配 IPX 的通訊協定系列，讓傳統的 IPX 應用程式可以移植到 Winsock。</span><span class="sxs-lookup"><span data-stu-id="a5fe1-117">This section discusses how to use Winsock with the IPX family of protocols, enabling traditional IPX applications to be ported to Winsock.</span></span> <span data-ttu-id="a5fe1-118">IPX 網路的運作方式與 IP 網路本質上不同，因此使用 IPX/SPX 時必須考慮這類差異。</span><span class="sxs-lookup"><span data-stu-id="a5fe1-118">IPX networks operate in a fundamentally different manner than IP networks, so such differences must be considered when using IPX/SPX.</span></span>

 

 



