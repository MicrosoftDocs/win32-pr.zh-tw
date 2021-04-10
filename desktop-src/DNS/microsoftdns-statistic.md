---
title: MicrosoftDNS_Statistic 類別
description: MicrosoftDNS \_ 統計資料類別代表單一 DNS 伺服器統計資料。
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- MicrosoftDNS_Statistic 類別 DNS
- MicrosoftDNS_Statistic 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025372"
---
# <a name="microsoftdns_statistic-class"></a><span data-ttu-id="fdaca-105">MicrosoftDNS \_ 統計資料類別</span><span class="sxs-lookup"><span data-stu-id="fdaca-105">MicrosoftDNS\_Statistic class</span></span>

<span data-ttu-id="fdaca-106">**MicrosoftDNS \_ 統計** 資料類別代表單一 DNS 伺服器統計資料。</span><span class="sxs-lookup"><span data-stu-id="fdaca-106">The **MicrosoftDNS\_Statistic** class represents a single DNS Server statistic.</span></span>

<span data-ttu-id="fdaca-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="fdaca-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdaca-108">語法</span><span class="sxs-lookup"><span data-stu-id="fdaca-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a><span data-ttu-id="fdaca-109">成員</span><span class="sxs-lookup"><span data-stu-id="fdaca-109">Members</span></span>

<span data-ttu-id="fdaca-110">**MicrosoftDNS \_ 統計** 資料類別有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fdaca-110">The **MicrosoftDNS\_Statistic** class has these types of members:</span></span>

-   [<span data-ttu-id="fdaca-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fdaca-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fdaca-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fdaca-112">Properties</span></span>

<span data-ttu-id="fdaca-113">**MicrosoftDNS \_ 統計** 資料類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fdaca-113">The **MicrosoftDNS\_Statistic** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fdaca-114">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="fdaca-114">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdaca-115">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fdaca-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fdaca-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdaca-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdaca-117">**CollectionName** 的數值標記法。</span><span class="sxs-lookup"><span data-stu-id="fdaca-117">Numeric representation of **CollectionName**.</span></span>

</dd> <dt>

<span data-ttu-id="fdaca-118">**CollectionName**</span><span class="sxs-lookup"><span data-stu-id="fdaca-118">**CollectionName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdaca-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fdaca-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdaca-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdaca-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdaca-121">統計資料所屬集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdaca-121">Name of the collection to which the statistic belongs.</span></span>

</dd> <dt>

<span data-ttu-id="fdaca-122">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="fdaca-122">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdaca-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fdaca-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdaca-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdaca-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdaca-125">指出包含統計資料之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fdaca-125">Indicates the FQDN or IP address of the DNS Server that contains the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="fdaca-126">**名稱**</span><span class="sxs-lookup"><span data-stu-id="fdaca-126">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdaca-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fdaca-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdaca-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdaca-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdaca-129">統計資料的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdaca-129">Name of the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="fdaca-130">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="fdaca-130">**StringValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdaca-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fdaca-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdaca-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdaca-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdaca-133">統計資料的字串值，只有在統計資料值未表示為 DWORD 時才會使用。</span><span class="sxs-lookup"><span data-stu-id="fdaca-133">String value of the statistic, used only when the statistic value is not represented as a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="fdaca-134">**值**</span><span class="sxs-lookup"><span data-stu-id="fdaca-134">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdaca-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fdaca-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fdaca-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdaca-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdaca-137">統計資料的數值，以 DWORD 表示。</span><span class="sxs-lookup"><span data-stu-id="fdaca-137">Numeric value of the statistic, represented as a DWORD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fdaca-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdaca-138">Requirements</span></span>



| <span data-ttu-id="fdaca-139">需求</span><span class="sxs-lookup"><span data-stu-id="fdaca-139">Requirement</span></span> | <span data-ttu-id="fdaca-140">值</span><span class="sxs-lookup"><span data-stu-id="fdaca-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdaca-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdaca-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fdaca-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="fdaca-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fdaca-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdaca-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fdaca-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdaca-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fdaca-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="fdaca-145">Namespace</span></span><br/>                | <span data-ttu-id="fdaca-146">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="fdaca-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fdaca-147">MOF</span><span class="sxs-lookup"><span data-stu-id="fdaca-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdaca-148"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdaca-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdaca-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdaca-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdaca-150">MicrosoftDNS \_ StatisticCollection</span><span class="sxs-lookup"><span data-stu-id="fdaca-150">MicrosoftDNS\_StatisticCollection</span></span>](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





