---
description: IPX 位址系列會定義使用標準 IPX 通訊端定址之通訊協定的定址結構。 針對這些傳輸，端點位址是由網路編號、節點位址和通訊端編號所組成。
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: AF_IPX 位址系列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113112"
---
# <a name="af_ipx-address-family"></a><span data-ttu-id="2566c-104">AF \_ IPX 位址系列</span><span class="sxs-lookup"><span data-stu-id="2566c-104">AF\_IPX Address Family</span></span>

<span data-ttu-id="2566c-105">IPX 位址系列會定義使用標準 IPX 通訊端定址之通訊協定的定址結構。</span><span class="sxs-lookup"><span data-stu-id="2566c-105">The IPX address family defines the addressing structure for protocols that use standard IPX socket addressing.</span></span> <span data-ttu-id="2566c-106">針對這些傳輸，端點位址是由網路編號、節點位址和通訊端編號所組成。</span><span class="sxs-lookup"><span data-stu-id="2566c-106">For these transports, an endpoint address consists of a network number, node address, and socket number.</span></span>

<span data-ttu-id="2566c-107">網路編號是系統管理網域，通常會命名單一乙太網路或權杖環形區段。</span><span class="sxs-lookup"><span data-stu-id="2566c-107">The network number is an administrative domain and typically names a single Ethernet or token ring segment.</span></span> <span data-ttu-id="2566c-108">節點編號是工作站的實體位址。</span><span class="sxs-lookup"><span data-stu-id="2566c-108">The node number is a station's physical address.</span></span> <span data-ttu-id="2566c-109">Net 和 node 的組合形成唯一的站位址，在世界中假設是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2566c-109">The combination of net and node form a unique station address that is presumed to be unique in the world.</span></span> <span data-ttu-id="2566c-110">淨和節點編號會以 ASCII 文字表示，區塊或虛線標記法為： ' 0101a040，00001b498765 ' 或 ' 01-01-a0-40，00-00-1b-49-87-65 '。</span><span class="sxs-lookup"><span data-stu-id="2566c-110">Net and node numbers are represented in ASCII text in either block or dashed notation as: '0101a040,00001b498765' or '01-01-a0-40,00-00-1b-49-87-65'.</span></span> <span data-ttu-id="2566c-111">前置零不需要存在。</span><span class="sxs-lookup"><span data-stu-id="2566c-111">Leading zeros need not be present.</span></span>

<span data-ttu-id="2566c-112">IPX 通訊端編號是網路/傳輸服務編號，與 TCP 通訊埠編號很類似，且不會與 Winsock 通訊端描述元混淆。</span><span class="sxs-lookup"><span data-stu-id="2566c-112">The IPX socket number is a network/transport service number much like a TCP port number and is not to be confused with the Winsock socket descriptor.</span></span> <span data-ttu-id="2566c-113">IPX 通訊端編號對終端機而言是全域的，且無法系結至特定的網路/節點位址。</span><span class="sxs-lookup"><span data-stu-id="2566c-113">IPX socket numbers are global to the end station and cannot be bound to specific net/node addresses.</span></span> <span data-ttu-id="2566c-114">比方說，如果終端工作站有兩張網路介面卡，系結的通訊端可以在這兩張卡片上傳送和接收。</span><span class="sxs-lookup"><span data-stu-id="2566c-114">For instance, if the end station has two network interface cards, a bound socket can send and receive on both cards.</span></span> <span data-ttu-id="2566c-115">尤其是，資料包通訊端會在這兩張卡片上接收廣播資料包。</span><span class="sxs-lookup"><span data-stu-id="2566c-115">In particular, datagram sockets would receive broadcast datagrams on both cards.</span></span>

> [!Caution]  
> <span data-ttu-id="2566c-116">SOCKADDR \_ IPX 長度為14個位元組，且比16位元組的 [**SOCKADDR**](sockaddr-2.md) 參考結構短。</span><span class="sxs-lookup"><span data-stu-id="2566c-116">SOCKADDR\_IPX is 14 bytes long and is shorter than the 16-byte [**sockaddr**](sockaddr-2.md) reference structure.</span></span> <span data-ttu-id="2566c-117">IPX/SPX 的執行可能會接受16位元組長度以及真正的長度。</span><span class="sxs-lookup"><span data-stu-id="2566c-117">IPX/SPX implementations may accept the 16-byte length as well as the true length.</span></span> <span data-ttu-id="2566c-118">如果您使用 SOCKADDR \_ 的 IPX 和硬式編碼長度的16個位元組，則實作為可能會假設它可以存取您的結構之後的2個位元組。</span><span class="sxs-lookup"><span data-stu-id="2566c-118">If you use SOCKADDR\_IPX and a hard-coded length of 16 bytes, the implementation may assume that it has access to the 2 bytes following your structure.</span></span>

 



| <span data-ttu-id="2566c-119">欄位</span><span class="sxs-lookup"><span data-stu-id="2566c-119">Field</span></span>           | <span data-ttu-id="2566c-120">值</span><span class="sxs-lookup"><span data-stu-id="2566c-120">Value</span></span>                                    |
|-----------------|------------------------------------------|
| <span data-ttu-id="2566c-121">**sa \_ 系列**</span><span class="sxs-lookup"><span data-stu-id="2566c-121">**sa\_family**</span></span>  | <span data-ttu-id="2566c-122">依 \_ 主機順序的位址家族 AF IPX。</span><span class="sxs-lookup"><span data-stu-id="2566c-122">Address family AF\_IPX in host order.</span></span>    |
| <span data-ttu-id="2566c-123">**Sa \_ netnum**</span><span class="sxs-lookup"><span data-stu-id="2566c-123">**Sa\_netnum**</span></span>  | <span data-ttu-id="2566c-124">網路順序中的 IPX 網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="2566c-124">IPX network identifier in network order.</span></span> |
| <span data-ttu-id="2566c-125">**Sa \_ nodenum**</span><span class="sxs-lookup"><span data-stu-id="2566c-125">**Sa\_nodenum**</span></span> | <span data-ttu-id="2566c-126">工作站節點位址，排清右邊。</span><span class="sxs-lookup"><span data-stu-id="2566c-126">Station node address, flushed right.</span></span>     |
| <span data-ttu-id="2566c-127">**Sa \_ 通訊端**</span><span class="sxs-lookup"><span data-stu-id="2566c-127">**Sa\_socket**</span></span>  | <span data-ttu-id="2566c-128">網路順序的 IPX 通訊端編號。</span><span class="sxs-lookup"><span data-stu-id="2566c-128">IPX socket number in network order.</span></span>      |



 

 

 



