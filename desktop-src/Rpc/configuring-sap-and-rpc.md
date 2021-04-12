---
title: 設定 SAP 和 RPC
description: Novell NetWare network 伺服器使用 (SAP) 的服務廣告通訊協定，將網路上可用服務的相關資訊廣播至其他網路裝置。
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385d60168a52cbe5d31368959ec4f21d52f9ad80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/15/2019
ms.locfileid: "104372718"
---
# <a name="configuring-sap-and-rpc"></a><span data-ttu-id="ae9dd-103">設定 SAP 和 RPC</span><span class="sxs-lookup"><span data-stu-id="ae9dd-103">Configuring SAP and RPC</span></span>

<span data-ttu-id="ae9dd-104">Novell NetWare network 伺服器使用 (SAP) 的服務廣告通訊協定，將網路上可用服務的相關資訊廣播至其他網路裝置。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-104">Novell NetWare network servers use the Service Advertising Protocol (SAP) to broadcast information about available services on the network to other networked devices.</span></span> <span data-ttu-id="ae9dd-105">伺服器可能會每隔60秒傳送一次 SAP 廣播，以通知其他網路裝置所提供的服務。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-105">A server may send out an SAP broadcast every 60 seconds to inform other network devices about the services it offers.</span></span> <span data-ttu-id="ae9dd-106">工作站會使用 Sap 來尋找網路上所需的服務。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-106">Workstations use SAPs to find services they need on the network.</span></span>

<span data-ttu-id="ae9dd-107">Windows 包含 SAP 代理程式服務，可讓 Windows 伺服器與 NetWare 伺服器互動。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-107">Windows includes a SAP Agent service to enable Windows-based servers to interact with NetWare servers.</span></span> <span data-ttu-id="ae9dd-108">SAP 代理程式服務會在伺服器上安裝並執行的 IPX 服務，接聽網路用戶端的 SAP 要求。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-108">The SAP Agent service will listen for network clients' SAP requests for IPX-based services that are installed and running on the server.</span></span>

<span data-ttu-id="ae9dd-109">設計成透過網路以服務方式公告的軟體（透過 SAP 廣播）將會每隔60秒發出 SAP 公告，而不會安裝 SAP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-109">Software that is designed to be advertised as a service over the network by means of a SAP broadcast will issue the SAP announcements every 60 seconds, without having the SAP Agent installed.</span></span> <span data-ttu-id="ae9dd-110">不過，為了讓網路用戶端快速找出 IPX 網路服務，維護服務資料庫的伺服器必須可在網路上使用，以回應服務位置要求。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-110">However, in order for network clients to quickly locate an IPX network service, a server that maintains a service database must be available on the network, to respond to the service location request.</span></span> <span data-ttu-id="ae9dd-111">此服務資料庫通常由 Novell NetWare 或受 NetWare 相容的伺服器維護。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-111">This service database is usually maintained by a Novell NetWare or by a NetWare compatible server.</span></span> <span data-ttu-id="ae9dd-112">適用于 NetWare 的 Microsoft 檔案和列印服務也會維護一個 IPX network service 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-112">Microsoft File and Print Services for NetWare will also maintain an IPX network service database.</span></span>

<span data-ttu-id="ae9dd-113">在執行 Windows Server 的電腦上，如果已安裝適用于 NetWare 的閘道服務 (GSNW) ，則 SAP 類型640會在遠端程序呼叫 (RPC) 服務的每60秒廣播。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-113">On a computer running Windows Server, if Gateway Services for NetWare (GSNW) is installed, a SAP Type 640 will broadcast every 60 seconds by the remote procedure call (RPC) service.</span></span> <span data-ttu-id="ae9dd-114">即使使用者停用 GSNW 和 SAP 代理程式服務，也會繼續進行此 SAP 廣播。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-114">This SAP broadcast will continue even if the user disables the GSNW and the SAP Agent Service.</span></span>

<span data-ttu-id="ae9dd-115">如果用戶端服務 for NetWare (CSNW) 和 SAP 代理程式服務已安裝，RPC 服務將會進行 SAP 廣播。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-115">The RPC service will do the SAP broadcast if the Client Services for NetWare (CSNW) and the SAP Agent service are installed.</span></span> <span data-ttu-id="ae9dd-116">即使使用者停用 SAP 代理程式，也會繼續進行此 SAP 廣播。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-116">This SAP broadcast will continue even if the user disables the SAP agent.</span></span>

<span data-ttu-id="ae9dd-117">根據預設，RPC 服務會檢查是否有適用于 NetWare 的閘道服務，以及執行 Windows Server 之電腦上的 SAP 代理程式服務。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-117">By default, the RPC service will check for the presence of Gateway Services for NetWare and the SAP Agent service on the computer running Windows Server.</span></span> <span data-ttu-id="ae9dd-118">安裝適用于 NetWare 的檔案和列印服務，會安裝 SAP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-118">Installing File and Print services for NetWare installs a SAP Agent.</span></span>

<span data-ttu-id="ae9dd-119">在使用 CSNW 執行用戶端版本 Windows 的電腦上，RPC 服務會檢查 SAP 代理程式服務。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-119">On the computer running a client version of Windows with CSNW, the RPC service checks for the SAP Agent service.</span></span> <span data-ttu-id="ae9dd-120">如果服務存在，RPC 將會啟動自己的執行緒，每分鐘都會進行 SAP 廣播類型640。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-120">If the services are present, RPC will start its own thread that will do the SAP broadcast Type 640 every minute.</span></span>

> [!NOTE]
> <span data-ttu-id="ae9dd-121">如果您不想要在網路上每隔60秒進行 SAP 廣播，則可以使用登錄編輯程式停用 SAP 廣播。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-121">If you don't want SAP broadcasts on the network every 60 seconds, you can disable SAP broadcasts using the Registry Editor.</span></span> <span data-ttu-id="ae9dd-122">請注意，使用登錄編輯程式不正確可能會導致嚴重問題，而可能需要您重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-122">Be warned that using Registry Editor incorrectly can cause serious problems that may require you to reinstall your operating system.</span></span> <span data-ttu-id="ae9dd-123">Microsoft 無法保證可以解決因不當使用登錄編輯程式所造成的問題。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-123">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="ae9dd-124">您必須自行負擔使用「登錄編輯程式」的風險。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-124">Use Registry Editor at your own risk.</span></span> <span data-ttu-id="ae9dd-125">您應該先備份登錄，然後再進行編輯。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-125">You should back up the registry before you edit it.</span></span>

 

<span data-ttu-id="ae9dd-126">**若要設定 SAP**</span><span class="sxs-lookup"><span data-stu-id="ae9dd-126">**To configure for SAP**</span></span>

1.  <span data-ttu-id="ae9dd-127">執行登錄編輯程式 (Regedt32.exe) 並移至登錄中的下列機碼：</span><span class="sxs-lookup"><span data-stu-id="ae9dd-127">Run Registry Editor (Regedt32.exe) and go to the following key in the registry:</span></span>

    <span data-ttu-id="ae9dd-128">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ RPC**</span><span class="sxs-lookup"><span data-stu-id="ae9dd-128">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\RPC**</span></span>

2.  <span data-ttu-id="ae9dd-129">在 [ **編輯** ] 功能表上，按一下 [ **新增值**]，然後使用下列專案：</span><span class="sxs-lookup"><span data-stu-id="ae9dd-129">On the **Edit** menu, click **Add Value**, and use the following entry:</span></span>
    1.  <span data-ttu-id="ae9dd-130">值名稱： AdvertiseRpcService</span><span class="sxs-lookup"><span data-stu-id="ae9dd-130">Value Name: AdvertiseRpcService</span></span>
    2.  <span data-ttu-id="ae9dd-131">資料類型： REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="ae9dd-131">Data Type: REG\_SZ</span></span>
    3.  <span data-ttu-id="ae9dd-132">字串：否</span><span class="sxs-lookup"><span data-stu-id="ae9dd-132">String: No</span></span>
3.  <span data-ttu-id="ae9dd-133">針對字串使用 No 會關閉 RPC SAP 廣播。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-133">Using No for the string turns RPC SAP broadcasting off.</span></span> <span data-ttu-id="ae9dd-134">針對字串使用 Yes 可將 RPC SAP 廣播開啟。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-134">Using Yes for the string turns RPC SAP broadcasting on.</span></span>
4.  <span data-ttu-id="ae9dd-135">重新開機電腦，登錄變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-135">Restart the computer for the registry change to take effect.</span></span>
    > [!NOTE]
    > <span data-ttu-id="ae9dd-136">如果在遵循這些步驟之後，SAP 廣播繼續進行，您可能會想要嘗試進行疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-136">If the SAP broadcasts continue after following these steps, you may want to try a troubleshooting step.</span></span> <span data-ttu-id="ae9dd-137">刪除下列登錄機碼中的 **Ncacn \_ spx** 字串值：</span><span class="sxs-lookup"><span data-stu-id="ae9dd-137">Delete the **Ncacn\_spx** string value in the following registry key:</span></span>
    >
    > <span data-ttu-id="ae9dd-138">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Rpc \\ ServerProtocols\\**</span><span class="sxs-lookup"><span data-stu-id="ae9dd-138">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc\\ServerProtocols\\**</span></span>

     

> [!NOTE]  
> <span data-ttu-id="ae9dd-139">這應該只用來作為疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-139">This should be used only as a troubleshooting step.</span></span> <span data-ttu-id="ae9dd-140">刪除此字串值會完全停用 SAP 廣播，而某些程式可能需要這些廣播才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="ae9dd-140">Deleting this string value completely disables SAP broadcasts which some programs may need in order to function properly.</span></span>