---
title: Modify MicrosoftDNS_HINFOType 類別的方法
description: Modify 方法會將主機資訊更新 (HINFO) 資源記錄。
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_HINFOType 類別
- MicrosoftDNS_HINFOType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685919"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="6f57d-106">Modify MicrosoftDNS \_ HINFOType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="6f57d-106">Modify method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="6f57d-107">**Modify** 方法會將主機資訊更新 (HINFO) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="6f57d-107">The **Modify** method updates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f57d-108">語法</span><span class="sxs-lookup"><span data-stu-id="6f57d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="6f57d-109">參數</span><span class="sxs-lookup"><span data-stu-id="6f57d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f57d-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6f57d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f57d-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6f57d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="6f57d-112">*CPU* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6f57d-112">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f57d-113">記錄擁有者的 CPU 類型。</span><span class="sxs-lookup"><span data-stu-id="6f57d-113">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="6f57d-114">*作業系統* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6f57d-114">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f57d-115">記錄擁有者的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6f57d-115">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="6f57d-116">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="6f57d-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6f57d-117">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="6f57d-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f57d-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f57d-118">Return value</span></span>

<span data-ttu-id="6f57d-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6f57d-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f57d-120">備註</span><span class="sxs-lookup"><span data-stu-id="6f57d-120">Remarks</span></span>

<span data-ttu-id="6f57d-121">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6f57d-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f57d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f57d-122">Requirements</span></span>



| <span data-ttu-id="6f57d-123">需求</span><span class="sxs-lookup"><span data-stu-id="6f57d-123">Requirement</span></span> | <span data-ttu-id="6f57d-124">值</span><span class="sxs-lookup"><span data-stu-id="6f57d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f57d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f57d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6f57d-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="6f57d-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6f57d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f57d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6f57d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f57d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f57d-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f57d-129">Namespace</span></span><br/>                | <span data-ttu-id="6f57d-130">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6f57d-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6f57d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6f57d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f57d-132"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f57d-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f57d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f57d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f57d-134">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="6f57d-134">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="6f57d-135">**MicrosoftDNS HINFOType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="6f57d-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6f57d-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6f57d-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





