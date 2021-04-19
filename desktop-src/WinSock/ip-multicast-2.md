---
description: IP 多播落在 nonrooted 資料平面和 nonrooted 控制平面的類別中。
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: IP 多播
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf9469822ae974b7c616b7904f9dc7120682acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973640"
---
# <a name="ip-multicast"></a><span data-ttu-id="ab54a-103">IP 多播</span><span class="sxs-lookup"><span data-stu-id="ab54a-103">IP Multicast</span></span>

<span data-ttu-id="ab54a-104">IP 多播落在 nonrooted 資料平面和 nonrooted 控制平面的類別中。</span><span class="sxs-lookup"><span data-stu-id="ab54a-104">IP multicast falls into the category of nonrooted data plane and nonrooted control plane.</span></span> <span data-ttu-id="ab54a-105">所有應用程式都扮演分葉角色。</span><span class="sxs-lookup"><span data-stu-id="ab54a-105">All applications play a leaf role.</span></span> <span data-ttu-id="ab54a-106">目前，大部分的 IP 多播採用都是由 Steve Deering 提供的一組通訊端選項， (IETF) 的網際網路工程任務推動力。</span><span class="sxs-lookup"><span data-stu-id="ab54a-106">Currently, most IP multicast implementations use a set of socket options proposed by Steve Deering to the Internet Engineering Task Force (IETF).</span></span> <span data-ttu-id="ab54a-107">因此有五個作業可供使用：</span><span class="sxs-lookup"><span data-stu-id="ab54a-107">Five operations are thus made available:</span></span>

-   <span data-ttu-id="ab54a-108">IP \_ 多播 \_ TTL —設定存留時間、控制多播會話的範圍。</span><span class="sxs-lookup"><span data-stu-id="ab54a-108">IP\_MULTICAST\_TTL—Sets time-to-live, controls scope of a multicast session.</span></span>
-   <span data-ttu-id="ab54a-109">IP \_ 多播 \_ IF-決定要用於多播的介面。</span><span class="sxs-lookup"><span data-stu-id="ab54a-109">IP\_MULTICAST\_IF—Determines interface to be used for multicasting.</span></span>
-   <span data-ttu-id="ab54a-110">IP \_ 新增 \_ MEMBERSHI：聯結指定的多播會話。</span><span class="sxs-lookup"><span data-stu-id="ab54a-110">IP\_ADD\_MEMBERSHI —Joins a specified multicast session.</span></span>
-   <span data-ttu-id="ab54a-111">IP \_ 捨棄 \_ 成員資格-捨棄多播會話。</span><span class="sxs-lookup"><span data-stu-id="ab54a-111">IP\_DROP\_MEMBERSHIP—Drops out of a multicast session.</span></span>
-   <span data-ttu-id="ab54a-112">IP \_ 多播 \_ 迴圈-控制多播流量的回送。</span><span class="sxs-lookup"><span data-stu-id="ab54a-112">IP\_MULTICAST\_LOOP—Controls loopback of multicast traffic.</span></span>

<span data-ttu-id="ab54a-113">設定 IP 多播通訊端的存留時間時，會直接對應到 \_ 針對 WSAIoctl 使用 SIO 多播 \_ 領域命令的程式碼[](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)。</span><span class="sxs-lookup"><span data-stu-id="ab54a-113">Setting the time-to-live for an IP-multicast socket maps directly to using the SIO\_MULTICAST\_SCOPE command code for [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl).</span></span>

<span data-ttu-id="ab54a-114">判斷要用於多播的 IP 介面的方法是透過 TCP/IP 特定通訊端選項，如 Windows 通訊端 2 Protocol-Specific 附錄中所述。</span><span class="sxs-lookup"><span data-stu-id="ab54a-114">The method for determining the IP interface to be used for multicasting is through a TCP/IP-specific socket option as described in the Windows Sockets 2 Protocol-Specific Annex.</span></span> <span data-ttu-id="ab54a-115">其餘的三項作業會在這裡說明的 Windows 通訊端2語義中妥善討論。</span><span class="sxs-lookup"><span data-stu-id="ab54a-115">The remaining three operations are covered well with the Windows Sockets 2 semantics described here.</span></span>

<span data-ttu-id="ab54a-116">應用程式會使用 WSASocket 中的 c 分 \_ 葉/d 分 \_ 葉旗標[](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)來開啟通訊端。</span><span class="sxs-lookup"><span data-stu-id="ab54a-116">The application would open sockets with c\_leaf/d\_leaf flags in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span></span> <span data-ttu-id="ab54a-117">它會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 將本身新增至預設介面（指定給多播作業）的多播群組。</span><span class="sxs-lookup"><span data-stu-id="ab54a-117">It would use [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add itself to a multicast group on the default interface designated for multicast operations.</span></span> <span data-ttu-id="ab54a-118">如果 **WSAJoinLeaf** 中的旗標指出這個通訊端只是傳送者，則聯結作業基本上是無作業，而且不需要傳送任何 IGMP 訊息。</span><span class="sxs-lookup"><span data-stu-id="ab54a-118">If the flag in **WSAJoinLeaf** indicates that this socket is only a sender, then the join operation is essentially a no-op and no IGMP messages need to be sent.</span></span> <span data-ttu-id="ab54a-119">否則，會將 IGMP 封包傳送給路由器，以指出接收傳送到指定多播位址的封包的興趣。</span><span class="sxs-lookup"><span data-stu-id="ab54a-119">Otherwise, an IGMP packet is sent out to the router to indicate interests in receiving packets sent to the specified multicast address.</span></span> <span data-ttu-id="ab54a-120">由於應用程式建立了專門用來執行多播的特殊 c 分 \_ 葉/d 分 \_ 葉通訊端，因此會使用標準 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式來捨棄多播會話。</span><span class="sxs-lookup"><span data-stu-id="ab54a-120">Since the application created special c\_leaf/d\_leaf sockets used only for performing multicast, the standard [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function would be used to drop out of the multicast session.</span></span> <span data-ttu-id="ab54a-121">適用于 \_ WSAIoctl 的 SIO MULTIPOINT \_ 回[](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)送命令程式碼提供了一般控制機制，用來判斷在 nonrooted MULTIPOINT 配置的 d 分葉通訊端上傳送的資料是否 \_ 也可以在相同的通訊端上接收。</span><span class="sxs-lookup"><span data-stu-id="ab54a-121">The SIO\_MULTIPOINT\_LOOPBACK command code for [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) provides a generic control mechanism for determining whether data sent on a d\_leaf socket in a nonrooted multipoint scheme can also be received on the same socket.</span></span>

> [!Note]  
> <span data-ttu-id="ab54a-122">IP 多播迴圈選項的 Winsock 版本在 \_ \_ 語義上與 ip \_ 多播迴圈選項的 UNIX 版本不同 \_ ：</span><span class="sxs-lookup"><span data-stu-id="ab54a-122">The Winsock version of the IP\_MULTICAST\_LOOP option is semantically different than the UNIX version of the IP\_MULTICAST\_LOOP option:</span></span>

 

-   <span data-ttu-id="ab54a-123">在 Winsock 中，IP \_ 多播 \_ 迴圈選項只會套用到接收路徑。</span><span class="sxs-lookup"><span data-stu-id="ab54a-123">In Winsock, the IP\_MULTICAST\_LOOP option applies only to the receive path.</span></span>
-   <span data-ttu-id="ab54a-124">在 UNIX 版本中，IP \_ 多播 \_ 迴圈選項會套用到傳送路徑。</span><span class="sxs-lookup"><span data-stu-id="ab54a-124">In the UNIX version, the IP\_MULTICAST\_LOOP option applies to the send path.</span></span>

<span data-ttu-id="ab54a-125">例如，開啟和關閉應用程式 (比 X 和 Y 更容易追蹤) 在相同介面上加入相同群組;上的應用程式會在上設定 IP \_ 多播 \_ 迴圈選項，應用程式 OFF 將 ip \_ 多播 \_ 迴圈選項設為關閉。</span><span class="sxs-lookup"><span data-stu-id="ab54a-125">For example, applications ON and OFF (which are easier to track than X and Y) join the same group on the same interface; application ON sets the IP\_MULTICAST\_LOOP option on, application OFF sets the IP\_MULTICAST\_LOOP option off.</span></span> <span data-ttu-id="ab54a-126">如果 ON 和 OFF 是 Winsock 應用程式，OFF 可以傳送至 ON，但無法傳送到 OFF。</span><span class="sxs-lookup"><span data-stu-id="ab54a-126">If ON and OFF are Winsock applications, OFF can send to ON, but ON cannot sent to OFF.</span></span> <span data-ttu-id="ab54a-127">相反地，如果 ON 和 OFF 是 UNIX 應用程式，則上的可以傳送至 OFF，但無法傳送至開啟。</span><span class="sxs-lookup"><span data-stu-id="ab54a-127">In contrast, if ON and OFF are UNIX applications, ON can send to OFF, but OFF cannot send to ON.</span></span>

 

 



