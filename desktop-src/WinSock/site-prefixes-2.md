---
description: 指定連結至介面4的前置詞 \# 。
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: IPv6 網站首碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971207"
---
# <a name="ipv6-site-prefixes"></a><span data-ttu-id="3dc87-103">IPv6 網站首碼</span><span class="sxs-lookup"><span data-stu-id="3dc87-103">IPv6 Site Prefixes</span></span>

<span data-ttu-id="3dc87-104">Ipv6 rtu 命令可讓您使用網站前置長度來設定已發佈的內部連結首碼。</span><span class="sxs-lookup"><span data-stu-id="3dc87-104">The ipv6 rtu command allows published on-link prefixes to be configured with a site prefix length.</span></span> <span data-ttu-id="3dc87-105">如果有指定，網站前置長度會放入路由器公告的首碼資訊選項中。</span><span class="sxs-lookup"><span data-stu-id="3dc87-105">If specified, the site prefix length is put into a prefix information option in router advertisements.</span></span> <span data-ttu-id="3dc87-106">例如：</span><span class="sxs-lookup"><span data-stu-id="3dc87-106">For example:</span></span>

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

<span data-ttu-id="3dc87-107">指定連結至介面4的前置詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="3dc87-107">specifies a prefix that is on-link to interface \#4.</span></span> <span data-ttu-id="3dc87-108">前置詞已發佈，這表示如果介面 \# 4 是廣告介面，則會將它包含在路由器公告中。</span><span class="sxs-lookup"><span data-stu-id="3dc87-108">The prefix is published, meaning that it is included in router advertisements if interface \#4 is an advertising interface.</span></span> <span data-ttu-id="3dc87-109">前置詞資訊選項中的存留期為1800秒 (30 分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="3dc87-109">The lifetime in the prefix information option is 1800 seconds (30 minutes).</span></span> <span data-ttu-id="3dc87-110">首碼資訊選項中的網站前置長度為48。</span><span class="sxs-lookup"><span data-stu-id="3dc87-110">The site prefix length in the prefix information option is 48.</span></span>

<span data-ttu-id="3dc87-111">接收指定網站首碼的首碼資訊選項會導致在網站首碼資料表中建立專案，您可以使用 ipv6 spt 命令來顯示專案。</span><span class="sxs-lookup"><span data-stu-id="3dc87-111">The receipt of a prefix information option that specifies a site prefix causes an entry to be created in the site prefix table, which can be displayed by using the ipv6 spt command.</span></span> <span data-ttu-id="3dc87-112">網站首碼資料表是用來移除 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和相關函式所傳回之不當的網站本機位址。</span><span class="sxs-lookup"><span data-stu-id="3dc87-112">The site prefix table is used to remove inappropriate site-local addresses from those returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and related functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dc87-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3dc87-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dc87-114">IPv6 連結-本機和網站-本機位址</span><span class="sxs-lookup"><span data-stu-id="3dc87-114">IPv6 Link-local and Site-local Addresses</span></span>](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="3dc87-115">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="3dc87-115">Netsh.exe</span></span>](netsh-exe.md)
</dt> </dl>

 

 



