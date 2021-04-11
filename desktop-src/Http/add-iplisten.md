---
title: add iplisten
description: 指定要新增至 IP 接聽清單的 IPv4 或 IPv6 位址。
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- 新增 iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "103932983"
---
# <a name="add-iplisten"></a><span data-ttu-id="907ea-104">add iplisten</span><span class="sxs-lookup"><span data-stu-id="907ea-104">add iplisten</span></span>

<span data-ttu-id="907ea-105">指定要新增至 IP 接聽清單的 IPv4 或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="907ea-105">Specifies an IPv4 or IPv6 address to be added to the IP listen list.</span></span>

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="907ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="907ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="907ea-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress = \]** *ipaddress*</span><span class="sxs-lookup"><span data-stu-id="907ea-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="907ea-108">指定要新增至 IP 接聽清單的 IPv4 或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="907ea-108">Specifies the IPv4 or IPv6 address to be added to the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="907ea-109">備註</span><span class="sxs-lookup"><span data-stu-id="907ea-109">Remarks</span></span>

<span data-ttu-id="907ea-110">將新的 IP 位址新增至 IP 接聽清單。</span><span class="sxs-lookup"><span data-stu-id="907ea-110">Adds a new IP address to the IP listen list.</span></span> <span data-ttu-id="907ea-111">其中不包括連接埠號碼。</span><span class="sxs-lookup"><span data-stu-id="907ea-111">This does not include the port number.</span></span> <span data-ttu-id="907ea-112">IP 接聽清單可用來界定 HTTP 服務所繫結的位址清單範圍。</span><span class="sxs-lookup"><span data-stu-id="907ea-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="907ea-113">"0.0.0.0" 表示任何 IPv4 位址，"::" 表示任何 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="907ea-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="907ea-114">範例</span><span class="sxs-lookup"><span data-stu-id="907ea-114">Examples</span></span>

<span data-ttu-id="907ea-115">**add iplisten ipaddress=fe80::1**</span><span class="sxs-lookup"><span data-stu-id="907ea-115">**add iplisten ipaddress=fe80::1**</span></span>

<span data-ttu-id="907ea-116">**add iplisten ipaddress=1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="907ea-116">**add iplisten ipaddress=1.1.1.1**</span></span>

<span data-ttu-id="907ea-117">**add iplisten ipaddress=0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="907ea-117">**add iplisten ipaddress=0.0.0.0**</span></span>

<span data-ttu-id="907ea-118">**add iplisten ipaddress=::**</span><span class="sxs-lookup"><span data-stu-id="907ea-118">**add iplisten ipaddress=::**</span></span>

 

 




