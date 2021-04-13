---
title: MicrosoftDNS_WINSRType 類別
description: '\_代表 WINS 反向查閱 (WINSR) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- MicrosoftDNS_WINSRType 類別 DNS
- MicrosoftDNS_WINSRType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9500c6a36a1c3a7cc243f1cbcfbc0edca6cecf2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385202"
---
# <a name="microsoftdns_winsrtype-class"></a><span data-ttu-id="13e33-105">MicrosoftDNS \_ WINSRType 類別</span><span class="sxs-lookup"><span data-stu-id="13e33-105">MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="13e33-106">代表 WINS 反向查閱 (WINSR) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="13e33-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a WINS Reverse Look-up (WINSR) record.</span></span>

<span data-ttu-id="13e33-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="13e33-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e33-108">語法</span><span class="sxs-lookup"><span data-stu-id="13e33-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a><span data-ttu-id="13e33-109">成員</span><span class="sxs-lookup"><span data-stu-id="13e33-109">Members</span></span>

<span data-ttu-id="13e33-110">**MicrosoftDNS \_ WINSRType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13e33-110">The **MicrosoftDNS\_WINSRType** class has these types of members:</span></span>

-   [<span data-ttu-id="13e33-111">方法</span><span class="sxs-lookup"><span data-stu-id="13e33-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="13e33-112">屬性</span><span class="sxs-lookup"><span data-stu-id="13e33-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="13e33-113">方法</span><span class="sxs-lookup"><span data-stu-id="13e33-113">Methods</span></span>

<span data-ttu-id="13e33-114">**MicrosoftDNS \_ WINSRType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="13e33-114">The **MicrosoftDNS\_WINSRType** class has these methods.</span></span>



| <span data-ttu-id="13e33-115">方法</span><span class="sxs-lookup"><span data-stu-id="13e33-115">Method</span></span>                             | <span data-ttu-id="13e33-116">描述</span><span class="sxs-lookup"><span data-stu-id="13e33-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e33-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="13e33-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="13e33-118">根據方法的輸入參數中的資料來具現化 WINSR 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及 WINS 對應旗標、反向查閱超時、WINS 快取超時和要附加的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="13e33-118">Instantiates a WINSR Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="13e33-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="13e33-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="13e33-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="13e33-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="13e33-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="13e33-121">**Modify**</span></span>                         | <span data-ttu-id="13e33-122">將 TTL、對應旗標、查閱超時、快取超時和結果網域更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="13e33-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="13e33-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="13e33-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="13e33-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="13e33-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="13e33-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="13e33-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="13e33-126">屬性</span><span class="sxs-lookup"><span data-stu-id="13e33-126">Properties</span></span>

<span data-ttu-id="13e33-127">**MicrosoftDNS \_ WINSRType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="13e33-127">The **MicrosoftDNS\_WINSRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13e33-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="13e33-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13e33-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="13e33-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13e33-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13e33-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13e33-131">使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="13e33-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="13e33-132">**LookupTimeout**</span><span class="sxs-lookup"><span data-stu-id="13e33-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13e33-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="13e33-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13e33-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13e33-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13e33-135">使用 WINS 反向查閱之 DNS 伺服器的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="13e33-135">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="13e33-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="13e33-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13e33-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="13e33-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13e33-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13e33-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13e33-139">WINSR 對應旗標，指定是否必須將記錄包含在區域複寫中。</span><span class="sxs-lookup"><span data-stu-id="13e33-139">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="13e33-140">它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。</span><span class="sxs-lookup"><span data-stu-id="13e33-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="13e33-141">**ResultDomain**</span><span class="sxs-lookup"><span data-stu-id="13e33-141">**ResultDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13e33-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13e33-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13e33-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13e33-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13e33-144">要附加至所傳回 NetBIOS 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="13e33-144">Domain name to append to returned NetBIOS names.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13e33-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="13e33-145">Requirements</span></span>



| <span data-ttu-id="13e33-146">需求</span><span class="sxs-lookup"><span data-stu-id="13e33-146">Requirement</span></span> | <span data-ttu-id="13e33-147">值</span><span class="sxs-lookup"><span data-stu-id="13e33-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13e33-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13e33-148">Minimum supported client</span></span><br/> | <span data-ttu-id="13e33-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="13e33-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="13e33-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13e33-150">Minimum supported server</span></span><br/> | <span data-ttu-id="13e33-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13e33-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13e33-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="13e33-152">Namespace</span></span><br/>                | <span data-ttu-id="13e33-153">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="13e33-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="13e33-154">MOF</span><span class="sxs-lookup"><span data-stu-id="13e33-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13e33-155"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="13e33-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e33-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13e33-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e33-157">**MicrosoftDNS WINSRType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="13e33-157">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="13e33-158">**Modify MicrosoftDNS \_ WINSRType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="13e33-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="13e33-159">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="13e33-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





