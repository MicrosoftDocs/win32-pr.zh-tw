---
title: Modify MicrosoftDNS_WINSRType 類別的方法
description: Modify 方法會將 WINS 反向查閱 (WINSR) 資源記錄。
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_WINSRType 類別
- MicrosoftDNS_WINSRType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105935"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="d09e6-106">Modify MicrosoftDNS \_ WINSRType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="d09e6-106">Modify method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="d09e6-107">**Modify** 方法會將 WINS 反向查閱 (WINSR) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="d09e6-107">The **Modify** method updates a WINS Reverse Look up (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09e6-108">語法</span><span class="sxs-lookup"><span data-stu-id="d09e6-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d09e6-109">參數</span><span class="sxs-lookup"><span data-stu-id="d09e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d09e6-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d09e6-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d09e6-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d09e6-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d09e6-112">*MappingFlag* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d09e6-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d09e6-113">WINSR 對應旗標，指定是否必須將記錄包含在區域複寫中。</span><span class="sxs-lookup"><span data-stu-id="d09e6-113">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="d09e6-114">它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。</span><span class="sxs-lookup"><span data-stu-id="d09e6-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="d09e6-115">*LookupTimeout* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d09e6-115">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d09e6-116">使用 WINS 反向查閱之 DNS 伺服器的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d09e6-116">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="d09e6-117">*CacheTimeout* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d09e6-117">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d09e6-118">使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d09e6-118">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="d09e6-119">*ResultDomain* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d09e6-119">*ResultDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d09e6-120">要附加至所傳回 NetBIOS 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="d09e6-120">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="d09e6-121">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="d09e6-121">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d09e6-122">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d09e6-122">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d09e6-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="d09e6-123">Return value</span></span>

<span data-ttu-id="d09e6-124">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d09e6-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d09e6-125">備註</span><span class="sxs-lookup"><span data-stu-id="d09e6-125">Remarks</span></span>

<span data-ttu-id="d09e6-126">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="d09e6-126">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09e6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d09e6-127">Requirements</span></span>



| <span data-ttu-id="d09e6-128">需求</span><span class="sxs-lookup"><span data-stu-id="d09e6-128">Requirement</span></span> | <span data-ttu-id="d09e6-129">值</span><span class="sxs-lookup"><span data-stu-id="d09e6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d09e6-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d09e6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d09e6-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="d09e6-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d09e6-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d09e6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d09e6-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d09e6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d09e6-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="d09e6-134">Namespace</span></span><br/>                | <span data-ttu-id="d09e6-135">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d09e6-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d09e6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d09e6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d09e6-137"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="d09e6-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09e6-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d09e6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09e6-139">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="d09e6-139">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="d09e6-140">**MicrosoftDNS WINSRType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="d09e6-140">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d09e6-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d09e6-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





