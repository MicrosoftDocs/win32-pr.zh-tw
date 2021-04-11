---
description: 啟用通訊端的本機埠擴充性。
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: 'SO_PORT_SCALABILITY (Ws2def) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113004"
---
# <a name="so_port_scalability"></a><span data-ttu-id="66eca-103">因此， \_ 埠擴充 \_ 性</span><span class="sxs-lookup"><span data-stu-id="66eca-103">SO\_PORT\_SCALABILITY</span></span>

<span data-ttu-id="66eca-104">**SO \_ 埠擴充 \_ 性** 通訊端選項可啟用通訊端的本機埠擴充性。</span><span class="sxs-lookup"><span data-stu-id="66eca-104">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability for a socket.</span></span>

<dl> <dt>

<span data-ttu-id="66eca-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**因此， \_ 埠擴充 \_ 性**</span><span class="sxs-lookup"><span data-stu-id="66eca-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**SO\_PORT\_SCALABILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66eca-106">0x3006</span><span class="sxs-lookup"><span data-stu-id="66eca-106">0x3006</span></span>
</dt> <dt>



<span data-ttu-id="66eca-107">**如此埠的擴充 \_ \_ 性** 通訊端選項可讓本機通訊埠可透過針對本機電腦上不同的本機位址通訊埠配對，多次配置萬用字元埠，藉以達到本機埠的擴充性。</span><span class="sxs-lookup"><span data-stu-id="66eca-107">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability by allowing port allocation to be maximized by allocating wildcard ports multiple times for different local address port pairs on a local machine.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66eca-108">備註</span><span class="sxs-lookup"><span data-stu-id="66eca-108">Remarks</span></span>

<span data-ttu-id="66eca-109">注意：在同時 \_ 支援埠擴充 \_ 性和 \_ 重複使用 UNICASTPORT 的平臺上 \_ ，最好使用，以 \_ 重複使用 \_ UNICASTPORT。</span><span class="sxs-lookup"><span data-stu-id="66eca-109">Note: on platforms where both SO\_PORT\_SCALABILITY and SO\_REUSE\_UNICASTPORT are supported, prefer to use SO\_REUSE\_UNICASTPORT.</span></span>

<span data-ttu-id="66eca-110">由於本機埠的可用性有限，因此 Proxy 伺服器環境有擴充性問題。</span><span class="sxs-lookup"><span data-stu-id="66eca-110">Proxy server environments have scalability issues because of limited local port availability.</span></span> <span data-ttu-id="66eca-111">解決此問題的方法之一是將更多 IP 位址新增至電腦。</span><span class="sxs-lookup"><span data-stu-id="66eca-111">One way to work around this is to add more IP addresses to the machine.</span></span> <span data-ttu-id="66eca-112">不過，根據預設，搭配 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) 函式使用的萬用字元埠會限制為本機電腦上動態埠範圍的大小 (最多64k 的埠，但在本機電腦上的 IP 位址數目通常較不) 。</span><span class="sxs-lookup"><span data-stu-id="66eca-112">However, by default wildcard ports used with the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function are limited to the size of the dynamic port range on the local machine (up to 64K ports, but usually less) no matter the number of IP addresses on the local machine.</span></span> <span data-ttu-id="66eca-113">解決此問題需要應用程式以埠保留或使用啟發學習法來維護其本身的埠集區。</span><span class="sxs-lookup"><span data-stu-id="66eca-113">Working around this requires the application to maintain its own port pool either with port reservation or by using heuristics.</span></span>

<span data-ttu-id="66eca-114">為了避免每個需要擴充的應用程式都能管理自己的埠集區，並允許更大的擴充性，同時維持應用程式相容性，Windows Server 2008 引進了「 **\_ 埠擴充 \_ 性** 通訊端」選項，可協助您最大化萬用字元埠配置。</span><span class="sxs-lookup"><span data-stu-id="66eca-114">To avoid having every application that requires scalability manage its own port pool, and to allow for greater scalability while maintaining application compatibility, Windows Server 2008 introduced the **SO\_PORT\_SCALABILITY** socket option to help maximize wildcard port allocation.</span></span> <span data-ttu-id="66eca-115">埠配置可讓應用程式針對每個唯一的本機位址和埠配對配置萬用字元埠，藉以達到最大效益。</span><span class="sxs-lookup"><span data-stu-id="66eca-115">Port allocation is maximized by allowing an application to allocate wildcard ports for each unique local address and port pair.</span></span> <span data-ttu-id="66eca-116">因此，如果本機電腦有四個 IP 位址，則可以使用萬用字元系結函式要求配置最多 256 K [**個萬用字元埠**](/windows/desktop/api/winsock/nf-winsock-bind) (64 k 埠×4個 ip 位址) 。</span><span class="sxs-lookup"><span data-stu-id="66eca-116">So if a local machine has four IP addresses, then up to 256 K wildcard ports (64 K ports × 4 IP addresses) can be allocated by wildcard [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function requests.</span></span>

<span data-ttu-id="66eca-117">在通訊端上設定 **SO \_ 埠 \_** 擴充通訊端選項，且對 [**指定的位址**](/windows/desktop/api/winsock/nf-winsock-bind) 和萬用字元埠進行系結函式的呼叫時 (*名稱* 參數設定為特定位址，埠為 0) ，Winsock 將配置指定位址的埠。</span><span class="sxs-lookup"><span data-stu-id="66eca-117">When the **SO\_PORT\_SCALABILITY** socket option is set on a socket and a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is made for a specified address and wildcard port (the *name* parameter is set with a specific address and a port of 0), Winsock will allocate a port for the specified address.</span></span> <span data-ttu-id="66eca-118">此配置會以本機電腦上的所有可能 IP 位址和埠/每個位址為基礎。</span><span class="sxs-lookup"><span data-stu-id="66eca-118">This allocation will be based on all of the possible IP addresses and ports/per address on the local computer.</span></span> <span data-ttu-id="66eca-119">如果使用 [ **\_ 埠擴充 \_ 性** ] 選項來取得萬用字元埠，則無法由另一個通訊端配置該埠，而不需要使用 [ **埠擴充 \_ \_ 性** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="66eca-119">If a wildcard port is acquired using the **SO\_PORT\_SCALABILITY** option, that port cannot be allocated by another socket without the **SO\_PORT\_SCALABILITY** option.</span></span> <span data-ttu-id="66eca-120">這項限制是為了避免應用程式的回溯相容性問題，而這些應用程式無法重複使用萬用字元本機埠。</span><span class="sxs-lookup"><span data-stu-id="66eca-120">This restriction is in place to avoid backward-compatibility problems with applications that assume a wildcard local port cannot be reused.</span></span> <span data-ttu-id="66eca-121">請注意，這表示使用的 **\_ 埠擴充 \_ 性** 取得大量埠的應用程式，可以使舊版的埠應用程式。</span><span class="sxs-lookup"><span data-stu-id="66eca-121">Note that this means that applications which acquire a large number of ports using **SO\_PORT\_SCALABILITY** can starve legacy applications of ports.</span></span> <span data-ttu-id="66eca-122">如果已針對至少一個位址取得 **\_ 埠擴充 \_ 性** 的所有可用暫時埠，則沒有通訊端選項，就無法再進行任何萬用字元配置。</span><span class="sxs-lookup"><span data-stu-id="66eca-122">If all available ephemeral ports have been acquired for at least one address with **SO\_PORT\_SCALABILITY** , then no more wildcard port allocations are possible without the socket option.</span></span>

<span data-ttu-id="66eca-123">若要有任何效果 [**，在呼叫**](/windows/desktop/api/winsock/nf-winsock-bind)系結函式之前，必須先設定 **SO 埠的擴充 \_ \_ 性** 選項。</span><span class="sxs-lookup"><span data-stu-id="66eca-123">To have any effect, the **SO\_PORT\_SCALABILITY** option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called.</span></span> <span data-ttu-id="66eca-124">在具有兩個位址的電腦上使用此方式的範例如下所示：</span><span class="sxs-lookup"><span data-stu-id="66eca-124">An example of how this would be used on a computer with two addresses is outlined below:</span></span>

-   <span data-ttu-id="66eca-125">處理常式會呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函數來建立通訊端。</span><span class="sxs-lookup"><span data-stu-id="66eca-125">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by a process to create a socket.</span></span>
-   <span data-ttu-id="66eca-126">呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式，以啟用新建立之通訊端上的「 **\_ 埠擴充 \_ 性** 通訊端」選項。</span><span class="sxs-lookup"><span data-stu-id="66eca-126">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created socket.</span></span>
-   <span data-ttu-id="66eca-127">呼叫[](/windows/desktop/api/winsock/nf-winsock-bind)系結函式，以便在其中一個本機電腦的 IP 位址和埠0上進行系結。</span><span class="sxs-lookup"><span data-stu-id="66eca-127">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called to do a bind on one of the local computer's IP addresses and port 0.</span></span>
-   <span data-ttu-id="66eca-128">接著會呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式以連接到遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="66eca-128">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="66eca-129">應用程式會視需要使用通訊端。</span><span class="sxs-lookup"><span data-stu-id="66eca-129">The socket is used by the application as needed.</span></span>
-   <span data-ttu-id="66eca-130">[**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket)函式是由相同的進程呼叫 (可能是不同的執行緒) 來建立第二個通訊端。</span><span class="sxs-lookup"><span data-stu-id="66eca-130">A [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by the same process (possibly a different thread) to create a second socket.</span></span>
-   <span data-ttu-id="66eca-131">呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式，以在新建立的第二通訊端上啟用「 **\_ 埠 \_** 擴充通訊端」選項。</span><span class="sxs-lookup"><span data-stu-id="66eca-131">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created second socket.</span></span>
-   <span data-ttu-id="66eca-132">使用本機電腦的第二個 IP 位址和埠0呼叫系 [**結函數。**](/windows/desktop/api/winsock/nf-winsock-bind)</span><span class="sxs-lookup"><span data-stu-id="66eca-132">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called with the local computer's second IP address and port 0.</span></span> <span data-ttu-id="66eca-133">即使先前已配置所有埠，此呼叫也會成功，因為本機電腦上有多個可用的 IP 位址，而且在相同的進程中，同時在這兩個通訊端上設定了 **\_ 埠 \_** 擴充通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="66eca-133">Even when all ports have been previously allocated, this call succeeds because there are multiple IP addresses available on the local computer and the **SO\_PORT\_SCALABILITY** socket option was set on both sockets in the same process.</span></span>
-   <span data-ttu-id="66eca-134">接著會呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式以連接到遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="66eca-134">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="66eca-135">應用程式會視需要使用第二個通訊端。</span><span class="sxs-lookup"><span data-stu-id="66eca-135">The second socket is used by the application as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="66eca-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="66eca-136">Requirements</span></span>



| <span data-ttu-id="66eca-137">需求</span><span class="sxs-lookup"><span data-stu-id="66eca-137">Requirement</span></span> | <span data-ttu-id="66eca-138">值</span><span class="sxs-lookup"><span data-stu-id="66eca-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66eca-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66eca-139">Minimum supported client</span></span><br/> | <span data-ttu-id="66eca-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="66eca-140">None supported</span></span><br/>                                                           |
| <span data-ttu-id="66eca-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66eca-141">Minimum supported server</span></span><br/> | <span data-ttu-id="66eca-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66eca-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="66eca-143">標頭</span><span class="sxs-lookup"><span data-stu-id="66eca-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="66eca-144"><dt>Ws2def。h</dt></span><span class="sxs-lookup"><span data-stu-id="66eca-144"><dt>Ws2def.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66eca-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66eca-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66eca-146">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="66eca-146">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="66eca-147">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="66eca-147">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="66eca-148">**SOL \_ 通訊端通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="66eca-148">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="66eca-149">**通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="66eca-149">**Socket Options**</span></span>](socket-options.md)
</dt> </dl>

 

 




