---
title: MicrosoftDNS_RootHints 類別
description: MicrosoftDNS \_ RootHints 類別描述儲存在 DNS 伺服器上的快取檔案中的 RootHints。 此類別簡化了 DNS 物件的內含專案的視覺化，而不是代表實際的物件。
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints 類別 DNS
- MicrosoftDNS_RootHints 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104159"
---
# <a name="microsoftdns_roothints-class"></a><span data-ttu-id="c59ad-106">MicrosoftDNS \_ RootHints 類別</span><span class="sxs-lookup"><span data-stu-id="c59ad-106">MicrosoftDNS\_RootHints class</span></span>

<span data-ttu-id="c59ad-107">**MicrosoftDNS \_ RootHints** 類別描述儲存在 DNS 伺服器上的快取檔案中的 RootHints。</span><span class="sxs-lookup"><span data-stu-id="c59ad-107">The **MicrosoftDNS\_RootHints** class describes the RootHints stored in a Cache file on a DNS Server.</span></span> <span data-ttu-id="c59ad-108">此類別簡化了 DNS 物件的內含專案的視覺化，而不是代表實際的物件。</span><span class="sxs-lookup"><span data-stu-id="c59ad-108">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span>

<span data-ttu-id="c59ad-109">**MicrosoftDNS \_RootHints** 是 DNS 伺服器在快取檔案中儲存之資源記錄的容器。</span><span class="sxs-lookup"><span data-stu-id="c59ad-109">**MicrosoftDNS\_RootHints** is a container for the resource records stored by the DNS Server in a Cache file.</span></span> <span data-ttu-id="c59ad-110">**MicrosoftDNS \_ RootHints** 類別的每個實例都必須只指派給一部 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c59ad-110">Every instance of the **MicrosoftDNS\_RootHints** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="c59ad-111">它可能會與多個 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 類別的實例相關聯。</span><span class="sxs-lookup"><span data-stu-id="c59ad-111">It may be associated with multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

<span data-ttu-id="c59ad-112">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c59ad-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59ad-113">語法</span><span class="sxs-lookup"><span data-stu-id="c59ad-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="c59ad-114">成員</span><span class="sxs-lookup"><span data-stu-id="c59ad-114">Members</span></span>

<span data-ttu-id="c59ad-115">**MicrosoftDNS \_ RootHints** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c59ad-115">The **MicrosoftDNS\_RootHints** class has these types of members:</span></span>

-   [<span data-ttu-id="c59ad-116">方法</span><span class="sxs-lookup"><span data-stu-id="c59ad-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c59ad-117">方法</span><span class="sxs-lookup"><span data-stu-id="c59ad-117">Methods</span></span>

<span data-ttu-id="c59ad-118">**MicrosoftDNS \_ RootHints** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c59ad-118">The **MicrosoftDNS\_RootHints** class has these methods.</span></span>



| <span data-ttu-id="c59ad-119">方法</span><span class="sxs-lookup"><span data-stu-id="c59ad-119">Method</span></span>                        | <span data-ttu-id="c59ad-120">描述</span><span class="sxs-lookup"><span data-stu-id="c59ad-120">Description</span></span>                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c59ad-121">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="c59ad-121">**GetDistinguishedName**</span></span>      | <span data-ttu-id="c59ad-122">捕獲區域的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="c59ad-122">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="c59ad-123">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="c59ad-123">Qualifiers: Implemented</span></span><br/>   |
| <span data-ttu-id="c59ad-124">**WriteBackRootHintDatafile**</span><span class="sxs-lookup"><span data-stu-id="c59ad-124">**WriteBackRootHintDatafile**</span></span> | <span data-ttu-id="c59ad-125">將 RootHints 回寫至 DNS 快取檔案。</span><span class="sxs-lookup"><span data-stu-id="c59ad-125">Writes the RootHints back to the DNS Cache file.</span></span> <br/> <span data-ttu-id="c59ad-126">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="c59ad-126">Qualifiers: Implemented</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c59ad-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c59ad-127">Requirements</span></span>



| <span data-ttu-id="c59ad-128">需求</span><span class="sxs-lookup"><span data-stu-id="c59ad-128">Requirement</span></span> | <span data-ttu-id="c59ad-129">值</span><span class="sxs-lookup"><span data-stu-id="c59ad-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c59ad-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c59ad-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c59ad-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="c59ad-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c59ad-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c59ad-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c59ad-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c59ad-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c59ad-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="c59ad-134">Namespace</span></span><br/>                | <span data-ttu-id="c59ad-135">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c59ad-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c59ad-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c59ad-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c59ad-137"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="c59ad-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59ad-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c59ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59ad-139">**MicrosoftDNS \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="c59ad-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="c59ad-140">**MicrosoftDNS RootHints 類別的 WriteBackRootHintDatafile 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="c59ad-140">**WriteBackRootHintDatafile Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[<span data-ttu-id="c59ad-141">**MicrosoftDNS RootHints 類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="c59ad-141">**GetDistinguishedName Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





