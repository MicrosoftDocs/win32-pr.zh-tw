---
title: MicrosoftDNS_MRType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示信箱重新命名 (MR) 記錄。
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- MicrosoftDNS_MRType 類別 DNS
- MicrosoftDNS_MRType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732f0e6f51963f5ae810e4730406a94264fdde47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105257"
---
# <a name="microsoftdns_mrtype-class"></a><span data-ttu-id="d5d2e-105">MicrosoftDNS \_ MRType 類別</span><span class="sxs-lookup"><span data-stu-id="d5d2e-105">MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="d5d2e-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示信箱重新命名 (MR) 記錄。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox Rename (MR) record.</span></span>

<span data-ttu-id="d5d2e-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d2e-108">語法</span><span class="sxs-lookup"><span data-stu-id="d5d2e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a><span data-ttu-id="d5d2e-109">成員</span><span class="sxs-lookup"><span data-stu-id="d5d2e-109">Members</span></span>

<span data-ttu-id="d5d2e-110">**MicrosoftDNS \_ MRType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d5d2e-110">The **MicrosoftDNS\_MRType** class has these types of members:</span></span>

-   [<span data-ttu-id="d5d2e-111">方法</span><span class="sxs-lookup"><span data-stu-id="d5d2e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d5d2e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d5d2e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d5d2e-113">方法</span><span class="sxs-lookup"><span data-stu-id="d5d2e-113">Methods</span></span>

<span data-ttu-id="d5d2e-114">**MicrosoftDNS \_ MRType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-114">The **MicrosoftDNS\_MRType** class has these methods.</span></span>



| <span data-ttu-id="d5d2e-115">方法</span><span class="sxs-lookup"><span data-stu-id="d5d2e-115">Method</span></span>                             | <span data-ttu-id="d5d2e-116">描述</span><span class="sxs-lookup"><span data-stu-id="d5d2e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d2e-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d5d2e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="d5d2e-118">這個方法會根據方法的輸入參數中的資料來具現化 RR 的 ' MR ' 類型：記錄的 DNS 伺服器名稱、信箱的擁有者名稱、類別 (預設 = IN) 、存留時間值和信箱重新命名。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-118">This method instantiates an 'MR' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox rename.</span></span> <span data-ttu-id="d5d2e-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="d5d2e-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="d5d2e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="d5d2e-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="d5d2e-121">**Modify**</span></span>                         | <span data-ttu-id="d5d2e-122">這個方法會將 TTL 和 MR 信箱更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-122">This method updates the TTL and MR Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="d5d2e-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="d5d2e-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="d5d2e-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="d5d2e-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="d5d2e-126">屬性</span><span class="sxs-lookup"><span data-stu-id="d5d2e-126">Properties</span></span>

<span data-ttu-id="d5d2e-127">**MicrosoftDNS \_ MRType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-127">The **MicrosoftDNS\_MRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5d2e-128">**MRMailbox**</span><span class="sxs-lookup"><span data-stu-id="d5d2e-128">**MRMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d2e-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d5d2e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5d2e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5d2e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5d2e-131">FQDN，指定在記錄的擁有者名稱中指定的信箱適當重新命名的信箱。</span><span class="sxs-lookup"><span data-stu-id="d5d2e-131">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5d2e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5d2e-132">Requirements</span></span>



| <span data-ttu-id="d5d2e-133">需求</span><span class="sxs-lookup"><span data-stu-id="d5d2e-133">Requirement</span></span> | <span data-ttu-id="d5d2e-134">值</span><span class="sxs-lookup"><span data-stu-id="d5d2e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d2e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5d2e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d2e-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="d5d2e-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d5d2e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5d2e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d2e-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5d2e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d5d2e-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="d5d2e-139">Namespace</span></span><br/>                | <span data-ttu-id="d5d2e-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d5d2e-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d5d2e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d5d2e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5d2e-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5d2e-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d2e-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5d2e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d2e-144">**MicrosoftDNS MRType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="d5d2e-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d5d2e-145">**Modify MicrosoftDNS \_ MRType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="d5d2e-145">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="d5d2e-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d5d2e-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





