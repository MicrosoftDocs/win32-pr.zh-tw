---
title: '應用層強制 (ALE) '
description: ALE 是一組 Windows 篩選平台 (WFP) 用於可設定狀態之篩選的核心模式層。
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375220"
---
# <a name="application-layer-enforcement-ale"></a><span data-ttu-id="1be2c-103">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="1be2c-103">Application Layer Enforcement (ALE)</span></span>

<span data-ttu-id="1be2c-104">ALE 是一組 Windows 篩選平台 (WFP) 用於可設定狀態之篩選的核心模式層。</span><span class="sxs-lookup"><span data-stu-id="1be2c-104">ALE is a set of Windows Filtering Platform (WFP) kernel-mode layers that are used for stateful filtering.</span></span>

<span data-ttu-id="1be2c-105">可設定狀態的篩選會追蹤網路連接的狀態，並只允許符合已知連接狀態的封包。</span><span class="sxs-lookup"><span data-stu-id="1be2c-105">Stateful filtering keeps track of the state of network connections and allows only packets that match a known connection state.</span></span> <span data-ttu-id="1be2c-106">例如，從防火牆後方起始之 TCP 連線的可設定狀態篩選，只允許符合受保護的合作物件所傳送之先前傳出封包的傳入封包。</span><span class="sxs-lookup"><span data-stu-id="1be2c-106">For example, stateful filtering for a TCP connection initiated from behind a firewall can allow only incoming packets that match previous outgoing packets sent by the party protected.</span></span>

<span data-ttu-id="1be2c-107">ALE 層中的篩選準則會授權輸入和輸出連線的建立、通訊埠指派、如 [**接聽 ()**](/windows/desktop/api/winsock2/nf-winsock2-listen)、原始通訊端建立和混合模式接收的通訊端作業。</span><span class="sxs-lookup"><span data-stu-id="1be2c-107">Filters in the ALE layers authorize inbound and outbound connection creation, port assignments, socket operations such as [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen), raw socket creation, and promiscuous mode receiving.</span></span>

<span data-ttu-id="1be2c-108">ALE 層的流量是依每一連線或每個通訊端作業分類。</span><span class="sxs-lookup"><span data-stu-id="1be2c-108">Traffic at the ALE layers is classified either per-connection or per-socket operation.</span></span> <span data-ttu-id="1be2c-109">在非 ALE 層級，篩選準則只能針對每個封包分類流量。</span><span class="sxs-lookup"><span data-stu-id="1be2c-109">At non-ALE layers, filters can only classify traffic on a per-packet basis.</span></span>

<span data-ttu-id="1be2c-110">ALE 層是唯一可用來根據應用程式識別（使用正規化的檔案名）或根據使用者身分識別（使用安全描述項）來篩選網路流量的 WFP 層。</span><span class="sxs-lookup"><span data-stu-id="1be2c-110">ALE layers are the only WFP layers where network traffic can be filtered based on the application identity—using a normalized file name—and based on the user identity—using a security descriptor.</span></span> <span data-ttu-id="1be2c-111">如需有關 \_ \_ \_ 正規化檔案名的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 檔中的 FLT 檔案名資訊 (。 ) </span><span class="sxs-lookup"><span data-stu-id="1be2c-111">(See FLT\_FILE\_NAME\_INFORMATION in the Windows Driver Kit (WDK) documentation, for more information on normalized file names.)</span></span>

<span data-ttu-id="1be2c-112">此外，使用 IPsec 保護連線時，也可以在遠端電腦身分識別和遠端使用者身分識別上執行 ALE 層級的篩選。</span><span class="sxs-lookup"><span data-stu-id="1be2c-112">In addition, when IPsec is used to secure the connection, filtering at ALE layers can also be performed on the remote machine identity and on the remote user identity.</span></span> <span data-ttu-id="1be2c-113">遠端電腦和使用者身分識別是從建立 IPsec 會話時所用的認證取得。</span><span class="sxs-lookup"><span data-stu-id="1be2c-113">The remote machine and user identities are obtained from the credentials used in the creation of an IPsec session.</span></span>

<span data-ttu-id="1be2c-114">基於這個理由，強制執行 (例如「系統管理員」 ) 和/或哪個應用程式 (例如「Internet Explorer」 ) 的原則會在 ALE 層級撰寫。</span><span class="sxs-lookup"><span data-stu-id="1be2c-114">For this reason, policies that enforce who (for example, "administrator") and/or which application (for example, "Internet Explorer") are allowed to perform the network operations mentioned above are authored at the ALE layers.</span></span>

<span data-ttu-id="1be2c-115">ALE 可提供原則的強制執行，例如「允許 Windows Messenger 在封鎖所有其他應用程式時存取網路」。</span><span class="sxs-lookup"><span data-stu-id="1be2c-115">ALE provides enforcement for policies such as "allow Windows Messenger all access to the network while blocking all other applications."</span></span> <span data-ttu-id="1be2c-116">在此範例中，當應用程式 "Messenger" 透過網路連線時，ALE 會攔截該事件，並判斷它是由 Messenger 起始，並查詢 WFP 篩選引擎來判斷是否應該允許該通訊端繼續進行。</span><span class="sxs-lookup"><span data-stu-id="1be2c-116">In such an example, when the application "Messenger" connects across the network, ALE traps the event, determines that it was initiated by Messenger and queries the WFP filter engine to determine whether the socket should be allowed to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="1be2c-117">由於真正的雙重 IP 通訊端本質，因此可能不會發生 IPv4 ALE 層的分類。</span><span class="sxs-lookup"><span data-stu-id="1be2c-117">Due to the nature of true dual-IP sockets, classifications at the IPv4 ALE layer may not occur.</span></span> <span data-ttu-id="1be2c-118">這是設計的，因為針對所有意圖和用途，通訊端是 IPv6 通訊端。</span><span class="sxs-lookup"><span data-stu-id="1be2c-118">This is by design, because for all intents and purposes, the socket is an IPv6 socket.</span></span> <span data-ttu-id="1be2c-119">若要查看這類通訊端的 V4 流量，請使用 IPv6 對應位址在 V6 層建立篩選器。</span><span class="sxs-lookup"><span data-stu-id="1be2c-119">To see the V4 traffic for such a socket, create filters at the V6 layer using the IPv6-mapped address.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1be2c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="1be2c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1be2c-121">ALE 層</span><span class="sxs-lookup"><span data-stu-id="1be2c-121">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="1be2c-122">ALE 具狀態篩選</span><span class="sxs-lookup"><span data-stu-id="1be2c-122">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="1be2c-123">ALE 多播/廣播流量</span><span class="sxs-lookup"><span data-stu-id="1be2c-123">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="1be2c-124">ALE 重新授權</span><span class="sxs-lookup"><span data-stu-id="1be2c-124">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="1be2c-125">ALE 流程自訂</span><span class="sxs-lookup"><span data-stu-id="1be2c-125">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 