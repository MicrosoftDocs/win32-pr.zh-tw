---
title: Modify MicrosoftDNS_MRType 類別的方法
description: Modify 方法會更新信箱重新命名 (MR) 資源記錄。
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MRType 類別
- MicrosoftDNS_MRType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465225"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="9f75d-106">Modify MicrosoftDNS \_ MRType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="9f75d-106">Modify method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="9f75d-107">**Modify** 方法會更新信箱重新命名 (MR) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="9f75d-107">The **Modify** method updates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f75d-108">語法</span><span class="sxs-lookup"><span data-stu-id="9f75d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9f75d-109">參數</span><span class="sxs-lookup"><span data-stu-id="9f75d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f75d-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9f75d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f75d-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9f75d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9f75d-112">*MRMailbox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f75d-112">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f75d-113">FQDN，指定在記錄的擁有者名稱中指定的信箱適當重新命名的信箱。</span><span class="sxs-lookup"><span data-stu-id="9f75d-113">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="9f75d-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="9f75d-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9f75d-115">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="9f75d-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f75d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f75d-116">Return value</span></span>

<span data-ttu-id="9f75d-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9f75d-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f75d-118">備註</span><span class="sxs-lookup"><span data-stu-id="9f75d-118">Remarks</span></span>

<span data-ttu-id="9f75d-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="9f75d-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f75d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f75d-120">Requirements</span></span>



| <span data-ttu-id="9f75d-121">需求</span><span class="sxs-lookup"><span data-stu-id="9f75d-121">Requirement</span></span> | <span data-ttu-id="9f75d-122">值</span><span class="sxs-lookup"><span data-stu-id="9f75d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f75d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f75d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9f75d-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="9f75d-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9f75d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f75d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9f75d-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f75d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9f75d-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="9f75d-127">Namespace</span></span><br/>                | <span data-ttu-id="9f75d-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="9f75d-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9f75d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9f75d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f75d-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f75d-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f75d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f75d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f75d-132">**MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="9f75d-132">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="9f75d-133">**MicrosoftDNS MRType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="9f75d-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9f75d-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="9f75d-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





