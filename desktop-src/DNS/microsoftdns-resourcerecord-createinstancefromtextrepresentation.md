---
title: MicrosoftDNS_ResourceRecord 類別的 CreateInstanceFromTextRepresentation 方法
description: CreateInstanceFromTextRepresentation 方法會具現化 MicrosoftDNS \_ ResourceRecord 物件。
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- CreateInstanceFromTextRepresentation 方法 DNS
- CreateInstanceFromTextRepresentation 方法 DNS，MicrosoftDNS_ResourceRecord 類別
- MicrosoftDNS_ResourceRecord 類別 DNS，CreateInstanceFromTextRepresentation 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025205"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="2a7d5-106">MicrosoftDNS ResourceRecord 類別的 CreateInstanceFromTextRepresentation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2a7d5-106">CreateInstanceFromTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="2a7d5-107">**CreateInstanceFromTextRepresentation** 方法會具現化 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)物件。</span><span class="sxs-lookup"><span data-stu-id="2a7d5-107">The **CreateInstanceFromTextRepresentation** method instantiates a [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a7d5-108">語法</span><span class="sxs-lookup"><span data-stu-id="2a7d5-108">Syntax</span></span>


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2a7d5-109">參數</span><span class="sxs-lookup"><span data-stu-id="2a7d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a7d5-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a7d5-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7d5-111">應該在其上建立 RR 的 DNS 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="2a7d5-111">Name of the DNS Server on which the RR should be created.</span></span>

</dd> <dt>

<span data-ttu-id="2a7d5-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a7d5-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7d5-113">應放置新 RR 的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="2a7d5-113">Name of the container into which the new RR should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="2a7d5-114">*TextRepresentation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a7d5-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7d5-115">要建立之 RR 實例的文字表示。</span><span class="sxs-lookup"><span data-stu-id="2a7d5-115">Text representation of the RR instance to be created.</span></span>

</dd> <dt>

<span data-ttu-id="2a7d5-116">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="2a7d5-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7d5-117">已具現化之 RR 的參考。</span><span class="sxs-lookup"><span data-stu-id="2a7d5-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a7d5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a7d5-118">Return value</span></span>

<span data-ttu-id="2a7d5-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2a7d5-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a7d5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a7d5-120">Requirements</span></span>



| <span data-ttu-id="2a7d5-121">需求</span><span class="sxs-lookup"><span data-stu-id="2a7d5-121">Requirement</span></span> | <span data-ttu-id="2a7d5-122">值</span><span class="sxs-lookup"><span data-stu-id="2a7d5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7d5-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a7d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2a7d5-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="2a7d5-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2a7d5-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a7d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2a7d5-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a7d5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2a7d5-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="2a7d5-127">Namespace</span></span><br/>                | <span data-ttu-id="2a7d5-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="2a7d5-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2a7d5-129">MOF</span><span class="sxs-lookup"><span data-stu-id="2a7d5-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a7d5-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a7d5-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a7d5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a7d5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7d5-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="2a7d5-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="2a7d5-133">**MicrosoftDNS ResourceRecord 類別的 GetObjectByTextRepresentation 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2a7d5-133">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





