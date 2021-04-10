---
title: MicrosoftDNS_NXTType 類別
description: '\_表示下一個 (NXT) RR 的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- MicrosoftDNS_NXTType 類別 DNS
- MicrosoftDNS_NXTType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79db82b3ae760c31d4e6fef80eb01469cb2bb41d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104165"
---
# <a name="microsoftdns_nxttype-class"></a><span data-ttu-id="87b24-105">MicrosoftDNS \_ NXTType 類別</span><span class="sxs-lookup"><span data-stu-id="87b24-105">MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="87b24-106">表示下一個 (NXT) RR 的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="87b24-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Next (NXT) RR.</span></span>

<span data-ttu-id="87b24-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="87b24-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b24-108">語法</span><span class="sxs-lookup"><span data-stu-id="87b24-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a><span data-ttu-id="87b24-109">成員</span><span class="sxs-lookup"><span data-stu-id="87b24-109">Members</span></span>

<span data-ttu-id="87b24-110">**MicrosoftDNS \_ NXTType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="87b24-110">The **MicrosoftDNS\_NXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="87b24-111">方法</span><span class="sxs-lookup"><span data-stu-id="87b24-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="87b24-112">屬性</span><span class="sxs-lookup"><span data-stu-id="87b24-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="87b24-113">方法</span><span class="sxs-lookup"><span data-stu-id="87b24-113">Methods</span></span>

<span data-ttu-id="87b24-114">**MicrosoftDNS \_ NXTType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="87b24-114">The **MicrosoftDNS\_NXTType** class has these methods.</span></span>



| <span data-ttu-id="87b24-115">方法</span><span class="sxs-lookup"><span data-stu-id="87b24-115">Method</span></span>                             | <span data-ttu-id="87b24-116">描述</span><span class="sxs-lookup"><span data-stu-id="87b24-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b24-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="87b24-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="87b24-118">根據方法的輸入參數中的資料具現化 NXT 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設 = IN) 、存留時間值，以及 WINS 對應旗標、反向查閱超時、WINS 快取超時，以及要附加的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="87b24-118">Instantiates an NXT Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out, and domain name to append.</span></span> <span data-ttu-id="87b24-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="87b24-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="87b24-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="87b24-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="87b24-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="87b24-121">**Modify**</span></span>                         | <span data-ttu-id="87b24-122">將 TTL、對應旗標、查閱超時、快取超時和結果網域更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="87b24-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="87b24-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="87b24-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="87b24-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="87b24-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="87b24-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="87b24-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="87b24-126">**Windows Server 2003：** 這個方法也會將 NextDomainName 和類型更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="87b24-126">**Windows Server 2003:** This method also updates the NextDomainName and Types to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="87b24-127">屬性</span><span class="sxs-lookup"><span data-stu-id="87b24-127">Properties</span></span>

<span data-ttu-id="87b24-128">**MicrosoftDNS \_ NXTType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="87b24-128">The **MicrosoftDNS\_NXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87b24-129">**NextDomainName**</span><span class="sxs-lookup"><span data-stu-id="87b24-129">**NextDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87b24-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="87b24-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87b24-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87b24-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87b24-132">下一個功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="87b24-132">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="87b24-133">**類型**</span><span class="sxs-lookup"><span data-stu-id="87b24-133">**Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87b24-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="87b24-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87b24-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87b24-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87b24-136">針對 NXT 資源記錄的擁有者名稱，以空格分隔的 RR 類型助憶鍵清單。</span><span class="sxs-lookup"><span data-stu-id="87b24-136">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87b24-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="87b24-137">Requirements</span></span>



| <span data-ttu-id="87b24-138">需求</span><span class="sxs-lookup"><span data-stu-id="87b24-138">Requirement</span></span> | <span data-ttu-id="87b24-139">值</span><span class="sxs-lookup"><span data-stu-id="87b24-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87b24-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87b24-140">Minimum supported client</span></span><br/> | <span data-ttu-id="87b24-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="87b24-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="87b24-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87b24-142">Minimum supported server</span></span><br/> | <span data-ttu-id="87b24-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87b24-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87b24-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="87b24-144">Namespace</span></span><br/>                | <span data-ttu-id="87b24-145">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="87b24-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="87b24-146">MOF</span><span class="sxs-lookup"><span data-stu-id="87b24-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87b24-147"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="87b24-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87b24-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87b24-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b24-149">**MicrosoftDNS NXTType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="87b24-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="87b24-150">**Modify MicrosoftDNS \_ NXTType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="87b24-150">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="87b24-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="87b24-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





