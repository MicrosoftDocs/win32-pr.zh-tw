---
title: Modify MicrosoftDNS_AAAAType 類別的方法
description: Modify 方法會 (AAAA) 資源記錄來更新 IPv6 位址。
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_AAAAType 類別
- MicrosoftDNS_AAAAType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843596"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="1b8fd-106">Modify MicrosoftDNS \_ AAAAType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="1b8fd-106">Modify method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="1b8fd-107">**Modify** 方法會 (AAAA) 資源記錄來更新 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1b8fd-107">The **Modify** method updates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b8fd-108">語法</span><span class="sxs-lookup"><span data-stu-id="1b8fd-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="1b8fd-109">參數</span><span class="sxs-lookup"><span data-stu-id="1b8fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b8fd-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1b8fd-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8fd-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1b8fd-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="1b8fd-112">*IPv6Address* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1b8fd-112">*IPv6Address* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8fd-113">主機的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1b8fd-113">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="1b8fd-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="1b8fd-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8fd-115">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1b8fd-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b8fd-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b8fd-116">Return value</span></span>

<span data-ttu-id="1b8fd-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1b8fd-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b8fd-118">備註</span><span class="sxs-lookup"><span data-stu-id="1b8fd-118">Remarks</span></span>

<span data-ttu-id="1b8fd-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="1b8fd-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8fd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b8fd-120">Requirements</span></span>



| <span data-ttu-id="1b8fd-121">需求</span><span class="sxs-lookup"><span data-stu-id="1b8fd-121">Requirement</span></span> | <span data-ttu-id="1b8fd-122">值</span><span class="sxs-lookup"><span data-stu-id="1b8fd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8fd-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b8fd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8fd-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="1b8fd-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1b8fd-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b8fd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8fd-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b8fd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1b8fd-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="1b8fd-127">Namespace</span></span><br/>                | <span data-ttu-id="1b8fd-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="1b8fd-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="1b8fd-129">MOF</span><span class="sxs-lookup"><span data-stu-id="1b8fd-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b8fd-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b8fd-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b8fd-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b8fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8fd-132">**MicrosoftDNS \_ AAAAType**</span><span class="sxs-lookup"><span data-stu-id="1b8fd-132">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="1b8fd-133">**MicrosoftDNS AAAAType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="1b8fd-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="1b8fd-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="1b8fd-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





