---
description: 媒體封包大小會影響 IPX 通訊協定在網路之間傳輸資料的能力，並可證明以與傳輸無關的方式處理的挑戰。
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: 關於媒體封包大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f97e36a81b90b72d4d1148e9461f58ae2147ba
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945707"
---
# <a name="about-media-packet-size"></a><span data-ttu-id="ac548-103">關於媒體封包大小</span><span class="sxs-lookup"><span data-stu-id="ac548-103">About Media Packet Size</span></span>

<span data-ttu-id="ac548-104">媒體封包大小會影響 IPX 通訊協定在網路之間傳輸資料的能力，並可證明以與傳輸無關的方式處理的挑戰。</span><span class="sxs-lookup"><span data-stu-id="ac548-104">Media packet size affects the ability of IPX protocols to transfer data across networks and can prove challenging to deal with in a transport-independent manner.</span></span> <span data-ttu-id="ac548-105">IPX 不會分割封包，也不會在因為大小違規而捨棄封包時進行報告。</span><span class="sxs-lookup"><span data-stu-id="ac548-105">IPX does not segment packets, nor does it report when packets are dropped due to size violations.</span></span> <span data-ttu-id="ac548-106">這表示，終端機上的某些實體必須知道要在任何指定的網路路徑上使用的封包大小上限。</span><span class="sxs-lookup"><span data-stu-id="ac548-106">This means that some entity on the end station must maintain knowledge of the maximum packet size to be used on any given internetwork path.</span></span> <span data-ttu-id="ac548-107">傳統上，IPX 資料包和 SPX 連接導向的服務已將這種負擔留給應用程式，而 SPXII 則使用大型的網際網路封包協商以透明的方式處理它。</span><span class="sxs-lookup"><span data-stu-id="ac548-107">Traditionally, IPX datagrams and SPX connection-oriented services have left this burden to the application, while SPXII has used large Internet packet negotiation to handle it transparently.</span></span>

<span data-ttu-id="ac548-108">Winsock 會嘗試為其各種 IPX 通訊協定設定合理的封包大小限制，如下一節所述。</span><span class="sxs-lookup"><span data-stu-id="ac548-108">Winsock attempts to set rational packet size limits for its various IPX protocols as described in the next section.</span></span> <span data-ttu-id="ac548-109">這些限制可透過 get/set 通訊端選項，由應用程式來查看及修改。</span><span class="sxs-lookup"><span data-stu-id="ac548-109">These limits can be viewed and modified by applications through get/set socket options.</span></span> <span data-ttu-id="ac548-110">判斷封包大小上限時，有三個重點：</span><span class="sxs-lookup"><span data-stu-id="ac548-110">When determining maximum packet size, the three areas of concern are:</span></span>

-   <span data-ttu-id="ac548-111">\# 媒體封包大小</span><span class="sxs-lookup"><span data-stu-id="ac548-111">\# Media packet size</span></span>
-   <span data-ttu-id="ac548-112">\# 可路由傳送的封包大小</span><span class="sxs-lookup"><span data-stu-id="ac548-112">\# Routable packet size</span></span>
-   <span data-ttu-id="ac548-113">\# 終端站封包大小</span><span class="sxs-lookup"><span data-stu-id="ac548-113">\# End-station packet size</span></span>

<span data-ttu-id="ac548-114">*媒體封包大小* 會反映封包流經目的地的任何媒體上可接受的封包大小上限。</span><span class="sxs-lookup"><span data-stu-id="ac548-114">*Media packet size* reflects the maximum packet size acceptable on any media the packet traverses to its destination.</span></span> <span data-ttu-id="ac548-115">封包大小會隨著不同的媒體（例如乙太網路和權杖環）而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ac548-115">Packet size varies among differing media such as Ethernet and token ring.</span></span> <span data-ttu-id="ac548-116">封包內的資料空間量也可能在指定的媒體內有所差異，視封包標頭的相片順序而定。</span><span class="sxs-lookup"><span data-stu-id="ac548-116">The amount of data space within a packet can also vary within a given media, depending on the packet header arrangement.</span></span> <span data-ttu-id="ac548-117">例如，乙太網路封包的有效資料大小會根據其類型是否為 Ethernet II、Ethernet 802.2 或 Ethernet 嵌入式管理單元而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ac548-117">For instance, the effective data size of an Ethernet packet varies depending on whether it is of the type Ethernet II, Ethernet 802.2, or Ethernet SNAP.</span></span>

<span data-ttu-id="ac548-118">可路由傳送的封 *包大小* 反映中繼路由器願意轉寄的封包大小上限。</span><span class="sxs-lookup"><span data-stu-id="ac548-118">*Routable packet size* reflects the maximum packet size an intermediate router is willing to forward.</span></span> <span data-ttu-id="ac548-119">大部分的 IPX 路由器都是為了路由傳送任何大小的資料包而建立的，只要它仍在傳送和接收網路的媒體大小內。</span><span class="sxs-lookup"><span data-stu-id="ac548-119">Most IPX routers are built to route any size datagram as long as it remains within the media size of the sending and receiving network.</span></span> <span data-ttu-id="ac548-120">不過，較舊的路由器可能會將封包大小上限限制為576個位元組，包括通訊協定標頭。</span><span class="sxs-lookup"><span data-stu-id="ac548-120">However, older routers may limit maximum packet size to 576 bytes, including protocol headers.</span></span>

<span data-ttu-id="ac548-121">*終端站封包大小* 會反映終端電臺張貼以接收連入封包的接聽緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="ac548-121">*End-station packet size* reflects the size of the listen buffers that end stations have posted to receive incoming packets.</span></span> <span data-ttu-id="ac548-122">即使媒體和路由器的限制允許封包通過，如果接收的應用程式已公佈較小的緩衝區，終端站可能會捨棄該封包。</span><span class="sxs-lookup"><span data-stu-id="ac548-122">Even when the media and router limits allow a packet through, it may be discarded by the end station if the receiving application has posted a smaller buffer.</span></span> <span data-ttu-id="ac548-123">許多傳統的 IPX/SPX 應用程式會限制接收緩衝區大小，讓資料部分不能大於512或1024位元組。</span><span class="sxs-lookup"><span data-stu-id="ac548-123">Many traditional IPX/SPX applications limit receive buffer size such that the data portion must be no larger than 512 or 1024 bytes.</span></span>

 

 



