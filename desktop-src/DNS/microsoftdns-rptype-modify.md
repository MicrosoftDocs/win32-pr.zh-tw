---
title: Modify MicrosoftDNS_RPType 類別的方法
description: Modify 方法會將負責任的人員 (RP) 資源記錄來更新。
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_RPType 類別
- MicrosoftDNS_RPType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843767"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="968ef-106">Modify MicrosoftDNS \_ RPType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="968ef-106">Modify method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="968ef-107">**Modify** 方法會將負責任的人員 (RP) 資源記錄來更新。</span><span class="sxs-lookup"><span data-stu-id="968ef-107">The **Modify** method updates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="968ef-108">語法</span><span class="sxs-lookup"><span data-stu-id="968ef-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="968ef-109">參數</span><span class="sxs-lookup"><span data-stu-id="968ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="968ef-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="968ef-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="968ef-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="968ef-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="968ef-112">*RPMailbox* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="968ef-112">*RPMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="968ef-113">指定負責任人員信箱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="968ef-113">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="968ef-114">*TXTDomainName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="968ef-114">*TXTDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="968ef-115">存在 TXT 資源記錄的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="968ef-115">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="968ef-116">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="968ef-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="968ef-117">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="968ef-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="968ef-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="968ef-118">Return value</span></span>

<span data-ttu-id="968ef-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="968ef-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="968ef-120">備註</span><span class="sxs-lookup"><span data-stu-id="968ef-120">Remarks</span></span>

<span data-ttu-id="968ef-121">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="968ef-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="968ef-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="968ef-122">Requirements</span></span>



| <span data-ttu-id="968ef-123">需求</span><span class="sxs-lookup"><span data-stu-id="968ef-123">Requirement</span></span> | <span data-ttu-id="968ef-124">值</span><span class="sxs-lookup"><span data-stu-id="968ef-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="968ef-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="968ef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="968ef-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="968ef-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="968ef-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="968ef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="968ef-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="968ef-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="968ef-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="968ef-129">Namespace</span></span><br/>                | <span data-ttu-id="968ef-130">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="968ef-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="968ef-131">MOF</span><span class="sxs-lookup"><span data-stu-id="968ef-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="968ef-132"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="968ef-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="968ef-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="968ef-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968ef-134">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="968ef-134">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="968ef-135">**MicrosoftDNS RPType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="968ef-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="968ef-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="968ef-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





