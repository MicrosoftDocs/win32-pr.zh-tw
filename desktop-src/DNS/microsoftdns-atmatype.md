---
title: MicrosoftDNS_ATMAType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示用來命名 (ATMA) 記錄的 ATM 位址。
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- MicrosoftDNS_ATMAType 類別 DNS
- MicrosoftDNS_ATMAType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934382"
---
# <a name="microsoftdns_atmatype-class"></a><span data-ttu-id="b0037-105">MicrosoftDNS \_ ATMAType 類別</span><span class="sxs-lookup"><span data-stu-id="b0037-105">MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="b0037-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示用來命名 (ATMA) 記錄的 ATM 位址。</span><span class="sxs-lookup"><span data-stu-id="b0037-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ATM Address to Name (ATMA) record.</span></span>

<span data-ttu-id="b0037-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="b0037-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0037-108">語法</span><span class="sxs-lookup"><span data-stu-id="b0037-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a><span data-ttu-id="b0037-109">成員</span><span class="sxs-lookup"><span data-stu-id="b0037-109">Members</span></span>

<span data-ttu-id="b0037-110">**MicrosoftDNS \_ ATMAType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b0037-110">The **MicrosoftDNS\_ATMAType** class has these types of members:</span></span>

-   [<span data-ttu-id="b0037-111">方法</span><span class="sxs-lookup"><span data-stu-id="b0037-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b0037-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b0037-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b0037-113">方法</span><span class="sxs-lookup"><span data-stu-id="b0037-113">Methods</span></span>

<span data-ttu-id="b0037-114">**MicrosoftDNS \_ ATMAType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b0037-114">The **MicrosoftDNS\_ATMAType** class has these methods.</span></span>



| <span data-ttu-id="b0037-115">方法</span><span class="sxs-lookup"><span data-stu-id="b0037-115">Method</span></span>                             | <span data-ttu-id="b0037-116">描述</span><span class="sxs-lookup"><span data-stu-id="b0037-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0037-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="b0037-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="b0037-118">根據方法的輸入參數中的資料具現化 ATMA 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者/節點名稱、類別 (預設值 = IN) 、存留時間值，以及 ATM 格式和位址。</span><span class="sxs-lookup"><span data-stu-id="b0037-118">Instantiates an ATMA Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Node Name, class (default = IN), time-to-live value, and ATM format and address.</span></span> <span data-ttu-id="b0037-119">將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="b0037-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="b0037-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="b0037-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="b0037-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="b0037-121">**Modify**</span></span>                         | <span data-ttu-id="b0037-122">將 TTL、格式和 ATMA 位址更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="b0037-122">Updates the TTL, Format and ATMA Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="b0037-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="b0037-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="b0037-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="b0037-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="b0037-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="b0037-125">Qualifiers: Implemented</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="b0037-126">屬性</span><span class="sxs-lookup"><span data-stu-id="b0037-126">Properties</span></span>

<span data-ttu-id="b0037-127">**MicrosoftDNS \_ ATMAType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b0037-127">The **MicrosoftDNS\_ATMAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0037-128">**ATMAddress**</span><span class="sxs-lookup"><span data-stu-id="b0037-128">**ATMAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0037-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0037-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0037-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0037-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0037-131">包含此 RR 所屬節點/擁有者之 ATM 位址的八位變數長度字串。</span><span class="sxs-lookup"><span data-stu-id="b0037-131">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="b0037-132">陣列的前4個位元組會用來儲存八位字串的大小。</span><span class="sxs-lookup"><span data-stu-id="b0037-132">The first 4 bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="b0037-133">最重要的位元組會儲存在位元組0中。</span><span class="sxs-lookup"><span data-stu-id="b0037-133">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="b0037-134">**格式**</span><span class="sxs-lookup"><span data-stu-id="b0037-134">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0037-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0037-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0037-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0037-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0037-137">ATM 位址格式。</span><span class="sxs-lookup"><span data-stu-id="b0037-137">ATM address format.</span></span> <span data-ttu-id="b0037-138">有效的值為：0，表示 ATM 終端系統位址 (AESA) 格式，1表示格式為164。</span><span class="sxs-lookup"><span data-stu-id="b0037-138">Valid values are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0037-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0037-139">Requirements</span></span>



| <span data-ttu-id="b0037-140">需求</span><span class="sxs-lookup"><span data-stu-id="b0037-140">Requirement</span></span> | <span data-ttu-id="b0037-141">值</span><span class="sxs-lookup"><span data-stu-id="b0037-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0037-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0037-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b0037-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="b0037-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b0037-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0037-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b0037-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0037-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b0037-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="b0037-146">Namespace</span></span><br/>                | <span data-ttu-id="b0037-147">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="b0037-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b0037-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b0037-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0037-149"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0037-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0037-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0037-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0037-151">**MicrosoftDNS ATMAType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="b0037-151">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b0037-152">**Modify MicrosoftDNS \_ ATMAType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="b0037-152">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="b0037-153">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="b0037-153">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





