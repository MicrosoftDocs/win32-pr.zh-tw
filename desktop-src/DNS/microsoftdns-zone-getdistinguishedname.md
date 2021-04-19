---
title: MicrosoftDNS_Zone 類別的 GetDistinguishedName 方法
description: GetDistinguishedName 方法會抓取區域的分辨名稱。 |MicrosoftDNS_Zone 類別的 GetDistinguishedName 方法
ms.assetid: 234dbb43-913e-43e2-b09d-d0c3e449af82
keywords:
- GetDistinguishedName 方法 DNS
- GetDistinguishedName 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，GetDistinguishedName 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73ed620761e4b7a07e7aeaf20d85f646a1aab6b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106985854"
---
# <a name="getdistinguishedname-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="789c9-107">MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="789c9-107">GetDistinguishedName method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="789c9-108">**GetDistinguishedName** 方法會抓取區域的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="789c9-108">The **GetDistinguishedName** method retrieves the distinguished name for the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="789c9-109">語法</span><span class="sxs-lookup"><span data-stu-id="789c9-109">Syntax</span></span>


```mof
string GetDistinguishedName();
```



## <a name="parameters"></a><span data-ttu-id="789c9-110">參數</span><span class="sxs-lookup"><span data-stu-id="789c9-110">Parameters</span></span>

<span data-ttu-id="789c9-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="789c9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="789c9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="789c9-112">Return value</span></span>

<span data-ttu-id="789c9-113">傳回區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="789c9-113">Returns the name of the zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="789c9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="789c9-114">Requirements</span></span>



| <span data-ttu-id="789c9-115">需求</span><span class="sxs-lookup"><span data-stu-id="789c9-115">Requirement</span></span> | <span data-ttu-id="789c9-116">值</span><span class="sxs-lookup"><span data-stu-id="789c9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="789c9-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="789c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="789c9-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="789c9-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="789c9-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="789c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="789c9-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="789c9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="789c9-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="789c9-121">Namespace</span></span><br/>                | <span data-ttu-id="789c9-122">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="789c9-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="789c9-123">MOF</span><span class="sxs-lookup"><span data-stu-id="789c9-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="789c9-124"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="789c9-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="789c9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="789c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789c9-126">**MicrosoftDNS \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="789c9-126">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="789c9-127">**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-127">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="789c9-128">**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-128">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="789c9-129">**MicrosoftDNS 區域類別的 CreateZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-129">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="789c9-130">**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-130">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="789c9-131">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-131">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="789c9-132">**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-132">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="789c9-133">**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-133">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="789c9-134">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-134">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="789c9-135">**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-135">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="789c9-136">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="789c9-136">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





