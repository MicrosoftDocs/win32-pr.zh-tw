---
title: IP 接聽清單
description: HTTP 伺服器 Api 在使用者註冊 UrlPrefix 之前，不會系結至任何 IP 位址和 TCP 通訊埠配對。
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932538"
---
# <a name="ip-listen-list"></a><span data-ttu-id="7330c-103">IP 接聽清單</span><span class="sxs-lookup"><span data-stu-id="7330c-103">IP Listen List</span></span>

<span data-ttu-id="7330c-104">HTTP 伺服器 Api 在使用者註冊 UrlPrefix 之前，不會系結至任何 IP 位址和 TCP 通訊埠配對。</span><span class="sxs-lookup"><span data-stu-id="7330c-104">The HTTP Server APIs do not bind to any IP address and TCP port pairs until a user registers a UrlPrefix.</span></span> <span data-ttu-id="7330c-105">根據預設，一旦在要求佇列中輸入註冊，HTTP 伺服器 API 就會系結至 UrlPrefix (中指定的埠，例如，所有 IP 位址的埠 80)  (INADDR \_ 任何或 INADDR6 \_ 電腦上可用的任何) 。</span><span class="sxs-lookup"><span data-stu-id="7330c-105">By default, once a registration is entered in the request queue, the HTTP Server API binds to the port specified in the UrlPrefix (for example port 80) for all IP addresses (INADDR\_ANY or INADDR6\_ANY) available on the machine.</span></span> <span data-ttu-id="7330c-106">當協力廠商應用程式 (不使用 HTTP 伺服器 Api 時，) 系結至電腦上的 IP 位址和埠80配對，就會發生問題。</span><span class="sxs-lookup"><span data-stu-id="7330c-106">Problems arise when third party applications (not using the HTTP Server APIs) bind to IP address and port 80 pairs on the machine.</span></span> <span data-ttu-id="7330c-107">HTTP 伺服器 API 提供一種方式來設定它所系結的 IP 位址清單，並解決這個共存問題。</span><span class="sxs-lookup"><span data-stu-id="7330c-107">The HTTP Server API provides a way to configure the list of IP addresses that it binds and solves this coexistence issue.</span></span> <span data-ttu-id="7330c-108">系統管理員會呼叫 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函數，並將 *ConfigId* 參數設定為 HttpServiceConfigIPListenList 值，以指定 IP 接聽清單。</span><span class="sxs-lookup"><span data-stu-id="7330c-108">The system administrator calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the *ConfigId* parameter set to the HttpServiceConfigIPListenList value to specify the IP listen list.</span></span> <span data-ttu-id="7330c-109">IPv4 和 IPv6 位址都可以新增至清單。</span><span class="sxs-lookup"><span data-stu-id="7330c-109">Both IPv4 and IPv6 addresses can be added to the list.</span></span> <span data-ttu-id="7330c-110">輸入的 IP 位址會套用至電腦上使用 HTTP 伺服器 API 的所有應用程式，並在機器重新開機時持續保存。</span><span class="sxs-lookup"><span data-stu-id="7330c-110">The IP addresses entered apply to all applications on the machine using the HTTP Server API and persist across reboots of the machine.</span></span> <span data-ttu-id="7330c-111">不過，IP 接聽清單設定的任何變更都不會以動態方式進行;在大部分的情況下，可能需要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="7330c-111">However, any changes to the IP listen list configuration do not take place dynamically; in most cases, a system reboot may be necessary.</span></span>

 

 




