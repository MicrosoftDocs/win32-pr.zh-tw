---
title: MicrosoftDNS_Cache 類別
description: MicrosoftDNS \_ cache 類別描述 DNS 伺服器上現有的快取。
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache 類別 DNS
- MicrosoftDNS_Cache 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025106"
---
# <a name="microsoftdns_cache-class"></a><span data-ttu-id="e5eca-105">MicrosoftDNS \_ Cache 類別</span><span class="sxs-lookup"><span data-stu-id="e5eca-105">MicrosoftDNS\_Cache class</span></span>

<span data-ttu-id="e5eca-106">**MicrosoftDNS \_ cache** 類別描述 DNS 伺服器上現有的快取。</span><span class="sxs-lookup"><span data-stu-id="e5eca-106">The **MicrosoftDNS\_Cache** class describes a cache existing on a DNS Server.</span></span> <span data-ttu-id="e5eca-107">此類別簡化了 DNS 物件的內含專案的視覺化，而不是代表實際的物件。</span><span class="sxs-lookup"><span data-stu-id="e5eca-107">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span> <span data-ttu-id="e5eca-108">**MicrosoftDNS \_ Cache** 類別是 DNS 伺服器所快取之資源記錄的容器。</span><span class="sxs-lookup"><span data-stu-id="e5eca-108">The **MicrosoftDNS\_Cache** class is a container for the resource records cached by the DNS Server.</span></span> <span data-ttu-id="e5eca-109">請勿將此與包含根提示的快取檔案混淆。</span><span class="sxs-lookup"><span data-stu-id="e5eca-109">Do not confuse this with a Cache file that contains root hints.</span></span>

<span data-ttu-id="e5eca-110">類別 MicrosoftDNS 快取的 **每 \_** 個實例都必須只指派給一部 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5eca-110">Every instance of the class **MicrosoftDNS\_Cache** must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="e5eca-111">它可能會與多個 [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md) 或 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 類別的實例相關聯。</span><span class="sxs-lookup"><span data-stu-id="e5eca-111">It may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="e5eca-112">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="e5eca-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5eca-113">語法</span><span class="sxs-lookup"><span data-stu-id="e5eca-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="e5eca-114">成員</span><span class="sxs-lookup"><span data-stu-id="e5eca-114">Members</span></span>

<span data-ttu-id="e5eca-115">**MicrosoftDNS \_ Cache** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e5eca-115">The **MicrosoftDNS\_Cache** class has these types of members:</span></span>

-   [<span data-ttu-id="e5eca-116">方法</span><span class="sxs-lookup"><span data-stu-id="e5eca-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e5eca-117">方法</span><span class="sxs-lookup"><span data-stu-id="e5eca-117">Methods</span></span>

<span data-ttu-id="e5eca-118">**MicrosoftDNS \_ Cache** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e5eca-118">The **MicrosoftDNS\_Cache** class has these methods.</span></span>



| <span data-ttu-id="e5eca-119">方法</span><span class="sxs-lookup"><span data-stu-id="e5eca-119">Method</span></span>                   | <span data-ttu-id="e5eca-120">描述</span><span class="sxs-lookup"><span data-stu-id="e5eca-120">Description</span></span>                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5eca-121">**ClearCache**</span><span class="sxs-lookup"><span data-stu-id="e5eca-121">**ClearCache**</span></span>           | <span data-ttu-id="e5eca-122">清除資源記錄的 DNS 伺服器快取。</span><span class="sxs-lookup"><span data-stu-id="e5eca-122">Clears the DNS Server cache of resource records.</span></span> <br/> <span data-ttu-id="e5eca-123">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="e5eca-123">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="e5eca-124">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="e5eca-124">**GetDistinguishedName**</span></span> | <span data-ttu-id="e5eca-125">捕獲區域的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="e5eca-125">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="e5eca-126">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="e5eca-126">Qualifiers: Implemented</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="e5eca-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5eca-127">Requirements</span></span>



| <span data-ttu-id="e5eca-128">需求</span><span class="sxs-lookup"><span data-stu-id="e5eca-128">Requirement</span></span> | <span data-ttu-id="e5eca-129">值</span><span class="sxs-lookup"><span data-stu-id="e5eca-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5eca-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5eca-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e5eca-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="e5eca-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e5eca-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5eca-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e5eca-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5eca-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e5eca-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5eca-134">Namespace</span></span><br/>                | <span data-ttu-id="e5eca-135">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e5eca-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e5eca-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e5eca-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5eca-137"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5eca-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5eca-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5eca-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5eca-139">**MicrosoftDNS \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="e5eca-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="e5eca-140">**MicrosoftDNS Cache 類別的 ClearCache 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="e5eca-140">**ClearCache Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-clearcache.md)
</dt> <dt>

[<span data-ttu-id="e5eca-141">**MicrosoftDNS Cache 類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="e5eca-141">**GetDistinguishedName Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





