---
title: Modify MicrosoftDNS_SRVType 類別的方法
description: Modify 方法會更新 (SRV) 資源記錄的服務。
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_SRVType 類別
- MicrosoftDNS_SRVType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025427"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="15332-106">Modify MicrosoftDNS \_ SRVType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="15332-106">Modify method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="15332-107">**Modify** 方法會更新 (SRV) 資源記錄的服務。</span><span class="sxs-lookup"><span data-stu-id="15332-107">The **Modify** method updates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="15332-108">語法</span><span class="sxs-lookup"><span data-stu-id="15332-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="15332-109">參數</span><span class="sxs-lookup"><span data-stu-id="15332-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15332-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15332-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15332-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="15332-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="15332-112">*優先順序* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15332-112">*Priority* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15332-113">擁有者名稱中指定的目標主機優先權。</span><span class="sxs-lookup"><span data-stu-id="15332-113">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="15332-114">數位下限表示較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="15332-114">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="15332-115">*權數* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15332-115">*Weight* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15332-116">目標主機的加權。</span><span class="sxs-lookup"><span data-stu-id="15332-116">Weight of the target host.</span></span> <span data-ttu-id="15332-117">在具有相同優先順序的主機之間進行選取時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="15332-117">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="15332-118">使用此主機的機率應與其權數成正比。</span><span class="sxs-lookup"><span data-stu-id="15332-118">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="15332-119">*埠* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15332-119">*Port* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15332-120">通訊協定服務的目標主機上所使用的埠。</span><span class="sxs-lookup"><span data-stu-id="15332-120">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="15332-121">*SRVDomainName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15332-121">*SRVDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15332-122">目標主機的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="15332-122">FQDN of the target host.</span></span> <span data-ttu-id="15332-123">的目標 \\ 。 \\ 表示此網域無法使用由於原子服務。</span><span class="sxs-lookup"><span data-stu-id="15332-123">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="15332-124">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="15332-124">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="15332-125">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="15332-125">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15332-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="15332-126">Return value</span></span>

<span data-ttu-id="15332-127">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="15332-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15332-128">備註</span><span class="sxs-lookup"><span data-stu-id="15332-128">Remarks</span></span>

<span data-ttu-id="15332-129">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="15332-129">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="15332-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="15332-130">Requirements</span></span>



| <span data-ttu-id="15332-131">需求</span><span class="sxs-lookup"><span data-stu-id="15332-131">Requirement</span></span> | <span data-ttu-id="15332-132">值</span><span class="sxs-lookup"><span data-stu-id="15332-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15332-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15332-133">Minimum supported client</span></span><br/> | <span data-ttu-id="15332-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="15332-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="15332-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15332-135">Minimum supported server</span></span><br/> | <span data-ttu-id="15332-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15332-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15332-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="15332-137">Namespace</span></span><br/>                | <span data-ttu-id="15332-138">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="15332-138">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="15332-139">MOF</span><span class="sxs-lookup"><span data-stu-id="15332-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15332-140"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="15332-140"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15332-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15332-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15332-142">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="15332-142">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="15332-143">**MicrosoftDNS SRVType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="15332-143">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="15332-144">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="15332-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





