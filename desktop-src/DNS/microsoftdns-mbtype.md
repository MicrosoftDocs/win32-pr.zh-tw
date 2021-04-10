---
title: MicrosoftDNS_MBType 類別
description: '\_代表信箱 (MB) 資源記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- MicrosoftDNS_MBType 類別 DNS
- MicrosoftDNS_MBType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ad6599ad058f65beba961f00c1bd6c43663487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934533"
---
# <a name="microsoftdns_mbtype-class"></a><span data-ttu-id="e15de-105">MicrosoftDNS \_ MBType 類別</span><span class="sxs-lookup"><span data-stu-id="e15de-105">MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="e15de-106">代表信箱 (MB) 資源記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="e15de-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox (MB) resource record.</span></span>

<span data-ttu-id="e15de-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="e15de-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15de-108">語法</span><span class="sxs-lookup"><span data-stu-id="e15de-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a><span data-ttu-id="e15de-109">成員</span><span class="sxs-lookup"><span data-stu-id="e15de-109">Members</span></span>

<span data-ttu-id="e15de-110">**MicrosoftDNS \_ MBType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e15de-110">The **MicrosoftDNS\_MBType** class has these types of members:</span></span>

-   [<span data-ttu-id="e15de-111">方法</span><span class="sxs-lookup"><span data-stu-id="e15de-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e15de-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e15de-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e15de-113">方法</span><span class="sxs-lookup"><span data-stu-id="e15de-113">Methods</span></span>

<span data-ttu-id="e15de-114">**MicrosoftDNS \_ MBType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e15de-114">The **MicrosoftDNS\_MBType** class has these methods.</span></span>



| <span data-ttu-id="e15de-115">方法</span><span class="sxs-lookup"><span data-stu-id="e15de-115">Method</span></span>                             | <span data-ttu-id="e15de-116">描述</span><span class="sxs-lookup"><span data-stu-id="e15de-116">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e15de-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e15de-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e15de-118">根據方法的輸入參數中的資料具現化 MB RR：記錄的 DNS 伺服器名稱、信箱名稱、信箱的擁有者名稱、類別 (預設值 = IN) 、存留時間值和信箱主機。</span><span class="sxs-lookup"><span data-stu-id="e15de-118">Instantiates an MB RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox host.</span></span> <span data-ttu-id="e15de-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="e15de-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e15de-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="e15de-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="e15de-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="e15de-121">**Modify**</span></span>                         | <span data-ttu-id="e15de-122">將 TTL 和 MB 主機更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="e15de-122">Updates the TTL and MB host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e15de-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="e15de-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e15de-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="e15de-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e15de-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="e15de-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="e15de-126">屬性</span><span class="sxs-lookup"><span data-stu-id="e15de-126">Properties</span></span>

<span data-ttu-id="e15de-127">**MicrosoftDNS \_ MBType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e15de-127">The **MicrosoftDNS\_MBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e15de-128">**MBHost**</span><span class="sxs-lookup"><span data-stu-id="e15de-128">**MBHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e15de-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e15de-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e15de-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e15de-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e15de-131">FQDN，指定記錄的擁有者名稱中指定之信箱的主機。</span><span class="sxs-lookup"><span data-stu-id="e15de-131">FQDN that specifies a host of the mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e15de-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e15de-132">Requirements</span></span>



| <span data-ttu-id="e15de-133">需求</span><span class="sxs-lookup"><span data-stu-id="e15de-133">Requirement</span></span> | <span data-ttu-id="e15de-134">值</span><span class="sxs-lookup"><span data-stu-id="e15de-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e15de-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e15de-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e15de-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="e15de-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e15de-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e15de-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e15de-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e15de-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e15de-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="e15de-139">Namespace</span></span><br/>                | <span data-ttu-id="e15de-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e15de-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e15de-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e15de-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e15de-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="e15de-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e15de-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e15de-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e15de-144">**MicrosoftDNS MBType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="e15de-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e15de-145">**Modify MicrosoftDNS \_ MBType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="e15de-145">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="e15de-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e15de-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





