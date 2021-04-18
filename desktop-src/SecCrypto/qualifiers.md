---
description: 表示限定詞的集合。
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: 'Iads 的限定詞物件 (.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989560"
---
# <a name="qualifiers-object"></a><span data-ttu-id="0bf16-103">限定詞物件</span><span class="sxs-lookup"><span data-stu-id="0bf16-103">Qualifiers object</span></span>

<span data-ttu-id="0bf16-104">\[**限定詞** 物件可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="0bf16-104">\[The **Qualifiers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0bf16-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="0bf16-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="0bf16-106">**限定詞** 物件代表一組限定詞。</span><span class="sxs-lookup"><span data-stu-id="0bf16-106">The **Qualifiers** object represents a collection of qualifiers.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0bf16-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="0bf16-107">When to use</span></span>

<span data-ttu-id="0bf16-108">**限定詞** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="0bf16-108">The **Qualifiers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="0bf16-109">從集合中取出特定的擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="0bf16-109">Retrieve a specific extended property from the collection.</span></span>
-   <span data-ttu-id="0bf16-110">取得集合中的擴充屬性數目。</span><span class="sxs-lookup"><span data-stu-id="0bf16-110">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="0bf16-111">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="0bf16-111">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="0bf16-112">成員</span><span class="sxs-lookup"><span data-stu-id="0bf16-112">Members</span></span>

<span data-ttu-id="0bf16-113">**限定詞** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0bf16-113">The **Qualifiers** object has these types of members:</span></span>

-   [<span data-ttu-id="0bf16-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0bf16-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bf16-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0bf16-115">Properties</span></span>

<span data-ttu-id="0bf16-116">**限定詞** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0bf16-116">The **Qualifiers** object has these properties.</span></span>



| <span data-ttu-id="0bf16-117">屬性</span><span class="sxs-lookup"><span data-stu-id="0bf16-117">Property</span></span>                                           | <span data-ttu-id="0bf16-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="0bf16-118">Access type</span></span>          | <span data-ttu-id="0bf16-119">Description</span><span class="sxs-lookup"><span data-stu-id="0bf16-119">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bf16-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="0bf16-120">**\_NewEnum**</span></span>](qualifiers-newenum.md)<br/> | <span data-ttu-id="0bf16-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="0bf16-121">Read-only</span></span><br/> | <span data-ttu-id="0bf16-122">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="0bf16-122">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="0bf16-123">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="0bf16-123">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="0bf16-124">**計數**</span><span class="sxs-lookup"><span data-stu-id="0bf16-124">**Count**</span></span>](qualifiers-count.md)<br/>       | <span data-ttu-id="0bf16-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="0bf16-125">Read-only</span></span><br/> | <span data-ttu-id="0bf16-126">抓取集合中的限定詞數目。</span><span class="sxs-lookup"><span data-stu-id="0bf16-126">Retrieves the number of qualifiers in the collection.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="0bf16-127">**項目**</span><span class="sxs-lookup"><span data-stu-id="0bf16-127">**Item**</span></span>](qualifiers-item.md)<br/>         | <span data-ttu-id="0bf16-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="0bf16-128">Read-only</span></span><br/> | <span data-ttu-id="0bf16-129">抓取代表集合之索引限定詞的辨識 [**符號**](qualifier.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0bf16-129">Retrieves a [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span> <span data-ttu-id="0bf16-130">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="0bf16-130">This is the default property.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="0bf16-131">備註</span><span class="sxs-lookup"><span data-stu-id="0bf16-131">Remarks</span></span>

<span data-ttu-id="0bf16-132">無法建立 **限定詞** 物件。</span><span class="sxs-lookup"><span data-stu-id="0bf16-132">The **Qualifiers** object cannot be created.</span></span>

<span data-ttu-id="0bf16-133">[**PolicyInformation 限定詞**](policyinformation-qualifiers.md)CAPICOM 物件屬性會傳回辨識符號 **物件。**</span><span class="sxs-lookup"><span data-stu-id="0bf16-133">The [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) CAPICOM object property returns a **Qualifiers** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf16-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bf16-134">Requirements</span></span>



| <span data-ttu-id="0bf16-135">需求</span><span class="sxs-lookup"><span data-stu-id="0bf16-135">Requirement</span></span> | <span data-ttu-id="0bf16-136">值</span><span class="sxs-lookup"><span data-stu-id="0bf16-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf16-137">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0bf16-137">Redistributable</span></span><br/> | <span data-ttu-id="0bf16-138">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0bf16-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0bf16-139">標頭</span><span class="sxs-lookup"><span data-stu-id="0bf16-139">Header</span></span><br/>          | <dl> <span data-ttu-id="0bf16-140"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="0bf16-140"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="0bf16-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0bf16-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="0bf16-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bf16-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
