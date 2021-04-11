---
description: 通訊端和 WSASocket 中的通訊協定參數是一種識別碼，可建立網路類型，以及用來識別網路上所執行之各種傳輸通訊協定的方法。
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: IPX 通訊協定識別碼系列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113049"
---
# <a name="ipx-family-of-protocol-identifiers"></a><span data-ttu-id="30f5f-103">IPX 通訊協定識別碼系列</span><span class="sxs-lookup"><span data-stu-id="30f5f-103">IPX Family of Protocol Identifiers</span></span>

<span data-ttu-id="30f5f-104">[**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket)和 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)中的 *通訊協定* 參數是一種識別碼，可建立網路類型，以及用來識別網路上所執行之各種傳輸通訊協定的方法。</span><span class="sxs-lookup"><span data-stu-id="30f5f-104">The *protocol* parameter in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) is an identifier that establishes a network type and a method for identifying the various transport protocols that run on the network.</span></span> <span data-ttu-id="30f5f-105">不同于 IP，IPX 不會使用單一通訊協定值來選取傳輸堆疊。</span><span class="sxs-lookup"><span data-stu-id="30f5f-105">Unlike IP, IPX does not use a single protocol value for selecting a transport stack.</span></span> <span data-ttu-id="30f5f-106">由於沒有任何網路需求可針對每個傳輸通訊協定使用特定的值，因此我們可以自由地以 Winsock 應用程式方便的方式指派它們。</span><span class="sxs-lookup"><span data-stu-id="30f5f-106">Since there is no network requirement to use a specific value for each transport protocol, we are free to assign them in a manner convenient for Winsock applications.</span></span> <span data-ttu-id="30f5f-107">我們會避免值0到255，以避免與對應的 PF \_ INET 通訊協定值發生衝突。</span><span class="sxs-lookup"><span data-stu-id="30f5f-107">We avoid values 0–255 in order to avoid collisions with the corresponding PF\_INET protocol values.</span></span>



| <span data-ttu-id="30f5f-108">Name</span><span class="sxs-lookup"><span data-stu-id="30f5f-108">Name</span></span>         | <span data-ttu-id="30f5f-109">值</span><span class="sxs-lookup"><span data-stu-id="30f5f-109">Value</span></span>       | <span data-ttu-id="30f5f-110">通訊端類型</span><span class="sxs-lookup"><span data-stu-id="30f5f-110">Socket types</span></span>              | <span data-ttu-id="30f5f-111">Description</span><span class="sxs-lookup"><span data-stu-id="30f5f-111">Description</span></span>                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| <span data-ttu-id="30f5f-112">保留</span><span class="sxs-lookup"><span data-stu-id="30f5f-112">Reserved</span></span>     | <span data-ttu-id="30f5f-113">0-255</span><span class="sxs-lookup"><span data-stu-id="30f5f-113">0-255</span></span>       |                           | <span data-ttu-id="30f5f-114">保留給 PF \_ INET 通訊協定值。</span><span class="sxs-lookup"><span data-stu-id="30f5f-114">Reserved for PF\_INET protocol values.</span></span>              |
| <span data-ttu-id="30f5f-115">NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="30f5f-115">NSPROTO\_IPX</span></span> | <span data-ttu-id="30f5f-116">1000-1255</span><span class="sxs-lookup"><span data-stu-id="30f5f-116">1000 - 1255</span></span> | <span data-ttu-id="30f5f-117">SOCK \_ DGRAM SOCK \_ RAW</span><span class="sxs-lookup"><span data-stu-id="30f5f-117">SOCK\_DGRAM SOCK\_RAW</span></span>     | <span data-ttu-id="30f5f-118">適用于 IPX 的資料包服務。</span><span class="sxs-lookup"><span data-stu-id="30f5f-118">Datagram service for IPX.</span></span>                           |
| <span data-ttu-id="30f5f-119">NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="30f5f-119">NSPROTO\_SPX</span></span> | <span data-ttu-id="30f5f-120">1256</span><span class="sxs-lookup"><span data-stu-id="30f5f-120">1256</span></span>        | <span data-ttu-id="30f5f-121">SOCK \_ STREAM SOCK \_ SEQPKT</span><span class="sxs-lookup"><span data-stu-id="30f5f-121">SOCK\_STREAM SOCK\_SEQPKT</span></span> | <span data-ttu-id="30f5f-122">使用固定大小的封包進行可靠的封包交換。</span><span class="sxs-lookup"><span data-stu-id="30f5f-122">Reliable packet exchange using fixed-sized packets.</span></span> |



 

> [!Note]  
> <span data-ttu-id="30f5f-123">指定 NSPROTO \_ spx 時，如果兩個端點都能夠執行此動作，則會自動使用 SPX II 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="30f5f-123">When NSPROTO\_SPX is specified, the SPX II protocol is automatically utilized if both endpoints are capable of doing so.</span></span>

 

 

 



