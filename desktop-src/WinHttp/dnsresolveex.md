---
description: 將主機字串解析為其 IP 位址
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: dnsResolveEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1c63ba3e20653c41864394d9c563c851f2aab5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985684"
---
# <a name="dnsresolveex-function"></a><span data-ttu-id="5777c-103">dnsResolveEx 函式</span><span class="sxs-lookup"><span data-stu-id="5777c-103">dnsResolveEx function</span></span>

<span data-ttu-id="5777c-104">將主機字串解析為其 IP 位址</span><span class="sxs-lookup"><span data-stu-id="5777c-104">Resolve a host string to its IP address</span></span>

## <a name="parameters"></a><span data-ttu-id="5777c-105">參數</span><span class="sxs-lookup"><span data-stu-id="5777c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5777c-106">*主機*</span><span class="sxs-lookup"><span data-stu-id="5777c-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="5777c-107">字串，其中包含提供給 FindProxyForUrl 的 HTTP 主控制項。</span><span class="sxs-lookup"><span data-stu-id="5777c-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5777c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5777c-108">Return value</span></span>

<span data-ttu-id="5777c-109">以分號分隔的字串，包含 IPv6 和 IPv4 位址，如果無法解析主機，則為空字串。</span><span class="sxs-lookup"><span data-stu-id="5777c-109">A semi-colon delimited string containing IPv6 and IPv4 addresses or an empty string if host is not resolvable.</span></span>

## <a name="remarks"></a><span data-ttu-id="5777c-110">備註</span><span class="sxs-lookup"><span data-stu-id="5777c-110">Remarks</span></span>

<span data-ttu-id="5777c-111">FindProxyforURLEx 實作者應該將會將以分號分隔的 IP 位址字串分隔成不同位址的程式碼。</span><span class="sxs-lookup"><span data-stu-id="5777c-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="5777c-112">範例</span><span class="sxs-lookup"><span data-stu-id="5777c-112">Examples</span></span>

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a><span data-ttu-id="5777c-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5777c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5777c-114">IPv6 感知 Proxy Helper API 定義</span><span class="sxs-lookup"><span data-stu-id="5777c-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="5777c-115">瀏覽器自動設定檔案格式的 IPv6 擴充功能</span><span class="sxs-lookup"><span data-stu-id="5777c-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



