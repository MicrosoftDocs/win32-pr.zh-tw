---
title: 負載平衡的最佳作法
description: 負載平衡的最佳作法
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933460"
---
# <a name="load-balancing-best-practices"></a><span data-ttu-id="8598e-103">負載平衡的最佳作法</span><span class="sxs-lookup"><span data-stu-id="8598e-103">Load Balancing Best Practices</span></span>

<span data-ttu-id="8598e-104">設定和設定 RPC 負載平衡時，應該遵循幾個最佳作法。</span><span class="sxs-lookup"><span data-stu-id="8598e-104">Several best practices should be followed when setting up and configuring RPC Load balancing.</span></span>

<span data-ttu-id="8598e-105">首先，安全性應該設定在傳入和傳出的磅通話上。</span><span class="sxs-lookup"><span data-stu-id="8598e-105">First, security should be set on incoming and outgoing LBS calls.</span></span> <span data-ttu-id="8598e-106">這表示兩個選用的 [NoSecurity](configuring-load-balancing.md) 登錄機碼應該不存在，或應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="8598e-106">This means both of the optional [NoSecurity](configuring-load-balancing.md) registry keys should either not be present or should be set to zero.</span></span>

<span data-ttu-id="8598e-107">第二，請注意必須支付與 RPC 負載平衡解決方案搭配使用的前端負載平衡解決方案。</span><span class="sxs-lookup"><span data-stu-id="8598e-107">Second, attention must be paid to the front end load balancing solution used in conjunction with the RPC Load Balancing solution.</span></span> <span data-ttu-id="8598e-108">例如，如果前端負載平衡器使用簡單的迴圈配置資源負載平衡，伺服器陣列中應該會有奇數部伺服器。</span><span class="sxs-lookup"><span data-stu-id="8598e-108">For example, if the front end load balancer uses simple round robin load balancing, an odd number of servers should exist in the server farm.</span></span> <span data-ttu-id="8598e-109">這是為了降低所有連接的可能性，因此可以由同一部伺服器或伺服器來提供服務。</span><span class="sxs-lookup"><span data-stu-id="8598e-109">This is to mitigate the possibility of all connections being forwarded and thus serviced by the same server or servers.</span></span>

<span data-ttu-id="8598e-110">基於安全性，通常最好讓防火牆控制 RPC Proxy 伺服器的存取權。</span><span class="sxs-lookup"><span data-stu-id="8598e-110">For security, it is commonly desirable to have a firewall control access to RPC Proxy servers.</span></span> <span data-ttu-id="8598e-111">如果採用以埠為基礎的防火牆解決方案，RPC 端點必須是靜態的，才能限制在防火牆中開啟的埠數目。</span><span class="sxs-lookup"><span data-stu-id="8598e-111">If a port based firewall solution is employed, RPC endpoints must be static in order to limit the number of ports that are opened in the firewall.</span></span> <span data-ttu-id="8598e-112">在 Windows Server 2008 和更新版本的 Windows 上，RPC 提供一種機制，可將靜態埠指派給動態端點。</span><span class="sxs-lookup"><span data-stu-id="8598e-112">On Windows Server 2008 and later versions of Windows, RPC provides a mechanism to assign a static port to dynamic endpoints.</span></span> <span data-ttu-id="8598e-113">這是透過 RPC netsh firewall 命令來達成。</span><span class="sxs-lookup"><span data-stu-id="8598e-113">This is achieved through the RPC netsh firewall commands.</span></span> <span data-ttu-id="8598e-114">將磅介面設定為靜態埠3010的範例命令集為：</span><span class="sxs-lookup"><span data-stu-id="8598e-114">An example set of commands to set the LBS interface to the static port of 3010 is:</span></span>

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

<span data-ttu-id="8598e-115">您可以使用 RPC netsh 命令，為任何動態或靜態介面設定靜態端點。</span><span class="sxs-lookup"><span data-stu-id="8598e-115">The RPC netsh command can be used to set a static endpoint for any dynamic or static interface.</span></span> <span data-ttu-id="8598e-116">當您限制對執行埠型防火牆解決方案的電腦進行存取時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="8598e-116">This is useful when restricting access to a machine running a port based firewall solution.</span></span> <span data-ttu-id="8598e-117">如果使用 Windows 防火牆解決方案，則可以封鎖或啟用 RPC 介面，而不需要將它指派給特定埠。</span><span class="sxs-lookup"><span data-stu-id="8598e-117">If the Windows firewall solution is used, the RPC interface can be blocked or enabled without having to assign it to a specific port.</span></span> <span data-ttu-id="8598e-118">如需詳細資訊，請參閱 [RPC netsh firewall 命令參考](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="8598e-118">For more information, see the [RPC netsh firewall command reference](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span></span>

 

 