---
title: Modify MicrosoftDNS_MDType 類別的方法
description: Modify 方法會更新網域 (MD) 資源記錄的郵件代理程式。
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MDType 類別
- MicrosoftDNS_MDType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094559"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="8d886-106">Modify MicrosoftDNS \_ MDType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="8d886-106">Modify method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="8d886-107">**Modify** 方法會更新網域 (MD) 資源記錄的郵件代理程式。</span><span class="sxs-lookup"><span data-stu-id="8d886-107">The **Modify** method updates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d886-108">語法</span><span class="sxs-lookup"><span data-stu-id="8d886-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8d886-109">參數</span><span class="sxs-lookup"><span data-stu-id="8d886-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d886-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8d886-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d886-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8d886-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8d886-112">*MDHost* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8d886-112">*MDHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d886-113">表示郵件傳遞主機的字串。</span><span class="sxs-lookup"><span data-stu-id="8d886-113">String representing the mail delivery host.</span></span>

</dd> <dt>

<span data-ttu-id="8d886-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="8d886-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8d886-115">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="8d886-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d886-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d886-116">Return value</span></span>

<span data-ttu-id="8d886-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8d886-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d886-118">備註</span><span class="sxs-lookup"><span data-stu-id="8d886-118">Remarks</span></span>

<span data-ttu-id="8d886-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="8d886-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d886-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d886-120">Requirements</span></span>



| <span data-ttu-id="8d886-121">需求</span><span class="sxs-lookup"><span data-stu-id="8d886-121">Requirement</span></span> | <span data-ttu-id="8d886-122">值</span><span class="sxs-lookup"><span data-stu-id="8d886-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d886-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d886-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8d886-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="8d886-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8d886-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d886-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8d886-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d886-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8d886-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="8d886-127">Namespace</span></span><br/>                | <span data-ttu-id="8d886-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8d886-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8d886-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8d886-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d886-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d886-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d886-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d886-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d886-132">**MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="8d886-132">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="8d886-133">**MicrosoftDNS MDType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="8d886-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8d886-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8d886-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





