---
title: MicrosoftDNS_MDType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，代表網域 (MD) 記錄的郵件代理程式。
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- MicrosoftDNS_MDType 類別 DNS
- MicrosoftDNS_MDType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843536"
---
# <a name="microsoftdns_mdtype-class"></a><span data-ttu-id="98506-105">MicrosoftDNS \_ MDType 類別</span><span class="sxs-lookup"><span data-stu-id="98506-105">MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="98506-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，代表網域 (MD) 記錄的郵件代理程式。</span><span class="sxs-lookup"><span data-stu-id="98506-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Agent for Domain (MD) record.</span></span>

<span data-ttu-id="98506-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="98506-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="98506-108">語法</span><span class="sxs-lookup"><span data-stu-id="98506-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a><span data-ttu-id="98506-109">成員</span><span class="sxs-lookup"><span data-stu-id="98506-109">Members</span></span>

<span data-ttu-id="98506-110">**MicrosoftDNS \_ MDType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="98506-110">The **MicrosoftDNS\_MDType** class has these types of members:</span></span>

-   [<span data-ttu-id="98506-111">方法</span><span class="sxs-lookup"><span data-stu-id="98506-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="98506-112">屬性</span><span class="sxs-lookup"><span data-stu-id="98506-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98506-113">方法</span><span class="sxs-lookup"><span data-stu-id="98506-113">Methods</span></span>

<span data-ttu-id="98506-114">**MicrosoftDNS \_ MDType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="98506-114">The **MicrosoftDNS\_MDType** class has these methods.</span></span>



| <span data-ttu-id="98506-115">方法</span><span class="sxs-lookup"><span data-stu-id="98506-115">Method</span></span>                             | <span data-ttu-id="98506-116">描述</span><span class="sxs-lookup"><span data-stu-id="98506-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98506-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="98506-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="98506-118">根據方法的輸入參數中的資料具現化 DNS MD 資源記錄：記錄的 DNS 伺服器名稱、網域的擁有者名稱、類別 (預設值 = IN) 、存留時間值和郵件代理程式的主機。</span><span class="sxs-lookup"><span data-stu-id="98506-118">Instantiates a DNS MD Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="98506-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="98506-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="98506-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="98506-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="98506-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="98506-121">**Modify**</span></span>                         | <span data-ttu-id="98506-122">將 TTL 和 MD 主機更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="98506-122">Updates the TTL and MD host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="98506-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="98506-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="98506-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="98506-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="98506-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="98506-125">Qualifiers: Implemented</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="98506-126">屬性</span><span class="sxs-lookup"><span data-stu-id="98506-126">Properties</span></span>

<span data-ttu-id="98506-127">**MicrosoftDNS \_ MDType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="98506-127">The **MicrosoftDNS\_MDType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98506-128">**MDHost**</span><span class="sxs-lookup"><span data-stu-id="98506-128">**MDHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98506-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="98506-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98506-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="98506-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98506-131">FQDN，指定具有可傳遞郵件給指定網域之郵件代理程式的主機。</span><span class="sxs-lookup"><span data-stu-id="98506-131">FQDN that specifies a host with a mail agent capable of delivering mail for the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98506-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="98506-132">Requirements</span></span>



| <span data-ttu-id="98506-133">需求</span><span class="sxs-lookup"><span data-stu-id="98506-133">Requirement</span></span> | <span data-ttu-id="98506-134">值</span><span class="sxs-lookup"><span data-stu-id="98506-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98506-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98506-135">Minimum supported client</span></span><br/> | <span data-ttu-id="98506-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="98506-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="98506-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98506-137">Minimum supported server</span></span><br/> | <span data-ttu-id="98506-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98506-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="98506-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="98506-139">Namespace</span></span><br/>                | <span data-ttu-id="98506-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="98506-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="98506-141">MOF</span><span class="sxs-lookup"><span data-stu-id="98506-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98506-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="98506-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98506-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98506-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98506-144">**MicrosoftDNS MDType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="98506-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="98506-145">**Modify MicrosoftDNS \_ MDType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="98506-145">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="98506-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="98506-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





