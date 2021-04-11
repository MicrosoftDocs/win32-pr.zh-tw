---
title: delete iplisten
description: 指定要從 IP 接聽清單中刪除的 IPv4 或 IPv6 位址。
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- 刪除 iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104022703"
---
# <a name="delete-iplisten"></a><span data-ttu-id="1a844-104">delete iplisten</span><span class="sxs-lookup"><span data-stu-id="1a844-104">delete iplisten</span></span>

<span data-ttu-id="1a844-105">指定要從 IP 接聽清單中刪除的 IPv4 或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1a844-105">Specifies an IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="1a844-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a844-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a844-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ 位址 = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="1a844-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[address=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="1a844-108">指定要從 IP 接聽清單中刪除的 IPv4 或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1a844-108">Specifies the IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a844-109">備註</span><span class="sxs-lookup"><span data-stu-id="1a844-109">Remarks</span></span>

<span data-ttu-id="1a844-110">刪除 ip 接聽清單的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1a844-110">Deletes an IP address to the IP listen list.</span></span> <span data-ttu-id="1a844-111">其中不包括連接埠號碼。</span><span class="sxs-lookup"><span data-stu-id="1a844-111">This does not include the port number.</span></span> <span data-ttu-id="1a844-112">IP 接聽清單可用來界定 HTTP 服務所繫結的位址清單範圍。</span><span class="sxs-lookup"><span data-stu-id="1a844-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="1a844-113">"0.0.0.0" 表示任何 IPv4 位址，"::" 表示任何 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1a844-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="1a844-114">範例</span><span class="sxs-lookup"><span data-stu-id="1a844-114">Examples</span></span>

<span data-ttu-id="1a844-115">**delete iplisten address = fe80：：1**</span><span class="sxs-lookup"><span data-stu-id="1a844-115">**delete iplisten address=fe80::1**</span></span>

<span data-ttu-id="1a844-116">**delete iplisten address = 1.1.1。1**</span><span class="sxs-lookup"><span data-stu-id="1a844-116">**delete iplisten address=1.1.1.1**</span></span>

<span data-ttu-id="1a844-117">**delete iplisten address = 0.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="1a844-117">**delete iplisten address=0.0.0.0**</span></span>

<span data-ttu-id="1a844-118">**delete iplisten address =：：**</span><span class="sxs-lookup"><span data-stu-id="1a844-118">**delete iplisten address=::**</span></span>

 

 




