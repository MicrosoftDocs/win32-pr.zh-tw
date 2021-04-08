---
title: Active Directory 伺服器和動態 DNS
description: Active Directory 伺服器會發佈其位址，讓用戶端可以找到只知道功能變數名稱的名稱。
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- 動態 DNS Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671015"
---
# <a name="active-directory-servers-and-dynamic-dns"></a><span data-ttu-id="4fa6c-104">Active Directory 伺服器和動態 DNS</span><span class="sxs-lookup"><span data-stu-id="4fa6c-104">Active Directory Servers and Dynamic DNS</span></span>

<span data-ttu-id="4fa6c-105">Active Directory 伺服器會發佈其位址，讓用戶端可以找到只知道功能變數名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-105">The Active Directory servers publish their addresses such that clients can find them knowing only the domain name.</span></span> <span data-ttu-id="4fa6c-106">Active Directory 的伺服器是使用 DNS 中 (SRV Rr) 的服務資源記錄來發佈。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-106">Active Directory servers are published using the Service Resource Records (SRV RRs) in DNS.</span></span> <span data-ttu-id="4fa6c-107">SRV RR 是用來將服務名稱對應至提供服務之伺服器位址的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-107">The SRV RR is a DNS record used to map the name of a service to the address of a server that offers the service.</span></span> <span data-ttu-id="4fa6c-108">SRV RR 的名稱格式如下：</span><span class="sxs-lookup"><span data-stu-id="4fa6c-108">The name of a SRV RR is in this form:</span></span>


```C++
<service>.<protocol>.<domain>
```



<span data-ttu-id="4fa6c-109">Active Directory 伺服器透過 TCP 通訊協定提供 LDAP 服務，讓發佈的名稱為 "LDAP net.tcp <domain> "。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-109">Active Directory servers offer the LDAP service over the TCP protocol so that published names are "ldap.tcp.<domain>".</span></span> <span data-ttu-id="4fa6c-110">因此，fabrikam.com 的 SRV RR 為 "ldap.tcp.fabrikam.com"。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-110">Thus, the SRV RR for fabrikam.com is "ldap.tcp.fabrikam.com".</span></span> <span data-ttu-id="4fa6c-111">SRV RR 的其他相關資料會指出伺服器的優先順序和權數，讓用戶端選擇最適合其需求的伺服器。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-111">Additional data about the SRV RR indicates the priority and weight for the server, enabling clients to choose the best server for their needs.</span></span>

<span data-ttu-id="4fa6c-112">安裝 Active Directory 伺服器時，它會使用動態 DNS 來發佈本身。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-112">When an Active Directory server is installed, it uses Dynamic DNS to publish itself.</span></span> <span data-ttu-id="4fa6c-113">因為 TCP/IP 位址可能會變更，所以伺服器會定期驗證他們的註冊，以確保它們是正確的，並視需要加以更新。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-113">Because TCP/IP addresses are subject to change, servers periodically verify their registrations to be sure they are correct, and update them if necessary.</span></span>

<span data-ttu-id="4fa6c-114">動態 DNS 是 DNS 標準的最新加入。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-114">Dynamic DNS is a recent addition to the DNS standard.</span></span> <span data-ttu-id="4fa6c-115">動態 DNS 會定義用來動態更新 DNS 伺服器與新資料的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-115">Dynamic DNS defines a protocol for dynamically updating a DNS server with new data.</span></span> <span data-ttu-id="4fa6c-116">在動態 DNS 之前，系統管理員必須手動設定 DNS 伺服器所儲存的記錄。</span><span class="sxs-lookup"><span data-stu-id="4fa6c-116">Prior to Dynamic DNS, administrators were required to manually configure the records stored by DNS servers.</span></span>

 

 




