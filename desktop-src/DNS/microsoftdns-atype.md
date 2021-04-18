---
title: MicrosoftDNS_AType 類別
description: MicrosoftDNS \_ ResourceRecord 的子類別，表示) 記錄 (的主機位址。
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- MicrosoftDNS_AType 類別 DNS
- MicrosoftDNS_AType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966112"
---
# <a name="microsoftdns_atype-class"></a><span data-ttu-id="fc30e-105">MicrosoftDNS \_ AType 類別</span><span class="sxs-lookup"><span data-stu-id="fc30e-105">MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="fc30e-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示) 記錄 (的主機位址。</span><span class="sxs-lookup"><span data-stu-id="fc30e-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a host Address (A) record.</span></span>

<span data-ttu-id="fc30e-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="fc30e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc30e-108">語法</span><span class="sxs-lookup"><span data-stu-id="fc30e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a><span data-ttu-id="fc30e-109">成員</span><span class="sxs-lookup"><span data-stu-id="fc30e-109">Members</span></span>

<span data-ttu-id="fc30e-110">**MicrosoftDNS \_ AType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fc30e-110">The **MicrosoftDNS\_AType** class has these types of members:</span></span>

-   [<span data-ttu-id="fc30e-111">方法</span><span class="sxs-lookup"><span data-stu-id="fc30e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc30e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fc30e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc30e-113">方法</span><span class="sxs-lookup"><span data-stu-id="fc30e-113">Methods</span></span>

<span data-ttu-id="fc30e-114">**MicrosoftDNS \_ AType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fc30e-114">The **MicrosoftDNS\_AType** class has these methods.</span></span>



| <span data-ttu-id="fc30e-115">方法</span><span class="sxs-lookup"><span data-stu-id="fc30e-115">Method</span></span>                             | <span data-ttu-id="fc30e-116">描述</span><span class="sxs-lookup"><span data-stu-id="fc30e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc30e-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fc30e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fc30e-118">根據方法的輸入參數中的資料，具現化主機位址 () RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設 = IN) 、存留時間值和主機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fc30e-118">Instantiates a Host Address (A) RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the IP address of the host.</span></span> <span data-ttu-id="fc30e-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="fc30e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fc30e-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="fc30e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fc30e-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="fc30e-121">**Modify**</span></span>                         | <span data-ttu-id="fc30e-122">將 TTL 和 IP 位址更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="fc30e-122">Updates the TTL and IP address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fc30e-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="fc30e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fc30e-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="fc30e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fc30e-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="fc30e-125">Qualifiers: Implemented</span></span><br/>             |



 

### <a name="properties"></a><span data-ttu-id="fc30e-126">屬性</span><span class="sxs-lookup"><span data-stu-id="fc30e-126">Properties</span></span>

<span data-ttu-id="fc30e-127">**MicrosoftDNS \_ AType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fc30e-127">The **MicrosoftDNS\_AType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc30e-128">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="fc30e-128">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc30e-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc30e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc30e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc30e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc30e-131">字串，代表主機的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="fc30e-131">String representing the IPv4 address of the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc30e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc30e-132">Requirements</span></span>



| <span data-ttu-id="fc30e-133">需求</span><span class="sxs-lookup"><span data-stu-id="fc30e-133">Requirement</span></span> | <span data-ttu-id="fc30e-134">值</span><span class="sxs-lookup"><span data-stu-id="fc30e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc30e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc30e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fc30e-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="fc30e-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fc30e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc30e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fc30e-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc30e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fc30e-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="fc30e-139">Namespace</span></span><br/>                | <span data-ttu-id="fc30e-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="fc30e-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fc30e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fc30e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc30e-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc30e-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc30e-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc30e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc30e-144">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="fc30e-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="fc30e-145">**MicrosoftDNS AType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fc30e-145">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fc30e-146">**Modify MicrosoftDNS \_ AType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="fc30e-146">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





