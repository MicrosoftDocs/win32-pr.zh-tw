---
title: Modify MicrosoftDNS_WKSType 類別的方法
description: Modify 方法會) 資源記錄更新 Well-Known Services (WKS。
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_WKSType 類別
- MicrosoftDNS_WKSType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843860"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="ac519-106">Modify MicrosoftDNS \_ WKSType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="ac519-106">Modify method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="ac519-107">**Modify** 方法會) 資源記錄更新 Well-Known SERVICES (WKS。</span><span class="sxs-lookup"><span data-stu-id="ac519-107">The **Modify** method updates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac519-108">語法</span><span class="sxs-lookup"><span data-stu-id="ac519-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ac519-109">參數</span><span class="sxs-lookup"><span data-stu-id="ac519-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac519-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ac519-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac519-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ac519-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ac519-112">*InternetAddress* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ac519-112">*InternetAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac519-113">記錄擁有者的網際網路 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ac519-113">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="ac519-114">*IPProtocol* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ac519-114">*IPProtocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac519-115">代表此記錄之 IP 通訊協定的字串。</span><span class="sxs-lookup"><span data-stu-id="ac519-115">String representing the IP protocol for this record.</span></span> <span data-ttu-id="ac519-116">有效的值為 UDP 或 TCP。</span><span class="sxs-lookup"><span data-stu-id="ac519-116">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="ac519-117">*服務* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ac519-117">*Services* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac519-118">字串，其中包含已知服務 (WKS) 記錄所使用的所有服務。</span><span class="sxs-lookup"><span data-stu-id="ac519-118">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="ac519-119">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="ac519-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ac519-120">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ac519-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac519-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac519-121">Return value</span></span>

<span data-ttu-id="ac519-122">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ac519-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac519-123">備註</span><span class="sxs-lookup"><span data-stu-id="ac519-123">Remarks</span></span>

<span data-ttu-id="ac519-124">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="ac519-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac519-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac519-125">Requirements</span></span>



| <span data-ttu-id="ac519-126">需求</span><span class="sxs-lookup"><span data-stu-id="ac519-126">Requirement</span></span> | <span data-ttu-id="ac519-127">值</span><span class="sxs-lookup"><span data-stu-id="ac519-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac519-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac519-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ac519-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="ac519-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ac519-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac519-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ac519-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac519-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ac519-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac519-132">Namespace</span></span><br/>                | <span data-ttu-id="ac519-133">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ac519-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ac519-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ac519-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac519-135"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac519-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac519-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac519-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac519-137">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="ac519-137">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="ac519-138">**MicrosoftDNS WKSType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ac519-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ac519-139">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ac519-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





