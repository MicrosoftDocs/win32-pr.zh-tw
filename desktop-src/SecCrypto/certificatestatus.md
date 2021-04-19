---
description: 包含如何建立憑證信任鏈的相關資訊。
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: CertificateStatus 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e9a6cb31a00f4d2943e68670930e6cbc4436b6b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978651"
---
# <a name="certificatestatus-object"></a><span data-ttu-id="17b17-103">CertificateStatus 物件</span><span class="sxs-lookup"><span data-stu-id="17b17-103">CertificateStatus object</span></span>

<span data-ttu-id="17b17-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="17b17-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="17b17-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="17b17-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="17b17-106">**CertificateStatus** 物件包含如何建立憑證信任鏈的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="17b17-106">The **CertificateStatus** object contains information about how to construct a certificate trust chain.</span></span>

## <a name="members"></a><span data-ttu-id="17b17-107">成員</span><span class="sxs-lookup"><span data-stu-id="17b17-107">Members</span></span>

<span data-ttu-id="17b17-108">**CertificateStatus** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="17b17-108">The **CertificateStatus** object has these types of members:</span></span>

-   [<span data-ttu-id="17b17-109">方法</span><span class="sxs-lookup"><span data-stu-id="17b17-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="17b17-110">屬性</span><span class="sxs-lookup"><span data-stu-id="17b17-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="17b17-111">方法</span><span class="sxs-lookup"><span data-stu-id="17b17-111">Methods</span></span>

<span data-ttu-id="17b17-112">**CertificateStatus** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="17b17-112">The **CertificateStatus** object has these methods.</span></span>



| <span data-ttu-id="17b17-113">方法</span><span class="sxs-lookup"><span data-stu-id="17b17-113">Method</span></span>                                                               | <span data-ttu-id="17b17-114">描述</span><span class="sxs-lookup"><span data-stu-id="17b17-114">Description</span></span>                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17b17-115">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="17b17-115">**ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md) | <span data-ttu-id="17b17-116">傳回 [**oid**](oids.md) 集合，表示應用程式原則 oid。</span><span class="sxs-lookup"><span data-stu-id="17b17-116">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs.</span></span><br/>                                           |
| [<span data-ttu-id="17b17-117">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="17b17-117">**CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md) | <span data-ttu-id="17b17-118">傳回 [**oid**](oids.md) 集合，這個集合表示在鏈大樓期間使用的憑證原則 oid。</span><span class="sxs-lookup"><span data-stu-id="17b17-118">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs used during chain building.</span></span><br/>                |
| [<span data-ttu-id="17b17-119">**EKU**</span><span class="sxs-lookup"><span data-stu-id="17b17-119">**EKU**</span></span>](certificatestatus-eku.md)                                 | <span data-ttu-id="17b17-120">傳回 [**eku**](eku.md) 物件，用來設定要檢查的 eku 元素，以建立憑證的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="17b17-120">Returns the [**EKU**](eku.md) object used to set the EKU elements to be checked in establishing a certificate's validity status.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="17b17-121">屬性</span><span class="sxs-lookup"><span data-stu-id="17b17-121">Properties</span></span>

<span data-ttu-id="17b17-122">**CertificateStatus** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="17b17-122">The **CertificateStatus** object has these properties.</span></span>



| <span data-ttu-id="17b17-123">屬性</span><span class="sxs-lookup"><span data-stu-id="17b17-123">Property</span></span>                                                                        | <span data-ttu-id="17b17-124">存取類型</span><span class="sxs-lookup"><span data-stu-id="17b17-124">Access type</span></span>           | <span data-ttu-id="17b17-125">Description</span><span class="sxs-lookup"><span data-stu-id="17b17-125">Description</span></span>                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17b17-126">**憑證**</span><span class="sxs-lookup"><span data-stu-id="17b17-126">**Certificates**</span></span>](certificatestatus-certificates.md)<br/>               | <span data-ttu-id="17b17-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17b17-127">Read/write</span></span><br/> | <span data-ttu-id="17b17-128">設定或抓取可以用來建立憑證鏈的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="17b17-128">Sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span><br/> <span data-ttu-id="17b17-129">**CAPICOM 2.0.0.3 和更早版本：** 不支援 [ [**憑證**](certificatestatus-certificates.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="17b17-129">**CAPICOM 2.0.0.3 and earlier:** The [**Certificates**](certificatestatus-certificates.md) property is not supported.</span></span><br/>                    |
| [<span data-ttu-id="17b17-130">**CheckFlag**</span><span class="sxs-lookup"><span data-stu-id="17b17-130">**CheckFlag**</span></span>](certificatestatus-checkflag.md)<br/>                     | <span data-ttu-id="17b17-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17b17-131">Read/write</span></span><br/> | <span data-ttu-id="17b17-132">有效性檢查旗標。</span><span class="sxs-lookup"><span data-stu-id="17b17-132">Validity check flag.</span></span> <span data-ttu-id="17b17-133">您可以使用邏輯 **OR** 運算子來聯結值。</span><span class="sxs-lookup"><span data-stu-id="17b17-133">Values can be joined by using a logical **OR** operator.</span></span> <span data-ttu-id="17b17-134">預設核取旗標為 [ [**\_ \_ 線上 \_ 所有的 CAPICOM 檢查**](capicom-check-flag.md)]。</span><span class="sxs-lookup"><span data-stu-id="17b17-134">The default check flag is [**CAPICOM\_CHECK\_ONLINE\_ALL**](capicom-check-flag.md).</span></span><br/>                                                                                     |
| [<span data-ttu-id="17b17-135">**結果**</span><span class="sxs-lookup"><span data-stu-id="17b17-135">**Result**</span></span>](certificatestatus-result.md)<br/>                           | <span data-ttu-id="17b17-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="17b17-136">Read-only</span></span><br/>  | <span data-ttu-id="17b17-137">指出憑證是否有效。</span><span class="sxs-lookup"><span data-stu-id="17b17-137">Indicates whether the certificate is valid.</span></span> <span data-ttu-id="17b17-138">使用 [**CheckFlag**](certificatestatus-checkflag.md) 屬性的目前設定和憑證的原則設定，檢查憑證的有效性。</span><span class="sxs-lookup"><span data-stu-id="17b17-138">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the policy settings of the certificate.</span></span> <span data-ttu-id="17b17-139">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="17b17-139">This is the default property.</span></span><br/> |
| [<span data-ttu-id="17b17-140">**UrlRetrievalTimeout**</span><span class="sxs-lookup"><span data-stu-id="17b17-140">**UrlRetrievalTimeout**</span></span>](certificatestatus-urlretrievaltimeout.md)<br/> | <span data-ttu-id="17b17-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17b17-141">Read/write</span></span><br/> | <span data-ttu-id="17b17-142">設定或抓取 URL 判定為無法存取之前的時間長度。</span><span class="sxs-lookup"><span data-stu-id="17b17-142">Sets or retrieves the length of time before a URL is determined to be unreachable.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="17b17-143">**VerificationTime**</span><span class="sxs-lookup"><span data-stu-id="17b17-143">**VerificationTime**</span></span>](certificatestatus-verificationtime.md)<br/>       | <span data-ttu-id="17b17-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17b17-144">Read/write</span></span><br/> | <span data-ttu-id="17b17-145">設定或抓取憑證驗證的時間。</span><span class="sxs-lookup"><span data-stu-id="17b17-145">Sets or retrieves the time that the certificate was verified.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="17b17-146">備註</span><span class="sxs-lookup"><span data-stu-id="17b17-146">Remarks</span></span>

<span data-ttu-id="17b17-147">無法建立 **CertificateStatus** 物件。</span><span class="sxs-lookup"><span data-stu-id="17b17-147">The **CertificateStatus** object cannot be created.</span></span>

<span data-ttu-id="17b17-148">**CertificateStatus** 物件是由 [**Certificate. IsValid**](certificate-isvalid.md)方法傳回。</span><span class="sxs-lookup"><span data-stu-id="17b17-148">The **CertificateStatus** object is returned by the [**Certificate.IsValid**](certificate-isvalid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b17-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="17b17-149">Requirements</span></span>



| <span data-ttu-id="17b17-150">需求</span><span class="sxs-lookup"><span data-stu-id="17b17-150">Requirement</span></span> | <span data-ttu-id="17b17-151">值</span><span class="sxs-lookup"><span data-stu-id="17b17-151">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b17-152">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="17b17-152">End of client support</span></span><br/> | <span data-ttu-id="17b17-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17b17-153">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="17b17-154">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="17b17-154">End of server support</span></span><br/> | <span data-ttu-id="17b17-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17b17-155">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="17b17-156">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="17b17-156">Redistributable</span></span><br/>       | <span data-ttu-id="17b17-157">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="17b17-157">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="17b17-158">DLL</span><span class="sxs-lookup"><span data-stu-id="17b17-158">DLL</span></span><br/>                   | <dl> <span data-ttu-id="17b17-159"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b17-159"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b17-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17b17-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b17-161">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="17b17-161">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="17b17-162">**鏈**</span><span class="sxs-lookup"><span data-stu-id="17b17-162">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
