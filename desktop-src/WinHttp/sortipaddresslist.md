---
description: 排序 IP 位址清單。
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: sortIpAddressList 函式
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
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972996"
---
# <a name="sortipaddresslist-function"></a><span data-ttu-id="98dc6-103">sortIpAddressList 函式</span><span class="sxs-lookup"><span data-stu-id="98dc6-103">sortIpAddressList function</span></span>

<span data-ttu-id="98dc6-104">排序 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="98dc6-104">Sorts a list of IP addresses.</span></span>

## <a name="parameters"></a><span data-ttu-id="98dc6-105">參數</span><span class="sxs-lookup"><span data-stu-id="98dc6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98dc6-106">*IpAddressList*</span><span class="sxs-lookup"><span data-stu-id="98dc6-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="98dc6-107">以分號分隔的字串，其中包含 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="98dc6-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98dc6-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="98dc6-108">Return value</span></span>

<span data-ttu-id="98dc6-109">已排序之分號分隔 IP 位址的清單，如果無法排序 IP 位址清單，則為空字串。</span><span class="sxs-lookup"><span data-stu-id="98dc6-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="98dc6-110">備註</span><span class="sxs-lookup"><span data-stu-id="98dc6-110">Remarks</span></span>

<span data-ttu-id="98dc6-111">FindProxyforURLEx 實作者應該將會將以分號分隔的 IP 位址字串分隔成不同位址的程式碼。</span><span class="sxs-lookup"><span data-stu-id="98dc6-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="98dc6-112">範例</span><span class="sxs-lookup"><span data-stu-id="98dc6-112">Examples</span></span>

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a><span data-ttu-id="98dc6-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98dc6-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98dc6-114">IPv6 感知 Proxy Helper API 定義</span><span class="sxs-lookup"><span data-stu-id="98dc6-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="98dc6-115">瀏覽器自動設定檔案格式的 IPv6 擴充功能</span><span class="sxs-lookup"><span data-stu-id="98dc6-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



