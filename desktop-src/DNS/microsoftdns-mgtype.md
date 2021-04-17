---
title: MicrosoftDNS_MGType 類別
description: '\_代表郵件群組 (MG) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- MicrosoftDNS_MGType 類別 DNS
- MicrosoftDNS_MGType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509371"
---
# <a name="microsoftdns_mgtype-class"></a><span data-ttu-id="55503-105">MicrosoftDNS \_ MGType 類別</span><span class="sxs-lookup"><span data-stu-id="55503-105">MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="55503-106">代表郵件群組 (MG) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="55503-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Group (MG) record.</span></span>

<span data-ttu-id="55503-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="55503-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="55503-108">語法</span><span class="sxs-lookup"><span data-stu-id="55503-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a><span data-ttu-id="55503-109">成員</span><span class="sxs-lookup"><span data-stu-id="55503-109">Members</span></span>

<span data-ttu-id="55503-110">**MicrosoftDNS \_ MGType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="55503-110">The **MicrosoftDNS\_MGType** class has these types of members:</span></span>

-   [<span data-ttu-id="55503-111">方法</span><span class="sxs-lookup"><span data-stu-id="55503-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="55503-112">屬性</span><span class="sxs-lookup"><span data-stu-id="55503-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55503-113">方法</span><span class="sxs-lookup"><span data-stu-id="55503-113">Methods</span></span>

<span data-ttu-id="55503-114">**MicrosoftDNS \_ MGType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="55503-114">The **MicrosoftDNS\_MGType** class has these methods.</span></span>



| <span data-ttu-id="55503-115">方法</span><span class="sxs-lookup"><span data-stu-id="55503-115">Method</span></span>                             | <span data-ttu-id="55503-116">描述</span><span class="sxs-lookup"><span data-stu-id="55503-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55503-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="55503-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="55503-118">這個方法會根據方法的輸入參數中的資料具現化以 MG 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、郵件群組的擁有者名稱、類別 (預設值 = IN) 、存留時間值和信箱名稱。</span><span class="sxs-lookup"><span data-stu-id="55503-118">This method instantiates an MG Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail group, class (default = IN), time-to-live value and the mailbox name.</span></span> <span data-ttu-id="55503-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="55503-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="55503-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="55503-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="55503-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="55503-121">**Modify**</span></span>                         | <span data-ttu-id="55503-122">這個方法會將 TTL 和 MG 信箱更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="55503-122">This method updates the TTL and MG Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="55503-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="55503-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="55503-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="55503-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="55503-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="55503-125">Qualifiers: Implemented</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="55503-126">屬性</span><span class="sxs-lookup"><span data-stu-id="55503-126">Properties</span></span>

<span data-ttu-id="55503-127">**MicrosoftDNS \_ MGType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="55503-127">The **MicrosoftDNS\_MGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55503-128">**MGMailbox**</span><span class="sxs-lookup"><span data-stu-id="55503-128">**MGMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55503-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="55503-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55503-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55503-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55503-131">FQDN，指定隸屬于記錄擁有者名稱所指定之郵件群組成員的信箱。</span><span class="sxs-lookup"><span data-stu-id="55503-131">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55503-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="55503-132">Requirements</span></span>



| <span data-ttu-id="55503-133">需求</span><span class="sxs-lookup"><span data-stu-id="55503-133">Requirement</span></span> | <span data-ttu-id="55503-134">值</span><span class="sxs-lookup"><span data-stu-id="55503-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55503-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55503-135">Minimum supported client</span></span><br/> | <span data-ttu-id="55503-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="55503-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="55503-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55503-137">Minimum supported server</span></span><br/> | <span data-ttu-id="55503-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55503-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="55503-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="55503-139">Namespace</span></span><br/>                | <span data-ttu-id="55503-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="55503-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="55503-141">MOF</span><span class="sxs-lookup"><span data-stu-id="55503-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55503-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="55503-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55503-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55503-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55503-144">**MicrosoftDNS MGType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="55503-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="55503-145">**Modify MicrosoftDNS \_ MGType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="55503-145">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="55503-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="55503-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





