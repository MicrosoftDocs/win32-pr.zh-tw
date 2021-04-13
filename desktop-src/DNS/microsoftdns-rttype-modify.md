---
title: Modify MicrosoftDNS_RTType 類別的方法
description: Modify 方法會透過 (RT) 資源記錄來更新路由。
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_RTType 類別
- MicrosoftDNS_RTType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508683"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="6f0b7-106">Modify MicrosoftDNS \_ RTType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="6f0b7-106">Modify method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="6f0b7-107">**Modify** 方法會透過 (RT) 資源記錄來更新路由。</span><span class="sxs-lookup"><span data-stu-id="6f0b7-107">The **Modify** method updates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f0b7-108">語法</span><span class="sxs-lookup"><span data-stu-id="6f0b7-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="6f0b7-109">參數</span><span class="sxs-lookup"><span data-stu-id="6f0b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f0b7-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6f0b7-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0b7-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6f0b7-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="6f0b7-112">*喜好* \[ 設定在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6f0b7-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0b7-113">在相同擁有者的其他專案中提供給此 RR 的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="6f0b7-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="6f0b7-114">偏好較低的值。</span><span class="sxs-lookup"><span data-stu-id="6f0b7-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="6f0b7-115">*IntermediateHost* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6f0b7-115">*IntermediateHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0b7-116">FQDN，指定主機做為中繼，以達到擁有者指定的主機。</span><span class="sxs-lookup"><span data-stu-id="6f0b7-116">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="6f0b7-117">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="6f0b7-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0b7-118">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="6f0b7-118">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f0b7-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f0b7-119">Return value</span></span>

<span data-ttu-id="6f0b7-120">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6f0b7-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f0b7-121">備註</span><span class="sxs-lookup"><span data-stu-id="6f0b7-121">Remarks</span></span>

<span data-ttu-id="6f0b7-122">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6f0b7-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f0b7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f0b7-123">Requirements</span></span>



| <span data-ttu-id="6f0b7-124">需求</span><span class="sxs-lookup"><span data-stu-id="6f0b7-124">Requirement</span></span> | <span data-ttu-id="6f0b7-125">值</span><span class="sxs-lookup"><span data-stu-id="6f0b7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f0b7-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f0b7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6f0b7-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="6f0b7-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6f0b7-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f0b7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6f0b7-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f0b7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f0b7-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f0b7-130">Namespace</span></span><br/>                | <span data-ttu-id="6f0b7-131">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6f0b7-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6f0b7-132">MOF</span><span class="sxs-lookup"><span data-stu-id="6f0b7-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f0b7-133"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f0b7-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f0b7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f0b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f0b7-135">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="6f0b7-135">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="6f0b7-136">**MicrosoftDNS RTType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="6f0b7-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6f0b7-137">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6f0b7-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





