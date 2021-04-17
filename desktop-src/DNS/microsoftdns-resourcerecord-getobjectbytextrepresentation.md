---
title: MicrosoftDNS_ResourceRecord 類別的 GetObjectByTextRepresentation 方法
description: GetObjectByTextRepresentation 方法會捕獲 MicrosoftDNS ResourceRecord 類別的現有實例 \_ 。
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- GetObjectByTextRepresentation 方法 DNS
- GetObjectByTextRepresentation 方法 DNS，MicrosoftDNS_ResourceRecord 類別
- MicrosoftDNS_ResourceRecord 類別 DNS，GetObjectByTextRepresentation 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465681"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="57843-106">MicrosoftDNS ResourceRecord 類別的 GetObjectByTextRepresentation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="57843-106">GetObjectByTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="57843-107">**GetObjectByTextRepresentation** 方法會捕獲 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)類別的現有實例。</span><span class="sxs-lookup"><span data-stu-id="57843-107">The **GetObjectByTextRepresentation** method retrieves an existing instance of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="57843-108">語法</span><span class="sxs-lookup"><span data-stu-id="57843-108">Syntax</span></span>


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a><span data-ttu-id="57843-109">參數</span><span class="sxs-lookup"><span data-stu-id="57843-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57843-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57843-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57843-111">應從中取出 RR 的 DNS 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="57843-111">Name of the DNS Server from which the RR should be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="57843-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57843-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57843-113">應從中取得 RR 的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="57843-113">Name of the container from which the RR should be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="57843-114">*TextRepresentation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57843-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57843-115">要抓取之 RR 的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="57843-115">Text representation of the RR to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="57843-116">*RR* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="57843-116">*RR* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57843-117">已具現化之 RR 的參考。</span><span class="sxs-lookup"><span data-stu-id="57843-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57843-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="57843-118">Return value</span></span>

<span data-ttu-id="57843-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="57843-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="57843-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="57843-120">Requirements</span></span>



| <span data-ttu-id="57843-121">需求</span><span class="sxs-lookup"><span data-stu-id="57843-121">Requirement</span></span> | <span data-ttu-id="57843-122">值</span><span class="sxs-lookup"><span data-stu-id="57843-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57843-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57843-123">Minimum supported client</span></span><br/> | <span data-ttu-id="57843-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="57843-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="57843-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57843-125">Minimum supported server</span></span><br/> | <span data-ttu-id="57843-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57843-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="57843-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="57843-127">Namespace</span></span><br/>                | <span data-ttu-id="57843-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="57843-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="57843-129">MOF</span><span class="sxs-lookup"><span data-stu-id="57843-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57843-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="57843-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57843-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57843-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57843-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="57843-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="57843-133">**MicrosoftDNS ResourceRecord 類別的 CreateInstanceFromTextRepresentation 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="57843-133">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





