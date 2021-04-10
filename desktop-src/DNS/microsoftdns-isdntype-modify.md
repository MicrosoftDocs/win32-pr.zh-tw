---
title: Modify MicrosoftDNS_ISDNType 類別的方法
description: Modify 方法會更新 ISDN 資源記錄。
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_ISDNType 類別
- MicrosoftDNS_ISDNType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933943"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="897bd-106">Modify MicrosoftDNS \_ ISDNType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="897bd-106">Modify method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="897bd-107">**Modify** 方法會更新 ISDN 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="897bd-107">The **Modify** method updates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="897bd-108">語法</span><span class="sxs-lookup"><span data-stu-id="897bd-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="897bd-109">參數</span><span class="sxs-lookup"><span data-stu-id="897bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="897bd-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="897bd-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="897bd-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="897bd-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="897bd-112">*ISDNNumber* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="897bd-112">*ISDNNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="897bd-113">記錄擁有者的 ISDN 號碼和 DDI。</span><span class="sxs-lookup"><span data-stu-id="897bd-113">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="897bd-114">子 *位址* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="897bd-114">*SubAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="897bd-115">擁有者的子位址（若已定義）。</span><span class="sxs-lookup"><span data-stu-id="897bd-115">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="897bd-116">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="897bd-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="897bd-117">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="897bd-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="897bd-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="897bd-118">Return value</span></span>

<span data-ttu-id="897bd-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="897bd-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="897bd-120">備註</span><span class="sxs-lookup"><span data-stu-id="897bd-120">Remarks</span></span>

<span data-ttu-id="897bd-121">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="897bd-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="897bd-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="897bd-122">Requirements</span></span>



| <span data-ttu-id="897bd-123">需求</span><span class="sxs-lookup"><span data-stu-id="897bd-123">Requirement</span></span> | <span data-ttu-id="897bd-124">值</span><span class="sxs-lookup"><span data-stu-id="897bd-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="897bd-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="897bd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="897bd-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="897bd-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="897bd-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="897bd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="897bd-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="897bd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="897bd-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="897bd-129">Namespace</span></span><br/>                | <span data-ttu-id="897bd-130">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="897bd-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="897bd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="897bd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="897bd-132"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="897bd-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="897bd-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="897bd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="897bd-134">**MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="897bd-134">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="897bd-135">**MicrosoftDNS ISDNType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="897bd-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="897bd-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="897bd-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





