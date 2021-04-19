---
description: 判斷指定的主機字串是否可解析為 IP 位址。
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isResolvableEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980626"
---
# <a name="isresolvableex-function"></a><span data-ttu-id="4e412-103">isResolvableEx 函式</span><span class="sxs-lookup"><span data-stu-id="4e412-103">isResolvableEx function</span></span>

<span data-ttu-id="4e412-104">判斷指定的主機字串是否可解析為 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4e412-104">Determines if a given host string can resolve to an IP address.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e412-105">參數</span><span class="sxs-lookup"><span data-stu-id="4e412-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e412-106">*主機*</span><span class="sxs-lookup"><span data-stu-id="4e412-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="4e412-107">字串，其中包含提供給 FindProxyForUrl 的 HTTP 主控制項。</span><span class="sxs-lookup"><span data-stu-id="4e412-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e412-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e412-108">Return value</span></span>

<span data-ttu-id="4e412-109">如果主機可解析為 IPv4 或 IPv6 位址，則為 TRUE;否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="4e412-109">TRUE if the host is resolvable to a IPv4 or IPv6 address; otherwise, FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="4e412-110">範例</span><span class="sxs-lookup"><span data-stu-id="4e412-110">Examples</span></span>

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a><span data-ttu-id="4e412-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e412-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e412-112">IPv6 感知 Proxy Helper API 定義</span><span class="sxs-lookup"><span data-stu-id="4e412-112">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="4e412-113">瀏覽器自動設定檔案格式的 IPv6 擴充功能</span><span class="sxs-lookup"><span data-stu-id="4e412-113">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



