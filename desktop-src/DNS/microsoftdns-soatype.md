---
title: MicrosoftDNS_SOAType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示 (SOA) 記錄的授權啟動。
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- MicrosoftDNS_SOAType 類別 DNS
- MicrosoftDNS_SOAType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024714"
---
# <a name="microsoftdns_soatype-class"></a><span data-ttu-id="b2682-105">MicrosoftDNS \_ SOAType 類別</span><span class="sxs-lookup"><span data-stu-id="b2682-105">MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="b2682-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示 (SOA) 記錄的授權啟動。</span><span class="sxs-lookup"><span data-stu-id="b2682-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Start Of Authority (SOA) record.</span></span>

<span data-ttu-id="b2682-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="b2682-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2682-108">語法</span><span class="sxs-lookup"><span data-stu-id="b2682-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a><span data-ttu-id="b2682-109">成員</span><span class="sxs-lookup"><span data-stu-id="b2682-109">Members</span></span>

<span data-ttu-id="b2682-110">**MicrosoftDNS \_ SOAType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b2682-110">The **MicrosoftDNS\_SOAType** class has these types of members:</span></span>

-   [<span data-ttu-id="b2682-111">方法</span><span class="sxs-lookup"><span data-stu-id="b2682-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b2682-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b2682-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b2682-113">方法</span><span class="sxs-lookup"><span data-stu-id="b2682-113">Methods</span></span>

<span data-ttu-id="b2682-114">**MicrosoftDNS \_ SOAType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b2682-114">The **MicrosoftDNS\_SOAType** class has these methods.</span></span>



| <span data-ttu-id="b2682-115">方法</span><span class="sxs-lookup"><span data-stu-id="b2682-115">Method</span></span>     | <span data-ttu-id="b2682-116">描述</span><span class="sxs-lookup"><span data-stu-id="b2682-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2682-117">**修改**</span><span class="sxs-lookup"><span data-stu-id="b2682-117">**Modify**</span></span> | <span data-ttu-id="b2682-118">將區域) 的 TTL、SOA 序號、主伺服器、負責合作物件、重新整理間隔、重試延遲、到期限制和最小 TTL (更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="b2682-118">Updates the TTL, SOA Serial Number, Primary Server, Responsible Party, Refresh Interval, Retry Delay, Expire Limit and Minimum TTL (for the zone) to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="b2682-119">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="b2682-119">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="b2682-120">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="b2682-120">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="b2682-121">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="b2682-121">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b2682-122">屬性</span><span class="sxs-lookup"><span data-stu-id="b2682-122">Properties</span></span>

<span data-ttu-id="b2682-123">**MicrosoftDNS \_ SOAType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b2682-123">The **MicrosoftDNS\_SOAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2682-124">**ExpireLimit**</span><span class="sxs-lookup"><span data-stu-id="b2682-124">**ExpireLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2682-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b2682-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2682-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2682-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2682-127">沒有回應的區域不再有授權之前的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b2682-127">Time, in seconds, before an unresponsive zone is no longer authoritative.</span></span>

</dd> <dt>

<span data-ttu-id="b2682-128">**MinimumTTL**</span><span class="sxs-lookup"><span data-stu-id="b2682-128">**MinimumTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2682-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b2682-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2682-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2682-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2682-131">允許 DNS 伺服器或快取解析程式從這個記錄所屬的區域快取任何資源記錄的時間限制下限（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b2682-131">Lower limit on the time, in seconds, that a DNS Server or Caching resolver are allowed to cache any resource record from the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="b2682-132">**>primaryserver**</span><span class="sxs-lookup"><span data-stu-id="b2682-132">**PrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2682-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b2682-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2682-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2682-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2682-135">記錄所屬區域的授權 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b2682-135">Authoritative DNS Server for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="b2682-136">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="b2682-136">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2682-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b2682-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2682-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2682-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2682-139">應重新整理包含此記錄之區域之前的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b2682-139">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="b2682-140">**ResponsibleParty**</span><span class="sxs-lookup"><span data-stu-id="b2682-140">**ResponsibleParty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2682-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b2682-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2682-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2682-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2682-143">記錄所屬區域的負責任合作物件名稱。</span><span class="sxs-lookup"><span data-stu-id="b2682-143">Name of the responsible party for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="b2682-144">**RetryDelay**</span><span class="sxs-lookup"><span data-stu-id="b2682-144">**RetryDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2682-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b2682-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2682-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2682-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2682-147">在重試此記錄所屬區域的重新整理失敗之前的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b2682-147">Time, in seconds, before retrying a failed refresh of the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="b2682-148">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b2682-148">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2682-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b2682-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2682-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b2682-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2682-151">SOA 記錄的序號。</span><span class="sxs-lookup"><span data-stu-id="b2682-151">Serial number of the SOA record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2682-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2682-152">Requirements</span></span>



| <span data-ttu-id="b2682-153">需求</span><span class="sxs-lookup"><span data-stu-id="b2682-153">Requirement</span></span> | <span data-ttu-id="b2682-154">值</span><span class="sxs-lookup"><span data-stu-id="b2682-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2682-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2682-155">Minimum supported client</span></span><br/> | <span data-ttu-id="b2682-156">都不支援</span><span class="sxs-lookup"><span data-stu-id="b2682-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b2682-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2682-157">Minimum supported server</span></span><br/> | <span data-ttu-id="b2682-158">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2682-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b2682-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="b2682-159">Namespace</span></span><br/>                | <span data-ttu-id="b2682-160">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="b2682-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b2682-161">MOF</span><span class="sxs-lookup"><span data-stu-id="b2682-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2682-162"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2682-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2682-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2682-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2682-164">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="b2682-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="b2682-165">**Modify MicrosoftDNS \_ SOAType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="b2682-165">**Modify Method of the MicrosoftDNS\_SOAType Class**</span></span>](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





