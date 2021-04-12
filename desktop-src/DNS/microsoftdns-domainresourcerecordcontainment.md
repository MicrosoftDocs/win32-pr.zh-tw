---
title: MicrosoftDNS_DomainResourceRecordContainment 類別
description: MicrosoftDNS \_ DomainResourceRecordContainment 類別可用於 RR 內含專案; MicrosoftDNS 網域的每個實例 \_ 可能包含多個 MicrosoftDNS \_ ResourceRecord 類別的實例。
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment 類別 DNS
- MicrosoftDNS_DomainResourceRecordContainment 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465333"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a><span data-ttu-id="952e9-105">MicrosoftDNS \_ DomainResourceRecordContainment 類別</span><span class="sxs-lookup"><span data-stu-id="952e9-105">MicrosoftDNS\_DomainResourceRecordContainment class</span></span>

<span data-ttu-id="952e9-106">**MicrosoftDNS \_ DomainResourceRecordContainment** 類別可用於 RR 內含專案; [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md)的每個實例可能包含多個 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="952e9-106">The **MicrosoftDNS\_DomainResourceRecordContainment** class is used for RR containment; every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) may contain multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span> <span data-ttu-id="952e9-107">**MicrosoftDNS \_ ResourceRecord** 類別的每個實例都屬於 **MicrosoftDNS \_ 網域** 類別的單一實例，且定義為該實例的弱式。</span><span class="sxs-lookup"><span data-stu-id="952e9-107">Every instance of the **MicrosoftDNS\_ResourceRecord** class belongs to a single instance of the **MicrosoftDNS\_Domain** class, and is defined to be weak to that instance.</span></span>

<span data-ttu-id="952e9-108">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="952e9-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="952e9-109">語法</span><span class="sxs-lookup"><span data-stu-id="952e9-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="952e9-110">成員</span><span class="sxs-lookup"><span data-stu-id="952e9-110">Members</span></span>

<span data-ttu-id="952e9-111">**MicrosoftDNS \_ DomainResourceRecordContainment** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="952e9-111">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="952e9-112">屬性</span><span class="sxs-lookup"><span data-stu-id="952e9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="952e9-113">屬性</span><span class="sxs-lookup"><span data-stu-id="952e9-113">Properties</span></span>

<span data-ttu-id="952e9-114">**MicrosoftDNS \_ DomainResourceRecordContainment** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="952e9-114">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="952e9-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="952e9-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e9-116">資料類型： **MicrosoftDNS \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="952e9-116">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="952e9-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="952e9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e9-118">限定詞： Key、Override ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="952e9-118">Qualifiers: Key, Override("GroupComponent")</span></span>

<span data-ttu-id="952e9-119">描述：直接包含資源記錄的區域、快取、RootHints 或網域。</span><span class="sxs-lookup"><span data-stu-id="952e9-119">Description: The Zone, Cache, RootHints or Domain directly containing the Resource Record.</span></span>

<span data-ttu-id="952e9-120">繼承自 CIM \_ 元件</span><span class="sxs-lookup"><span data-stu-id="952e9-120">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="952e9-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="952e9-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e9-122">資料類型： **MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="952e9-122">Data type: **MicrosoftDNS\_ResourceRecord**</span></span>
</dt> <dt>

<span data-ttu-id="952e9-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="952e9-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e9-124">限定詞： Key、Override ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="952e9-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="952e9-125">描述：網域、區域、快取或 RootHints 中包含的資源記錄。</span><span class="sxs-lookup"><span data-stu-id="952e9-125">Description: The resource record contained in a Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="952e9-126">繼承自 CIM \_ 元件。</span><span class="sxs-lookup"><span data-stu-id="952e9-126">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="952e9-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="952e9-127">Requirements</span></span>



| <span data-ttu-id="952e9-128">需求</span><span class="sxs-lookup"><span data-stu-id="952e9-128">Requirement</span></span> | <span data-ttu-id="952e9-129">值</span><span class="sxs-lookup"><span data-stu-id="952e9-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="952e9-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="952e9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="952e9-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="952e9-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="952e9-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="952e9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="952e9-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952e9-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="952e9-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="952e9-134">Namespace</span></span><br/>                | <span data-ttu-id="952e9-135">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="952e9-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="952e9-136">MOF</span><span class="sxs-lookup"><span data-stu-id="952e9-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="952e9-137"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="952e9-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="952e9-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="952e9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="952e9-139">**MicrosoftDNS \_ ServerDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="952e9-139">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="952e9-140">**MicrosoftDNS \_ DomainDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="952e9-140">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="952e9-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="952e9-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





