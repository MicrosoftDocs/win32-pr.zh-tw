---
title: Modify MicrosoftDNS_CNAMEType 類別的方法
description: Modify 方法會 (CNAME) 資源記錄來更新正式名稱。
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_CNAMEType 類別
- MicrosoftDNS_CNAMEType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465337"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="ad8ed-106">Modify MicrosoftDNS \_ CNAMEType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="ad8ed-106">Modify method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="ad8ed-107">**Modify** 方法會 (CNAME) 資源記錄來更新正式名稱。</span><span class="sxs-lookup"><span data-stu-id="ad8ed-107">The **Modify** method updates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad8ed-108">語法</span><span class="sxs-lookup"><span data-stu-id="ad8ed-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ad8ed-109">參數</span><span class="sxs-lookup"><span data-stu-id="ad8ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad8ed-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ad8ed-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad8ed-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad8ed-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ad8ed-112">*PrimaryName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ad8ed-112">*PrimaryName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad8ed-113">表示 CNAME 記錄之主要名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="ad8ed-113">String representing the primary name for the CNAME record.</span></span>

</dd> <dt>

<span data-ttu-id="ad8ed-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="ad8ed-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ad8ed-115">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ad8ed-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad8ed-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad8ed-116">Return value</span></span>

<span data-ttu-id="ad8ed-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ad8ed-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad8ed-118">備註</span><span class="sxs-lookup"><span data-stu-id="ad8ed-118">Remarks</span></span>

<span data-ttu-id="ad8ed-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="ad8ed-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad8ed-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad8ed-120">Requirements</span></span>



| <span data-ttu-id="ad8ed-121">需求</span><span class="sxs-lookup"><span data-stu-id="ad8ed-121">Requirement</span></span> | <span data-ttu-id="ad8ed-122">值</span><span class="sxs-lookup"><span data-stu-id="ad8ed-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8ed-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad8ed-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ad8ed-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="ad8ed-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ad8ed-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad8ed-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ad8ed-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad8ed-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ad8ed-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="ad8ed-127">Namespace</span></span><br/>                | <span data-ttu-id="ad8ed-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ad8ed-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ad8ed-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ad8ed-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad8ed-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad8ed-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad8ed-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad8ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad8ed-132">**MicrosoftDNS \_ CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="ad8ed-132">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="ad8ed-133">**MicrosoftDNS CNAMEType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ad8ed-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ad8ed-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ad8ed-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





