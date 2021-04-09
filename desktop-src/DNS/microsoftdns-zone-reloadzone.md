---
title: MicrosoftDNS_Zone 類別的 ReloadZone 方法
description: ReloadZone 方法會從其資料庫重載 DNS 區域。
ms.assetid: 9fb3c216-563c-4603-a29a-27627ac644d8
keywords:
- ReloadZone 方法 DNS
- ReloadZone 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，ReloadZone 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ReloadZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e22d9becc5084407267e75d713082ce5dcbb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934696"
---
# <a name="reloadzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="61ef7-106">MicrosoftDNS 區域類別的 ReloadZone 方法 \_</span><span class="sxs-lookup"><span data-stu-id="61ef7-106">ReloadZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="61ef7-107">**ReloadZone** 方法會從其資料庫重載 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="61ef7-107">The **ReloadZone** method reloads the DNS Zone from its database.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ef7-108">語法</span><span class="sxs-lookup"><span data-stu-id="61ef7-108">Syntax</span></span>


```mof
void ReloadZone();
```



## <a name="parameters"></a><span data-ttu-id="61ef7-109">參數</span><span class="sxs-lookup"><span data-stu-id="61ef7-109">Parameters</span></span>

<span data-ttu-id="61ef7-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="61ef7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61ef7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="61ef7-111">Return value</span></span>

<span data-ttu-id="61ef7-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="61ef7-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="61ef7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="61ef7-113">Requirements</span></span>



| <span data-ttu-id="61ef7-114">需求</span><span class="sxs-lookup"><span data-stu-id="61ef7-114">Requirement</span></span> | <span data-ttu-id="61ef7-115">值</span><span class="sxs-lookup"><span data-stu-id="61ef7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61ef7-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61ef7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61ef7-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="61ef7-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="61ef7-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61ef7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61ef7-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61ef7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="61ef7-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="61ef7-120">Namespace</span></span><br/>                | <span data-ttu-id="61ef7-121">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="61ef7-121">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="61ef7-122">MOF</span><span class="sxs-lookup"><span data-stu-id="61ef7-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61ef7-123"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="61ef7-123"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61ef7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61ef7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ef7-125">**MicrosoftDNS \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="61ef7-125">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="61ef7-126">**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-126">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="61ef7-127">**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-127">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="61ef7-128">**MicrosoftDNS 區域類別的 CreateZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-128">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="61ef7-129">**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-129">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="61ef7-130">**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-130">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="61ef7-131">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-131">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="61ef7-132">**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-132">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="61ef7-133">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-133">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="61ef7-134">**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-134">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="61ef7-135">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="61ef7-135">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





