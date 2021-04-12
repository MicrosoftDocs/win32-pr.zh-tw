---
title: Modify MicrosoftDNS_ATMAType 類別的方法
description: Modify 方法會將 ATM 位址更新為 (ATMA) 資源記錄的名稱。
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_ATMAType 類別
- MicrosoftDNS_ATMAType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025108"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="3162d-106">Modify MicrosoftDNS \_ ATMAType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="3162d-106">Modify method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="3162d-107">**Modify** 方法會將 ATM 位址更新為 (ATMA) 資源記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="3162d-107">The **Modify** method updates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3162d-108">語法</span><span class="sxs-lookup"><span data-stu-id="3162d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3162d-109">參數</span><span class="sxs-lookup"><span data-stu-id="3162d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3162d-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="3162d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3162d-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3162d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3162d-112">*格式* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="3162d-112">*Format* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3162d-113">ATM 位址格式。</span><span class="sxs-lookup"><span data-stu-id="3162d-113">ATM address format.</span></span> <span data-ttu-id="3162d-114">格式有兩個可能的值：0表示 ATM 終端系統位址 (AESA) 格式，而1表示電子164格式。</span><span class="sxs-lookup"><span data-stu-id="3162d-114">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="3162d-115">*ATMAddress* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="3162d-115">*ATMAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3162d-116">包含此 RR 所屬節點/擁有者之 ATM 位址的八位變數長度字串。</span><span class="sxs-lookup"><span data-stu-id="3162d-116">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="3162d-117">陣列的前四個位元組是用來儲存八位字串的大小。</span><span class="sxs-lookup"><span data-stu-id="3162d-117">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="3162d-118">最重要的位元組會儲存在位元組0中。</span><span class="sxs-lookup"><span data-stu-id="3162d-118">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="3162d-119">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="3162d-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3162d-120">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="3162d-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3162d-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="3162d-121">Return value</span></span>

<span data-ttu-id="3162d-122">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3162d-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3162d-123">備註</span><span class="sxs-lookup"><span data-stu-id="3162d-123">Remarks</span></span>

<span data-ttu-id="3162d-124">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="3162d-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3162d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3162d-125">Requirements</span></span>



| <span data-ttu-id="3162d-126">需求</span><span class="sxs-lookup"><span data-stu-id="3162d-126">Requirement</span></span> | <span data-ttu-id="3162d-127">值</span><span class="sxs-lookup"><span data-stu-id="3162d-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3162d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3162d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3162d-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="3162d-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3162d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3162d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3162d-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3162d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3162d-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="3162d-132">Namespace</span></span><br/>                | <span data-ttu-id="3162d-133">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="3162d-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3162d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3162d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3162d-135"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="3162d-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3162d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3162d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3162d-137">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="3162d-137">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="3162d-138">**MicrosoftDNS ATMAType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="3162d-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3162d-139">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3162d-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





