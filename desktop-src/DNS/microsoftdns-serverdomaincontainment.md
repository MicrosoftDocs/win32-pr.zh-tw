---
title: MicrosoftDNS_ServerDomainContainment 類別
description: MicrosoftDNS \_ 伺服器關聯 WMI 類別的每個實例都可以包含多個 MicrosoftDNS \_ 網域類別的實例。
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- MicrosoftDNS_ServerDomainContainment 類別 DNS
- MicrosoftDNS_ServerDomainContainment 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685599"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a><span data-ttu-id="c9507-105">MicrosoftDNS \_ ServerDomainContainment 類別</span><span class="sxs-lookup"><span data-stu-id="c9507-105">MicrosoftDNS\_ServerDomainContainment class</span></span>

<span data-ttu-id="c9507-106">[**MicrosoftDNS \_ 伺服器**](microsoftdns-server.md)關聯 WMI 類別的每個實例都可以包含多個 [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c9507-106">Every instance of the [**MicrosoftDNS\_Server**](microsoftdns-server.md) association WMI class may contain multiple instances of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class.</span></span> <span data-ttu-id="c9507-107">**MicrosoftDNS \_ 網域** 類別的每個實例都屬於 **MicrosoftDNS \_ 伺服器** 類別的單一實例，且定義為該伺服器的弱式。</span><span class="sxs-lookup"><span data-stu-id="c9507-107">Every instance of the **MicrosoftDNS\_Domain** class belongs to a single instance of the **MicrosoftDNS\_Server** class, and is defined to be weak to that server.</span></span>

<span data-ttu-id="c9507-108">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c9507-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9507-109">語法</span><span class="sxs-lookup"><span data-stu-id="c9507-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c9507-110">成員</span><span class="sxs-lookup"><span data-stu-id="c9507-110">Members</span></span>

<span data-ttu-id="c9507-111">**MicrosoftDNS \_ ServerDomainContainment** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c9507-111">The **MicrosoftDNS\_ServerDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="c9507-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c9507-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9507-113">屬性</span><span class="sxs-lookup"><span data-stu-id="c9507-113">Properties</span></span>

<span data-ttu-id="c9507-114">**MicrosoftDNS \_ ServerDomainContainment** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c9507-114">The **MicrosoftDNS\_ServerDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9507-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c9507-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9507-116">資料類型： **MicrosoftDNS \_ Server**</span><span class="sxs-lookup"><span data-stu-id="c9507-116">Data type: **MicrosoftDNS\_Server**</span></span>
</dt> <dt>

<span data-ttu-id="c9507-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c9507-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9507-118">限定詞： Key、Override ( "GroupComponent" ) 、Min (1) 、Max (1) </span><span class="sxs-lookup"><span data-stu-id="c9507-118">Qualifiers: Key, Override ("GroupComponent"), Min (1), Max (1)</span></span>

<span data-ttu-id="c9507-119">描述： DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c9507-119">Description: The DNS Server.</span></span>

<span data-ttu-id="c9507-120">繼承自 **CIM \_ 元件**。</span><span class="sxs-lookup"><span data-stu-id="c9507-120">Inherited from **CIM\_Component**.</span></span>

</dd> <dt>

<span data-ttu-id="c9507-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c9507-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9507-122">資料類型： **MicrosoftDNS \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="c9507-122">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="c9507-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c9507-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9507-124">限定詞： Key、Override ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="c9507-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="c9507-125">描述： DNS 伺服器所管理的網域、區域、快取或 RootHints。</span><span class="sxs-lookup"><span data-stu-id="c9507-125">Description: A Domain, Zone, Cache, or RootHints managed by the DNS Server.</span></span>

<span data-ttu-id="c9507-126">繼承自 **CIM \_ 元件**。</span><span class="sxs-lookup"><span data-stu-id="c9507-126">Inherited from **CIM\_Component**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9507-127">備註</span><span class="sxs-lookup"><span data-stu-id="c9507-127">Remarks</span></span>

<span data-ttu-id="c9507-128">**MicrosoftDNS \_ ServerDomainContainment** 類別衍生自 **CIM \_ 元件** 類別。</span><span class="sxs-lookup"><span data-stu-id="c9507-128">The **MicrosoftDNS\_ServerDomainContainment** class is derived from the **CIM\_Component** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9507-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9507-129">Requirements</span></span>



| <span data-ttu-id="c9507-130">需求</span><span class="sxs-lookup"><span data-stu-id="c9507-130">Requirement</span></span> | <span data-ttu-id="c9507-131">值</span><span class="sxs-lookup"><span data-stu-id="c9507-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9507-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9507-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c9507-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="c9507-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c9507-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9507-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c9507-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9507-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c9507-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9507-136">Namespace</span></span><br/>                | <span data-ttu-id="c9507-137">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c9507-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c9507-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c9507-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9507-139"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9507-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9507-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9507-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9507-141">**MicrosoftDNS \_ DomainDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="c9507-141">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="c9507-142">**MicrosoftDNS \_ DomainResourceRecordContainment**</span><span class="sxs-lookup"><span data-stu-id="c9507-142">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="c9507-143">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c9507-143">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





