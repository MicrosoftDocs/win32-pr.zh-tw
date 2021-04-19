---
title: MicrosoftDNS_Zone 類別的 ForceRefresh 方法
description: ForceRefresh 方法會從主伺服器強制更新次要 DNS 伺服器。
ms.assetid: 8dde1703-53c3-4d1e-bfb3-f6d5d1666740
keywords:
- ForceRefresh 方法 DNS
- ForceRefresh 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，ForceRefresh 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ForceRefresh
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85390230b0a0852ee479bc8b7e396972f6e69080
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973342"
---
# <a name="forcerefresh-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="72095-106">MicrosoftDNS 區域類別的 ForceRefresh 方法 \_</span><span class="sxs-lookup"><span data-stu-id="72095-106">ForceRefresh method of the MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="72095-107">本文包含「主伺服器」一詞的參考，也就是 Microsoft 不再使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="72095-107">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="72095-108">從軟體中移除該字詞時，我們也會將其從本文中移除。</span><span class="sxs-lookup"><span data-stu-id="72095-108">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="72095-109">**ForceRefresh** 方法會從主伺服器強制更新次要 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="72095-109">The **ForceRefresh** method forces an update of the secondary DNS Server from the master server.</span></span>

## <a name="syntax"></a><span data-ttu-id="72095-110">語法</span><span class="sxs-lookup"><span data-stu-id="72095-110">Syntax</span></span>


```mof
void ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="72095-111">參數</span><span class="sxs-lookup"><span data-stu-id="72095-111">Parameters</span></span>

<span data-ttu-id="72095-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="72095-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72095-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="72095-113">Return value</span></span>

<span data-ttu-id="72095-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="72095-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="72095-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="72095-115">Requirements</span></span>



| <span data-ttu-id="72095-116">需求</span><span class="sxs-lookup"><span data-stu-id="72095-116">Requirement</span></span> | <span data-ttu-id="72095-117">值</span><span class="sxs-lookup"><span data-stu-id="72095-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72095-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72095-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72095-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="72095-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="72095-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72095-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72095-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72095-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="72095-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="72095-122">Namespace</span></span><br/>                | <span data-ttu-id="72095-123">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="72095-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="72095-124">MOF</span><span class="sxs-lookup"><span data-stu-id="72095-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72095-125"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="72095-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72095-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72095-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72095-127">**MicrosoftDNS \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="72095-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="72095-128">**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="72095-129">**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="72095-130">**MicrosoftDNS 區域類別的 CreateZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="72095-131">**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-131">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="72095-132">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-132">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="72095-133">**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-133">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="72095-134">**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-134">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="72095-135">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-135">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="72095-136">**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-136">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="72095-137">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="72095-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





