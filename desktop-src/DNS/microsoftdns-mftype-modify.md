---
title: Modify MicrosoftDNS_MFType 類別的方法
description: Modify 方法會更新網域 (MF) 資源記錄的郵件轉送代理程式。
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MFType 類別
- MicrosoftDNS_MFType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0a363290580c7cecf47dbe00c6dd7895d23dbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466057"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="c68d8-106">Modify MicrosoftDNS \_ MFType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="c68d8-106">Modify method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="c68d8-107">**Modify** 方法會更新網域 (MF) 資源記錄的郵件轉送代理程式。</span><span class="sxs-lookup"><span data-stu-id="c68d8-107">The **Modify** method updates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68d8-108">語法</span><span class="sxs-lookup"><span data-stu-id="c68d8-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c68d8-109">參數</span><span class="sxs-lookup"><span data-stu-id="c68d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68d8-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c68d8-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c68d8-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c68d8-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c68d8-112">*MFHost* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c68d8-112">*MFHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c68d8-113">提供郵件轉送代理程式的主控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="c68d8-113">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="c68d8-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="c68d8-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c68d8-115">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="c68d8-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c68d8-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c68d8-116">Return value</span></span>

<span data-ttu-id="c68d8-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c68d8-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c68d8-118">備註</span><span class="sxs-lookup"><span data-stu-id="c68d8-118">Remarks</span></span>

<span data-ttu-id="c68d8-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="c68d8-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c68d8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c68d8-120">Requirements</span></span>



| <span data-ttu-id="c68d8-121">需求</span><span class="sxs-lookup"><span data-stu-id="c68d8-121">Requirement</span></span> | <span data-ttu-id="c68d8-122">值</span><span class="sxs-lookup"><span data-stu-id="c68d8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c68d8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c68d8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c68d8-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="c68d8-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c68d8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c68d8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c68d8-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c68d8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c68d8-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="c68d8-127">Namespace</span></span><br/>                | <span data-ttu-id="c68d8-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c68d8-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c68d8-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c68d8-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c68d8-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="c68d8-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68d8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c68d8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68d8-132">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="c68d8-132">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="c68d8-133">**MicrosoftDNS MFType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="c68d8-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c68d8-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c68d8-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





