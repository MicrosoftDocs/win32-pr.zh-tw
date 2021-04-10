---
title: Modify MicrosoftDNS_AType 類別的方法
description: Modify 方法會更新主機位址的 TTL 和 IP 位址 () 資源記錄。
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_AType 類別
- MicrosoftDNS_AType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025107"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="790a7-106">Modify MicrosoftDNS \_ AType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="790a7-106">Modify method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="790a7-107">**Modify** 方法會更新主機位址的 TTL 和 IP 位址 () 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="790a7-107">The **Modify** method updates the TTL and IP address of a host Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="790a7-108">語法</span><span class="sxs-lookup"><span data-stu-id="790a7-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="790a7-109">參數</span><span class="sxs-lookup"><span data-stu-id="790a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="790a7-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="790a7-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="790a7-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="790a7-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="790a7-112">*IPAddress* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="790a7-112">*IPAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="790a7-113">代表主機 IP 位址的字串。</span><span class="sxs-lookup"><span data-stu-id="790a7-113">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="790a7-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="790a7-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="790a7-115">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="790a7-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="790a7-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="790a7-116">Return value</span></span>

<span data-ttu-id="790a7-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="790a7-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="790a7-118">備註</span><span class="sxs-lookup"><span data-stu-id="790a7-118">Remarks</span></span>

<span data-ttu-id="790a7-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="790a7-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="790a7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="790a7-120">Requirements</span></span>



| <span data-ttu-id="790a7-121">需求</span><span class="sxs-lookup"><span data-stu-id="790a7-121">Requirement</span></span> | <span data-ttu-id="790a7-122">值</span><span class="sxs-lookup"><span data-stu-id="790a7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="790a7-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="790a7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="790a7-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="790a7-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="790a7-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="790a7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="790a7-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="790a7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="790a7-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="790a7-127">Namespace</span></span><br/>                | <span data-ttu-id="790a7-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="790a7-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="790a7-129">MOF</span><span class="sxs-lookup"><span data-stu-id="790a7-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="790a7-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="790a7-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="790a7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="790a7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="790a7-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="790a7-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="790a7-133">**MicrosoftDNS AType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="790a7-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





