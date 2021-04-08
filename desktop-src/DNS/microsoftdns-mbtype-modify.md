---
title: Modify MicrosoftDNS_MBType 類別的方法
description: Modify 方法會更新信箱 (MB) 資源記錄。
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MBType 類別
- MicrosoftDNS_MBType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d6f0fcb0faf5c1e8da152798863c8cecc8641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686030"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="3bad1-106">Modify MicrosoftDNS \_ MBType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="3bad1-106">Modify method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="3bad1-107">**Modify** 方法會更新信箱 (MB) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="3bad1-107">The **Modify** method updates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bad1-108">語法</span><span class="sxs-lookup"><span data-stu-id="3bad1-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3bad1-109">參數</span><span class="sxs-lookup"><span data-stu-id="3bad1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bad1-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="3bad1-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bad1-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3bad1-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3bad1-112">*MBHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bad1-112">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bad1-113">表示 MB 記錄之信箱主機名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="3bad1-113">String representing the mailbox host name for the MB record.</span></span>

</dd> <dt>

<span data-ttu-id="3bad1-114">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="3bad1-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3bad1-115">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="3bad1-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bad1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bad1-116">Return value</span></span>

<span data-ttu-id="3bad1-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3bad1-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bad1-118">備註</span><span class="sxs-lookup"><span data-stu-id="3bad1-118">Remarks</span></span>

<span data-ttu-id="3bad1-119">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="3bad1-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bad1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bad1-120">Requirements</span></span>



| <span data-ttu-id="3bad1-121">需求</span><span class="sxs-lookup"><span data-stu-id="3bad1-121">Requirement</span></span> | <span data-ttu-id="3bad1-122">值</span><span class="sxs-lookup"><span data-stu-id="3bad1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bad1-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bad1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3bad1-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="3bad1-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3bad1-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bad1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3bad1-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bad1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3bad1-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="3bad1-127">Namespace</span></span><br/>                | <span data-ttu-id="3bad1-128">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="3bad1-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3bad1-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3bad1-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bad1-130"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bad1-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bad1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bad1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bad1-132">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="3bad1-132">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="3bad1-133">**MicrosoftDNS MBType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="3bad1-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3bad1-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3bad1-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





