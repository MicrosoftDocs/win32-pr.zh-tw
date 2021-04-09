---
title: MicrosoftDNS_MXType 類別
description: '\_代表郵件交換 (MR) RR 的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- MicrosoftDNS_MXType 類別 DNS
- MicrosoftDNS_MXType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934378"
---
# <a name="microsoftdns_mxtype-class"></a><span data-ttu-id="01f04-105">MicrosoftDNS \_ MXType 類別</span><span class="sxs-lookup"><span data-stu-id="01f04-105">MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="01f04-106">代表郵件交換 (MR) RR 的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="01f04-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Exchanger (MR) RR.</span></span>

<span data-ttu-id="01f04-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="01f04-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f04-108">語法</span><span class="sxs-lookup"><span data-stu-id="01f04-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a><span data-ttu-id="01f04-109">成員</span><span class="sxs-lookup"><span data-stu-id="01f04-109">Members</span></span>

<span data-ttu-id="01f04-110">**MicrosoftDNS \_ MXType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="01f04-110">The **MicrosoftDNS\_MXType** class has these types of members:</span></span>

-   [<span data-ttu-id="01f04-111">方法</span><span class="sxs-lookup"><span data-stu-id="01f04-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="01f04-112">屬性</span><span class="sxs-lookup"><span data-stu-id="01f04-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="01f04-113">方法</span><span class="sxs-lookup"><span data-stu-id="01f04-113">Methods</span></span>

<span data-ttu-id="01f04-114">**MicrosoftDNS \_ MXType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="01f04-114">The **MicrosoftDNS\_MXType** class has these methods.</span></span>



| <span data-ttu-id="01f04-115">方法</span><span class="sxs-lookup"><span data-stu-id="01f04-115">Method</span></span>                             | <span data-ttu-id="01f04-116">描述</span><span class="sxs-lookup"><span data-stu-id="01f04-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f04-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="01f04-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="01f04-118">根據方法的輸入參數中的資料具現化 MX 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值、記錄喜好設定，以及願意作為郵件交換的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="01f04-118">Instantiates an MX Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, record preference, and host name willing to be a mail exchange.</span></span> <span data-ttu-id="01f04-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="01f04-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="01f04-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="01f04-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="01f04-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="01f04-121">**Modify**</span></span>                         | <span data-ttu-id="01f04-122">將 TTL、喜好設定和郵件交換更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="01f04-122">Updates the TTL, Preference, and Mail Exchange to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="01f04-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="01f04-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="01f04-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="01f04-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="01f04-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="01f04-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="01f04-126">屬性</span><span class="sxs-lookup"><span data-stu-id="01f04-126">Properties</span></span>

<span data-ttu-id="01f04-127">**MicrosoftDNS \_ MXType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="01f04-127">The **MicrosoftDNS\_MXType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01f04-128">**MailExchange**</span><span class="sxs-lookup"><span data-stu-id="01f04-128">**MailExchange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f04-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01f04-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01f04-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f04-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01f04-131">FQDN 指定的主機願意作為擁有者名稱的郵件交換。</span><span class="sxs-lookup"><span data-stu-id="01f04-131">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="01f04-132">**偏好**</span><span class="sxs-lookup"><span data-stu-id="01f04-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f04-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="01f04-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01f04-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f04-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01f04-135">在相同擁有者的其他專案中提供給此 RR 的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="01f04-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="01f04-136">偏好較低的值。</span><span class="sxs-lookup"><span data-stu-id="01f04-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01f04-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="01f04-137">Requirements</span></span>



| <span data-ttu-id="01f04-138">需求</span><span class="sxs-lookup"><span data-stu-id="01f04-138">Requirement</span></span> | <span data-ttu-id="01f04-139">值</span><span class="sxs-lookup"><span data-stu-id="01f04-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01f04-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01f04-140">Minimum supported client</span></span><br/> | <span data-ttu-id="01f04-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="01f04-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="01f04-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01f04-142">Minimum supported server</span></span><br/> | <span data-ttu-id="01f04-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01f04-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="01f04-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="01f04-144">Namespace</span></span><br/>                | <span data-ttu-id="01f04-145">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="01f04-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="01f04-146">MOF</span><span class="sxs-lookup"><span data-stu-id="01f04-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01f04-147"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="01f04-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01f04-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01f04-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f04-149">**MicrosoftDNS MXType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="01f04-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="01f04-150">**Modify MicrosoftDNS \_ MXType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="01f04-150">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="01f04-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="01f04-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





