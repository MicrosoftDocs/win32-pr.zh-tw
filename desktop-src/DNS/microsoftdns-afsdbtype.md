---
title: MicrosoftDNS_AFSDBType 類別
description: '\_代表 Andrew 檔案系統資料庫伺服器 (AFSDB) 記錄之 MicrosoftDNS ResourceRecord 的子類別。'
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- MicrosoftDNS_AFSDBType 類別 DNS
- MicrosoftDNS_AFSDBType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025112"
---
# <a name="microsoftdns_afsdbtype-class"></a><span data-ttu-id="be4b4-105">MicrosoftDNS \_ AFSDBType 類別</span><span class="sxs-lookup"><span data-stu-id="be4b4-105">MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="be4b4-106">代表 Andrew 檔案系統資料庫伺服器 (AFSDB) 記錄之 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 的子類別。</span><span class="sxs-lookup"><span data-stu-id="be4b4-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an Andrew File System Database Server (AFSDB) record.</span></span>

<span data-ttu-id="be4b4-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="be4b4-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="be4b4-108">語法</span><span class="sxs-lookup"><span data-stu-id="be4b4-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a><span data-ttu-id="be4b4-109">成員</span><span class="sxs-lookup"><span data-stu-id="be4b4-109">Members</span></span>

<span data-ttu-id="be4b4-110">**MicrosoftDNS \_ AFSDBType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="be4b4-110">The **MicrosoftDNS\_AFSDBType** class has these types of members:</span></span>

-   [<span data-ttu-id="be4b4-111">方法</span><span class="sxs-lookup"><span data-stu-id="be4b4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="be4b4-112">屬性</span><span class="sxs-lookup"><span data-stu-id="be4b4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="be4b4-113">方法</span><span class="sxs-lookup"><span data-stu-id="be4b4-113">Methods</span></span>

<span data-ttu-id="be4b4-114">**MicrosoftDNS \_ AFSDBType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="be4b4-114">The **MicrosoftDNS\_AFSDBType** class has these methods.</span></span>



| <span data-ttu-id="be4b4-115">方法</span><span class="sxs-lookup"><span data-stu-id="be4b4-115">Method</span></span>                             | <span data-ttu-id="be4b4-116">描述</span><span class="sxs-lookup"><span data-stu-id="be4b4-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be4b4-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="be4b4-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="be4b4-118">根據方法的輸入參數中的資料具現化 AFSDB 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者/資料格名稱、類別 (預設值 = IN) 、存留時間值，以及主機 AFS 伺服器子類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="be4b4-118">Instantiates an AFSDB Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Cell Name, class (default = IN), time-to-live value, and host AFS server subtype and name.</span></span> <span data-ttu-id="be4b4-119">將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="be4b4-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="be4b4-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="be4b4-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="be4b4-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="be4b4-121">**Modify**</span></span>                         | <span data-ttu-id="be4b4-122">這個方法會將 TTL、子類型和伺服器名稱更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="be4b4-122">This method updates the TTL, Subtype and Server Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="be4b4-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="be4b4-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="be4b4-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="be4b4-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="be4b4-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="be4b4-125">Qualifiers: Implemented</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="be4b4-126">屬性</span><span class="sxs-lookup"><span data-stu-id="be4b4-126">Properties</span></span>

<span data-ttu-id="be4b4-127">**MicrosoftDNS \_ AFSDBType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="be4b4-127">The **MicrosoftDNS\_AFSDBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be4b4-128">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="be4b4-128">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be4b4-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="be4b4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be4b4-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="be4b4-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be4b4-131">FQDN 指定主機，該主機的擁有者名稱中指定的 AFS 資料格具有伺服器。</span><span class="sxs-lookup"><span data-stu-id="be4b4-131">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="be4b4-132">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="be4b4-132">**Subtype**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be4b4-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="be4b4-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be4b4-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="be4b4-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be4b4-135">主機 AFS 伺服器的子類型。</span><span class="sxs-lookup"><span data-stu-id="be4b4-135">Subtype of the host AFS server.</span></span> <span data-ttu-id="be4b4-136">針對子類型 1 (值 = 1) ，主機具有適用于已命名 AFS 資料格的 AFS 3.0 磁片區位置伺服器。</span><span class="sxs-lookup"><span data-stu-id="be4b4-136">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="be4b4-137">在子類型 2 (值 = 2) 的情況下，主機會有經過驗證的名稱伺服器，保留命名的 DCE/NCA 資料格的資料格根目錄節點。</span><span class="sxs-lookup"><span data-stu-id="be4b4-137">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be4b4-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="be4b4-138">Requirements</span></span>



| <span data-ttu-id="be4b4-139">需求</span><span class="sxs-lookup"><span data-stu-id="be4b4-139">Requirement</span></span> | <span data-ttu-id="be4b4-140">值</span><span class="sxs-lookup"><span data-stu-id="be4b4-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be4b4-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be4b4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="be4b4-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="be4b4-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be4b4-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be4b4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="be4b4-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be4b4-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="be4b4-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="be4b4-145">Namespace</span></span><br/>                | <span data-ttu-id="be4b4-146">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="be4b4-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="be4b4-147">MOF</span><span class="sxs-lookup"><span data-stu-id="be4b4-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be4b4-148"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="be4b4-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be4b4-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be4b4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4b4-150">**MicrosoftDNS AFSDBType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="be4b4-150">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="be4b4-151">**Modify MicrosoftDNS \_ AFSDBType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="be4b4-151">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="be4b4-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="be4b4-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





