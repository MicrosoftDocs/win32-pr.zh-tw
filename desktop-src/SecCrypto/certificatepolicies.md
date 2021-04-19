---
description: PolicyInformation 物件的集合。
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: CertificatePolicies 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995299"
---
# <a name="certificatepolicies-object"></a><span data-ttu-id="addc7-103">CertificatePolicies 物件</span><span class="sxs-lookup"><span data-stu-id="addc7-103">CertificatePolicies object</span></span>

<span data-ttu-id="addc7-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="addc7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="addc7-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來取得憑證原則。\]</span><span class="sxs-lookup"><span data-stu-id="addc7-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="addc7-106">**CertificatePolicies** 物件代表 [**PolicyInformation**](policyinformation.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="addc7-106">The **CertificatePolicies** object represents a collection of [**PolicyInformation**](policyinformation.md) objects.</span></span> <span data-ttu-id="addc7-107">每個 [**PolicyInformation**](policyinformation.md) 物件都代表一個憑證原則。</span><span class="sxs-lookup"><span data-stu-id="addc7-107">Each [**PolicyInformation**](policyinformation.md) object represents a single certificate policy.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="addc7-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="addc7-108">When to use</span></span>

<span data-ttu-id="addc7-109">**CertificatePolicies** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="addc7-109">The **CertificatePolicies** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="addc7-110">取得集合中的憑證原則數目。</span><span class="sxs-lookup"><span data-stu-id="addc7-110">Retrieve the number of certificate policies in the collection.</span></span>
-   <span data-ttu-id="addc7-111">從集合中取出特定的 [**PolicyInformation**](policyinformation.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="addc7-111">Retrieve a specific [**PolicyInformation**](policyinformation.md) object from the collection.</span></span>
-   <span data-ttu-id="addc7-112">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="addc7-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="addc7-113">成員</span><span class="sxs-lookup"><span data-stu-id="addc7-113">Members</span></span>

<span data-ttu-id="addc7-114">**CertificatePolicies** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="addc7-114">The **CertificatePolicies** object has these types of members:</span></span>

-   [<span data-ttu-id="addc7-115">屬性</span><span class="sxs-lookup"><span data-stu-id="addc7-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="addc7-116">屬性</span><span class="sxs-lookup"><span data-stu-id="addc7-116">Properties</span></span>

<span data-ttu-id="addc7-117">**CertificatePolicies** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="addc7-117">The **CertificatePolicies** object has these properties.</span></span>



| <span data-ttu-id="addc7-118">屬性</span><span class="sxs-lookup"><span data-stu-id="addc7-118">Property</span></span>                                                    | <span data-ttu-id="addc7-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="addc7-119">Access type</span></span>          | <span data-ttu-id="addc7-120">Description</span><span class="sxs-lookup"><span data-stu-id="addc7-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="addc7-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="addc7-121">**\_NewEnum**</span></span>](certificatepolicies-newenum.md)<br/> | <span data-ttu-id="addc7-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="addc7-122">Read-only</span></span><br/> | <span data-ttu-id="addc7-123">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="addc7-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="addc7-124">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="addc7-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="addc7-125">**計數**</span><span class="sxs-lookup"><span data-stu-id="addc7-125">**Count**</span></span>](certificatepolicies-count.md)<br/>       | <span data-ttu-id="addc7-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="addc7-126">Read-only</span></span><br/> | <span data-ttu-id="addc7-127">抓取集合中的 [**PolicyInformation**](policyinformation.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="addc7-127">Retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="addc7-128">**項目**</span><span class="sxs-lookup"><span data-stu-id="addc7-128">**Item**</span></span>](certificatepolicies-item.md)<br/>         | <span data-ttu-id="addc7-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="addc7-129">Read-only</span></span><br/> | <span data-ttu-id="addc7-130">抓取 [**PolicyInformation**](policyinformation.md) 物件，該物件代表集合的索引憑證原則。</span><span class="sxs-lookup"><span data-stu-id="addc7-130">Retrieves a [**PolicyInformation**](policyinformation.md) object that represents the indexed certificate policy of the collection.</span></span> <span data-ttu-id="addc7-131">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="addc7-131">This is the default property.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="addc7-132">備註</span><span class="sxs-lookup"><span data-stu-id="addc7-132">Remarks</span></span>

<span data-ttu-id="addc7-133">無法建立 **CertificatePolicies** 物件。</span><span class="sxs-lookup"><span data-stu-id="addc7-133">The **CertificatePolicies** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="addc7-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="addc7-134">Requirements</span></span>



| <span data-ttu-id="addc7-135">需求</span><span class="sxs-lookup"><span data-stu-id="addc7-135">Requirement</span></span> | <span data-ttu-id="addc7-136">值</span><span class="sxs-lookup"><span data-stu-id="addc7-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="addc7-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="addc7-137">End of client support</span></span><br/> | <span data-ttu-id="addc7-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="addc7-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="addc7-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="addc7-139">End of server support</span></span><br/> | <span data-ttu-id="addc7-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="addc7-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="addc7-141">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="addc7-141">Redistributable</span></span><br/>       | <span data-ttu-id="addc7-142">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="addc7-142">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="addc7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="addc7-143">DLL</span></span><br/>                   | <dl> <span data-ttu-id="addc7-144"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="addc7-144"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
