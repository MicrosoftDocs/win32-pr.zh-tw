---
title: 關於網路清單管理員 API
description: 關於網路清單管理員 API
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675259"
---
# <a name="about-the-network-list-manager-api"></a><span data-ttu-id="8c66a-103">關於網路清單管理員 API</span><span class="sxs-lookup"><span data-stu-id="8c66a-103">About the Network List Manager API</span></span>

<span data-ttu-id="8c66a-104">Microsoft Windows 網路環境可讓多重主目錄電腦同時連線到多個網路。</span><span class="sxs-lookup"><span data-stu-id="8c66a-104">The Microsoft Windows networking environment allows multihomed computers to connect to several networks simultaneously.</span></span> <span data-ttu-id="8c66a-105">可能有多個無線網路可用，以及區域網路和撥號連線。</span><span class="sxs-lookup"><span data-stu-id="8c66a-105">There may be multiple wireless networks available along with LAN and dial-up connections.</span></span> <span data-ttu-id="8c66a-106">網路清單管理員會識別可用的網路，並將網路屬性資料傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c66a-106">Network List Manager identifies available networks and returns network attribute data to the application.</span></span>

<span data-ttu-id="8c66a-107">網路清單管理員 API 會與網路清單管理員服務互動，以找出並抓取電腦所連線之每個網路的屬性。</span><span class="sxs-lookup"><span data-stu-id="8c66a-107">The Network List Manager API interacts with the Network List Manager service to identify and retrieve properties of each network that the PC connects to.</span></span> <span data-ttu-id="8c66a-108">每個網路都會使用網路簽章來唯一識別，並以該網路的可唯一識別屬性為基礎。</span><span class="sxs-lookup"><span data-stu-id="8c66a-108">Each network is uniquely identified with a network signature based on the uniquely identifiable properties of that network.</span></span> <span data-ttu-id="8c66a-109">當應用程式註冊網路清單管理員通知時，應用程式會收到新網路連線可用性或現有網路連線變更的相關通知。</span><span class="sxs-lookup"><span data-stu-id="8c66a-109">When an application registers for Network List Manager notifications, the application receives notifications about the availability of new network connections or changes to existing network connections.</span></span> <span data-ttu-id="8c66a-110">應用程式可以根據下列程式來調整其邏輯：它們所連線的網路：它們所連線的網路連接;或網路屬性的內容。</span><span class="sxs-lookup"><span data-stu-id="8c66a-110">Applications can adjust their logic depending on: which network they are connected to; which network connection they are connected to; or what the network properties are.</span></span> <span data-ttu-id="8c66a-111">透過此資訊，應用程式可以根據目前的網路狀況微調其動作</span><span class="sxs-lookup"><span data-stu-id="8c66a-111">With this information applications can fine tune their actions based on current network conditions</span></span>

<span data-ttu-id="8c66a-112">Windows Vista 引進了新的介面，可用來取得這些網路特性及更多的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8c66a-112">Windows Vista introduces new interfaces that can be used to obtain detailed information about these network characteristics and more.</span></span> <span data-ttu-id="8c66a-113">有了 [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) 介面，您就可以輕鬆地列舉所有網路 ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) 電腦上的所有網路，或只是連線的網路，或只是已中斷連線的網路。</span><span class="sxs-lookup"><span data-stu-id="8c66a-113">With the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface it is easy to enumerate all networks ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) a computer has ever seen, or just the connected networks, or just the disconnected networks.</span></span> <span data-ttu-id="8c66a-114">**INetworkListManager** 介面也可讓您輕鬆地列舉電腦上的網路介面。</span><span class="sxs-lookup"><span data-stu-id="8c66a-114">The **INetworkListManager** interface also makes it easy to enumerate the network interfaces on a computer.</span></span>

<span data-ttu-id="8c66a-115">[**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)介面是用來判斷網路連線的屬性：名稱、描述、識別碼、受管理/已驗證、連線/中斷連線等等。</span><span class="sxs-lookup"><span data-stu-id="8c66a-115">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface is used to determine the properties of a network connection: name, description, ID, managed/authenticated, connected/disconnected, and more.</span></span> <span data-ttu-id="8c66a-116">單一網路可能會連接到數個介面，因此透過 **INetwork** 介面，您也可以列舉正在使用之 **INetwork** 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="8c66a-116">It is possible that a single network is connected to several interfaces, so through an **INetwork** interface you can also enumerate the instances of the **INetwork** interface being used.</span></span>

<span data-ttu-id="8c66a-117">[**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)介面會告訴您介面的相關屬性：識別碼、GUID、類型 (受控、已驗證的) ，以及狀態 (連線、中斷連線、V4 本機、V4 網際網路、v6 本機、v6 網際網路) 。</span><span class="sxs-lookup"><span data-stu-id="8c66a-117">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface tells you the relevant properties of an interface: ID, GUID, Type (managed, authenticated), and State (connected, disconnected, V4 Local, V4 Internet, V6 Local, V6 Internet).</span></span> <span data-ttu-id="8c66a-118">V4 區域表示第四版網際網路協定 (IPv4) 本機存取。</span><span class="sxs-lookup"><span data-stu-id="8c66a-118">V4 Local means Internet Protocol version 4 (IPv4) local access.</span></span> <span data-ttu-id="8c66a-119">V4 網際網路指的是 IPv4 與網際網路的存取。</span><span class="sxs-lookup"><span data-stu-id="8c66a-119">V4 Internet means IPv4 with internet access.</span></span> <span data-ttu-id="8c66a-120">V6 本機和 V6 網際網路平均 IPv6。</span><span class="sxs-lookup"><span data-stu-id="8c66a-120">V6 Local and V6 Internet mean IPv6.</span></span>

<span data-ttu-id="8c66a-121">網路位置的物件樹狀結構根目錄是 [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="8c66a-121">The root of the object tree for Network Location is the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface.</span></span> <span data-ttu-id="8c66a-122">此介面會在 **CLSID \_ NetworkListManager** coclass 上執行。</span><span class="sxs-lookup"><span data-stu-id="8c66a-122">This interface is implemented on the **CLSID\_NetworkListManager** coclass.</span></span> <span data-ttu-id="8c66a-123">若要使用此介面，您必須建立 NetworkListManager COM 物件的 **CLSID \_** ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8c66a-123">In order to use this interface, it is necessary to create the **CLSID\_NetworkListManager** COM object as demonstrated:</span></span>


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




