---
title: MicrosoftDNS_WINSType 類別
description: '\_代表 Windows 網際網路名稱服務 (WINS) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- MicrosoftDNS_WINSType 類別 DNS
- MicrosoftDNS_WINSType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843864"
---
# <a name="microsoftdns_winstype-class"></a><span data-ttu-id="5d458-105">MicrosoftDNS \_ WINSType 類別</span><span class="sxs-lookup"><span data-stu-id="5d458-105">MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="5d458-106">代表 Windows 網際網路名稱服務 (WINS) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="5d458-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Windows Internet Name Service (WINS) record.</span></span>

<span data-ttu-id="5d458-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="5d458-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d458-108">語法</span><span class="sxs-lookup"><span data-stu-id="5d458-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a><span data-ttu-id="5d458-109">成員</span><span class="sxs-lookup"><span data-stu-id="5d458-109">Members</span></span>

<span data-ttu-id="5d458-110">**MicrosoftDNS \_ WINSType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5d458-110">The **MicrosoftDNS\_WINSType** class has these types of members:</span></span>

-   [<span data-ttu-id="5d458-111">方法</span><span class="sxs-lookup"><span data-stu-id="5d458-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5d458-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5d458-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5d458-113">方法</span><span class="sxs-lookup"><span data-stu-id="5d458-113">Methods</span></span>

<span data-ttu-id="5d458-114">**MicrosoftDNS \_ WINSType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5d458-114">The **MicrosoftDNS\_WINSType** class has these methods.</span></span>



| <span data-ttu-id="5d458-115">方法</span><span class="sxs-lookup"><span data-stu-id="5d458-115">Method</span></span>                             | <span data-ttu-id="5d458-116">描述</span><span class="sxs-lookup"><span data-stu-id="5d458-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d458-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="5d458-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="5d458-118">根據方法的輸入參數中的資料具現化 WINS 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及 WINS 對應旗標、查閱超時、快取超時和 IP 位址清單以便查閱。</span><span class="sxs-lookup"><span data-stu-id="5d458-118">Instantiates a WINS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, look-up time out, cache time out and list of IP addresses for look up.</span></span> <span data-ttu-id="5d458-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="5d458-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="5d458-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="5d458-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="5d458-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="5d458-121">**Modify**</span></span>                         | <span data-ttu-id="5d458-122">將 TTL、對應旗標、查閱超時、快取超時和 Wins 伺服器更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="5d458-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Wins Servers to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="5d458-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="5d458-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="5d458-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="5d458-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="5d458-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="5d458-125">Qualifiers: Implemented</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="5d458-126">屬性</span><span class="sxs-lookup"><span data-stu-id="5d458-126">Properties</span></span>

<span data-ttu-id="5d458-127">**MicrosoftDNS \_ WINSType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5d458-127">The **MicrosoftDNS\_WINSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d458-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="5d458-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d458-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5d458-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d458-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d458-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d458-131">使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d458-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="5d458-132">**LookupTimeout**</span><span class="sxs-lookup"><span data-stu-id="5d458-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d458-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5d458-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d458-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d458-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d458-135">DNS 伺服器使用 WINS 查詢來嘗試解析的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d458-135">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="5d458-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="5d458-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d458-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5d458-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d458-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d458-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d458-139">WINS 對應旗標，指定是否必須將記錄包含在區域複寫中。</span><span class="sxs-lookup"><span data-stu-id="5d458-139">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="5d458-140">它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。</span><span class="sxs-lookup"><span data-stu-id="5d458-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="5d458-141">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="5d458-141">The following values are valid.</span></span>



| <span data-ttu-id="5d458-142">值</span><span class="sxs-lookup"><span data-stu-id="5d458-142">Value</span></span>                                                                                                                                               | <span data-ttu-id="5d458-143">意義</span><span class="sxs-lookup"><span data-stu-id="5d458-143">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="5d458-144"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="5d458-144"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="5d458-145">複寫旗標</span><span class="sxs-lookup"><span data-stu-id="5d458-145">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="5d458-146"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="5d458-146"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="5d458-147">無複寫 (本機記錄) 旗標</span><span class="sxs-lookup"><span data-stu-id="5d458-147">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5d458-148">**WinsServers**</span><span class="sxs-lookup"><span data-stu-id="5d458-148">**WinsServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d458-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5d458-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d458-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d458-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d458-151">WINS 查詢中使用之 WINS 伺服器的逗點分隔 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="5d458-151">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d458-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d458-152">Requirements</span></span>



| <span data-ttu-id="5d458-153">需求</span><span class="sxs-lookup"><span data-stu-id="5d458-153">Requirement</span></span> | <span data-ttu-id="5d458-154">值</span><span class="sxs-lookup"><span data-stu-id="5d458-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d458-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d458-155">Minimum supported client</span></span><br/> | <span data-ttu-id="5d458-156">都不支援</span><span class="sxs-lookup"><span data-stu-id="5d458-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5d458-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d458-157">Minimum supported server</span></span><br/> | <span data-ttu-id="5d458-158">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d458-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5d458-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="5d458-159">Namespace</span></span><br/>                | <span data-ttu-id="5d458-160">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="5d458-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5d458-161">MOF</span><span class="sxs-lookup"><span data-stu-id="5d458-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d458-162"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d458-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d458-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d458-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d458-164">**MicrosoftDNS WINSType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="5d458-164">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5d458-165">**Modify MicrosoftDNS \_ WINSType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="5d458-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="5d458-166">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5d458-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





