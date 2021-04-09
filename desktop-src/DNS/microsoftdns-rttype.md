---
title: MicrosoftDNS_RTType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示透過 (RT) 記錄的路由。
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- MicrosoftDNS_RTType 類別 DNS
- MicrosoftDNS_RTType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934527"
---
# <a name="microsoftdns_rttype-class"></a><span data-ttu-id="8201d-105">MicrosoftDNS \_ RTType 類別</span><span class="sxs-lookup"><span data-stu-id="8201d-105">MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="8201d-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示透過 (RT) 記錄的路由。</span><span class="sxs-lookup"><span data-stu-id="8201d-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Route Through (RT) record.</span></span>

<span data-ttu-id="8201d-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="8201d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8201d-108">語法</span><span class="sxs-lookup"><span data-stu-id="8201d-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a><span data-ttu-id="8201d-109">成員</span><span class="sxs-lookup"><span data-stu-id="8201d-109">Members</span></span>

<span data-ttu-id="8201d-110">**MicrosoftDNS \_ RTType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8201d-110">The **MicrosoftDNS\_RTType** class has these types of members:</span></span>

-   [<span data-ttu-id="8201d-111">方法</span><span class="sxs-lookup"><span data-stu-id="8201d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8201d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8201d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8201d-113">方法</span><span class="sxs-lookup"><span data-stu-id="8201d-113">Methods</span></span>

<span data-ttu-id="8201d-114">**MicrosoftDNS \_ RTType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8201d-114">The **MicrosoftDNS\_RTType** class has these methods.</span></span>



| <span data-ttu-id="8201d-115">方法</span><span class="sxs-lookup"><span data-stu-id="8201d-115">Method</span></span>                             | <span data-ttu-id="8201d-116">描述</span><span class="sxs-lookup"><span data-stu-id="8201d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8201d-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="8201d-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="8201d-118">根據方法的輸入參數中的資料具現化 RT 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者/主機名稱、類別 (預設值 = IN) 、存留時間值、記錄喜好設定和轉送主機名。</span><span class="sxs-lookup"><span data-stu-id="8201d-118">Instantiates an RT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/host Name, class (default = IN), time-to-live value, record preference and intermediate host name.</span></span> <span data-ttu-id="8201d-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="8201d-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="8201d-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="8201d-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="8201d-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="8201d-121">**Modify**</span></span>                         | <span data-ttu-id="8201d-122">將 TTL、喜好設定和轉送主機更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="8201d-122">Updates the TTL, Preference, and Intermediate Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="8201d-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="8201d-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="8201d-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="8201d-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="8201d-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="8201d-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="8201d-126">屬性</span><span class="sxs-lookup"><span data-stu-id="8201d-126">Properties</span></span>

<span data-ttu-id="8201d-127">**MicrosoftDNS \_ RTType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8201d-127">The **MicrosoftDNS\_RTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8201d-128">**IntermediateHost**</span><span class="sxs-lookup"><span data-stu-id="8201d-128">**IntermediateHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8201d-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8201d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8201d-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8201d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8201d-131">FQDN，指定主機做為中繼，以達到擁有者指定的主機。</span><span class="sxs-lookup"><span data-stu-id="8201d-131">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="8201d-132">**偏好**</span><span class="sxs-lookup"><span data-stu-id="8201d-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8201d-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8201d-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8201d-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8201d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8201d-135">在相同擁有者的其他專案中提供給此 RR 的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="8201d-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="8201d-136">偏好較低的值。</span><span class="sxs-lookup"><span data-stu-id="8201d-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8201d-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="8201d-137">Requirements</span></span>



| <span data-ttu-id="8201d-138">需求</span><span class="sxs-lookup"><span data-stu-id="8201d-138">Requirement</span></span> | <span data-ttu-id="8201d-139">值</span><span class="sxs-lookup"><span data-stu-id="8201d-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8201d-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8201d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8201d-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="8201d-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8201d-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8201d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8201d-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8201d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8201d-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="8201d-144">Namespace</span></span><br/>                | <span data-ttu-id="8201d-145">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8201d-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8201d-146">MOF</span><span class="sxs-lookup"><span data-stu-id="8201d-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8201d-147"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="8201d-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8201d-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8201d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8201d-149">**MicrosoftDNS RTType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="8201d-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8201d-150">**Modify MicrosoftDNS \_ RTType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="8201d-150">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="8201d-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8201d-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





