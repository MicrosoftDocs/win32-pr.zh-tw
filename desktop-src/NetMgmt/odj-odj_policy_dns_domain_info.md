---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO IDL 定義
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "103684205"
---
# <a name="odj_policy_dns_domain_info-structure"></a><span data-ttu-id="1290d-103">ODJ_POLICY_DNS_DOMAIN_INFO 結構</span><span class="sxs-lookup"><span data-stu-id="1290d-103">ODJ_POLICY_DNS_DOMAIN_INFO structure</span></span>

<span data-ttu-id="1290d-104">包含用戶端應加入之網域和樹系的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1290d-104">Contains information about the domain and forest that a client should be joined to.</span></span>

## <a name="syntax"></a><span data-ttu-id="1290d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1290d-105">Syntax</span></span>

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a><span data-ttu-id="1290d-106">成員</span><span class="sxs-lookup"><span data-stu-id="1290d-106">Members</span></span>

### <a name="name"></a><span data-ttu-id="1290d-107">Name</span><span class="sxs-lookup"><span data-stu-id="1290d-107">Name</span></span>

<span data-ttu-id="1290d-108">必須設定為 Netbios 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="1290d-108">Must be set to a Netbios domain name.</span></span>

### <a name="dnsdomainname"></a><span data-ttu-id="1290d-109">DnsDomainName</span><span class="sxs-lookup"><span data-stu-id="1290d-109">DnsDomainName</span></span>

<span data-ttu-id="1290d-110">必須設定為 DNS 格式的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="1290d-110">Must be set to a domain name in DNS format.</span></span>

### <a name="dnsforestname"></a><span data-ttu-id="1290d-111">DnsForestName</span><span class="sxs-lookup"><span data-stu-id="1290d-111">DnsForestName</span></span>

<span data-ttu-id="1290d-112">必須設定為 DNS 格式的樹系名稱。</span><span class="sxs-lookup"><span data-stu-id="1290d-112">Must be set to a forest name in DNS format.</span></span>

### <a name="domainguid"></a><span data-ttu-id="1290d-113">DomainGuid</span><span class="sxs-lookup"><span data-stu-id="1290d-113">DomainGuid</span></span>

<span data-ttu-id="1290d-114">必須設定為網域 guid。</span><span class="sxs-lookup"><span data-stu-id="1290d-114">Must be set to the domain guid.</span></span>

### <a name="sid"></a><span data-ttu-id="1290d-115">Sid</span><span class="sxs-lookup"><span data-stu-id="1290d-115">Sid</span></span>

<span data-ttu-id="1290d-116">必須設定為網域 sid。</span><span class="sxs-lookup"><span data-stu-id="1290d-116">Must be set to the domain sid.</span></span>

## <a name="see-also"></a><span data-ttu-id="1290d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1290d-117">See also</span></span>

[<span data-ttu-id="1290d-118">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="1290d-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="1290d-119">**ODJ \_ UNICODE \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="1290d-119">**ODJ\_UNICODE\_STRING**</span></span>](odj-odj_unicode_string.md)

[<span data-ttu-id="1290d-120">**ODJ \_ SID**</span><span class="sxs-lookup"><span data-stu-id="1290d-120">**ODJ\_SID**</span></span>](odj-odj_sid.md)
