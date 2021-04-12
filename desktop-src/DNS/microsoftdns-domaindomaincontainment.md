---
title: MicrosoftDNS_DomainDomainContainment 類別
description: MicrosoftDNS \_ DomainDomainContainment 類別用於定義域內含專案;DNS 網域可能包含其他 DNS 網域。
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment 類別 DNS
- MicrosoftDNS_DomainDomainContainment 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025341"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a><span data-ttu-id="71f85-105">MicrosoftDNS \_ DomainDomainContainment 類別</span><span class="sxs-lookup"><span data-stu-id="71f85-105">MicrosoftDNS\_DomainDomainContainment class</span></span>

<span data-ttu-id="71f85-106">**MicrosoftDNS \_ DomainDomainContainment** 類別用於定義域內含專案;DNS 網域可能包含其他 DNS 網域。</span><span class="sxs-lookup"><span data-stu-id="71f85-106">The **MicrosoftDNS\_DomainDomainContainment** class is used for domain containment; DNS domains may contain other DNS domains.</span></span> <span data-ttu-id="71f85-107">[**MicrosoftDNS \_ 網域**](microsoftdns-domain.md)類別的每個實例都可以包含多個 **MicrosoftDNS \_ 網域** 的其他實例。</span><span class="sxs-lookup"><span data-stu-id="71f85-107">Every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class may contain multiple other instances of **MicrosoftDNS\_Domain**.</span></span> <span data-ttu-id="71f85-108">**MicrosoftDNS \_ 網域** 物件的實例直接包含在一個以上的較高層級 **MicrosoftDNS \_ 網域** 中。</span><span class="sxs-lookup"><span data-stu-id="71f85-108">An instance of a **MicrosoftDNS\_Domain** object is directly contained in no more than one higher level **MicrosoftDNS\_Domain**.</span></span>

<span data-ttu-id="71f85-109">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="71f85-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f85-110">語法</span><span class="sxs-lookup"><span data-stu-id="71f85-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="71f85-111">成員</span><span class="sxs-lookup"><span data-stu-id="71f85-111">Members</span></span>

<span data-ttu-id="71f85-112">**MicrosoftDNS \_ DomainDomainContainment** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="71f85-112">The **MicrosoftDNS\_DomainDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="71f85-113">屬性</span><span class="sxs-lookup"><span data-stu-id="71f85-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71f85-114">屬性</span><span class="sxs-lookup"><span data-stu-id="71f85-114">Properties</span></span>

<span data-ttu-id="71f85-115">**MicrosoftDNS \_ DomainDomainContainment** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="71f85-115">The **MicrosoftDNS\_DomainDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71f85-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="71f85-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f85-117">資料類型： **MicrosoftDNS \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="71f85-117">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="71f85-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71f85-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71f85-119">限定詞：索引鍵、最大 (1) 、覆寫 ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="71f85-119">Qualifiers: Key, Max(1), Override("GroupComponent")</span></span>

<span data-ttu-id="71f85-120">描述：較高層級的網域、區域、快取或 RootHints。</span><span class="sxs-lookup"><span data-stu-id="71f85-120">Description: A higher level Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="71f85-121">繼承自 CIM \_ 元件</span><span class="sxs-lookup"><span data-stu-id="71f85-121">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="71f85-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="71f85-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f85-123">資料類型： **MicrosoftDNS \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="71f85-123">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="71f85-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71f85-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71f85-125">限定詞： Key、Override ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="71f85-125">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="71f85-126">描述：較高層級網域、區域、快取或 RootHints 所包含的網域。</span><span class="sxs-lookup"><span data-stu-id="71f85-126">Description: The Domain contained by a higher level Domain, Zone, Cache or RootHints.</span></span>

<span data-ttu-id="71f85-127">繼承自 CIM \_ 元件。</span><span class="sxs-lookup"><span data-stu-id="71f85-127">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71f85-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="71f85-128">Requirements</span></span>



| <span data-ttu-id="71f85-129">需求</span><span class="sxs-lookup"><span data-stu-id="71f85-129">Requirement</span></span> | <span data-ttu-id="71f85-130">值</span><span class="sxs-lookup"><span data-stu-id="71f85-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71f85-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71f85-131">Minimum supported client</span></span><br/> | <span data-ttu-id="71f85-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="71f85-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="71f85-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71f85-133">Minimum supported server</span></span><br/> | <span data-ttu-id="71f85-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71f85-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="71f85-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="71f85-135">Namespace</span></span><br/>                | <span data-ttu-id="71f85-136">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="71f85-136">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="71f85-137">MOF</span><span class="sxs-lookup"><span data-stu-id="71f85-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71f85-138"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="71f85-138"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71f85-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71f85-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f85-140">**MicrosoftDNS \_ DomainResourceRecordContainment**</span><span class="sxs-lookup"><span data-stu-id="71f85-140">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="71f85-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="71f85-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="71f85-142">**MicrosoftDNS \_ ServerDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="71f85-142">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





