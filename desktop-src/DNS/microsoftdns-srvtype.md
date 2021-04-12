---
title: MicrosoftDNS_SRVType 類別
description: '\_代表服務 (SRV) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- MicrosoftDNS_SRVType 類別 DNS
- MicrosoftDNS_SRVType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465673"
---
# <a name="microsoftdns_srvtype-class"></a><span data-ttu-id="36044-105">MicrosoftDNS \_ SRVType 類別</span><span class="sxs-lookup"><span data-stu-id="36044-105">MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="36044-106">代表服務 (SRV) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="36044-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Service (SRV) record.</span></span>

<span data-ttu-id="36044-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="36044-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="36044-108">語法</span><span class="sxs-lookup"><span data-stu-id="36044-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a><span data-ttu-id="36044-109">成員</span><span class="sxs-lookup"><span data-stu-id="36044-109">Members</span></span>

<span data-ttu-id="36044-110">**MicrosoftDNS \_ SRVType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="36044-110">The **MicrosoftDNS\_SRVType** class has these types of members:</span></span>

-   [<span data-ttu-id="36044-111">方法</span><span class="sxs-lookup"><span data-stu-id="36044-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="36044-112">屬性</span><span class="sxs-lookup"><span data-stu-id="36044-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="36044-113">方法</span><span class="sxs-lookup"><span data-stu-id="36044-113">Methods</span></span>

<span data-ttu-id="36044-114">**MicrosoftDNS \_ SRVType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="36044-114">The **MicrosoftDNS\_SRVType** class has these methods.</span></span>



| <span data-ttu-id="36044-115">方法</span><span class="sxs-lookup"><span data-stu-id="36044-115">Method</span></span>                             | <span data-ttu-id="36044-116">描述</span><span class="sxs-lookup"><span data-stu-id="36044-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36044-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="36044-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="36044-118">根據方法的輸入參數中的資料具現化 SRV 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者/目標名稱、類別 (預設值 = IN) 、存留時間值，以及目標主機的優先順序、權數、埠和功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="36044-118">Instantiates an SRV Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/target Name, class (default = IN), time-to-live value, and target host's priority, weight, port, and domain name.</span></span> <span data-ttu-id="36044-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="36044-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="36044-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="36044-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="36044-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="36044-121">**Modify**</span></span>                         | <span data-ttu-id="36044-122">將 TTL、優先順序、權數、埠和功能變數名稱更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="36044-122">Updates the TTL, Priority, Weight, Port, and Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="36044-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="36044-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="36044-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="36044-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="36044-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="36044-125">Qualifiers: Implemented</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="36044-126">屬性</span><span class="sxs-lookup"><span data-stu-id="36044-126">Properties</span></span>

<span data-ttu-id="36044-127">**MicrosoftDNS \_ SRVType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="36044-127">The **MicrosoftDNS\_SRVType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36044-128">**通訊埠**</span><span class="sxs-lookup"><span data-stu-id="36044-128">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36044-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="36044-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36044-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36044-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36044-131">通訊協定服務的目標主機上所使用的埠。</span><span class="sxs-lookup"><span data-stu-id="36044-131">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="36044-132">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="36044-132">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36044-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="36044-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36044-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36044-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36044-135">擁有者名稱中指定的目標主機優先權。</span><span class="sxs-lookup"><span data-stu-id="36044-135">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="36044-136">數位下限表示較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="36044-136">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="36044-137">**SRVDomainName**</span><span class="sxs-lookup"><span data-stu-id="36044-137">**SRVDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36044-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36044-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36044-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36044-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36044-140">目標主機的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="36044-140">FQDN of the target host.</span></span> <span data-ttu-id="36044-141">的目標 \\ 。 \\ 表示此網域無法使用由於原子服務。</span><span class="sxs-lookup"><span data-stu-id="36044-141">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="36044-142">**Weight**</span><span class="sxs-lookup"><span data-stu-id="36044-142">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36044-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="36044-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36044-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36044-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36044-145">目標主機的加權。</span><span class="sxs-lookup"><span data-stu-id="36044-145">Weight of the target host.</span></span> <span data-ttu-id="36044-146">在具有相同優先順序的主機之間進行選取時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="36044-146">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="36044-147">使用此主機的機率應與其權數成正比。</span><span class="sxs-lookup"><span data-stu-id="36044-147">The chances of using this host should be proportional to its weight.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36044-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="36044-148">Requirements</span></span>



| <span data-ttu-id="36044-149">需求</span><span class="sxs-lookup"><span data-stu-id="36044-149">Requirement</span></span> | <span data-ttu-id="36044-150">值</span><span class="sxs-lookup"><span data-stu-id="36044-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36044-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36044-151">Minimum supported client</span></span><br/> | <span data-ttu-id="36044-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="36044-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="36044-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36044-153">Minimum supported server</span></span><br/> | <span data-ttu-id="36044-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36044-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="36044-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="36044-155">Namespace</span></span><br/>                | <span data-ttu-id="36044-156">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="36044-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="36044-157">MOF</span><span class="sxs-lookup"><span data-stu-id="36044-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36044-158"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="36044-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36044-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36044-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36044-160">**MicrosoftDNS SRVType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="36044-160">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="36044-161">**Modify MicrosoftDNS \_ SRVType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="36044-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="36044-162">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="36044-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





