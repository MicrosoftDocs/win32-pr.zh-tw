---
description: 代表憑證信任鏈。
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chain 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982574"
---
# <a name="chain-object"></a><span data-ttu-id="98e0f-103">Chain 物件</span><span class="sxs-lookup"><span data-stu-id="98e0f-103">Chain object</span></span>

<span data-ttu-id="98e0f-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="98e0f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="98e0f-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="98e0f-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="98e0f-106">**Chain** 物件代表憑證信任鏈。</span><span class="sxs-lookup"><span data-stu-id="98e0f-106">The **Chain** object represents a certificate trust chain.</span></span>

<span data-ttu-id="98e0f-107">此物件提供屬性和方法，以建立憑證信任鏈來檢查憑證的有效性。</span><span class="sxs-lookup"><span data-stu-id="98e0f-107">This object provides properties and methods to build a certificate trust chain to check the validity of certificates.</span></span> <span data-ttu-id="98e0f-108">此鏈是使用 [**CertificateStatus CheckFlag**](certificatestatus-checkflag.md) 屬性值和 [**CertificateStatus**](certificatestatus.md) 物件的原則設定所建立。</span><span class="sxs-lookup"><span data-stu-id="98e0f-108">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property value and the policy settings of a [**CertificateStatus**](certificatestatus.md) object.</span></span>

<span data-ttu-id="98e0f-109">**Chain** 物件會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="98e0f-109">The **Chain** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="98e0f-110">**IChain2**：在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="98e0f-110">**IChain2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="98e0f-111">**IChain**：在 CAPICOM 1.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="98e0f-111">**IChain**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="98e0f-112">使用時機</span><span class="sxs-lookup"><span data-stu-id="98e0f-112">When to use</span></span>

<span data-ttu-id="98e0f-113">**Chain** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="98e0f-113">The **Chain** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="98e0f-114">建立憑證信任鏈。</span><span class="sxs-lookup"><span data-stu-id="98e0f-114">Build a certificate trust chain.</span></span>
-   <span data-ttu-id="98e0f-115">取得所有憑證的 Oid，以及對此鏈有效的應用程式原則。</span><span class="sxs-lookup"><span data-stu-id="98e0f-115">Obtain the OIDs of all the certificate and application policies valid for the chain.</span></span>
-   <span data-ttu-id="98e0f-116">確認鏈中的憑證狀態。</span><span class="sxs-lookup"><span data-stu-id="98e0f-116">Verify the status of the certificates in the chain.</span></span>
-   <span data-ttu-id="98e0f-117">取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="98e0f-117">Obtain extended error information.</span></span>
-   <span data-ttu-id="98e0f-118">取得鏈中的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="98e0f-118">Retrieve the collection of certificates in the chain.</span></span>

## <a name="members"></a><span data-ttu-id="98e0f-119">成員</span><span class="sxs-lookup"><span data-stu-id="98e0f-119">Members</span></span>

<span data-ttu-id="98e0f-120">**Chain** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="98e0f-120">The **Chain** object has these types of members:</span></span>

-   [<span data-ttu-id="98e0f-121">方法</span><span class="sxs-lookup"><span data-stu-id="98e0f-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="98e0f-122">屬性</span><span class="sxs-lookup"><span data-stu-id="98e0f-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98e0f-123">方法</span><span class="sxs-lookup"><span data-stu-id="98e0f-123">Methods</span></span>

<span data-ttu-id="98e0f-124">**Chain** 物件具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="98e0f-124">The **Chain** object has these methods.</span></span>



| <span data-ttu-id="98e0f-125">方法</span><span class="sxs-lookup"><span data-stu-id="98e0f-125">Method</span></span>                                                   | <span data-ttu-id="98e0f-126">描述</span><span class="sxs-lookup"><span data-stu-id="98e0f-126">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98e0f-127">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="98e0f-127">**ApplicationPolicies**</span></span>](chain-applicationpolicies.md) | <span data-ttu-id="98e0f-128">傳回 [**oid**](oids.md) 集合，這個集合表示對鏈有效的應用程式原則 oid。</span><span class="sxs-lookup"><span data-stu-id="98e0f-128">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="98e0f-129"> (繼承自 **ChainIChain2**) </span><span class="sxs-lookup"><span data-stu-id="98e0f-129">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="98e0f-130">**組建**</span><span class="sxs-lookup"><span data-stu-id="98e0f-130">**Build**</span></span>](chain-build.md)                             | <span data-ttu-id="98e0f-131">從終端憑證建立憑證驗證鏈至受信任的 [*根憑證*](../secgloss/r-gly.md)，並傳回布林值，指出鏈的整體有效性。</span><span class="sxs-lookup"><span data-stu-id="98e0f-131">Builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md), returning a Boolean value that indicates the overall validity of the chain.</span></span><br/> <span data-ttu-id="98e0f-132"> (繼承自 **ChainIChain2IChain**) </span><span class="sxs-lookup"><span data-stu-id="98e0f-132">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="98e0f-133">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="98e0f-133">**CertificatePolicies**</span></span>](chain-certificatepolicies.md) | <span data-ttu-id="98e0f-134">傳回 [**oid**](oids.md) 集合，這個集合表示對鏈有效的憑證原則 oid。</span><span class="sxs-lookup"><span data-stu-id="98e0f-134">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="98e0f-135"> (繼承自 **ChainIChain2**) </span><span class="sxs-lookup"><span data-stu-id="98e0f-135">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="98e0f-136">**ExtendedErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="98e0f-136">**ExtendedErrorInfo**</span></span>](chain-extendederrorinfo.md)     | <span data-ttu-id="98e0f-137">傳回字串，其中包含有關已編制索引之專案的其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="98e0f-137">Returns a string that contains additional error information about the indexed entry.</span></span><br/> <span data-ttu-id="98e0f-138"> (繼承自 **ChainIChain2**) </span><span class="sxs-lookup"><span data-stu-id="98e0f-138">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="98e0f-139">屬性</span><span class="sxs-lookup"><span data-stu-id="98e0f-139">Properties</span></span>

<span data-ttu-id="98e0f-140">**Chain** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="98e0f-140">The **Chain** object has these properties.</span></span>



| <span data-ttu-id="98e0f-141">屬性</span><span class="sxs-lookup"><span data-stu-id="98e0f-141">Property</span></span>                                              | <span data-ttu-id="98e0f-142">存取類型</span><span class="sxs-lookup"><span data-stu-id="98e0f-142">Access type</span></span>          | <span data-ttu-id="98e0f-143">Description</span><span class="sxs-lookup"><span data-stu-id="98e0f-143">Description</span></span>                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98e0f-144">**憑證**</span><span class="sxs-lookup"><span data-stu-id="98e0f-144">**Certificates**</span></span>](chain-certificates.md)<br/> | <span data-ttu-id="98e0f-145">唯讀</span><span class="sxs-lookup"><span data-stu-id="98e0f-145">Read-only</span></span><br/> | <span data-ttu-id="98e0f-146">抓取代表鏈中憑證的 [**憑證**](certificates.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="98e0f-146">Retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="98e0f-147">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="98e0f-147">This is the default property.</span></span><br/> <span data-ttu-id="98e0f-148"> (繼承自 **ChainIChain2IChain**) </span><span class="sxs-lookup"><span data-stu-id="98e0f-148">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="98e0f-149">**狀態**</span><span class="sxs-lookup"><span data-stu-id="98e0f-149">**Status**</span></span>](chain-status.md)<br/>             | <span data-ttu-id="98e0f-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="98e0f-150">Read-only</span></span><br/> | <span data-ttu-id="98e0f-151">抓取鏈的有效狀態或鏈中的特定憑證。</span><span class="sxs-lookup"><span data-stu-id="98e0f-151">Retrieves the validity status of the chain or a specific certificate in the chain.</span></span><br/> <span data-ttu-id="98e0f-152"> (繼承自 **ChainIChain2IChain**) </span><span class="sxs-lookup"><span data-stu-id="98e0f-152">(Inherited from **ChainIChain2IChain**)</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="98e0f-153">備註</span><span class="sxs-lookup"><span data-stu-id="98e0f-153">Remarks</span></span>

<span data-ttu-id="98e0f-154">您可以建立 **Chain** 物件，並且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="98e0f-154">The **Chain** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="98e0f-155">**連鎖店** 物件的 ProgID 為 "CAPICOM。Chain 2」。</span><span class="sxs-lookup"><span data-stu-id="98e0f-155">The ProgID for the **Chain** object is "CAPICOM.Chain.2".</span></span>

<span data-ttu-id="98e0f-156">**CAPICOM 1。*x*：** **Chain** 物件的 ProgID 是 CAPICOM。Chain. 1。</span><span class="sxs-lookup"><span data-stu-id="98e0f-156">**CAPICOM 1.*x*:** The ProgID for the **Chain** object is CAPICOM.Chain.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e0f-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="98e0f-157">Requirements</span></span>



| <span data-ttu-id="98e0f-158">需求</span><span class="sxs-lookup"><span data-stu-id="98e0f-158">Requirement</span></span> | <span data-ttu-id="98e0f-159">值</span><span class="sxs-lookup"><span data-stu-id="98e0f-159">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e0f-160">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="98e0f-160">End of client support</span></span><br/> | <span data-ttu-id="98e0f-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98e0f-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="98e0f-162">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="98e0f-162">End of server support</span></span><br/> | <span data-ttu-id="98e0f-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98e0f-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="98e0f-164">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="98e0f-164">Redistributable</span></span><br/>       | <span data-ttu-id="98e0f-165">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="98e0f-165">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="98e0f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="98e0f-166">DLL</span></span><br/>                   | <dl> <span data-ttu-id="98e0f-167"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98e0f-167"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e0f-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98e0f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e0f-169">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="98e0f-169">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
