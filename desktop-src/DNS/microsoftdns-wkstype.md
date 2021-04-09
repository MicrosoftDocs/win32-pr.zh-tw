---
title: MicrosoftDNS_WKSType 類別
description: '\_代表 Well-Known 服務 (WKS) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- MicrosoftDNS_WKSType 類別 DNS
- MicrosoftDNS_WKSType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7fde08721bb8bb62b93f72b792060b06c15dad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934615"
---
# <a name="microsoftdns_wkstype-class"></a><span data-ttu-id="25baa-105">MicrosoftDNS \_ WKSType 類別</span><span class="sxs-lookup"><span data-stu-id="25baa-105">MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="25baa-106">代表 Well-Known 服務 (WKS) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="25baa-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Well-Known Services (WKS) record.</span></span>

<span data-ttu-id="25baa-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="25baa-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="25baa-108">語法</span><span class="sxs-lookup"><span data-stu-id="25baa-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a><span data-ttu-id="25baa-109">成員</span><span class="sxs-lookup"><span data-stu-id="25baa-109">Members</span></span>

<span data-ttu-id="25baa-110">**MicrosoftDNS \_ WKSType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="25baa-110">The **MicrosoftDNS\_WKSType** class has these types of members:</span></span>

-   [<span data-ttu-id="25baa-111">方法</span><span class="sxs-lookup"><span data-stu-id="25baa-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="25baa-112">屬性</span><span class="sxs-lookup"><span data-stu-id="25baa-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="25baa-113">方法</span><span class="sxs-lookup"><span data-stu-id="25baa-113">Methods</span></span>

<span data-ttu-id="25baa-114">**MicrosoftDNS \_ WKSType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="25baa-114">The **MicrosoftDNS\_WKSType** class has these methods.</span></span>



| <span data-ttu-id="25baa-115">方法</span><span class="sxs-lookup"><span data-stu-id="25baa-115">Method</span></span>                             | <span data-ttu-id="25baa-116">描述</span><span class="sxs-lookup"><span data-stu-id="25baa-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25baa-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="25baa-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="25baa-118">根據方法的輸入參數中的資料具現化 WKS 的 WKS 類型：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及擁有者的網際網路位址、IP 通訊協定和埠位遮罩。</span><span class="sxs-lookup"><span data-stu-id="25baa-118">Instantiates a WKS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the owner's Internet Address, IP protocol and port bit mask.</span></span> <span data-ttu-id="25baa-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="25baa-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="25baa-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="25baa-120">Qualifiers: Implemented, static</span></span><br/>  |
| <span data-ttu-id="25baa-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="25baa-121">**Modify**</span></span>                         | <span data-ttu-id="25baa-122">這個方法會將 TTL、網際網路位址、IP 通訊協定和服務，更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="25baa-122">This method updates the TTL, Internet Address, IP Protocol, and Services to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="25baa-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="25baa-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="25baa-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="25baa-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="25baa-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="25baa-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="25baa-126">屬性</span><span class="sxs-lookup"><span data-stu-id="25baa-126">Properties</span></span>

<span data-ttu-id="25baa-127">**MicrosoftDNS \_ WKSType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="25baa-127">The **MicrosoftDNS\_WKSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25baa-128">**InternetAddress**</span><span class="sxs-lookup"><span data-stu-id="25baa-128">**InternetAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25baa-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="25baa-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25baa-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25baa-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25baa-131">記錄擁有者的網際網路 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="25baa-131">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="25baa-132">**IPProtocol**</span><span class="sxs-lookup"><span data-stu-id="25baa-132">**IPProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25baa-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="25baa-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25baa-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25baa-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25baa-135">代表此記錄之 IP 通訊協定的字串。</span><span class="sxs-lookup"><span data-stu-id="25baa-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="25baa-136">有效的值為 UDP 或 TCP。</span><span class="sxs-lookup"><span data-stu-id="25baa-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="25baa-137">**服務**</span><span class="sxs-lookup"><span data-stu-id="25baa-137">**Services**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25baa-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="25baa-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25baa-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25baa-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25baa-140">字串，其中包含已知服務 (WKS) 記錄所使用的所有服務。</span><span class="sxs-lookup"><span data-stu-id="25baa-140">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25baa-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="25baa-141">Requirements</span></span>



| <span data-ttu-id="25baa-142">需求</span><span class="sxs-lookup"><span data-stu-id="25baa-142">Requirement</span></span> | <span data-ttu-id="25baa-143">值</span><span class="sxs-lookup"><span data-stu-id="25baa-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25baa-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25baa-144">Minimum supported client</span></span><br/> | <span data-ttu-id="25baa-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="25baa-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="25baa-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25baa-146">Minimum supported server</span></span><br/> | <span data-ttu-id="25baa-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25baa-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="25baa-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="25baa-148">Namespace</span></span><br/>                | <span data-ttu-id="25baa-149">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="25baa-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="25baa-150">MOF</span><span class="sxs-lookup"><span data-stu-id="25baa-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25baa-151"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="25baa-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25baa-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25baa-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25baa-153">**MicrosoftDNS WKSType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="25baa-153">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="25baa-154">**Modify MicrosoftDNS \_ WKSType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="25baa-154">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="25baa-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="25baa-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





