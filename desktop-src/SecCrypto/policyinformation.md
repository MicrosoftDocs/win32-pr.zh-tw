---
description: 提供存取擴充功能的原則資訊。
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: PolicyInformation 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975958"
---
# <a name="policyinformation-object"></a><span data-ttu-id="a7725-103">PolicyInformation 物件</span><span class="sxs-lookup"><span data-stu-id="a7725-103">PolicyInformation object</span></span>

<span data-ttu-id="a7725-104">\[**PolicyInformation** 物件可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a7725-104">\[The **PolicyInformation** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a7725-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來處理憑證原則延伸中的原則資訊。\]</span><span class="sxs-lookup"><span data-stu-id="a7725-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="a7725-106">**PolicyInformation** 物件可讓您存取延伸模組的原則資訊。</span><span class="sxs-lookup"><span data-stu-id="a7725-106">The **PolicyInformation** object provides access to the policy information of an extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a7725-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="a7725-107">When to use</span></span>

<span data-ttu-id="a7725-108">**PolicyInformation** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="a7725-108">The **PolicyInformation** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="a7725-109">取出原則 OID。</span><span class="sxs-lookup"><span data-stu-id="a7725-109">Retrieve the policy OID.</span></span>
-   <span data-ttu-id="a7725-110">取出原則的限定詞集合。</span><span class="sxs-lookup"><span data-stu-id="a7725-110">Retrieve a collection of the policy's qualifiers.</span></span>

## <a name="members"></a><span data-ttu-id="a7725-111">成員</span><span class="sxs-lookup"><span data-stu-id="a7725-111">Members</span></span>

<span data-ttu-id="a7725-112">**PolicyInformation** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a7725-112">The **PolicyInformation** object has these types of members:</span></span>

-   [<span data-ttu-id="a7725-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a7725-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7725-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a7725-114">Properties</span></span>

<span data-ttu-id="a7725-115">**PolicyInformation** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a7725-115">The **PolicyInformation** object has these properties.</span></span>



| <span data-ttu-id="a7725-116">屬性</span><span class="sxs-lookup"><span data-stu-id="a7725-116">Property</span></span>                                                      | <span data-ttu-id="a7725-117">描述</span><span class="sxs-lookup"><span data-stu-id="a7725-117">Description</span></span>                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7725-118">**老**</span><span class="sxs-lookup"><span data-stu-id="a7725-118">**OID**</span></span>](policyinformation-oid.md)<br/>               | <span data-ttu-id="a7725-119">以 [**oid**](oid.md) 物件形式抓取原則的 oid。</span><span class="sxs-lookup"><span data-stu-id="a7725-119">Retrieves the policy's OID, as an [**OID**](oid.md) object.</span></span> <span data-ttu-id="a7725-120">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="a7725-120">This is the default property.</span></span><br/>       |
| [<span data-ttu-id="a7725-121">**限定詞**</span><span class="sxs-lookup"><span data-stu-id="a7725-121">**Qualifiers**</span></span>](policyinformation-qualifiers.md)<br/> | <span data-ttu-id="a7725-122">以 [**限定詞**](qualifiers.md) 物件形式抓取原則的限定詞集合。</span><span class="sxs-lookup"><span data-stu-id="a7725-122">Retrieves a collection of the policy's qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7725-123">備註</span><span class="sxs-lookup"><span data-stu-id="a7725-123">Remarks</span></span>

<span data-ttu-id="a7725-124">無法建立 **PolicyInformation** 物件。</span><span class="sxs-lookup"><span data-stu-id="a7725-124">The **PolicyInformation** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7725-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7725-125">Requirements</span></span>



| <span data-ttu-id="a7725-126">需求</span><span class="sxs-lookup"><span data-stu-id="a7725-126">Requirement</span></span> | <span data-ttu-id="a7725-127">值</span><span class="sxs-lookup"><span data-stu-id="a7725-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7725-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a7725-128">Redistributable</span></span><br/> | <span data-ttu-id="a7725-129">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a7725-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a7725-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a7725-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="a7725-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7725-131"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
