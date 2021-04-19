---
description: 提供憑證的金鑰使用方式屬性的唯讀存取。
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: KeyUsage 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999066"
---
# <a name="keyusage-object"></a><span data-ttu-id="f6b5a-103">KeyUsage 物件</span><span class="sxs-lookup"><span data-stu-id="f6b5a-103">KeyUsage object</span></span>

<span data-ttu-id="f6b5a-104">\[**KeyUsage** 物件可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-104">\[The **KeyUsage** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f6b5a-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="f6b5a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f6b5a-106">**KeyUsage** 物件提供對憑證的金鑰使用方式屬性的唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-106">The **KeyUsage** object provides read-only access to key usage properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="f6b5a-107">成員</span><span class="sxs-lookup"><span data-stu-id="f6b5a-107">Members</span></span>

<span data-ttu-id="f6b5a-108">**KeyUsage** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f6b5a-108">The **KeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="f6b5a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f6b5a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6b5a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f6b5a-110">Properties</span></span>

<span data-ttu-id="f6b5a-111">**KeyUsage** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-111">The **KeyUsage** object has these properties.</span></span>



| <span data-ttu-id="f6b5a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f6b5a-112">Property</span></span>                                                                           | <span data-ttu-id="f6b5a-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="f6b5a-113">Access type</span></span>          | <span data-ttu-id="f6b5a-114">Description</span><span class="sxs-lookup"><span data-stu-id="f6b5a-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6b5a-115">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-115">**IsCritical**</span></span>](keyusage-iscritical.md)<br/>                               | <span data-ttu-id="f6b5a-116">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-116">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-117">抓取布林值，指出 **KeyUsage** 延伸模組是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-117">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is marked critical.</span></span><br/>                                  |
| [<span data-ttu-id="f6b5a-118">**IsCRLSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-118">**IsCRLSignEnabled**</span></span>](keyusage-iscrlsignenabled.md)<br/>                   | <span data-ttu-id="f6b5a-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-119">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-120">抓取布林值，指出是否已設定 CRLSign 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-120">Retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span><br/>                                                         |
| [<span data-ttu-id="f6b5a-121">**IsDataEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-121">**IsDataEnciphermentEnabled**</span></span>](keyusage-isdataenciphermentenabled.md)<br/> | <span data-ttu-id="f6b5a-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-122">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-123">抓取布林值，指出是否已設定 dataEncipherment 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-123">Retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="f6b5a-124">**IsDecipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-124">**IsDecipherOnlyEnabled**</span></span>](keyusage-isdecipheronlyenabled.md)<br/>         | <span data-ttu-id="f6b5a-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-125">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-126">抓取布林值，指出是否已設定 decipherOnly 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-126">Retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="f6b5a-127">**IsDigitalSignatureEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-127">**IsDigitalSignatureEnabled**</span></span>](keyusage-isdigitalsignatureenabled.md)<br/> | <span data-ttu-id="f6b5a-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-128">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-129">抓取布林值，指出是否已設定 digitalSignature 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-129">Retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="f6b5a-130">**IsEncipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-130">**IsEncipherOnlyEnabled**</span></span>](keyusage-isencipheronlyenabled.md)<br/>         | <span data-ttu-id="f6b5a-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-131">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-132">抓取布林值，指出是否已設定 encipherOnly 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-132">Retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="f6b5a-133">**IsKeyAgreementEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-133">**IsKeyAgreementEnabled**</span></span>](keyusage-iskeyagreementenabled.md)<br/>         | <span data-ttu-id="f6b5a-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-134">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-135">抓取布林值，指出是否已設定 keyAgreement 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-135">Retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="f6b5a-136">**IsKeyCertSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-136">**IsKeyCertSignEnabled**</span></span>](keyusage-iskeycertsignenabled.md)<br/>           | <span data-ttu-id="f6b5a-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-137">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-138">抓取布林值，指出是否已設定 keyCertSign 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-138">Retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span><br/>                                                     |
| [<span data-ttu-id="f6b5a-139">**IsKeyEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-139">**IsKeyEnciphermentEnabled**</span></span>](keyusage-iskeyenciphermentenabled.md)<br/>   | <span data-ttu-id="f6b5a-140">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-140">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-141">抓取布林值，指出是否已設定 keyEncipherment 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-141">Retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span><br/>                                                 |
| [<span data-ttu-id="f6b5a-142">**IsNonRepudiationEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-142">**IsNonRepudiationEnabled**</span></span>](keyusage-isnonrepudiationenabled.md)<br/>     | <span data-ttu-id="f6b5a-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-143">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-144">抓取布林值，指出是否已設定 nonRepudiationEnabled 位。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-144">Retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span><br/>                                           |
| [<span data-ttu-id="f6b5a-145">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-145">**IsPresent**</span></span>](keyusage-ispresent.md)<br/>                                 | <span data-ttu-id="f6b5a-146">唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b5a-146">Read-only</span></span><br/> | <span data-ttu-id="f6b5a-147">抓取布林值，指出 **KeyUsage** 延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-147">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is present.</span></span><br/> <span data-ttu-id="f6b5a-148">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-148">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6b5a-149">備註</span><span class="sxs-lookup"><span data-stu-id="f6b5a-149">Remarks</span></span>

<span data-ttu-id="f6b5a-150">無法建立 **KeyUsage** 物件。</span><span class="sxs-lookup"><span data-stu-id="f6b5a-150">The **KeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b5a-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6b5a-151">Requirements</span></span>



| <span data-ttu-id="f6b5a-152">需求</span><span class="sxs-lookup"><span data-stu-id="f6b5a-152">Requirement</span></span> | <span data-ttu-id="f6b5a-153">值</span><span class="sxs-lookup"><span data-stu-id="f6b5a-153">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b5a-154">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f6b5a-154">Redistributable</span></span><br/> | <span data-ttu-id="f6b5a-155">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f6b5a-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f6b5a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f6b5a-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="f6b5a-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6b5a-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6b5a-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6b5a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b5a-159">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="f6b5a-159">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
