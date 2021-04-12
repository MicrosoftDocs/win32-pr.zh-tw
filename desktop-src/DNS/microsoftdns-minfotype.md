---
title: MicrosoftDNS_MINFOType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示 (MINFO) 記錄的郵件資訊。
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- MicrosoftDNS_MINFOType 類別 DNS
- MicrosoftDNS_MINFOType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105936"
---
# <a name="microsoftdns_minfotype-class"></a><span data-ttu-id="f150c-105">MicrosoftDNS \_ MINFOType 類別</span><span class="sxs-lookup"><span data-stu-id="f150c-105">MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="f150c-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示 (MINFO) 記錄的郵件資訊。</span><span class="sxs-lookup"><span data-stu-id="f150c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Information (MINFO) record.</span></span>

<span data-ttu-id="f150c-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="f150c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f150c-108">語法</span><span class="sxs-lookup"><span data-stu-id="f150c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a><span data-ttu-id="f150c-109">成員</span><span class="sxs-lookup"><span data-stu-id="f150c-109">Members</span></span>

<span data-ttu-id="f150c-110">**MicrosoftDNS \_ MINFOType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f150c-110">The **MicrosoftDNS\_MINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="f150c-111">方法</span><span class="sxs-lookup"><span data-stu-id="f150c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f150c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f150c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f150c-113">方法</span><span class="sxs-lookup"><span data-stu-id="f150c-113">Methods</span></span>

<span data-ttu-id="f150c-114">**MicrosoftDNS \_ MINFOType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f150c-114">The **MicrosoftDNS\_MINFOType** class has these methods.</span></span>



| <span data-ttu-id="f150c-115">方法</span><span class="sxs-lookup"><span data-stu-id="f150c-115">Method</span></span>                             | <span data-ttu-id="f150c-116">描述</span><span class="sxs-lookup"><span data-stu-id="f150c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f150c-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f150c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="f150c-118">根據方法的輸入參數中的資料具現化 MINFO 類型的 RR：記錄的 DNS 伺服器名稱、功能變數名稱、郵寄清單/box 的擁有者名稱、類別 (預設值 =) 、存留時間值以及負責任和錯誤信箱。</span><span class="sxs-lookup"><span data-stu-id="f150c-118">Instantiates an MINFO Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail list/box, class (default = IN), time-to-live value and the responsible and error mailboxes.</span></span> <span data-ttu-id="f150c-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="f150c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="f150c-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="f150c-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="f150c-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="f150c-121">**Modify**</span></span>                         | <span data-ttu-id="f150c-122">這個方法會將 TTL、負責任的信箱和錯誤信箱更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="f150c-122">This method updates the TTL, Responsible Mailbox, and Error Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="f150c-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="f150c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="f150c-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="f150c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="f150c-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="f150c-125">Qualifiers: Implemented</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="f150c-126">屬性</span><span class="sxs-lookup"><span data-stu-id="f150c-126">Properties</span></span>

<span data-ttu-id="f150c-127">**MicrosoftDNS \_ MINFOType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f150c-127">The **MicrosoftDNS\_MINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f150c-128">**ErrorMailbox**</span><span class="sxs-lookup"><span data-stu-id="f150c-128">**ErrorMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f150c-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f150c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f150c-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f150c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f150c-131">FQDN，指定信箱以接收與郵寄清單相關的錯誤訊息，或 MINFO 記錄的擁有者名稱所指定的信箱。</span><span class="sxs-lookup"><span data-stu-id="f150c-131">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="f150c-132">**ResponsibleMailbox**</span><span class="sxs-lookup"><span data-stu-id="f150c-132">**ResponsibleMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f150c-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f150c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f150c-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f150c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f150c-135">FQDN，指定負責記錄的擁有者名稱中所指定之郵寄清單或信箱的信箱。</span><span class="sxs-lookup"><span data-stu-id="f150c-135">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f150c-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="f150c-136">Requirements</span></span>



| <span data-ttu-id="f150c-137">需求</span><span class="sxs-lookup"><span data-stu-id="f150c-137">Requirement</span></span> | <span data-ttu-id="f150c-138">值</span><span class="sxs-lookup"><span data-stu-id="f150c-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f150c-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f150c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f150c-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="f150c-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f150c-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f150c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f150c-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f150c-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f150c-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="f150c-143">Namespace</span></span><br/>                | <span data-ttu-id="f150c-144">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="f150c-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f150c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="f150c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f150c-146"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="f150c-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f150c-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f150c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f150c-148">**MicrosoftDNS MINFOType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="f150c-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f150c-149">**Modify MicrosoftDNS \_ MINFOType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="f150c-149">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="f150c-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f150c-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





