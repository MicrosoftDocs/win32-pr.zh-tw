---
title: MicrosoftDNS_X25Type 類別
description: '\_代表 (X25) 記錄之 MicrosoftDNS ResourceRecord 的子類別。'
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- MicrosoftDNS_X25Type 類別 DNS
- MicrosoftDNS_X25Type 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969183"
---
# <a name="microsoftdns_x25type-class"></a><span data-ttu-id="d4319-105">MicrosoftDNS \_ X25Type 類別</span><span class="sxs-lookup"><span data-stu-id="d4319-105">MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="d4319-106">代表 (X25) 記錄之 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 的子類別。</span><span class="sxs-lookup"><span data-stu-id="d4319-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an X.25 (X25) record.</span></span>

<span data-ttu-id="d4319-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d4319-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4319-108">語法</span><span class="sxs-lookup"><span data-stu-id="d4319-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a><span data-ttu-id="d4319-109">成員</span><span class="sxs-lookup"><span data-stu-id="d4319-109">Members</span></span>

<span data-ttu-id="d4319-110">**MicrosoftDNS \_ X25Type** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d4319-110">The **MicrosoftDNS\_X25Type** class has these types of members:</span></span>

-   [<span data-ttu-id="d4319-111">方法</span><span class="sxs-lookup"><span data-stu-id="d4319-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d4319-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d4319-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d4319-113">方法</span><span class="sxs-lookup"><span data-stu-id="d4319-113">Methods</span></span>

<span data-ttu-id="d4319-114">**MicrosoftDNS \_ X25Type** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d4319-114">The **MicrosoftDNS\_X25Type** class has these methods.</span></span>



| <span data-ttu-id="d4319-115">方法</span><span class="sxs-lookup"><span data-stu-id="d4319-115">Method</span></span>                             | <span data-ttu-id="d4319-116">描述</span><span class="sxs-lookup"><span data-stu-id="d4319-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4319-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d4319-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="d4319-118">根據方法輸入參數中的資料具現化 RR 的 ' X25 ' 類型：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值和 PSDN 位址。</span><span class="sxs-lookup"><span data-stu-id="d4319-118">Instantiates an 'X25' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the PSDN address.</span></span> <span data-ttu-id="d4319-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="d4319-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="d4319-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="d4319-120">Qualifiers: Implemented, static</span></span><br/>              |
| <span data-ttu-id="d4319-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="d4319-121">**Modify**</span></span>                         | <span data-ttu-id="d4319-122">這個方法會將 TTL 和 PSDN 位址更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="d4319-122">This method updates the TTL and PSDN Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="d4319-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="d4319-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="d4319-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="d4319-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="d4319-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="d4319-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d4319-126">屬性</span><span class="sxs-lookup"><span data-stu-id="d4319-126">Properties</span></span>

<span data-ttu-id="d4319-127">**MicrosoftDNS \_ X25Type** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d4319-127">The **MicrosoftDNS\_X25Type** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4319-128">**PSDNAddress**</span><span class="sxs-lookup"><span data-stu-id="d4319-128">**PSDNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4319-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d4319-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4319-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d4319-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4319-131">RR 擁有者的 PSDN 位址。</span><span class="sxs-lookup"><span data-stu-id="d4319-131">PSDN address of the owner of the RR.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4319-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4319-132">Requirements</span></span>



| <span data-ttu-id="d4319-133">需求</span><span class="sxs-lookup"><span data-stu-id="d4319-133">Requirement</span></span> | <span data-ttu-id="d4319-134">值</span><span class="sxs-lookup"><span data-stu-id="d4319-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4319-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4319-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d4319-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="d4319-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d4319-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4319-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d4319-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4319-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d4319-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="d4319-139">Namespace</span></span><br/>                | <span data-ttu-id="d4319-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d4319-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d4319-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d4319-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4319-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4319-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4319-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4319-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4319-144">**MicrosoftDNS X25Type 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="d4319-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d4319-145">**Modify MicrosoftDNS \_ X25Type 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="d4319-145">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="d4319-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d4319-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





