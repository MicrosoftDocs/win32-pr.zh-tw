---
title: 主機名稱和 IP 位址
description: TCP/IP 網路需要先將主機名稱解析為 IP 位址，才能使用位址資訊來建立連線。
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- SNMP 的主機名稱和 IP 位址
- 主機名稱，解析 SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672587"
---
# <a name="host-names-and-ip-addresses"></a><span data-ttu-id="bebd8-105">主機名稱和 IP 位址</span><span class="sxs-lookup"><span data-stu-id="bebd8-105">Host Names and IP Addresses</span></span>

<span data-ttu-id="bebd8-106">TCP/IP 網路需要先將主機名稱解析為 IP 位址，才能使用位址資訊來建立連線。</span><span class="sxs-lookup"><span data-stu-id="bebd8-106">TCP/IP networks require host names to be resolved to IP addresses before the address information can be used to create a connection.</span></span> <span data-ttu-id="bebd8-107">在 Windows 作業系統上執行的電腦會使用主機檔案，基於此目的，會將主機名稱對應至 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bebd8-107">Computers running on the Windows operating system use a host file that, for this purpose, maps host names to IP addresses.</span></span>

<span data-ttu-id="bebd8-108">主機檔案是一個文字檔，其中列出明確的主機名稱和 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bebd8-108">The host file is a text file that lists explicit host names and IP addresses.</span></span> <span data-ttu-id="bebd8-109">主機檔案會在啟動時自動載入至記憶體，並在主機名稱需要解析時進行諮詢。</span><span class="sxs-lookup"><span data-stu-id="bebd8-109">The host file is automatically loaded into memory on startup and consulted when a host name requires resolution.</span></span> <span data-ttu-id="bebd8-110">如果主機檔案未包含將特定主機名稱解析為其 IP 位址所需的對應資訊，則會對 DNS 伺服器進行解析查詢。</span><span class="sxs-lookup"><span data-stu-id="bebd8-110">If the host file does not contain the mapping information that is required to resolve a specific host name to its IP address, a resolution query is made to a DNS server.</span></span>

<span data-ttu-id="bebd8-111">SNMP 會使用 Windows 網際網路命名服務 (WINS) 來進行主機名稱解析。</span><span class="sxs-lookup"><span data-stu-id="bebd8-111">SNMP uses the Windows Internet Naming Service (WINS) for host name resolution.</span></span> <span data-ttu-id="bebd8-112">WINS 可以將 NetBIOS 名稱或電腦名稱稱對應至 TCP/IP 網路上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bebd8-112">WINS makes it possible to map NetBIOS names, or machine names, to IP addresses on TCP/IP networks.</span></span> <span data-ttu-id="bebd8-113">如果電腦無法存取 WINS 伺服器，SNMP 服務會使用主機檔案來將主機名稱解析為 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bebd8-113">If the computer cannot access a WINS server, the SNMP service uses the host file to resolve host names to IP addresses.</span></span>

<span data-ttu-id="bebd8-114">SNMP 服務支援使用主機名稱和 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bebd8-114">The SNMP service supports the use of both host names and IP addresses.</span></span> <span data-ttu-id="bebd8-115">但是，當您選擇使用主機名稱或 IP 位址來識別網路位置時，您的 SNMP 管理應用程式應該使用主機名稱。</span><span class="sxs-lookup"><span data-stu-id="bebd8-115">However, when you have a choice between using host names or IP addresses to identify network locations, your SNMP management applications should use host names.</span></span> <span data-ttu-id="bebd8-116">如果您使用主機名稱，請將參與系統的所有主機名稱和 IP 位址對應新增至主機檔案。</span><span class="sxs-lookup"><span data-stu-id="bebd8-116">If you use host names, add all host name and IP address mappings of the participating systems to the host file.</span></span>

 

 




