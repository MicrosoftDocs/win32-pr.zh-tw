---
title: MicrosoftDNS_Zone 類別的 UpdateFromDS 方法
description: UpdateFromDS 方法會強制將區域從目錄服務更新 (DS) 。
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- UpdateFromDS 方法 DNS
- UpdateFromDS 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，UpdateFromDS 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106571"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="fce5d-106">MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fce5d-106">UpdateFromDS method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="fce5d-107">**UpdateFromDS** 方法會強制將區域從目錄服務更新 (DS) 。</span><span class="sxs-lookup"><span data-stu-id="fce5d-107">The **UpdateFromDS** method forces an update of the zone from the Directory Service (DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="fce5d-108">語法</span><span class="sxs-lookup"><span data-stu-id="fce5d-108">Syntax</span></span>


```mof
void UpdateFromDS();
```



## <a name="parameters"></a><span data-ttu-id="fce5d-109">參數</span><span class="sxs-lookup"><span data-stu-id="fce5d-109">Parameters</span></span>

<span data-ttu-id="fce5d-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fce5d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fce5d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fce5d-111">Return value</span></span>

<span data-ttu-id="fce5d-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fce5d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fce5d-113">備註</span><span class="sxs-lookup"><span data-stu-id="fce5d-113">Remarks</span></span>

<span data-ttu-id="fce5d-114">為了順利執行此方法，ZoneType 必須為零，而且必須將區域儲存在 DS 上。</span><span class="sxs-lookup"><span data-stu-id="fce5d-114">In order to successfully execute this method, the ZoneType must be zero, and the zone must be stored on the DS.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce5d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fce5d-115">Requirements</span></span>



| <span data-ttu-id="fce5d-116">需求</span><span class="sxs-lookup"><span data-stu-id="fce5d-116">Requirement</span></span> | <span data-ttu-id="fce5d-117">值</span><span class="sxs-lookup"><span data-stu-id="fce5d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fce5d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fce5d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fce5d-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="fce5d-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fce5d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fce5d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fce5d-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fce5d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fce5d-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="fce5d-122">Namespace</span></span><br/>                | <span data-ttu-id="fce5d-123">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="fce5d-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fce5d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="fce5d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fce5d-125"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="fce5d-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce5d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fce5d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce5d-127">**MicrosoftDNS \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="fce5d-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="fce5d-128">**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="fce5d-129">**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="fce5d-130">**MicrosoftDNS 區域類別的 CreateZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="fce5d-131">**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-131">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="fce5d-132">**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-132">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="fce5d-133">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-133">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="fce5d-134">**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-134">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="fce5d-135">**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-135">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="fce5d-136">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-136">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="fce5d-137">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fce5d-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





