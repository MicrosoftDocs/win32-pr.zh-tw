---
title: MicrosoftDNS_Zone 類別的 ResetSecondaries 方法
description: ResetSecondaries 方法會重設區域中次要 DNS 伺服器的 IP 位址。
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- ResetSecondaries 方法 DNS
- ResetSecondaries 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，ResetSecondaries 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934695"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="caf89-106">MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_</span><span class="sxs-lookup"><span data-stu-id="caf89-106">ResetSecondaries method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="caf89-107">**ResetSecondaries** 方法會重設區域中次要 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="caf89-107">The **ResetSecondaries** method resets the IP addresses for secondary DNS Servers in the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf89-108">語法</span><span class="sxs-lookup"><span data-stu-id="caf89-108">Syntax</span></span>


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="caf89-109">參數</span><span class="sxs-lookup"><span data-stu-id="caf89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf89-110">*SecondaryServers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caf89-110">*SecondaryServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf89-111">次要 DNS 伺服器的 IP 位址陣列。</span><span class="sxs-lookup"><span data-stu-id="caf89-111">Array of IP addresses for secondary DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="caf89-112">*SecureSecondaries* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caf89-112">*SecureSecondaries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf89-113">指定要套用的安全性，而且必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="caf89-113">Specifies the security to be applied and must be one of the following:</span></span>

-   <span data-ttu-id="caf89-114">區域 \_ SECSECURE \_ 無 \_ 安全性</span><span class="sxs-lookup"><span data-stu-id="caf89-114">ZONE\_SECSECURE\_NO\_SECURITY</span></span>
-   <span data-ttu-id="caf89-115">\_ \_ 僅限區域 SECSECURE NS \_</span><span class="sxs-lookup"><span data-stu-id="caf89-115">ZONE\_SECSECURE\_NS\_ONLY</span></span>
-   <span data-ttu-id="caf89-116">\_ \_ 僅限區域 SECSECURE 清單 \_</span><span class="sxs-lookup"><span data-stu-id="caf89-116">ZONE\_SECSECURE\_LIST\_ONLY</span></span>
-   <span data-ttu-id="caf89-117">區域 \_ SECSECURE \_ 沒有 \_ XFR</span><span class="sxs-lookup"><span data-stu-id="caf89-117">ZONE\_SECSECURE\_NO\_XFR</span></span>

</dd> <dt>

<span data-ttu-id="caf89-118">*NotifyServers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caf89-118">*NotifyServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf89-119">當區域變更時要通知的 DNS 伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="caf89-119">IP address of DNS Servers to be notified when the zone changes.</span></span>

</dd> <dt>

<span data-ttu-id="caf89-120">*通知* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caf89-120">*Notify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf89-121">通知設定，必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="caf89-121">Notification setting and must be one of the following:</span></span>

-   <span data-ttu-id="caf89-122">區域 \_ 通知 \_ 關閉</span><span class="sxs-lookup"><span data-stu-id="caf89-122">ZONE\_NOTIFY\_OFF</span></span>
-   <span data-ttu-id="caf89-123">區域 \_ 通知 \_ 所有 \_ 次要資料庫</span><span class="sxs-lookup"><span data-stu-id="caf89-123">ZONE\_NOTIFY\_ALL\_SECONDARIES</span></span>
-   <span data-ttu-id="caf89-124">\_ \_ 僅限區域通知清單 \_</span><span class="sxs-lookup"><span data-stu-id="caf89-124">ZONE\_NOTIFY\_LIST\_ONLY</span></span>

</dd> <dt>

<span data-ttu-id="caf89-125">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="caf89-125">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="caf89-126">[**MicrosoftDNS \_ 區域**](microsoftdns-zone.md)類型的 RR。</span><span class="sxs-lookup"><span data-stu-id="caf89-126">RR of type [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caf89-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="caf89-127">Return value</span></span>

<span data-ttu-id="caf89-128">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="caf89-128">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="caf89-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="caf89-129">Requirements</span></span>



| <span data-ttu-id="caf89-130">需求</span><span class="sxs-lookup"><span data-stu-id="caf89-130">Requirement</span></span> | <span data-ttu-id="caf89-131">值</span><span class="sxs-lookup"><span data-stu-id="caf89-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="caf89-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="caf89-132">Minimum supported client</span></span><br/> | <span data-ttu-id="caf89-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="caf89-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="caf89-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="caf89-134">Minimum supported server</span></span><br/> | <span data-ttu-id="caf89-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caf89-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="caf89-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="caf89-136">Namespace</span></span><br/>                | <span data-ttu-id="caf89-137">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="caf89-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="caf89-138">MOF</span><span class="sxs-lookup"><span data-stu-id="caf89-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="caf89-139"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="caf89-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caf89-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caf89-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf89-141">**MicrosoftDNS \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="caf89-141">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="caf89-142">**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-142">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="caf89-143">**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-143">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="caf89-144">**MicrosoftDNS 區域類別的 CreateZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-144">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="caf89-145">**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-145">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="caf89-146">**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-146">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="caf89-147">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-147">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="caf89-148">**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-148">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="caf89-149">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-149">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="caf89-150">**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-150">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="caf89-151">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="caf89-151">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





