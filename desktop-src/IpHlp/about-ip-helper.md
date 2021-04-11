---
description: 網際網路通訊協定協助程式 (IP 協助程式) 可讓應用程式抓取本機電腦網路設定的相關資訊，以及修改該設定，以協助本機電腦的網路管理。
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: 關於 IP Helper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50587b4abdcbad0cddd6d6ce3281c908fdebef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026244"
---
# <a name="about-ip-helper"></a><span data-ttu-id="9ad2c-103">關於 IP Helper</span><span class="sxs-lookup"><span data-stu-id="9ad2c-103">About IP Helper</span></span>

<span data-ttu-id="9ad2c-104">網際網路通訊協定協助程式 (IP 協助程式) 可讓應用程式抓取本機電腦網路設定的相關資訊，以及修改該設定，以協助本機電腦的網路管理。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-104">Internet Protocol Helper (IP Helper) assists network administration of the local computer by enabling applications to retrieve information about the network configuration of the local computer, and to modify that configuration.</span></span> <span data-ttu-id="9ad2c-105">IP 協助程式也提供通知機制，以確保應用程式會在本機電腦網路設定的特定層面變更時收到通知。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-105">IP Helper also provides notification mechanisms to ensure that an application is notified when certain aspects of the local computer network configuration change.</span></span>

<span data-ttu-id="9ad2c-106">許多 IP Helper 函式都會傳遞結構參數，以代表與 [管理資訊基礎](/previous-versions/windows/desktop/mib/about-management-information-base) 技術相關聯的資料類型。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-106">Many of the IP Helper functions pass structure parameters that represent data types associated with the [Management Information Base](/previous-versions/windows/desktop/mib/about-management-information-base) technology.</span></span> <span data-ttu-id="9ad2c-107">IP Helper 函式會使用這些結構來代表各種網路資訊，例如 ARP 快取專案。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-107">The IP Helper functions use these structures to represent various networking information, such as ARP cache entries.</span></span> <span data-ttu-id="9ad2c-108">由於 MIB API 也會使用這些結構，因此會在 [管理資訊基底參考](/previous-versions/windows/desktop/mib/management-information-base-reference)中說明這些結構。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-108">Since these structures are also used by the MIB API, they are described in the [Management Information Base Reference](/previous-versions/windows/desktop/mib/management-information-base-reference).</span></span> <span data-ttu-id="9ad2c-109">雖然 IP 協助程式 API 使用這些結構，但 IP 協助程式與管理資訊基礎 (MIB) 和簡單的網路管理通訊協定 (SNMP) 不同。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-109">Although the IP Helper API uses these structures, IP Helper is distinct from the Management Information Base (MIB) and Simple Network Management Protocol (SNMP).</span></span>

<span data-ttu-id="9ad2c-110">IP 協助程式檔會廣泛地使用「介面卡」和「介面」詞彙。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-110">The IP Helper documentation uses the terms "adapter" and "interface" extensively.</span></span> <span data-ttu-id="9ad2c-111">「介面卡」是一種舊版的詞彙，它是一種網路介面卡的縮寫形式，最初指的是某種形式的網路硬體。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-111">An "adapter" is a legacy term that is an abbreviated form of network adapter which originally referred to some form of network hardware.</span></span> <span data-ttu-id="9ad2c-112">介面卡是一種交叉連結層級的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-112">An adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="9ad2c-113">「介面」是在 IETF RFC 檔中使用的較新詞彙。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-113">An "interface" is a newer term used in the IETF RFC documents.</span></span> <span data-ttu-id="9ad2c-114">Rfc 將介面定義為抽象概念，以表示連結的節點附件。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-114">The RFCs define an interface as an abstract concept that represents a node's attachment to a link.</span></span> <span data-ttu-id="9ad2c-115">介面是 IP 層級的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-115">An interface is an IP-level abstraction.</span></span>

<span data-ttu-id="9ad2c-116">IP 協助程式檔中的介面卡和介面詞彙會稍微交替使用。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-116">The adapter and interface terms are used somewhat interchangeably in the IP Helper documentation.</span></span> <span data-ttu-id="9ad2c-117">在 IP 協助程式檔中，介面卡清單可能包含軟體 WAN 介面以及回送介面 (這兩個都不是指硬體裝置) 。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-117">In IP Helper documentation, a list of adapters could include a software WAN interface as well as the loopback interface (neither of these refer to a hardware device).</span></span> <span data-ttu-id="9ad2c-118">在 IP 協助程式 Api 中，有一個介面卡與介面的一對一對應。</span><span class="sxs-lookup"><span data-stu-id="9ad2c-118">In the IP Helper APIs, there is a one-to-one mapping of adapters to interfaces.</span></span>

<span data-ttu-id="9ad2c-119">IP 協助程式提供下列方面的功能：</span><span class="sxs-lookup"><span data-stu-id="9ad2c-119">IP Helper provides capabilities in the following areas:</span></span>

-   [<span data-ttu-id="9ad2c-120">正在抓取網路設定的相關資訊</span><span class="sxs-lookup"><span data-stu-id="9ad2c-120">Retrieving Information About Network Configuration</span></span>](retrieving-information-about-network-configuration.md)
-   [<span data-ttu-id="9ad2c-121">管理網路介面卡</span><span class="sxs-lookup"><span data-stu-id="9ad2c-121">Managing Network Adapters</span></span>](managing-network-adapters.md)
-   [<span data-ttu-id="9ad2c-122">管理介面</span><span class="sxs-lookup"><span data-stu-id="9ad2c-122">Managing Interfaces</span></span>](managing-interfaces.md)
-   [<span data-ttu-id="9ad2c-123">管理 IP 位址</span><span class="sxs-lookup"><span data-stu-id="9ad2c-123">Managing IP Addresses</span></span>](managing-ip-addresses.md)
-   [<span data-ttu-id="9ad2c-124">使用位址解析通訊協定</span><span class="sxs-lookup"><span data-stu-id="9ad2c-124">Using the Address Resolution Protocol</span></span>](using-the-address-resolution-protocol.md)
-   [<span data-ttu-id="9ad2c-125">在網際網路通訊協定和網際網路控制訊息通訊協定上抓取資訊</span><span class="sxs-lookup"><span data-stu-id="9ad2c-125">Retrieving Information on the Internet Protocol and the Internet Control Message Protocol</span></span>](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [<span data-ttu-id="9ad2c-126">管理路由</span><span class="sxs-lookup"><span data-stu-id="9ad2c-126">Managing Routing</span></span>](managing-routing.md)
-   [<span data-ttu-id="9ad2c-127">接收網路事件的通知</span><span class="sxs-lookup"><span data-stu-id="9ad2c-127">Receiving Notification of Network Events</span></span>](receiving-notification-of-network-events.md)
-   [<span data-ttu-id="9ad2c-128">正在抓取傳輸控制通訊協定和使用者資料包協定的相關資訊</span><span class="sxs-lookup"><span data-stu-id="9ad2c-128">Retrieving Information About the Transmission Control Protocol and the User Datagram Protocol</span></span>](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
