---
description: 判斷 IP 位址是否在特定子網中。
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isInNetEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979320"
---
# <a name="isinnetex-function"></a><span data-ttu-id="2f786-103">isInNetEx 函式</span><span class="sxs-lookup"><span data-stu-id="2f786-103">isInNetEx function</span></span>

<span data-ttu-id="2f786-104">判斷 IP 位址是否在特定子網中。</span><span class="sxs-lookup"><span data-stu-id="2f786-104">Determines if an IP address is in a specific subnet.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f786-105">參數</span><span class="sxs-lookup"><span data-stu-id="2f786-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f786-106">*址*</span><span class="sxs-lookup"><span data-stu-id="2f786-106">*IPaddress*</span></span> 
</dt> <dd>

<span data-ttu-id="2f786-107">包含 IPv6/IPv4 位址的字串。</span><span class="sxs-lookup"><span data-stu-id="2f786-107">A string containing IPv6/IPv4 addresses.</span></span>

</dd> <dt>

<span data-ttu-id="2f786-108">*IPprefix*</span><span class="sxs-lookup"><span data-stu-id="2f786-108">*IPprefix*</span></span> 
</dt> <dd>

<span data-ttu-id="2f786-109">字串，其中包含以冒號分隔的 IP 前置詞，並在位欄位中指定前 n 個位 (亦即3ffe：8311： ffff：：/48 或 123.112.0.0/16) 。</span><span class="sxs-lookup"><span data-stu-id="2f786-109">A string containing colon delimited IP prefix with top n bits specified in the bit field (i.e. 3ffe:8311:ffff::/48 or 123.112.0.0/16).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f786-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f786-110">Return value</span></span>

<span data-ttu-id="2f786-111">如果主機位於相同的子網中，則為 TRUE;否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="2f786-111">TRUE if the host is in the same subnet; otherwise, FALSE.</span></span>

<span data-ttu-id="2f786-112">如果前置詞的格式不正確，或在比較 (（例如 IPv4 首碼和 IPv6 位址) ）中使用不同類型的位址和前置詞，也會傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="2f786-112">Also returns FALSE if the prefix is not in the correct format or if addresses and prefixes of different types are used in the comparison (i.e. IPv4 prefix and an IPv6 address).</span></span>

## <a name="examples"></a><span data-ttu-id="2f786-113">範例</span><span class="sxs-lookup"><span data-stu-id="2f786-113">Examples</span></span>

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a><span data-ttu-id="2f786-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f786-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f786-115">IPv6 感知 Proxy Helper API 定義</span><span class="sxs-lookup"><span data-stu-id="2f786-115">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="2f786-116">瀏覽器自動設定檔案格式的 IPv6 擴充功能</span><span class="sxs-lookup"><span data-stu-id="2f786-116">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



