---
description: 網路位置感知 (NLA) 服務提供者對於可能在不同網路間移動的電腦或裝置而言很重要，而且當有一個以上的設定可供使用時，可以選取最佳設定。
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: NLA 的角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192207"
---
# <a name="the-role-of-nla"></a><span data-ttu-id="a2dbc-103">NLA 的角色</span><span class="sxs-lookup"><span data-stu-id="a2dbc-103">The Role of NLA</span></span>

<span data-ttu-id="a2dbc-104">網路位置感知 (NLA) 服務提供者對於可能在不同網路間移動的電腦或裝置而言很重要，而且當有一個以上的設定可供使用時，可以選取最佳設定。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-104">The Network Location Awareness (NLA) service provider is vital for computers or devices that might move between different networks, and for selecting optimal configurations when more than one is available.</span></span> <span data-ttu-id="a2dbc-105">例如，實體網路之間的無線電腦漫遊可以根據其可用網路連線的相關資訊，使用 NLA 判斷適當的設定。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-105">For example, a wireless computer roaming between physical networks can use NLA to determine the proper configuration based on information about its available network connection.</span></span> <span data-ttu-id="a2dbc-106">當多重主目錄電腦具有一個網路的實體連線，同時透過撥號連線或通道連線到另一個網路時，NLA 也可證明有價值。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-106">NLA also proves valuable when a multihomed computer has a physical connection to one network while also connected to another network through a dial-up connection or a tunnel.</span></span>

<span data-ttu-id="a2dbc-107">在過去，開發人員必須取得邏輯網路介面的相關資訊，因此會根據許多不同的網路資訊來決定網路連線能力。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-107">In the past, developers had to obtain information about a logical network interface, and therefore make decisions about network connectivity, based on a multitude of disparate network information.</span></span> <span data-ttu-id="a2dbc-108">在這些情況下，開發人員必須根據 IP 位址、介面的子網、網域名稱系統 (與介面相關聯的 DNS) 名稱、NIC 的 MAC 位址、無線網路名稱或其他網路資訊，來選擇適當的網路介面。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-108">In those circumstances, developers had to choose the appropriate network interface based on the IP address, the subnet of the interface, the Domain Name System (DNS) name associated with the interface, the MAC address of a NIC, a wireless network name, or other network information.</span></span> <span data-ttu-id="a2dbc-109">NLA 藉由提供用來列舉邏輯網路附件資訊的標準介面、將它與實體網路介面資訊相關聯，然後在先前傳回的資訊失效時提供通知，來減輕這個問題。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-109">NLA alleviates this problem by supplying a standard interface for enumerating logical network attachment information, correlating it with physical network interface information, and then providing notification when previously returned information gets invalidated.</span></span>

<span data-ttu-id="a2dbc-110">NLA 提供下列網路位置資訊：</span><span class="sxs-lookup"><span data-stu-id="a2dbc-110">NLA provides the following network location information:</span></span>

<dl> <dt>

<span data-ttu-id="a2dbc-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>邏輯網路身分識別</span><span class="sxs-lookup"><span data-stu-id="a2dbc-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Logical Network Identity</span></span>
</dt> <dd>

<span data-ttu-id="a2dbc-112">NLA 會先嘗試依照其 DNS 功能變數名稱來識別邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-112">NLA first attempts to identify a logical network by its DNS domain name.</span></span> <span data-ttu-id="a2dbc-113">如果邏輯網路沒有功能變數名稱，NLA 會從儲存在登錄中的自訂靜態資訊識別網路，最後從其子網位址識別網路。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-113">If a logical network does not have a domain name, NLA identifies the network from custom static information stored in the registry, and finally from its subnet address.</span></span>

</dd> <dt>

<span data-ttu-id="a2dbc-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>邏輯網路介面</span><span class="sxs-lookup"><span data-stu-id="a2dbc-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logical Network Interfaces</span></span>
</dt> <dd>

<span data-ttu-id="a2dbc-115">針對電腦所連接的每個網路，NLA 提供可唯一識別實體介面（例如 NIC）或邏輯介面（例如 RAS 連線）的 *AdapterName* 。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-115">For each network to which a computer is attached, NLA supplies an *AdapterName* that uniquely identifies a physical interface such as a NIC, or a logical interface such as a RAS connection.</span></span> <span data-ttu-id="a2dbc-116">然後，AdapterName 可搭配 IP 協助程式 API 中提供的函式使用，以取得進一步的介面特性。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-116">The AdapterName can then be used with functions available in the IP Helper API to obtain further interface characteristics.</span></span>

</dd> </dl>

<span data-ttu-id="a2dbc-117">NLA 會使用相關聯的類別 GUID 和屬性，將邏輯網路實作為服務類別。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-117">NLA implements the logical network as a service class, with an associated class GUID and properties.</span></span> <span data-ttu-id="a2dbc-118">NLA 傳回信息的每個邏輯網路是該服務類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a2dbc-118">Each logical network for which NLA returns information is an instance of that service class.</span></span>

 

 



