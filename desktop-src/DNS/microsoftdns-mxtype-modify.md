---
title: Modify MicrosoftDNS_MXType 類別的方法
description: Modify 方法會將郵件交換程式更新 (MR) 資源記錄。
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MXType 類別
- MicrosoftDNS_MXType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935051"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="2a273-106">Modify MicrosoftDNS \_ MXType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="2a273-106">Modify method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="2a273-107">**Modify** 方法會將郵件交換程式更新 (MR) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="2a273-107">The **Modify** method updates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a273-108">語法</span><span class="sxs-lookup"><span data-stu-id="2a273-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2a273-109">參數</span><span class="sxs-lookup"><span data-stu-id="2a273-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a273-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2a273-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a273-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2a273-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="2a273-112">*喜好* \[ 設定在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2a273-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a273-113">在相同擁有者的其他專案中提供給此 RR 的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="2a273-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="2a273-114">偏好較低的值。</span><span class="sxs-lookup"><span data-stu-id="2a273-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="2a273-115">*MailExchange* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2a273-115">*MailExchange* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a273-116">FQDN 指定的主機願意作為擁有者名稱的郵件交換。</span><span class="sxs-lookup"><span data-stu-id="2a273-116">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="2a273-117">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="2a273-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2a273-118">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="2a273-118">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a273-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a273-119">Return value</span></span>

<span data-ttu-id="2a273-120">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2a273-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a273-121">備註</span><span class="sxs-lookup"><span data-stu-id="2a273-121">Remarks</span></span>

<span data-ttu-id="2a273-122">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="2a273-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a273-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a273-123">Requirements</span></span>



| <span data-ttu-id="2a273-124">需求</span><span class="sxs-lookup"><span data-stu-id="2a273-124">Requirement</span></span> | <span data-ttu-id="2a273-125">值</span><span class="sxs-lookup"><span data-stu-id="2a273-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a273-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a273-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2a273-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="2a273-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2a273-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a273-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2a273-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a273-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2a273-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="2a273-130">Namespace</span></span><br/>                | <span data-ttu-id="2a273-131">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="2a273-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2a273-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2a273-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a273-133"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a273-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a273-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a273-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a273-135">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="2a273-135">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="2a273-136">**MicrosoftDNS MXType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2a273-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2a273-137">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="2a273-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





