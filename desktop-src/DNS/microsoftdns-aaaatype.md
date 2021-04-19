---
title: MicrosoftDNS_AAAAType 類別
description: '\_代表 IPv6 位址 (AAAA) 記錄的 MicrosoftDNS ResourceRecord 子類別。 AAAA 記錄通常會發音為 0034; 四-a 記錄 \ 0034;。'
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- MicrosoftDNS_AAAAType 類別 DNS
- MicrosoftDNS_AAAAType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969168"
---
# <a name="microsoftdns_aaaatype-class"></a><span data-ttu-id="a4904-106">MicrosoftDNS \_ AAAAType 類別</span><span class="sxs-lookup"><span data-stu-id="a4904-106">MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="a4904-107">代表 IPv6 位址 (AAAA) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="a4904-107">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an IPv6 Address (AAAA) record.</span></span> <span data-ttu-id="a4904-108">AAAA 記錄通常會發音為「四 a 記錄」。</span><span class="sxs-lookup"><span data-stu-id="a4904-108">The AAAA record is commonly pronounced "quad-a record".</span></span>

<span data-ttu-id="a4904-109">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="a4904-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4904-110">語法</span><span class="sxs-lookup"><span data-stu-id="a4904-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a><span data-ttu-id="a4904-111">成員</span><span class="sxs-lookup"><span data-stu-id="a4904-111">Members</span></span>

<span data-ttu-id="a4904-112">**MicrosoftDNS \_ AAAAType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a4904-112">The **MicrosoftDNS\_AAAAType** class has these types of members:</span></span>

-   [<span data-ttu-id="a4904-113">方法</span><span class="sxs-lookup"><span data-stu-id="a4904-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a4904-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a4904-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a4904-115">方法</span><span class="sxs-lookup"><span data-stu-id="a4904-115">Methods</span></span>

<span data-ttu-id="a4904-116">**MicrosoftDNS \_ AAAAType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a4904-116">The **MicrosoftDNS\_AAAAType** class has these methods.</span></span>



| <span data-ttu-id="a4904-117">方法</span><span class="sxs-lookup"><span data-stu-id="a4904-117">Method</span></span>                             | <span data-ttu-id="a4904-118">描述</span><span class="sxs-lookup"><span data-stu-id="a4904-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4904-119">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a4904-119">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="a4904-120">根據方法的輸入參數中的資料來具現化 ' AAAA ' 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者/主機名稱、類別 (預設值 = IN) 、存留時間值和 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="a4904-120">Instantiates an 'AAAA' type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Host Name, class (default = IN), time-to-live value, and the IPv6 address.</span></span> <span data-ttu-id="a4904-121">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="a4904-121">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a4904-122">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="a4904-122">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="a4904-123">**修改**</span><span class="sxs-lookup"><span data-stu-id="a4904-123">**Modify**</span></span>                         | <span data-ttu-id="a4904-124">將 TTL 和 IPv6 位址更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="a4904-124">Updates the TTL and IPv6 address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a4904-125">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="a4904-125">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="a4904-126">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="a4904-126">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a4904-127">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="a4904-127">Qualifiers: Implemented</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="a4904-128">屬性</span><span class="sxs-lookup"><span data-stu-id="a4904-128">Properties</span></span>

<span data-ttu-id="a4904-129">**MicrosoftDNS \_ AAAAType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a4904-129">The **MicrosoftDNS\_AAAAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4904-130">**IPv6Address**</span><span class="sxs-lookup"><span data-stu-id="a4904-130">**IPv6Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4904-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4904-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4904-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a4904-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4904-133">主機的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="a4904-133">IPv6 address for the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4904-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4904-134">Requirements</span></span>



| <span data-ttu-id="a4904-135">需求</span><span class="sxs-lookup"><span data-stu-id="a4904-135">Requirement</span></span> | <span data-ttu-id="a4904-136">值</span><span class="sxs-lookup"><span data-stu-id="a4904-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4904-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4904-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a4904-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="a4904-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a4904-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4904-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a4904-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4904-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a4904-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4904-141">Namespace</span></span><br/>                | <span data-ttu-id="a4904-142">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="a4904-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a4904-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a4904-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4904-144"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4904-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4904-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4904-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4904-146">**MicrosoftDNS AAAAType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="a4904-146">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a4904-147">**Modify MicrosoftDNS \_ AAAAType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="a4904-147">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="a4904-148">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a4904-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





