---
title: Teredo 的名稱解析
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 深入瞭解： Teredo 的名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700b5d40fda0546c29bd7c47ee773977c374784c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980017"
---
# <a name="name-resolution-for-teredo"></a><span data-ttu-id="6e9bc-103">Teredo 的名稱解析</span><span class="sxs-lookup"><span data-stu-id="6e9bc-103">Name Resolution For Teredo</span></span>

<span data-ttu-id="6e9bc-104">Teredo 介面目前會利用下列通訊協定來進行名稱解析：</span><span class="sxs-lookup"><span data-stu-id="6e9bc-104">The Teredo interface currently utilizes the following protocols for name resolution:</span></span>

## <a name="domain-name-system"></a><span data-ttu-id="6e9bc-105">網域名稱系統</span><span class="sxs-lookup"><span data-stu-id="6e9bc-105">Domain Name System</span></span>

<span data-ttu-id="6e9bc-106">網域名稱系統 (DNS) 目前是網際網路上最顯著的名稱解析技術。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-106">The Domain Name System (DNS) is currently the most prominent name resolution technology on the Internet.</span></span> <span data-ttu-id="6e9bc-107">大部分的網頁伺服器都會向 DNS 伺服器註冊 URL 位址。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-107">Most web servers register URL addresses with DNS servers.</span></span> <span data-ttu-id="6e9bc-108">不過，家用網路的位址並不會登錄到 DNS 伺服器，因為大部分的家庭使用者透過動態主機設定通訊協定 (DHCP) 從其網際網路服務提供者取得 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-108">However, the addresses of a home network are not registered with DNS servers since most home users obtain IP addresses via Dynamic Host Configuration Protocol (DHCP) from their Internet Service Provider.</span></span> <span data-ttu-id="6e9bc-109">DHCP 租用的持續時間相對較短，而從48到72小時的任何時間都需要將名稱傳播到整個 DNS 雲端。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-109">DHCP leases are of relatively short duration and take anywhere from 48 to 72 hours to propagate a name throughout the DNS cloud.</span></span> <span data-ttu-id="6e9bc-110">如此一來，DNS 已證明成為取得家庭使用者的公用 IP 位址的無效方法。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-110">As a result DNS has proven to be an ineffective method of obtaining a home user's public IP address.</span></span> <span data-ttu-id="6e9bc-111">Teredo 位址包含公用 IPv4 位址，因此至少會繼承相同的 IPv4 位址變動性。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-111">A Teredo address includes the public IPv4 address and hence inherits at least the same volatility of the IPv4 addresses.</span></span> <span data-ttu-id="6e9bc-112">因此，Teredo 位址目前未在 DNS 中註冊。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-112">Hence, Teredo addresses are currently not registered in DNS.</span></span>

## <a name="peer-name-resolution-protocol"></a><span data-ttu-id="6e9bc-113">對等名稱解析通訊協定</span><span class="sxs-lookup"><span data-stu-id="6e9bc-113">Peer Name Resolution Protocol</span></span>

<span data-ttu-id="6e9bc-114">對等名稱解析通訊協定 (PNRP) 是一種分散式 DNS 技術，可將 IP 位址儲存在屬於 PNRP 雲端一部分的數千部使用者電腦上。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-114">The Peer Name Resolution Protocol (PNRP) is a distributed DNS technology that stores IP addresses on thousands of user machines that are a part of a PNRP cloud.</span></span> <span data-ttu-id="6e9bc-115">使用 Windows Vista，任何家庭使用者都可以選擇成為 PNRP 雲端的成員，並在 PNRP 網路上通告其 Teredo IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-115">Using Windows Vista, any home user can choose to become a member of a PNRP cloud and advertise their Teredo IPv6 address on the PNRP network.</span></span> <span data-ttu-id="6e9bc-116">不同于提供給 DNS 伺服器的位址，PNRP 網路上的位址通常需要不到一分鐘的時間來傳播。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-116">Unlike addresses given to DNS servers, addresses on the PNRP network often take less than a minute to propagate.</span></span> <span data-ttu-id="6e9bc-117">由於 Teredo 位址可以經常變更 (ISP 提供的外部 IPv4 位址可能會變更，或者使用者的網際網路閘道裝置所使用的外部埠可能會變更) ，PNRP 已證明是適用于家庭使用者的有效機制。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-117">Since Teredo addresses can change frequently (external IPv4 address provided by the ISP can change or the external port used by the user's internet gateway device can change), PNRP has proven to be an effective mechanism for home users.</span></span> <span data-ttu-id="6e9bc-118">PNRP 名稱是以 ". pnrp.net" 結尾的位址，是以不會變更的唯一系統屬性為基礎。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-118">PNRP names, addresses ending with ".pnrp.net" are based on a unique system properties that do not change.</span></span> <span data-ttu-id="6e9bc-119">因此，PNRP 名稱是連接到家庭使用者的可靠方式。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-119">As a result a PNRP name is a reliable way to connect to a home user.</span></span> <span data-ttu-id="6e9bc-120">[**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) API 可用來取得使用 PNRP 技術 (DNS 名稱結尾為 ". pnrp.net" ) 的 IP 位址，並建立與其他主機的連接。</span><span class="sxs-lookup"><span data-stu-id="6e9bc-120">The [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) API can be used to obtain IP address using PNRP technology (DNS names ending with ".pnrp.net") and establish connection with other hosts.</span></span>

 

 
