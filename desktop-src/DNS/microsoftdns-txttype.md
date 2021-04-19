---
title: MicrosoftDNS_TXTType 類別
description: '\_代表文字 (TXT) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- MicrosoftDNS_TXTType 類別 DNS
- MicrosoftDNS_TXTType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969201"
---
# <a name="microsoftdns_txttype-class"></a><span data-ttu-id="c9eb2-105">MicrosoftDNS \_ TXTType 類別</span><span class="sxs-lookup"><span data-stu-id="c9eb2-105">MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="c9eb2-106">代表文字 (TXT) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Text (TXT) record.</span></span>

<span data-ttu-id="c9eb2-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9eb2-108">語法</span><span class="sxs-lookup"><span data-stu-id="c9eb2-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a><span data-ttu-id="c9eb2-109">成員</span><span class="sxs-lookup"><span data-stu-id="c9eb2-109">Members</span></span>

<span data-ttu-id="c9eb2-110">**MicrosoftDNS \_ TXTType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c9eb2-110">The **MicrosoftDNS\_TXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="c9eb2-111">方法</span><span class="sxs-lookup"><span data-stu-id="c9eb2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c9eb2-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c9eb2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c9eb2-113">方法</span><span class="sxs-lookup"><span data-stu-id="c9eb2-113">Methods</span></span>

<span data-ttu-id="c9eb2-114">**MicrosoftDNS \_ TXTType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-114">The **MicrosoftDNS\_TXTType** class has these methods.</span></span>



| <span data-ttu-id="c9eb2-115">方法</span><span class="sxs-lookup"><span data-stu-id="c9eb2-115">Method</span></span>                             | <span data-ttu-id="c9eb2-116">描述</span><span class="sxs-lookup"><span data-stu-id="c9eb2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9eb2-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c9eb2-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c9eb2-118">根據方法的輸入參數中的資料具現化 TXT 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及記錄的文字。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-118">Instantiates a TXT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the record's text.</span></span> <span data-ttu-id="c9eb2-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c9eb2-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="c9eb2-120">Qualifiers: Implemented, static</span></span><br/>        |
| <span data-ttu-id="c9eb2-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="c9eb2-121">**Modify**</span></span>                         | <span data-ttu-id="c9eb2-122">將 TTL 和描述性文字更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-122">Updates the TTL and Descriptive Text to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c9eb2-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c9eb2-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c9eb2-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="c9eb2-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c9eb2-126">屬性</span><span class="sxs-lookup"><span data-stu-id="c9eb2-126">Properties</span></span>

<span data-ttu-id="c9eb2-127">**MicrosoftDNS \_ TXTType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-127">The **MicrosoftDNS\_TXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9eb2-128">**DescriptiveText**</span><span class="sxs-lookup"><span data-stu-id="c9eb2-128">**DescriptiveText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9eb2-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c9eb2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9eb2-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c9eb2-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9eb2-131">描述性文字，相依于擁有者網域的語法。</span><span class="sxs-lookup"><span data-stu-id="c9eb2-131">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9eb2-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9eb2-132">Requirements</span></span>



| <span data-ttu-id="c9eb2-133">需求</span><span class="sxs-lookup"><span data-stu-id="c9eb2-133">Requirement</span></span> | <span data-ttu-id="c9eb2-134">值</span><span class="sxs-lookup"><span data-stu-id="c9eb2-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9eb2-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9eb2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c9eb2-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="c9eb2-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c9eb2-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9eb2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c9eb2-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9eb2-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c9eb2-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9eb2-139">Namespace</span></span><br/>                | <span data-ttu-id="c9eb2-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c9eb2-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c9eb2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c9eb2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9eb2-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9eb2-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9eb2-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9eb2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9eb2-144">**MicrosoftDNS TXTType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="c9eb2-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c9eb2-145">**Modify MicrosoftDNS \_ TXTType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="c9eb2-145">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="c9eb2-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c9eb2-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





