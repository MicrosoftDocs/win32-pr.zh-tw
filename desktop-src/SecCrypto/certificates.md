---
description: 憑證物件-表示憑證物件的集合。
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: 憑證物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8efb9221f39b8544eabe8f6c00d21f6cfdf20c14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098386"
---
# <a name="certificates-object"></a><span data-ttu-id="912e9-103">憑證物件</span><span class="sxs-lookup"><span data-stu-id="912e9-103">Certificates object</span></span>

<span data-ttu-id="912e9-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="912e9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="912e9-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/previous-versions/windows/embedded/hh424013(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="912e9-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="912e9-106">**憑證** 物件代表 [**憑證**](certificate.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="912e9-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="912e9-107">每個 [**憑證**](certificate.md) 物件都代表一個 [*數位憑證*](../secgloss/d-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="912e9-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="912e9-108">**憑證** 物件會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="912e9-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="912e9-109">**ICertificates2**：在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="912e9-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="912e9-110">**ICertificates**：在 CAPICOM 1.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="912e9-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="912e9-111">使用時機</span><span class="sxs-lookup"><span data-stu-id="912e9-111">When to use</span></span>

<span data-ttu-id="912e9-112">**憑證** 物件用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="912e9-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="912e9-113">在集合中加入或移除 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="912e9-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="912e9-114">藉由尋找一組憑證或顯示對話方塊來選取憑證，以產生集合的子集。</span><span class="sxs-lookup"><span data-stu-id="912e9-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="912e9-115">清除集合中的所有 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="912e9-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="912e9-116">取得集合中的憑證數目。</span><span class="sxs-lookup"><span data-stu-id="912e9-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="912e9-117">從集合中取出特定的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="912e9-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="912e9-118">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="912e9-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="912e9-119">成員</span><span class="sxs-lookup"><span data-stu-id="912e9-119">Members</span></span>

<span data-ttu-id="912e9-120">**憑證** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="912e9-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="912e9-121">方法</span><span class="sxs-lookup"><span data-stu-id="912e9-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="912e9-122">屬性</span><span class="sxs-lookup"><span data-stu-id="912e9-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="912e9-123">方法</span><span class="sxs-lookup"><span data-stu-id="912e9-123">Methods</span></span>

<span data-ttu-id="912e9-124">**憑證** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="912e9-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="912e9-125">方法</span><span class="sxs-lookup"><span data-stu-id="912e9-125">Method</span></span>                                | <span data-ttu-id="912e9-126">描述</span><span class="sxs-lookup"><span data-stu-id="912e9-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="912e9-127">**添加**</span><span class="sxs-lookup"><span data-stu-id="912e9-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="912e9-128">將 [**憑證**](certificate.md) 物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="912e9-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="912e9-129"> (繼承自 **CertificatesICertificates2**) </span><span class="sxs-lookup"><span data-stu-id="912e9-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="912e9-130">**清楚**</span><span class="sxs-lookup"><span data-stu-id="912e9-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="912e9-131">從集合中移除所有的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="912e9-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="912e9-132"> (繼承自 **CertificatesICertificates2**) </span><span class="sxs-lookup"><span data-stu-id="912e9-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="912e9-133">**Find**</span><span class="sxs-lookup"><span data-stu-id="912e9-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="912e9-134">傳回 **憑證** 物件，其中包含符合指定之搜尋準則的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="912e9-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="912e9-135"> (繼承自 **CertificatesICertificates2**) </span><span class="sxs-lookup"><span data-stu-id="912e9-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="912e9-136">**移除**</span><span class="sxs-lookup"><span data-stu-id="912e9-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="912e9-137">從集合中移除單一 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="912e9-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="912e9-138"> (繼承自 **CertificatesICertificates2**) </span><span class="sxs-lookup"><span data-stu-id="912e9-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="912e9-139">**儲存**</span><span class="sxs-lookup"><span data-stu-id="912e9-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="912e9-140">將憑證儲存至指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="912e9-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="912e9-141"> (繼承自 **CertificatesICertificates2**) </span><span class="sxs-lookup"><span data-stu-id="912e9-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="912e9-142">**選取**</span><span class="sxs-lookup"><span data-stu-id="912e9-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="912e9-143">顯示用來選取憑證的對話方塊，並傳回選取的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="912e9-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="912e9-144"> (繼承自 **CertificatesICertificates2**) </span><span class="sxs-lookup"><span data-stu-id="912e9-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="912e9-145">屬性</span><span class="sxs-lookup"><span data-stu-id="912e9-145">Properties</span></span>

<span data-ttu-id="912e9-146">**憑證** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="912e9-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="912e9-147">屬性</span><span class="sxs-lookup"><span data-stu-id="912e9-147">Property</span></span>                                             | <span data-ttu-id="912e9-148">存取類型</span><span class="sxs-lookup"><span data-stu-id="912e9-148">Access type</span></span>          | <span data-ttu-id="912e9-149">Description</span><span class="sxs-lookup"><span data-stu-id="912e9-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="912e9-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="912e9-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="912e9-151">唯讀</span><span class="sxs-lookup"><span data-stu-id="912e9-151">Read-only</span></span><br/> | <span data-ttu-id="912e9-152">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="912e9-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="912e9-153">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="912e9-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="912e9-154">**計數**</span><span class="sxs-lookup"><span data-stu-id="912e9-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="912e9-155">唯讀</span><span class="sxs-lookup"><span data-stu-id="912e9-155">Read-only</span></span><br/> | <span data-ttu-id="912e9-156">抓取集合中的 [**憑證**](certificate.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="912e9-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="912e9-157">**項目**</span><span class="sxs-lookup"><span data-stu-id="912e9-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="912e9-158">唯讀</span><span class="sxs-lookup"><span data-stu-id="912e9-158">Read-only</span></span><br/> | <span data-ttu-id="912e9-159">抓取代表集合之索引憑證的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="912e9-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="912e9-160">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="912e9-160">This is the default property.</span></span><br/> <span data-ttu-id="912e9-161"> (繼承自 **CertificatesICertificates2ICertificates**) </span><span class="sxs-lookup"><span data-stu-id="912e9-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="912e9-162">備註</span><span class="sxs-lookup"><span data-stu-id="912e9-162">Remarks</span></span>

<span data-ttu-id="912e9-163">您可以建立 **憑證** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="912e9-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="912e9-164">**憑證** 物件的 ProgID 是「CAPICOM」。[憑證]。2。</span><span class="sxs-lookup"><span data-stu-id="912e9-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="912e9-165">**CAPICOM 1。*x*：** **憑證** 物件的 ProgID 是「CAPICOM」。憑證. 1」。</span><span class="sxs-lookup"><span data-stu-id="912e9-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="912e9-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="912e9-166">Requirements</span></span>



| <span data-ttu-id="912e9-167">需求</span><span class="sxs-lookup"><span data-stu-id="912e9-167">Requirement</span></span> | <span data-ttu-id="912e9-168">值</span><span class="sxs-lookup"><span data-stu-id="912e9-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="912e9-169">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="912e9-169">End of client support</span></span><br/> | <span data-ttu-id="912e9-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="912e9-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="912e9-171">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="912e9-171">End of server support</span></span><br/> | <span data-ttu-id="912e9-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="912e9-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="912e9-173">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="912e9-173">Redistributable</span></span><br/>       | <span data-ttu-id="912e9-174">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="912e9-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="912e9-175">DLL</span><span class="sxs-lookup"><span data-stu-id="912e9-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="912e9-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="912e9-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="912e9-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="912e9-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912e9-178">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="912e9-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
