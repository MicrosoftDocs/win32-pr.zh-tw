---
title: Modify MicrosoftDNS_MINFOType 類別的方法
description: Modify 方法會更新郵件資訊 (MINFO) 資源記錄。
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MINFOType 類別
- MicrosoftDNS_MINFOType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464752"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="40ee8-106">Modify MicrosoftDNS \_ MINFOType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="40ee8-106">Modify method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="40ee8-107">**Modify** 方法會更新郵件資訊 (MINFO) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="40ee8-107">The **Modify** method updates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ee8-108">語法</span><span class="sxs-lookup"><span data-stu-id="40ee8-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="40ee8-109">參數</span><span class="sxs-lookup"><span data-stu-id="40ee8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ee8-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="40ee8-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="40ee8-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="40ee8-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="40ee8-112">*ResponsibleMailbox* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="40ee8-112">*ResponsibleMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="40ee8-113">FQDN，指定負責記錄的擁有者名稱中所指定之郵寄清單或信箱的信箱。</span><span class="sxs-lookup"><span data-stu-id="40ee8-113">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="40ee8-114">*ErrorMailbox* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="40ee8-114">*ErrorMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="40ee8-115">FQDN，指定信箱以接收與郵寄清單相關的錯誤訊息，或 MINFO 記錄的擁有者名稱所指定的信箱。</span><span class="sxs-lookup"><span data-stu-id="40ee8-115">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="40ee8-116">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="40ee8-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="40ee8-117">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="40ee8-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40ee8-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="40ee8-118">Return value</span></span>

<span data-ttu-id="40ee8-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="40ee8-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40ee8-120">備註</span><span class="sxs-lookup"><span data-stu-id="40ee8-120">Remarks</span></span>

<span data-ttu-id="40ee8-121">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="40ee8-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ee8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="40ee8-122">Requirements</span></span>



| <span data-ttu-id="40ee8-123">需求</span><span class="sxs-lookup"><span data-stu-id="40ee8-123">Requirement</span></span> | <span data-ttu-id="40ee8-124">值</span><span class="sxs-lookup"><span data-stu-id="40ee8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40ee8-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40ee8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="40ee8-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="40ee8-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="40ee8-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40ee8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="40ee8-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40ee8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="40ee8-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="40ee8-129">Namespace</span></span><br/>                | <span data-ttu-id="40ee8-130">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="40ee8-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="40ee8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="40ee8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40ee8-132"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="40ee8-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ee8-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40ee8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ee8-134">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="40ee8-134">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="40ee8-135">**MicrosoftDNS MINFOType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="40ee8-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="40ee8-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="40ee8-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





