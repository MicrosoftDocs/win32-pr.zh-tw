---
title: MicrosoftDNS_CNAMEType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示 (CNAME) 記錄的標準名稱。
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- MicrosoftDNS_CNAMEType 類別 DNS
- MicrosoftDNS_CNAMEType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dca8729c2c750e1cef774b5f0f3eadc3e2f6fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843592"
---
# <a name="microsoftdns_cnametype-class"></a><span data-ttu-id="78430-105">MicrosoftDNS \_ CNAMEType 類別</span><span class="sxs-lookup"><span data-stu-id="78430-105">MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="78430-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示 (CNAME) 記錄的標準名稱。</span><span class="sxs-lookup"><span data-stu-id="78430-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Canonical Name (CNAME) record.</span></span>

<span data-ttu-id="78430-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="78430-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="78430-108">語法</span><span class="sxs-lookup"><span data-stu-id="78430-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a><span data-ttu-id="78430-109">成員</span><span class="sxs-lookup"><span data-stu-id="78430-109">Members</span></span>

<span data-ttu-id="78430-110">**MicrosoftDNS \_ CNAMEType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="78430-110">The **MicrosoftDNS\_CNAMEType** class has these types of members:</span></span>

-   [<span data-ttu-id="78430-111">方法</span><span class="sxs-lookup"><span data-stu-id="78430-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="78430-112">屬性</span><span class="sxs-lookup"><span data-stu-id="78430-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78430-113">方法</span><span class="sxs-lookup"><span data-stu-id="78430-113">Methods</span></span>

<span data-ttu-id="78430-114">**MicrosoftDNS \_ CNAMEType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="78430-114">The **MicrosoftDNS\_CNAMEType** class has these methods.</span></span>



| <span data-ttu-id="78430-115">方法</span><span class="sxs-lookup"><span data-stu-id="78430-115">Method</span></span>                             | <span data-ttu-id="78430-116">描述</span><span class="sxs-lookup"><span data-stu-id="78430-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78430-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="78430-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="78430-118">根據方法的輸入參數中的資料具現化 CNAME 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及 CNAME 記錄的主要名稱。</span><span class="sxs-lookup"><span data-stu-id="78430-118">Instantiates a CNAME Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the primary name of the CNAME record.</span></span> <span data-ttu-id="78430-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="78430-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="78430-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="78430-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="78430-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="78430-121">**Modify**</span></span>                         | <span data-ttu-id="78430-122">將 TTL 和主要名稱更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="78430-122">Updates the TTL and Primary Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="78430-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="78430-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="78430-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="78430-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="78430-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="78430-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="78430-126">屬性</span><span class="sxs-lookup"><span data-stu-id="78430-126">Properties</span></span>

<span data-ttu-id="78430-127">**MicrosoftDNS \_ CNAMEType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="78430-127">The **MicrosoftDNS\_CNAMEType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78430-128">**PrimaryName**</span><span class="sxs-lookup"><span data-stu-id="78430-128">**PrimaryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78430-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78430-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78430-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78430-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78430-131">CNAME 記錄擁有者的標準或主要名稱。</span><span class="sxs-lookup"><span data-stu-id="78430-131">Canonical, or primary name for the owner of the CNAME record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78430-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="78430-132">Requirements</span></span>



| <span data-ttu-id="78430-133">需求</span><span class="sxs-lookup"><span data-stu-id="78430-133">Requirement</span></span> | <span data-ttu-id="78430-134">值</span><span class="sxs-lookup"><span data-stu-id="78430-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78430-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78430-135">Minimum supported client</span></span><br/> | <span data-ttu-id="78430-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="78430-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="78430-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78430-137">Minimum supported server</span></span><br/> | <span data-ttu-id="78430-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78430-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="78430-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="78430-139">Namespace</span></span><br/>                | <span data-ttu-id="78430-140">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="78430-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="78430-141">MOF</span><span class="sxs-lookup"><span data-stu-id="78430-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78430-142"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="78430-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78430-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78430-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78430-144">**MicrosoftDNS CNAMEType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="78430-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="78430-145">**Modify MicrosoftDNS \_ CNAMEType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="78430-145">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="78430-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="78430-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





