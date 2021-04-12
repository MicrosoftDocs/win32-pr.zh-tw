---
title: MicrosoftDNS_PTRType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示指標 (PTR) 記錄。
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- MicrosoftDNS_PTRType 類別 DNS
- MicrosoftDNS_PTRType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65dc434eb751ed925ab9efcdaf29f04741b749ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508691"
---
# <a name="microsoftdns_ptrtype-class"></a><span data-ttu-id="78b9b-105">MicrosoftDNS \_ PTRType 類別</span><span class="sxs-lookup"><span data-stu-id="78b9b-105">MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="78b9b-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示指標 (PTR) 記錄。</span><span class="sxs-lookup"><span data-stu-id="78b9b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Pointer (PTR) record.</span></span>

<span data-ttu-id="78b9b-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="78b9b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="78b9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="78b9b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a><span data-ttu-id="78b9b-109">成員</span><span class="sxs-lookup"><span data-stu-id="78b9b-109">Members</span></span>

<span data-ttu-id="78b9b-110">**MicrosoftDNS \_ PTRType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="78b9b-110">The **MicrosoftDNS\_PTRType** class has these types of members:</span></span>

-   [<span data-ttu-id="78b9b-111">方法</span><span class="sxs-lookup"><span data-stu-id="78b9b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="78b9b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="78b9b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78b9b-113">方法</span><span class="sxs-lookup"><span data-stu-id="78b9b-113">Methods</span></span>

<span data-ttu-id="78b9b-114">**MicrosoftDNS \_ PTRType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="78b9b-114">The **MicrosoftDNS\_PTRType** class has these methods.</span></span>



| <span data-ttu-id="78b9b-115">方法</span><span class="sxs-lookup"><span data-stu-id="78b9b-115">Method</span></span>                             | <span data-ttu-id="78b9b-116">描述</span><span class="sxs-lookup"><span data-stu-id="78b9b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78b9b-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="78b9b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="78b9b-118">根據方法的輸入參數中的資料具現化 DNS PTR 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值以及 PTR 記錄的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="78b9b-118">Instantiates a DNS PTR Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the FQDN of the PTR record.</span></span> <span data-ttu-id="78b9b-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="78b9b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="78b9b-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="78b9b-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="78b9b-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="78b9b-121">**Modify**</span></span>                         | <span data-ttu-id="78b9b-122">將 TTL 和 PTR 功能變數名稱更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="78b9b-122">Updates the TTL and PTR Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="78b9b-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="78b9b-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="78b9b-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="78b9b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="78b9b-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="78b9b-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="78b9b-126">屬性</span><span class="sxs-lookup"><span data-stu-id="78b9b-126">Properties</span></span>

<span data-ttu-id="78b9b-127">**MicrosoftDNS \_ PTRType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="78b9b-127">The **MicrosoftDNS\_PTRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78b9b-128">**PTRDomainName**</span><span class="sxs-lookup"><span data-stu-id="78b9b-128">**PTRDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b9b-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78b9b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b9b-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78b9b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78b9b-131">PTR 記錄資料的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="78b9b-131">FQDN of the PTR record data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78b9b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="78b9b-132">Requirements</span></span>



| <span data-ttu-id="78b9b-133">需求</span><span class="sxs-lookup"><span data-stu-id="78b9b-133">Requirement</span></span> | <span data-ttu-id="78b9b-134">值</span><span class="sxs-lookup"><span data-stu-id="78b9b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78b9b-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78b9b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="78b9b-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="78b9b-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="78b9b-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78b9b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="78b9b-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78b9b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="78b9b-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="78b9b-139">Namespace</span></span><br/>                | <span data-ttu-id="78b9b-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="78b9b-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="78b9b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="78b9b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78b9b-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="78b9b-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78b9b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78b9b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b9b-144">**MicrosoftDNS PTRType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="78b9b-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="78b9b-145">**Modify MicrosoftDNS \_ PTRType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="78b9b-145">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="78b9b-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="78b9b-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





