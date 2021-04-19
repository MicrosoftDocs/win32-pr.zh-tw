---
title: Modify MicrosoftDNS_AFSDBType 類別的方法
description: Modify 方法會更新 Andrew 檔案系統資料庫伺服器 (AFSDB) 資源記錄。
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_AFSDBType 類別
- MicrosoftDNS_AFSDBType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966113"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="1b4e8-106">Modify MicrosoftDNS \_ AFSDBType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="1b4e8-106">Modify method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="1b4e8-107">**Modify** 方法會更新 Andrew 檔案系統資料庫伺服器 (AFSDB) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-107">The **Modify** method updates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4e8-108">語法</span><span class="sxs-lookup"><span data-stu-id="1b4e8-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="1b4e8-109">參數</span><span class="sxs-lookup"><span data-stu-id="1b4e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4e8-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1b4e8-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e8-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e8-112">*子類型* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1b4e8-112">*Subtype* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e8-113">主機 AFS 伺服器的子類型。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-113">Subtype of the host AFS server.</span></span> <span data-ttu-id="1b4e8-114">針對子類型 1 (值 = 1) ，主機具有適用于已命名 AFS 資料格的 AFS 3.0 磁片區位置伺服器。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-114">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="1b4e8-115">在子類型 2 (值 = 2) 的情況下，主機會有經過驗證的名稱伺服器，保留命名的 DCE/NCA 資料格的資料格根目錄節點。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-115">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e8-116">*ServerName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1b4e8-116">*ServerName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e8-117">FQDN 指定主機，該主機的擁有者名稱中指定的 AFS 資料格具有伺服器。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-117">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e8-118">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="1b4e8-118">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e8-119">修改過之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-119">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4e8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b4e8-120">Return value</span></span>

<span data-ttu-id="1b4e8-121">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b4e8-122">備註</span><span class="sxs-lookup"><span data-stu-id="1b4e8-122">Remarks</span></span>

<span data-ttu-id="1b4e8-123">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-123">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4e8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b4e8-124">Requirements</span></span>



| <span data-ttu-id="1b4e8-125">需求</span><span class="sxs-lookup"><span data-stu-id="1b4e8-125">Requirement</span></span> | <span data-ttu-id="1b4e8-126">值</span><span class="sxs-lookup"><span data-stu-id="1b4e8-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4e8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b4e8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4e8-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="1b4e8-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1b4e8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b4e8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4e8-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b4e8-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1b4e8-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="1b4e8-131">Namespace</span></span><br/>                | <span data-ttu-id="1b4e8-132">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="1b4e8-132">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="1b4e8-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1b4e8-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b4e8-134"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b4e8-134"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b4e8-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b4e8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4e8-136">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="1b4e8-136">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="1b4e8-137">**MicrosoftDNS AFSDBType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="1b4e8-137">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="1b4e8-138">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="1b4e8-138">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





