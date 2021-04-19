---
title: 伺服器和工作站傳輸功能
description: 網路管理伺服器和工作站傳輸功能可處理傳輸通訊協定與伺服器和重新導向程式之間的系結和解除系結。
ms.assetid: 64342e21-98f1-42d3-b541-46b826391fad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1ab4a4ce5dcc3b887eb9eb9d5759db89dfed55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967416"
---
# <a name="server-and-workstation-transport-functions"></a><span data-ttu-id="90ca2-103">伺服器和工作站傳輸功能</span><span class="sxs-lookup"><span data-stu-id="90ca2-103">Server and Workstation Transport Functions</span></span>

<span data-ttu-id="90ca2-104">網路管理伺服器和工作站傳輸功能可處理傳輸通訊協定與伺服器和重新導向程式之間的系結和解除系結。</span><span class="sxs-lookup"><span data-stu-id="90ca2-104">The network management server and workstation transport functions handle binding and unbinding of transport protocols to and from the server and redirector.</span></span> <span data-ttu-id="90ca2-105">伺服器傳輸功能會處理由伺服器管理的傳輸通訊協定;工作站傳輸功能會處理由重新導向程式管理的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-105">The server transport functions deal with transport protocols managed by the server; the workstation transport functions deal with transport protocols managed by the redirector.</span></span>

<span data-ttu-id="90ca2-106">傳輸裝置與伺服器之間的檔案共用有兩個元件：</span><span class="sxs-lookup"><span data-stu-id="90ca2-106">File sharing between a transport device and a server has two components:</span></span>

-   <span data-ttu-id="90ca2-107">檔案所在的伺服器電腦</span><span class="sxs-lookup"><span data-stu-id="90ca2-107">The server computer where the files reside</span></span>
-   <span data-ttu-id="90ca2-108">存取檔案 (SMB) 用戶端的伺服器訊息區</span><span class="sxs-lookup"><span data-stu-id="90ca2-108">A Server Message Block (SMB) client that accesses the files</span></span>

<span data-ttu-id="90ca2-109">用戶端電腦會使用傳輸通訊協定，透過區域網路與伺服器電腦進行通訊;例如，TCP 或 XNS。</span><span class="sxs-lookup"><span data-stu-id="90ca2-109">The client computer communicates with the server computer over a local area network using a transport protocol; for example, TCP or XNS.</span></span> <span data-ttu-id="90ca2-110">用戶端會將要求傳送到伺服器以取得資料。</span><span class="sxs-lookup"><span data-stu-id="90ca2-110">The client sends requests to the server to retrieve data.</span></span> <span data-ttu-id="90ca2-111">用戶端電腦上產生檔案要求的軟體稱為重新導向器， *因為它* 會將本機檔案要求重新導向至伺服器電腦。</span><span class="sxs-lookup"><span data-stu-id="90ca2-111">The software on the client computer that generates the file requests is called the *redirector* because it redirects local file requests to the server computer.</span></span> <span data-ttu-id="90ca2-112">電腦上接收和操作檔案要求的軟體稱為「 *伺服器* 」，因為它會為用戶端提供服務。</span><span class="sxs-lookup"><span data-stu-id="90ca2-112">The software on the computer that receives and acts on the file requests is called the *server* because it serves the clients.</span></span> <span data-ttu-id="90ca2-113">這些要求的特定格式稱為 SMB 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-113">The format specific to these requests is called the SMB protocol.</span></span>

<span data-ttu-id="90ca2-114">伺服器傳輸函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="90ca2-114">The server transport functions are listed following.</span></span>



| <span data-ttu-id="90ca2-115">函式</span><span class="sxs-lookup"><span data-stu-id="90ca2-115">Function</span></span>                                                     | <span data-ttu-id="90ca2-116">描述</span><span class="sxs-lookup"><span data-stu-id="90ca2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90ca2-117">**NetServerComputerNameAdd**</span><span class="sxs-lookup"><span data-stu-id="90ca2-117">**NetServerComputerNameAdd**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | <span data-ttu-id="90ca2-118">將模擬的伺服器名稱系結至伺服器使用中的每個傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-118">Binds an emulated server name to each of the transport protocols on which a server is active.</span></span> <span data-ttu-id="90ca2-119"> (結合 [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) 函式和 [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) 函數的功能。 ) </span><span class="sxs-lookup"><span data-stu-id="90ca2-119">(Combines the functionality of the [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) function and the [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) function.)</span></span>                                            |
| [<span data-ttu-id="90ca2-120">**NetServerComputerNameDel**</span><span class="sxs-lookup"><span data-stu-id="90ca2-120">**NetServerComputerNameDel**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | <span data-ttu-id="90ca2-121">將每個網路傳輸通訊協定與先前呼叫 **NetServerComputerNameAdd** 函式所設定的模擬伺服器名稱中斷連線。</span><span class="sxs-lookup"><span data-stu-id="90ca2-121">Disconnects each network transport protocol from an emulated server name set by a previous call to the **NetServerComputerNameAdd** function.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="90ca2-122">**NetServerTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="90ca2-122">**NetServerTransportAdd**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | <span data-ttu-id="90ca2-123">將指定的伺服器系結至傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-123">Binds the specified server to the transport protocol.</span></span> <span data-ttu-id="90ca2-124"> (此函式只支援 [**伺服器 \_ 傳輸 \_ 資訊 \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) 資訊層級。 ) </span><span class="sxs-lookup"><span data-stu-id="90ca2-124">(This function supports only the [**SERVER\_TRANSPORT\_INFO\_0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) information level.)</span></span>                                                                                                                                                |
| [<span data-ttu-id="90ca2-125">**NetServerTransportAddEx**</span><span class="sxs-lookup"><span data-stu-id="90ca2-125">**NetServerTransportAddEx**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | <span data-ttu-id="90ca2-126">將指定的伺服器系結至傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-126">Binds the specified server to the transport protocol.</span></span> <span data-ttu-id="90ca2-127"> (此擴充功能可支援 [**伺服器 \_ 傳輸 \_ 資訊 \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)、 [**伺服器 \_ 傳輸 \_ 資訊 \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)和 [**伺服器 \_ 傳輸資訊 \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) 資訊層級。 ) </span><span class="sxs-lookup"><span data-stu-id="90ca2-127">(This extended function supports the [**SERVER\_TRANSPORT\_INFO\_1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**SERVER\_TRANSPORT\_INFO\_2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2), and [**SERVER\_TRANSPORT\_INFO\_3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) information levels.)</span></span> |
| [<span data-ttu-id="90ca2-128">**NetServerTransportDel**</span><span class="sxs-lookup"><span data-stu-id="90ca2-128">**NetServerTransportDel**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | <span data-ttu-id="90ca2-129">中斷傳輸通訊協定與伺服器的連線。</span><span class="sxs-lookup"><span data-stu-id="90ca2-129">Disconnects the transport protocol from the server.</span></span>                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="90ca2-130">**NetServerTransportEnum**</span><span class="sxs-lookup"><span data-stu-id="90ca2-130">**NetServerTransportEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | <span data-ttu-id="90ca2-131">列舉伺服器所管理的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-131">Enumerates the transport protocols managed by the server.</span></span>                                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="90ca2-132">您可以從下列資訊層級取得伺服器傳輸功能：</span><span class="sxs-lookup"><span data-stu-id="90ca2-132">Server transport functions are available at the following information levels:</span></span>

-   [<span data-ttu-id="90ca2-133">**伺服器 \_ 傳輸 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="90ca2-133">**SERVER\_TRANSPORT\_INFO\_0**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)
-   [<span data-ttu-id="90ca2-134">**伺服器 \_ 傳輸 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="90ca2-134">**SERVER\_TRANSPORT\_INFO\_1**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)
-   [<span data-ttu-id="90ca2-135">**伺服器 \_ 傳輸 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="90ca2-135">**SERVER\_TRANSPORT\_INFO\_2**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)
-   [<span data-ttu-id="90ca2-136">**伺服器 \_ 傳輸 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="90ca2-136">**SERVER\_TRANSPORT\_INFO\_3**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3)

<span data-ttu-id="90ca2-137">工作站傳輸功能會對工作站執行對等的作業。</span><span class="sxs-lookup"><span data-stu-id="90ca2-137">The workstation transport functions perform equivalent operations for the workstation.</span></span>

<span data-ttu-id="90ca2-138">**Windows Server 2003 和 WINDOWS XP/2000：** 重新導向器不支援 [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd) 函數或 [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel) 函數。</span><span class="sxs-lookup"><span data-stu-id="90ca2-138">**Windows Server 2003 and Windows XP/2000:** The redirector does not support the [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd) function or the [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel) function.</span></span> <span data-ttu-id="90ca2-139">您可以透過 [**網路和撥號連線**] 資料夾中的 [**本機區域** 線上內容] 對話方塊，手動變更傳輸通訊協定的預設設定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-139">You can change the default settings for transport protocols manually through the **Local Area Connection Properties** dialog box in the **Network and Dial-Up Connections** folder.</span></span>

<span data-ttu-id="90ca2-140">工作站傳輸功能如下所示。</span><span class="sxs-lookup"><span data-stu-id="90ca2-140">The workstation transport functions are listed following.</span></span>



| <span data-ttu-id="90ca2-141">函式</span><span class="sxs-lookup"><span data-stu-id="90ca2-141">Function</span></span>                                               | <span data-ttu-id="90ca2-142">描述</span><span class="sxs-lookup"><span data-stu-id="90ca2-142">Description</span></span>                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="90ca2-143">**NetWkstaTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="90ca2-143">**NetWkstaTransportAdd**</span></span>](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)   | <span data-ttu-id="90ca2-144">將重新導向程式連接至傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-144">Connects the redirector to the transport protocol.</span></span>                |
| [<span data-ttu-id="90ca2-145">**NetWkstaTransportDel**</span><span class="sxs-lookup"><span data-stu-id="90ca2-145">**NetWkstaTransportDel**</span></span>](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)   | <span data-ttu-id="90ca2-146">中斷傳輸通訊協定與重新導向器的連線。</span><span class="sxs-lookup"><span data-stu-id="90ca2-146">Disconnects the transport protocol from the redirector.</span></span>           |
| [<span data-ttu-id="90ca2-147">**NetWkstaTransportEnum**</span><span class="sxs-lookup"><span data-stu-id="90ca2-147">**NetWkstaTransportEnum**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum) | <span data-ttu-id="90ca2-148">列出由重新導向程式管理的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90ca2-148">Lists the transport protocols that are managed by the redirector.</span></span> |



 

<span data-ttu-id="90ca2-149">工作站傳輸功能可在一個資訊層級使用：</span><span class="sxs-lookup"><span data-stu-id="90ca2-149">Workstation transport functions are available at one information level:</span></span>

-   [<span data-ttu-id="90ca2-150">**WKSTA \_ 傳輸 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="90ca2-150">**WKSTA\_TRANSPORT\_INFO\_0**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_transport_info_0)

 

 




