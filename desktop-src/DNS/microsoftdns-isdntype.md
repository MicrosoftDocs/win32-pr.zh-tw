---
title: MicrosoftDNS_ISDNType 類別
description: 代表 ISDN 記錄之 MicrosoftDNS ResourceRecord 的子類別 \_ 。
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- MicrosoftDNS_ISDNType 類別 DNS
- MicrosoftDNS_ISDNType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e8b50d75f7b6d57226247c978ced45e07b1acc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093907"
---
# <a name="microsoftdns_isdntype-class"></a><span data-ttu-id="0eaa7-105">MicrosoftDNS \_ ISDNType 類別</span><span class="sxs-lookup"><span data-stu-id="0eaa7-105">MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="0eaa7-106">代表 ISDN 記錄之 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 的子類別。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ISDN record.</span></span>

<span data-ttu-id="0eaa7-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eaa7-108">語法</span><span class="sxs-lookup"><span data-stu-id="0eaa7-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a><span data-ttu-id="0eaa7-109">成員</span><span class="sxs-lookup"><span data-stu-id="0eaa7-109">Members</span></span>

<span data-ttu-id="0eaa7-110">**MicrosoftDNS \_ ISDNType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0eaa7-110">The **MicrosoftDNS\_ISDNType** class has these types of members:</span></span>

-   [<span data-ttu-id="0eaa7-111">方法</span><span class="sxs-lookup"><span data-stu-id="0eaa7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0eaa7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0eaa7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0eaa7-113">方法</span><span class="sxs-lookup"><span data-stu-id="0eaa7-113">Methods</span></span>

<span data-ttu-id="0eaa7-114">**MicrosoftDNS \_ ISDNType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-114">The **MicrosoftDNS\_ISDNType** class has these methods.</span></span>



| <span data-ttu-id="0eaa7-115">方法</span><span class="sxs-lookup"><span data-stu-id="0eaa7-115">Method</span></span>                             | <span data-ttu-id="0eaa7-116">描述</span><span class="sxs-lookup"><span data-stu-id="0eaa7-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eaa7-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="0eaa7-118">根據方法的輸入參數中的資料具現化 ISDN 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及擁有者的 ISDN 號碼和子位址。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-118">Instantiates an ISDN Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the ISDN number and subaddress of the owner.</span></span> <span data-ttu-id="0eaa7-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="0eaa7-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="0eaa7-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="0eaa7-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-121">**Modify**</span></span>                         | <span data-ttu-id="0eaa7-122">將 TTL、ISDN 號碼和子位址更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-122">Updates the TTL, ISDN Number, and Subaddress to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="0eaa7-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="0eaa7-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="0eaa7-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="0eaa7-125">Qualifiers: Implemented</span></span><br/>                   |



 

### <a name="properties"></a><span data-ttu-id="0eaa7-126">屬性</span><span class="sxs-lookup"><span data-stu-id="0eaa7-126">Properties</span></span>

<span data-ttu-id="0eaa7-127">**MicrosoftDNS \_ ISDNType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-127">The **MicrosoftDNS\_ISDNType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0eaa7-128">**ISDNNumber**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-128">**ISDNNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eaa7-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0eaa7-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0eaa7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eaa7-131">記錄擁有者的 ISDN 號碼和 DDI。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-131">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="0eaa7-132">**首先**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-132">**SubAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eaa7-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0eaa7-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0eaa7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eaa7-135">擁有者的子位址（若已定義）。</span><span class="sxs-lookup"><span data-stu-id="0eaa7-135">Subaddress of the owner, if defined.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0eaa7-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="0eaa7-136">Requirements</span></span>



| <span data-ttu-id="0eaa7-137">需求</span><span class="sxs-lookup"><span data-stu-id="0eaa7-137">Requirement</span></span> | <span data-ttu-id="0eaa7-138">值</span><span class="sxs-lookup"><span data-stu-id="0eaa7-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0eaa7-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0eaa7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0eaa7-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="0eaa7-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0eaa7-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0eaa7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0eaa7-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0eaa7-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0eaa7-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="0eaa7-143">Namespace</span></span><br/>                | <span data-ttu-id="0eaa7-144">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="0eaa7-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="0eaa7-145">MOF</span><span class="sxs-lookup"><span data-stu-id="0eaa7-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0eaa7-146"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="0eaa7-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eaa7-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0eaa7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eaa7-148">**MicrosoftDNS ISDNType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="0eaa7-149">**Modify MicrosoftDNS \_ ISDNType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-149">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="0eaa7-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="0eaa7-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





