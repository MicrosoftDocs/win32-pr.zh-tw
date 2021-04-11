---
title: Modify MicrosoftDNS_X25Type 類別的方法
description: Modify 方法會更新 (X25) 資源記錄的 X.25。
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_X25Type 類別
- MicrosoftDNS_X25Type 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10db2fa770d3da8487a712e631c41fdd4256bf7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104411"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="d1c43-106">Modify MicrosoftDNS \_ X25Type 類別的方法</span><span class="sxs-lookup"><span data-stu-id="d1c43-106">Modify method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="d1c43-107">**Modify** 方法會更新 (X25) 資源記錄的 x.25。</span><span class="sxs-lookup"><span data-stu-id="d1c43-107">The **Modify** method updates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c43-108">語法</span><span class="sxs-lookup"><span data-stu-id="d1c43-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d1c43-109">參數</span><span class="sxs-lookup"><span data-stu-id="d1c43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c43-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1c43-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c43-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d1c43-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d1c43-112">*PSDNAddress* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1c43-112">*PSDNAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c43-113">RR 擁有者的 PSDN 位址。</span><span class="sxs-lookup"><span data-stu-id="d1c43-113">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="d1c43-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="d1c43-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c43-115">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d1c43-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c43-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1c43-116">Return value</span></span>

<span data-ttu-id="d1c43-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d1c43-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1c43-118">備註</span><span class="sxs-lookup"><span data-stu-id="d1c43-118">Remarks</span></span>

<span data-ttu-id="d1c43-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="d1c43-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c43-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1c43-120">Requirements</span></span>



| <span data-ttu-id="d1c43-121">需求</span><span class="sxs-lookup"><span data-stu-id="d1c43-121">Requirement</span></span> | <span data-ttu-id="d1c43-122">值</span><span class="sxs-lookup"><span data-stu-id="d1c43-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c43-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1c43-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c43-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="d1c43-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d1c43-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1c43-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c43-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1c43-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d1c43-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="d1c43-127">Namespace</span></span><br/>                | <span data-ttu-id="d1c43-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d1c43-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d1c43-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d1c43-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1c43-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1c43-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1c43-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1c43-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c43-132">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="d1c43-132">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="d1c43-133">**MicrosoftDNS X25Type 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="d1c43-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d1c43-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d1c43-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





