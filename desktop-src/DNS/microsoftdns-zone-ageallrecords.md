---
title: MicrosoftDNS_Zone 類別的 AgeAllRecords 方法
description: AgeAllRecords 方法可讓區域中的部分或所有非 NS 和非 SOA 記錄過時。
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- AgeAllRecords 方法 DNS
- AgeAllRecords 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，AgeAllRecords 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466481"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="b7cf6-106">MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b7cf6-106">AgeAllRecords method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="b7cf6-107">**AgeAllRecords** 方法可讓區域中的部分或所有非 NS 和非 SOA 記錄過時。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-107">The **AgeAllRecords** method enables aging for some or all non-NS and non-SOA records in a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cf6-108">語法</span><span class="sxs-lookup"><span data-stu-id="b7cf6-108">Syntax</span></span>


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a><span data-ttu-id="b7cf6-109">參數</span><span class="sxs-lookup"><span data-stu-id="b7cf6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7cf6-110">*NodeName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b7cf6-110">*NodeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cf6-111">要存在之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-111">Name of the node to age.</span></span>

</dd> <dt>

<span data-ttu-id="b7cf6-112">*ApplyToSubtree* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b7cf6-112">*ApplyToSubtree* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cf6-113">指定是否要將過時套用至子樹中的所有記錄。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-113">Specifies whether aging should apply to all records in the subtree.</span></span> <span data-ttu-id="b7cf6-114">設定為 TRUE 會將過時套用至子樹中的所有記錄（以 NodeName 開頭）。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-114">Set to TRUE to apply aging to all records in the subtree, beginning with NodeName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7cf6-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7cf6-115">Return value</span></span>

<span data-ttu-id="b7cf6-116">錯誤 \_ 成功表示已順利完成過時。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-116">ERROR\_SUCCESS indicates the aging was successfully completed.</span></span> <span data-ttu-id="b7cf6-117">任何其他值都是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-117">Any other value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7cf6-118">備註</span><span class="sxs-lookup"><span data-stu-id="b7cf6-118">Remarks</span></span>

<span data-ttu-id="b7cf6-119">如果未指定 *NodeName* ，所有記錄都會受到過時和清除的規定。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-119">If *NodeName* is not specified, all records will be subject to aging and scavenging.</span></span>

<span data-ttu-id="b7cf6-120">如果指定了 *NodeName* ，且 *ApplyToSubtree* 未指定或設定為零，則指定節點上的記錄會被視為過時和清除。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-120">If *NodeName* is specified and *ApplyToSubtree* is not specified or set to zero, records at the specified node will be subjected to aging and scavenging.</span></span>

<span data-ttu-id="b7cf6-121">如果指定了 *NodeName* ，且 *ApplyToSubtree* 設定為1，則從 *nodename* 開始的子樹狀結構的所有記錄都會被視為過時和清除。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-121">If *NodeName* is specified and *ApplyToSubtree* is set to 1, all records of the subtree starting at *NodeName* will be subjected to aging and scavenging.</span></span> <span data-ttu-id="b7cf6-122">時間戳記會設定為所有非 NS 和非 SOA Rr 的目前時間，其擁有者名稱 (s) 由輸入參數識別。</span><span class="sxs-lookup"><span data-stu-id="b7cf6-122">The time stamp is set to the current time for all non-NS and non-SOA RRs with the owner name(s) identified by the input parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7cf6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7cf6-123">Requirements</span></span>



| <span data-ttu-id="b7cf6-124">需求</span><span class="sxs-lookup"><span data-stu-id="b7cf6-124">Requirement</span></span> | <span data-ttu-id="b7cf6-125">值</span><span class="sxs-lookup"><span data-stu-id="b7cf6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cf6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7cf6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b7cf6-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="b7cf6-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b7cf6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7cf6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b7cf6-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7cf6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b7cf6-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="b7cf6-130">Namespace</span></span><br/>                | <span data-ttu-id="b7cf6-131">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="b7cf6-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b7cf6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b7cf6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7cf6-133"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7cf6-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7cf6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7cf6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7cf6-135">**MicrosoftDNS \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-135">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-136">**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-136">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-137">**MicrosoftDNS 區域類別的 CreateZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-137">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-138">**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-138">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-139">**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-139">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-140">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-140">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-141">**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-141">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-142">**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-142">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-143">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-143">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-144">**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-144">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="b7cf6-145">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b7cf6-145">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





