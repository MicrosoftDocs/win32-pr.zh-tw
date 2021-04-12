---
title: 設定 SPX/IPX 的 RPC
description: 使用 ncacn 的 \_ spx 和 ncadg 的 \_ ipx 傳輸時，伺服器名稱與 Windows 上的伺服器名稱完全相同。
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462340"
---
# <a name="configuring-rpc-for-spxipx"></a><span data-ttu-id="5f5d0-103">設定 SPX/IPX 的 RPC</span><span class="sxs-lookup"><span data-stu-id="5f5d0-103">Configuring RPC for SPX/IPX</span></span>

<span data-ttu-id="5f5d0-104">使用 ncacn 的 **\_ spx** 和 **ncadg 的 \_ ipx** 傳輸時，伺服器名稱與 Windows 上的伺服器名稱完全相同。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-104">When using the **ncacn\_spx** and **ncadg\_ipx** transports, the server name is exactly the same as the server name on Windows.</span></span> <span data-ttu-id="5f5d0-105">不過，因為名稱是使用 Novell 通訊協定來散發，所以它們必須符合 Novell 命名慣例。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-105">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="5f5d0-106">如果伺服器名稱不是有效的 Novell 名稱，伺服器將無法使用 **ncacn 的 \_ spx** 或 **ncadg \_ ipx** 傳輸來建立端點。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-106">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** or **ncadg\_ipx** transports.</span></span>

<span data-ttu-id="5f5d0-107">有效的 Novell 伺服器名稱只包含0x20 和0x7f 之間的字元。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-107">A valid Novell server name contains only the characters between 0x20 and 0x7f.</span></span> <span data-ttu-id="5f5d0-108">小寫字元會變更為大寫。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-108">Lowercase characters are changed to uppercase.</span></span> <span data-ttu-id="5f5d0-109">無法使用下列字元：</span><span class="sxs-lookup"><span data-stu-id="5f5d0-109">The following characters cannot be used:</span></span>

<span data-ttu-id="5f5d0-110">" \* 、./：; <=>？\[\]\\\|\]</span><span class="sxs-lookup"><span data-stu-id="5f5d0-110">"\*,./:;<=>?\[\]\\\|\]</span></span>

<span data-ttu-id="5f5d0-111">為了維持與第一個 Windows NT 版本的相容性， **ncacn \_ spx** 和 **ncadg \_ ipx** 也可讓您使用伺服器名稱的特殊格式，稱為波狀符號名稱。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-111">To maintain compatibility with the first version of Windows NT, **ncacn\_spx** and **ncadg\_ipx** also enable you to use a special format of the server name known as the tilde name.</span></span> <span data-ttu-id="5f5d0-112">波狀符號名稱包含波狀符號 (~) ，後面接著伺服器的八位數網路編號，然後再接著12位數的乙太網路位址。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-112">The tilde name consists of a tilde (~), followed by the server's eight-digit network number, and then followed by its 12-digit Ethernet address.</span></span> <span data-ttu-id="5f5d0-113">波形名稱有一個優點，就是它們不需要任何名稱服務功能。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-113">Tilde names have an advantage in that they do not require any name service capabilities.</span></span> <span data-ttu-id="5f5d0-114">因此，如果您連接到伺服器，則波狀符號名稱將會運作。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-114">Thus, if you are connected to a server, the tilde name will work.</span></span>

<span data-ttu-id="5f5d0-115">下表包含兩個範例設定，說明先前所述的點。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-115">The following tables contain two sample configurations that illustrate the points previously described.</span></span>



| <span data-ttu-id="5f5d0-116">元件</span><span class="sxs-lookup"><span data-stu-id="5f5d0-116">Component</span></span>                            | <span data-ttu-id="5f5d0-117">設定為</span><span class="sxs-lookup"><span data-stu-id="5f5d0-117">Configured as</span></span>      |
|--------------------------------------|--------------------|
| <span data-ttu-id="5f5d0-118">Windows 伺服器</span><span class="sxs-lookup"><span data-stu-id="5f5d0-118">Windows server</span></span>                       | <span data-ttu-id="5f5d0-119">NWCS</span><span class="sxs-lookup"><span data-stu-id="5f5d0-119">NWCS</span></span>               |
| <span data-ttu-id="5f5d0-120">Windows 用戶端</span><span class="sxs-lookup"><span data-stu-id="5f5d0-120">Windows client</span></span>                       | <span data-ttu-id="5f5d0-121">NWCS</span><span class="sxs-lookup"><span data-stu-id="5f5d0-121">NWCS</span></span>               |
| <span data-ttu-id="5f5d0-122">16位 Windows 用戶端，MS-DOS 用戶端</span><span class="sxs-lookup"><span data-stu-id="5f5d0-122">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="5f5d0-123">NetWare 重新導向程式</span><span class="sxs-lookup"><span data-stu-id="5f5d0-123">NetWare Redirector</span></span> |



 

<span data-ttu-id="5f5d0-124">上表中的設定要求您的網路上必須有 NetWare 檔案伺服器或路由器。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-124">The configuration in the previous table requires that you have NetWare file servers or routers on your network.</span></span> <span data-ttu-id="5f5d0-125">它會產生最佳效能，因為伺服器名稱會儲存在 NetWare 平構伺服器中。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-125">It will produce the best performance because the server names are stored in the NetWare Bindery.</span></span>



| <span data-ttu-id="5f5d0-126">元件</span><span class="sxs-lookup"><span data-stu-id="5f5d0-126">Component</span></span>                            | <span data-ttu-id="5f5d0-127">設定為</span><span class="sxs-lookup"><span data-stu-id="5f5d0-127">Configured as</span></span> |
|--------------------------------------|---------------|
| <span data-ttu-id="5f5d0-128">Windows 伺服器</span><span class="sxs-lookup"><span data-stu-id="5f5d0-128">Windows server</span></span>                       | <span data-ttu-id="5f5d0-129">SAP 代理程式</span><span class="sxs-lookup"><span data-stu-id="5f5d0-129">SAP Agent</span></span>     |
| <span data-ttu-id="5f5d0-130">Windows 用戶端</span><span class="sxs-lookup"><span data-stu-id="5f5d0-130">Windows client</span></span>                       | <span data-ttu-id="5f5d0-131">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="5f5d0-131">IPX/SPX</span></span>       |
| <span data-ttu-id="5f5d0-132">16位 Windows 用戶端，MS-DOS 用戶端</span><span class="sxs-lookup"><span data-stu-id="5f5d0-132">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="5f5d0-133">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="5f5d0-133">IPX/SPX</span></span>       |



 

<span data-ttu-id="5f5d0-134">第二個設定適用于不包含 NetWare 檔案伺服器或路由器的環境 (例如，兩部電腦的網路： Windows server 和 MS-DOS 用戶端) 。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-134">The second configuration works in an environment that does not contain NetWare file servers or routers (for example, a network of two computers: a Windows server and an MS-DOS client).</span></span> <span data-ttu-id="5f5d0-135">名稱解析是在第一次呼叫系結控制碼時完成的，會比第一次設定時稍微慢一點。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-135">Name resolution, which is accomplished during the first call over a binding handle, will be slightly slower than in the first configuration.</span></span> <span data-ttu-id="5f5d0-136">此外，第二個設定會導致透過網路產生更多流量。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-136">In addition, the second configuration results in more traffic generated over the network.</span></span>

<span data-ttu-id="5f5d0-137">若要執行名稱解析，當 RPC 伺服器使用 SPX 或 IPX 端點時，伺服器名稱和端點會註冊為服務公告通訊協定， (640 類型的 SAP) 伺服器 (十六進位) 。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-137">To implement name resolution, when an RPC server uses an SPX or IPX endpoint, the server name and endpoint are registered as a Service Advertising Protocol (SAP) server of type 640 (hexadecimal).</span></span> <span data-ttu-id="5f5d0-138">為了解析伺服器名稱，RPC 用戶端會針對相同類型的所有服務傳送 SAP 要求，然後掃描回應清單中的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-138">To resolve a server name, the RPC client sends a SAP request for all services of the same type, and then scans the list of responses for the name of the server.</span></span> <span data-ttu-id="5f5d0-139">此進程會在每個系結控制碼的第一個 RPC 呼叫期間發生。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-139">This process occurs during the first RPC call over each binding handle.</span></span> <span data-ttu-id="5f5d0-140">如需有關適用于 Novell 的 SAP 通訊協定的詳細資訊，請參閱您的 NetWare 檔。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-140">For additional information on the SAP protocol for Novell, see your NetWare documentation.</span></span>

> [!Note]  
> <span data-ttu-id="5f5d0-141">使用 **ncacn \_ spx** 或 **ncadg \_ Ipx** 傳輸的16位 Windows 用戶端應用程式需要安裝 Nwipxspx.dll 的檔案，才能在 WOW 子系統下執行。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-141">The 16-bit Windows client applications that use the **ncacn\_spx** or **ncadg\_ipx** transports require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="5f5d0-142">請聯絡 Novell 以取得此檔案。</span><span class="sxs-lookup"><span data-stu-id="5f5d0-142">Contact Novell to obtain this file.</span></span>

 

 

 




