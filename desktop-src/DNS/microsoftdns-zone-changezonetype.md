---
title: MicrosoftDNS_Zone 類別的 ChangeZoneType 方法
description: ChangeZoneType 方法會變更區域的類型。
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- ChangeZoneType 方法 DNS
- ChangeZoneType 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，ChangeZoneType 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024974"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="2fa0f-106">MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2fa0f-106">ChangeZoneType method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="2fa0f-107">**ChangeZoneType** 方法會變更區域的類型。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-107">The **ChangeZoneType** method changes the type of a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa0f-108">語法</span><span class="sxs-lookup"><span data-stu-id="2fa0f-108">Syntax</span></span>


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2fa0f-109">參數</span><span class="sxs-lookup"><span data-stu-id="2fa0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa0f-110">*ZoneType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2fa0f-110">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa0f-111">區欄位型別。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-111">Type of zone.</span></span> <span data-ttu-id="2fa0f-112">有效的值如下：</span><span class="sxs-lookup"><span data-stu-id="2fa0f-112">Valid values are the following:</span></span>



| <span data-ttu-id="2fa0f-113">值</span><span class="sxs-lookup"><span data-stu-id="2fa0f-113">Value</span></span>                                                                        | <span data-ttu-id="2fa0f-114">意義</span><span class="sxs-lookup"><span data-stu-id="2fa0f-114">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2fa0f-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2fa0f-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="2fa0f-116">主要區域。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-116">Primary zone.</span></span><br/>   |
| <dl> <span data-ttu-id="2fa0f-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2fa0f-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="2fa0f-118">次要區域。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-118">Secondary zone.</span></span><br/> |
| <dl> <span data-ttu-id="2fa0f-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2fa0f-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2fa0f-120">虛設常式區域。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-120">Stub zone.</span></span><br/>      |
| <dl> <span data-ttu-id="2fa0f-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2fa0f-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2fa0f-122">區域轉寄站。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-122">Zone forwarder.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2fa0f-123">*DataFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2fa0f-123">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa0f-124">與區域相關聯的資料檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-124">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="2fa0f-125">*IpAddr* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2fa0f-125">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa0f-126">區域的宿主 DNS 伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-126">IP address of the mater DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="2fa0f-127">*AdminEmailName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2fa0f-127">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa0f-128">負責區域之系統管理員的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-128">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="2fa0f-129">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="2fa0f-129">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa0f-130">**MicrosoftDns \_ 區域** 類型的 RR。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-130">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa0f-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fa0f-131">Return value</span></span>

<span data-ttu-id="2fa0f-132">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2fa0f-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fa0f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fa0f-133">Requirements</span></span>



| <span data-ttu-id="2fa0f-134">需求</span><span class="sxs-lookup"><span data-stu-id="2fa0f-134">Requirement</span></span> | <span data-ttu-id="2fa0f-135">值</span><span class="sxs-lookup"><span data-stu-id="2fa0f-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa0f-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fa0f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa0f-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="2fa0f-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2fa0f-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fa0f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa0f-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fa0f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2fa0f-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="2fa0f-140">Namespace</span></span><br/>                | <span data-ttu-id="2fa0f-141">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="2fa0f-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2fa0f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2fa0f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fa0f-143"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fa0f-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa0f-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fa0f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa0f-145">**MicrosoftDNS \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-145">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-146">**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-146">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-147">**MicrosoftDNS 區域類別的 CreateZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-147">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-148">**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-148">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-149">**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-149">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-150">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-150">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-151">**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-151">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-152">**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-152">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-153">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-153">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-154">**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-154">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="2fa0f-155">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa0f-155">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





