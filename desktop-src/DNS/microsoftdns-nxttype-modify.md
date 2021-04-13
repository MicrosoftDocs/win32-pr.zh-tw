---
title: Modify MicrosoftDNS_NXTType 類別的方法
description: Modify 方法會更新下一個 (NXT) 資源記錄。
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_NXTType 類別
- MicrosoftDNS_NXTType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464749"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="29213-106">Modify MicrosoftDNS \_ NXTType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="29213-106">Modify method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="29213-107">**Modify** 方法會更新下一個 (NXT) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="29213-107">The **Modify** method updates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="29213-108">語法</span><span class="sxs-lookup"><span data-stu-id="29213-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="29213-109">參數</span><span class="sxs-lookup"><span data-stu-id="29213-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29213-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="29213-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29213-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="29213-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="29213-112">*NextDomainName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29213-112">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29213-113">下一個功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="29213-113">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="29213-114">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29213-114">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29213-115">針對 NXT 資源記錄的擁有者名稱，以空格分隔的 RR 類型助憶鍵清單。</span><span class="sxs-lookup"><span data-stu-id="29213-115">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="29213-116">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="29213-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="29213-117">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="29213-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29213-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="29213-118">Return value</span></span>

<span data-ttu-id="29213-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="29213-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29213-120">備註</span><span class="sxs-lookup"><span data-stu-id="29213-120">Remarks</span></span>

<span data-ttu-id="29213-121">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="29213-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="29213-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="29213-122">Requirements</span></span>



| <span data-ttu-id="29213-123">需求</span><span class="sxs-lookup"><span data-stu-id="29213-123">Requirement</span></span> | <span data-ttu-id="29213-124">值</span><span class="sxs-lookup"><span data-stu-id="29213-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29213-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29213-125">Minimum supported client</span></span><br/> | <span data-ttu-id="29213-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="29213-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="29213-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29213-127">Minimum supported server</span></span><br/> | <span data-ttu-id="29213-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29213-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="29213-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="29213-129">Namespace</span></span><br/>                | <span data-ttu-id="29213-130">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="29213-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="29213-131">MOF</span><span class="sxs-lookup"><span data-stu-id="29213-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29213-132"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="29213-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29213-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29213-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29213-134">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="29213-134">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="29213-135">**MicrosoftDNS NXTType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="29213-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="29213-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="29213-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





