---
title: Modify MicrosoftDNS_MGType 類別的方法
description: Modify 方法會更新郵件群組 (MG) 資源記錄。
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MGType 類別
- MicrosoftDNS_MGType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104736"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="87a77-106">Modify MicrosoftDNS \_ MGType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="87a77-106">Modify method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="87a77-107">**Modify** 方法會更新郵件群組 (MG) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="87a77-107">The **Modify** method updates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a77-108">語法</span><span class="sxs-lookup"><span data-stu-id="87a77-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="87a77-109">參數</span><span class="sxs-lookup"><span data-stu-id="87a77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a77-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="87a77-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87a77-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="87a77-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="87a77-112">*MGMailbox* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="87a77-112">*MGMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87a77-113">FQDN，指定隸屬于記錄擁有者名稱所指定之郵件群組成員的信箱。</span><span class="sxs-lookup"><span data-stu-id="87a77-113">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="87a77-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="87a77-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="87a77-115">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="87a77-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a77-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="87a77-116">Return value</span></span>

<span data-ttu-id="87a77-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="87a77-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87a77-118">備註</span><span class="sxs-lookup"><span data-stu-id="87a77-118">Remarks</span></span>

<span data-ttu-id="87a77-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="87a77-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a77-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="87a77-120">Requirements</span></span>



| <span data-ttu-id="87a77-121">需求</span><span class="sxs-lookup"><span data-stu-id="87a77-121">Requirement</span></span> | <span data-ttu-id="87a77-122">值</span><span class="sxs-lookup"><span data-stu-id="87a77-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87a77-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87a77-123">Minimum supported client</span></span><br/> | <span data-ttu-id="87a77-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="87a77-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="87a77-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87a77-125">Minimum supported server</span></span><br/> | <span data-ttu-id="87a77-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87a77-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87a77-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="87a77-127">Namespace</span></span><br/>                | <span data-ttu-id="87a77-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="87a77-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="87a77-129">MOF</span><span class="sxs-lookup"><span data-stu-id="87a77-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87a77-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="87a77-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a77-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87a77-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a77-132">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="87a77-132">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="87a77-133">**MicrosoftDNS MGType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="87a77-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="87a77-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="87a77-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





