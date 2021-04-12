---
title: MicrosoftDNS_Zone 類別的 CreateZone 方法
description: CreateZone 方法會建立 DNS 區域。
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- CreateZone 方法 DNS
- CreateZone 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，CreateZone 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025272"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="9b01e-106">MicrosoftDNS 區域類別的 CreateZone 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9b01e-106">CreateZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="9b01e-107">**CreateZone** 方法會建立 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="9b01e-107">The **CreateZone** method creates a DNS zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b01e-108">語法</span><span class="sxs-lookup"><span data-stu-id="9b01e-108">Syntax</span></span>


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9b01e-109">參數</span><span class="sxs-lookup"><span data-stu-id="9b01e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b01e-110">*ZoneName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b01e-110">*ZoneName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b01e-111">代表區功能變數名稱稱的字串。</span><span class="sxs-lookup"><span data-stu-id="9b01e-111">String representing the name of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="9b01e-112">*ZoneType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b01e-112">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b01e-113">區欄位型別。</span><span class="sxs-lookup"><span data-stu-id="9b01e-113">Type of zone.</span></span> <span data-ttu-id="9b01e-114">有效的值如下：</span><span class="sxs-lookup"><span data-stu-id="9b01e-114">Valid values are the following:</span></span>



| <span data-ttu-id="9b01e-115">值</span><span class="sxs-lookup"><span data-stu-id="9b01e-115">Value</span></span>                                                                        | <span data-ttu-id="9b01e-116">意義</span><span class="sxs-lookup"><span data-stu-id="9b01e-116">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9b01e-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9b01e-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="9b01e-118">AD 整合。</span><span class="sxs-lookup"><span data-stu-id="9b01e-118">AD integrated.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="9b01e-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9b01e-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="9b01e-120">次要區域。</span><span class="sxs-lookup"><span data-stu-id="9b01e-120">Secondary zone.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="9b01e-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9b01e-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9b01e-122">虛設常式區域。</span><span class="sxs-lookup"><span data-stu-id="9b01e-122">Stub zone.</span></span><br/> <span data-ttu-id="9b01e-123">**Windows Server 2003：** 此區欄位型別是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="9b01e-123">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/>      |
| <dl> <span data-ttu-id="9b01e-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9b01e-124"><dt>4</dt></span></span> </dl> | <span data-ttu-id="9b01e-125">區域轉寄站。</span><span class="sxs-lookup"><span data-stu-id="9b01e-125">Zone forwarder.</span></span><br/> <span data-ttu-id="9b01e-126">**Windows Server 2003：** 此區欄位型別是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="9b01e-126">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9b01e-127">*DsIntegrated* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b01e-127">*DsIntegrated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b01e-128">指出區域資料是否儲存在 Active Directory 或檔案中。</span><span class="sxs-lookup"><span data-stu-id="9b01e-128">Indicates whether zone data is stored in the Active Directory or in files.</span></span> <span data-ttu-id="9b01e-129">若為 TRUE，則會將資料儲存在 Active Directory;如果為 FALSE，則表示資料儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="9b01e-129">If TRUE, the data is stored in the Active Directory; if FALSE, the data is stored in files.</span></span>

</dd> <dt>

<span data-ttu-id="9b01e-130">*DataFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9b01e-130">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b01e-131">與區域相關聯的資料檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="9b01e-131">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="9b01e-132">*IpAddr* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9b01e-132">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b01e-133">區域主要 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9b01e-133">IP address of the master DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="9b01e-134">*AdminEmailName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9b01e-134">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b01e-135">負責區域之系統管理員的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="9b01e-135">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="9b01e-136">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="9b01e-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9b01e-137">**MicrosoftDns \_ 區域** 類型的 RR。</span><span class="sxs-lookup"><span data-stu-id="9b01e-137">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b01e-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b01e-138">Return value</span></span>

<span data-ttu-id="9b01e-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9b01e-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b01e-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b01e-140">Requirements</span></span>



| <span data-ttu-id="9b01e-141">需求</span><span class="sxs-lookup"><span data-stu-id="9b01e-141">Requirement</span></span> | <span data-ttu-id="9b01e-142">值</span><span class="sxs-lookup"><span data-stu-id="9b01e-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b01e-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b01e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9b01e-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="9b01e-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9b01e-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b01e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9b01e-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b01e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9b01e-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="9b01e-147">Namespace</span></span><br/>                | <span data-ttu-id="9b01e-148">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="9b01e-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9b01e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="9b01e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b01e-150"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b01e-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b01e-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b01e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b01e-152">**MicrosoftDNS \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="9b01e-152">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="9b01e-153">**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-153">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="9b01e-154">**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-154">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="9b01e-155">**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-155">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="9b01e-156">**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-156">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="9b01e-157">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-157">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="9b01e-158">**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-158">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="9b01e-159">**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-159">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="9b01e-160">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-160">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="9b01e-161">**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-161">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="9b01e-162">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9b01e-162">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





