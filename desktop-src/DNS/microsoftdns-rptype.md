---
title: MicrosoftDNS_RPType 類別
description: '\_代表負責任人員 (RP) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- MicrosoftDNS_RPType 類別 DNS
- MicrosoftDNS_RPType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aae8686016d26cb9007b21a06c125d56ed5207f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843764"
---
# <a name="microsoftdns_rptype-class"></a><span data-ttu-id="ff218-105">MicrosoftDNS \_ RPType 類別</span><span class="sxs-lookup"><span data-stu-id="ff218-105">MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="ff218-106">代表負責任人員 (RP) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="ff218-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Responsible Person (RP) record.</span></span>

<span data-ttu-id="ff218-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="ff218-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff218-108">語法</span><span class="sxs-lookup"><span data-stu-id="ff218-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a><span data-ttu-id="ff218-109">成員</span><span class="sxs-lookup"><span data-stu-id="ff218-109">Members</span></span>

<span data-ttu-id="ff218-110">**MicrosoftDNS \_ RPType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ff218-110">The **MicrosoftDNS\_RPType** class has these types of members:</span></span>

-   [<span data-ttu-id="ff218-111">方法</span><span class="sxs-lookup"><span data-stu-id="ff218-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ff218-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ff218-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ff218-113">方法</span><span class="sxs-lookup"><span data-stu-id="ff218-113">Methods</span></span>

<span data-ttu-id="ff218-114">**MicrosoftDNS \_ RPType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ff218-114">The **MicrosoftDNS\_RPType** class has these methods.</span></span>



| <span data-ttu-id="ff218-115">方法</span><span class="sxs-lookup"><span data-stu-id="ff218-115">Method</span></span>                             | <span data-ttu-id="ff218-116">描述</span><span class="sxs-lookup"><span data-stu-id="ff218-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff218-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ff218-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ff218-118">根據方法的輸入參數中的資料來具現化 RP 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者/負責任的人員名稱、類別 (預設值 = IN) 、存留時間值以及人員信箱和 TXT RR 位置的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ff218-118">Instantiates an RP Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/responsible person Name, class (default = IN), time-to-live value and the domain names for the person's mailbox and TXT RR locations.</span></span> <span data-ttu-id="ff218-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="ff218-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ff218-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="ff218-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ff218-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="ff218-121">**Modify**</span></span>                         | <span data-ttu-id="ff218-122">這個方法會將 TTL、RP 信箱和 TXT 功能變數名稱更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="ff218-122">This method updates the TTL, RP Mailbox and TXT Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ff218-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="ff218-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ff218-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="ff218-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ff218-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ff218-125">Qualifiers: Implemented</span></span><br/>                                  |



 

### <a name="properties"></a><span data-ttu-id="ff218-126">屬性</span><span class="sxs-lookup"><span data-stu-id="ff218-126">Properties</span></span>

<span data-ttu-id="ff218-127">**MicrosoftDNS \_ RPType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ff218-127">The **MicrosoftDNS\_RPType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff218-128">**RPMailbox**</span><span class="sxs-lookup"><span data-stu-id="ff218-128">**RPMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff218-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ff218-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff218-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ff218-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff218-131">指定負責任人員信箱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ff218-131">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="ff218-132">**TXTDomainName**</span><span class="sxs-lookup"><span data-stu-id="ff218-132">**TXTDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff218-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ff218-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff218-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ff218-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff218-135">存在 TXT 資源記錄的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ff218-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff218-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff218-136">Requirements</span></span>



| <span data-ttu-id="ff218-137">需求</span><span class="sxs-lookup"><span data-stu-id="ff218-137">Requirement</span></span> | <span data-ttu-id="ff218-138">值</span><span class="sxs-lookup"><span data-stu-id="ff218-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff218-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff218-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ff218-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="ff218-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ff218-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff218-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ff218-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff218-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ff218-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="ff218-143">Namespace</span></span><br/>                | <span data-ttu-id="ff218-144">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ff218-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ff218-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ff218-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff218-146"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff218-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff218-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff218-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff218-148">**MicrosoftDNS RPType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ff218-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ff218-149">**Modify MicrosoftDNS \_ RPType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="ff218-149">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="ff218-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ff218-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





