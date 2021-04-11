---
title: Modify MicrosoftDNS_WINSType 類別的方法
description: Modify 方法會更新 Windows 網際網路名稱服務 (WINS) 資源記錄。
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_WINSType 類別
- MicrosoftDNS_WINSType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843867"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="ea01f-106">Modify MicrosoftDNS \_ WINSType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="ea01f-106">Modify method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="ea01f-107">**Modify** 方法會更新 Windows 網際網路名稱服務 (WINS) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="ea01f-107">The **Modify** method updates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea01f-108">語法</span><span class="sxs-lookup"><span data-stu-id="ea01f-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ea01f-109">參數</span><span class="sxs-lookup"><span data-stu-id="ea01f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea01f-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ea01f-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea01f-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ea01f-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ea01f-112">*MappingFlag* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ea01f-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea01f-113">WINS 對應旗標，指定是否必須將記錄包含在區域複寫中。</span><span class="sxs-lookup"><span data-stu-id="ea01f-113">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="ea01f-114">它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。</span><span class="sxs-lookup"><span data-stu-id="ea01f-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="ea01f-115">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="ea01f-115">The following values are valid.</span></span>



| <span data-ttu-id="ea01f-116">值</span><span class="sxs-lookup"><span data-stu-id="ea01f-116">Value</span></span>                                                                                                                                               | <span data-ttu-id="ea01f-117">意義</span><span class="sxs-lookup"><span data-stu-id="ea01f-117">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="ea01f-118"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="ea01f-118"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="ea01f-119">複寫旗標</span><span class="sxs-lookup"><span data-stu-id="ea01f-119">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="ea01f-120"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="ea01f-120"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="ea01f-121">無複寫 (本機記錄) 旗標</span><span class="sxs-lookup"><span data-stu-id="ea01f-121">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ea01f-122">*LookupTimeout* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ea01f-122">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea01f-123">DNS 伺服器使用 WINS 查詢來嘗試解析的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ea01f-123">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="ea01f-124">*CacheTimeout* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ea01f-124">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea01f-125">使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ea01f-125">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="ea01f-126">*WinsServers* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ea01f-126">*WinsServers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea01f-127">WINS 查詢中使用之 WINS 伺服器的逗點分隔 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="ea01f-127">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="ea01f-128">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="ea01f-128">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ea01f-129">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ea01f-129">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea01f-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea01f-130">Return value</span></span>

<span data-ttu-id="ea01f-131">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ea01f-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea01f-132">備註</span><span class="sxs-lookup"><span data-stu-id="ea01f-132">Remarks</span></span>

<span data-ttu-id="ea01f-133">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="ea01f-133">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea01f-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea01f-134">Requirements</span></span>



| <span data-ttu-id="ea01f-135">需求</span><span class="sxs-lookup"><span data-stu-id="ea01f-135">Requirement</span></span> | <span data-ttu-id="ea01f-136">值</span><span class="sxs-lookup"><span data-stu-id="ea01f-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea01f-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea01f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ea01f-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="ea01f-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ea01f-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea01f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ea01f-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea01f-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea01f-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="ea01f-141">Namespace</span></span><br/>                | <span data-ttu-id="ea01f-142">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ea01f-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ea01f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ea01f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea01f-144"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea01f-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea01f-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea01f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea01f-146">**MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="ea01f-146">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="ea01f-147">**MicrosoftDNS WINSType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ea01f-147">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ea01f-148">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ea01f-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





