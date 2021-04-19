---
description: 提供對憑證的「擴充金鑰使用方法」 (EKU) 屬性的唯讀存取權。
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: ExtendedKeyUsage 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994990"
---
# <a name="extendedkeyusage-object"></a><span data-ttu-id="7065c-103">ExtendedKeyUsage 物件</span><span class="sxs-lookup"><span data-stu-id="7065c-103">ExtendedKeyUsage object</span></span>

<span data-ttu-id="7065c-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7065c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7065c-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="7065c-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7065c-106">**ExtendedKeyUsage** 物件提供對憑證的「擴充金鑰使用方法」 (EKU) 屬性的唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="7065c-106">The **ExtendedKeyUsage** object provides read-only access to the extended key usage (EKU) properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="7065c-107">成員</span><span class="sxs-lookup"><span data-stu-id="7065c-107">Members</span></span>

<span data-ttu-id="7065c-108">**ExtendedKeyUsage** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7065c-108">The **ExtendedKeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="7065c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7065c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7065c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7065c-110">Properties</span></span>

<span data-ttu-id="7065c-111">**ExtendedKeyUsage** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7065c-111">The **ExtendedKeyUsage** object has these properties.</span></span>



| <span data-ttu-id="7065c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7065c-112">Property</span></span>                                                     | <span data-ttu-id="7065c-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="7065c-113">Access type</span></span>          | <span data-ttu-id="7065c-114">Description</span><span class="sxs-lookup"><span data-stu-id="7065c-114">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7065c-115">**Eku**</span><span class="sxs-lookup"><span data-stu-id="7065c-115">**EKUs**</span></span>](extendedkeyusage-ekus.md)<br/>             | <span data-ttu-id="7065c-116">唯讀</span><span class="sxs-lookup"><span data-stu-id="7065c-116">Read-only</span></span><br/> | <span data-ttu-id="7065c-117">[**Eku**](ekus.md) 集合，其中包含憑證的 [**EKU**](eku.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7065c-117">[**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span><br/>                            |
| [<span data-ttu-id="7065c-118">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="7065c-118">**IsCritical**</span></span>](extendedkeyusage-iscritical.md)<br/> | <span data-ttu-id="7065c-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="7065c-119">Read-only</span></span><br/> | <span data-ttu-id="7065c-120">抓取 **布林** 值，指出 EKU 延伸是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="7065c-120">Retrieves a **Boolean** value that indicates whether the EKU extension is marked critical.</span></span><br/>                                   |
| [<span data-ttu-id="7065c-121">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="7065c-121">**IsPresent**</span></span>](extendedkeyusage-ispresent.md)<br/>   | <span data-ttu-id="7065c-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="7065c-122">Read-only</span></span><br/> | <span data-ttu-id="7065c-123">抓取 **布林** 值，指出 EKU 延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="7065c-123">Retrieves a **Boolean** value that indicates whether the EKU extension is present.</span></span><br/> <span data-ttu-id="7065c-124">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="7065c-124">This is the default property.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="7065c-125">備註</span><span class="sxs-lookup"><span data-stu-id="7065c-125">Remarks</span></span>

<span data-ttu-id="7065c-126">無法建立 **ExtendedKeyUsage** 物件。</span><span class="sxs-lookup"><span data-stu-id="7065c-126">The **ExtendedKeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="7065c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7065c-127">Requirements</span></span>



| <span data-ttu-id="7065c-128">需求</span><span class="sxs-lookup"><span data-stu-id="7065c-128">Requirement</span></span> | <span data-ttu-id="7065c-129">值</span><span class="sxs-lookup"><span data-stu-id="7065c-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7065c-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7065c-130">End of client support</span></span><br/> | <span data-ttu-id="7065c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7065c-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7065c-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7065c-132">End of server support</span></span><br/> | <span data-ttu-id="7065c-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7065c-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7065c-134">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7065c-134">Redistributable</span></span><br/>       | <span data-ttu-id="7065c-135">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7065c-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7065c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7065c-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7065c-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7065c-137"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7065c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7065c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7065c-139">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="7065c-139">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
