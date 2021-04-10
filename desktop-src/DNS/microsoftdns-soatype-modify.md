---
title: Modify MicrosoftDNS_SOAType 類別的方法
description: Modify 方法會更新 (SOA) 資源記錄的授權啟動。
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_SOAType 類別
- MicrosoftDNS_SOAType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024715"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a><span data-ttu-id="d788b-106">Modify MicrosoftDNS \_ SOAType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="d788b-106">Modify method of the MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="d788b-107">**Modify** 方法會更新 (SOA) 資源記錄的授權啟動。</span><span class="sxs-lookup"><span data-stu-id="d788b-107">The **Modify** method updates a Start Of Authority (SOA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d788b-108">語法</span><span class="sxs-lookup"><span data-stu-id="d788b-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d788b-109">參數</span><span class="sxs-lookup"><span data-stu-id="d788b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d788b-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d788b-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d788b-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d788b-112">*SerialNumber* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d788b-112">*SerialNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-113">SOA 序號，代表區域已更新的次數， [*次要伺服器*](s-gly.md) 會使用這些序號來判斷是否需要進列區域轉送。</span><span class="sxs-lookup"><span data-stu-id="d788b-113">SOA serial number representing the number of times the zone has been updated, used by [*secondary servers*](s-gly.md) to determine whether zone transfer is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="d788b-114">*>primaryserver* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d788b-114">*PrimaryServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-115">主伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d788b-115">Name of the primary server.</span></span>

</dd> <dt>

<span data-ttu-id="d788b-116">*ResponsibleParty* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d788b-116">*ResponsibleParty* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-117">負責任之合作物件的信箱位址（以別名的形式），例如 xyz.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="d788b-117">Mailbox address of the responsible party, in the form of alias.domain, such as xyz.microsoft.com.</span></span> <span data-ttu-id="d788b-118">請注意，使用句點而不是 at 符號 ( @ ) 。</span><span class="sxs-lookup"><span data-stu-id="d788b-118">Note the use of a period rather than an at symbol (@).</span></span>

</dd> <dt>

<span data-ttu-id="d788b-119">*RefreshInterval* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d788b-119">*RefreshInterval* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-120">應重新整理包含此記錄之區域之前的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d788b-120">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="d788b-121">*RetryDelay* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d788b-121">*RetryDelay* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-122">DNS 伺服器應該在名稱解析嘗試之間延遲的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d788b-122">Time, in seconds, the DNS Server should delay between name resolution attempts.</span></span>

</dd> <dt>

<span data-ttu-id="d788b-123">*ExpireLimit* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d788b-123">*ExpireLimit* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-124">次要伺服器在將其區域檔案的複本捨棄為無效之前，應該等候主伺服器回應的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d788b-124">Time, in seconds, that secondary servers should wait for a response from the primary server before discarding their copies of the zone file as invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d788b-125">*MinimumTTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d788b-125">*MinimumTTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-126">TTL 時間（以秒為單位），套用至區域中未指定其專屬 TTL 的資源記錄。</span><span class="sxs-lookup"><span data-stu-id="d788b-126">TTL time, in seconds, applied to resource records in the zone that do not specify their own TTL.</span></span>

</dd> <dt>

<span data-ttu-id="d788b-127">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="d788b-127">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d788b-128">修改過之物件的參考</span><span class="sxs-lookup"><span data-stu-id="d788b-128">Reference to the modified object</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d788b-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="d788b-129">Return value</span></span>

<span data-ttu-id="d788b-130">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d788b-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d788b-131">備註</span><span class="sxs-lookup"><span data-stu-id="d788b-131">Remarks</span></span>

<span data-ttu-id="d788b-132">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="d788b-132">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d788b-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d788b-133">Requirements</span></span>



| <span data-ttu-id="d788b-134">需求</span><span class="sxs-lookup"><span data-stu-id="d788b-134">Requirement</span></span> | <span data-ttu-id="d788b-135">值</span><span class="sxs-lookup"><span data-stu-id="d788b-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d788b-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d788b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d788b-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="d788b-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d788b-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d788b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d788b-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d788b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d788b-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="d788b-140">Namespace</span></span><br/>                | <span data-ttu-id="d788b-141">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d788b-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d788b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d788b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d788b-143"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="d788b-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d788b-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d788b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d788b-145">**MicrosoftDNS \_ SOAType**</span><span class="sxs-lookup"><span data-stu-id="d788b-145">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)
</dt> <dt>

[<span data-ttu-id="d788b-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d788b-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





