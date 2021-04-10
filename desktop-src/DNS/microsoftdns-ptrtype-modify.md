---
title: Modify MicrosoftDNS_PTRType 類別的方法
description: Modify 方法會更新 PTR) 資源記錄 (的指標。
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_PTRType 類別
- MicrosoftDNS_PTRType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934531"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="c0ece-106">Modify MicrosoftDNS \_ PTRType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="c0ece-106">Modify method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="c0ece-107">**Modify** 方法會更新 PTR) 資源記錄 (的指標。</span><span class="sxs-lookup"><span data-stu-id="c0ece-107">The **Modify** method updates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ece-108">語法</span><span class="sxs-lookup"><span data-stu-id="c0ece-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c0ece-109">參數</span><span class="sxs-lookup"><span data-stu-id="c0ece-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0ece-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c0ece-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ece-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c0ece-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c0ece-112">*PTRDomainName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c0ece-112">*PTRDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ece-113">PTR 記錄的功能變數名稱位址。</span><span class="sxs-lookup"><span data-stu-id="c0ece-113">Domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="c0ece-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="c0ece-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ece-115">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="c0ece-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0ece-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0ece-116">Return value</span></span>

<span data-ttu-id="c0ece-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c0ece-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0ece-118">備註</span><span class="sxs-lookup"><span data-stu-id="c0ece-118">Remarks</span></span>

<span data-ttu-id="c0ece-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="c0ece-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ece-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0ece-120">Requirements</span></span>



| <span data-ttu-id="c0ece-121">需求</span><span class="sxs-lookup"><span data-stu-id="c0ece-121">Requirement</span></span> | <span data-ttu-id="c0ece-122">值</span><span class="sxs-lookup"><span data-stu-id="c0ece-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ece-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0ece-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ece-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="c0ece-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c0ece-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0ece-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ece-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0ece-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c0ece-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="c0ece-127">Namespace</span></span><br/>                | <span data-ttu-id="c0ece-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c0ece-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c0ece-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c0ece-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0ece-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0ece-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ece-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0ece-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ece-132">**MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="c0ece-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="c0ece-133">**MicrosoftDNS PTRType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="c0ece-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c0ece-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c0ece-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





