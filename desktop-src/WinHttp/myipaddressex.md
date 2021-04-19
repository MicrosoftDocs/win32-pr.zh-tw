---
description: 尋找 localhost 的所有 IP 位址。
ms.assetid: 47f7d03e-c1a1-4395-9889-01891208fe0f
title: myIPAddressEx 函式
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
ms.openlocfilehash: 88c205dbd5ce071a809cf87f4f97bb6d42120dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996793"
---
# <a name="myipaddressex-function"></a><span data-ttu-id="e2084-103">myIPAddressEx 函式</span><span class="sxs-lookup"><span data-stu-id="e2084-103">myIPAddressEx function</span></span>

<span data-ttu-id="e2084-104">尋找 localhost 的所有 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e2084-104">Finds all the IP addresses for localhost.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2084-105">參數</span><span class="sxs-lookup"><span data-stu-id="e2084-105">Parameters</span></span>

<span data-ttu-id="e2084-106">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="e2084-106">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2084-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2084-107">Return value</span></span>

<span data-ttu-id="e2084-108">以分號分隔的字串，其中包含 localhost (IPv6 和（或） IPv4) 的所有 IP 位址，如果無法將 localhost 解析為 IP 位址，則為空字串。</span><span class="sxs-lookup"><span data-stu-id="e2084-108">A semi-colon delimited string containing all IP addresses for localhost (IPv6 and/or IPv4), or an empty string if unable to resolve localhost to an IP address.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2084-109">備註</span><span class="sxs-lookup"><span data-stu-id="e2084-109">Remarks</span></span>

<span data-ttu-id="e2084-110">FindProxyforURLEx 實作者應該將會將以分號分隔的 IP 位址字串分隔成不同位址的程式碼。</span><span class="sxs-lookup"><span data-stu-id="e2084-110">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="e2084-111">範例</span><span class="sxs-lookup"><span data-stu-id="e2084-111">Examples</span></span>

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a><span data-ttu-id="e2084-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2084-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2084-113">IPv6 感知 Proxy Helper API 定義</span><span class="sxs-lookup"><span data-stu-id="e2084-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="e2084-114">瀏覽器自動設定檔案格式的 IPv6 擴充功能</span><span class="sxs-lookup"><span data-stu-id="e2084-114">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



