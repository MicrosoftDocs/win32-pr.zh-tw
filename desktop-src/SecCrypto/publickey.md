---
description: PublicKey 物件代表憑證物件中的公開金鑰。
title: PublicKey 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978507"
---
# <a name="publickey-object"></a><span data-ttu-id="44e09-103">PublicKey 物件</span><span class="sxs-lookup"><span data-stu-id="44e09-103">PublicKey object</span></span>

<span data-ttu-id="44e09-104">\[**PublicKey** 物件可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="44e09-104">\[The **PublicKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="44e09-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="44e09-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="44e09-106">**PublicKey** 物件代表 [**憑證**](certificate.md)物件中的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="44e09-106">The **PublicKey** object represents a public key in a [**Certificate**](certificate.md) object.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="44e09-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="44e09-107">When to use</span></span>

<span data-ttu-id="44e09-108">**PublicKey** 物件是用來取得公開金鑰的相關資料。</span><span class="sxs-lookup"><span data-stu-id="44e09-108">The **PublicKey** object is used to retrieve data about the public key.</span></span>

## <a name="members"></a><span data-ttu-id="44e09-109">成員</span><span class="sxs-lookup"><span data-stu-id="44e09-109">Members</span></span>

<span data-ttu-id="44e09-110">**PublicKey** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="44e09-110">The **PublicKey** object has these types of members:</span></span>

-   [<span data-ttu-id="44e09-111">屬性</span><span class="sxs-lookup"><span data-stu-id="44e09-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44e09-112">屬性</span><span class="sxs-lookup"><span data-stu-id="44e09-112">Properties</span></span>

<span data-ttu-id="44e09-113">**PublicKey** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="44e09-113">The **PublicKey** object has these properties.</span></span>



| <span data-ttu-id="44e09-114">屬性</span><span class="sxs-lookup"><span data-stu-id="44e09-114">Property</span></span>                                                            | <span data-ttu-id="44e09-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="44e09-115">Access type</span></span>          | <span data-ttu-id="44e09-116">Description</span><span class="sxs-lookup"><span data-stu-id="44e09-116">Description</span></span>                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44e09-117">**演算法**</span><span class="sxs-lookup"><span data-stu-id="44e09-117">**Algorithm**</span></span>](publickey-algorithm.md)<br/>                 | <span data-ttu-id="44e09-118">唯讀</span><span class="sxs-lookup"><span data-stu-id="44e09-118">Read-only</span></span><br/> | <span data-ttu-id="44e09-119">抓取標識公開金鑰所使用之演算法的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="44e09-119">Retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="44e09-120">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="44e09-120">This is the default property.</span></span><br/> |
| [<span data-ttu-id="44e09-121">**EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="44e09-121">**EncodedKey**</span></span>](publickey-encodedkey.md)<br/>               | <span data-ttu-id="44e09-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="44e09-122">Read-only</span></span><br/> | <span data-ttu-id="44e09-123">抓取可存取公開金鑰值的 [**EncodedData**](encodeddata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="44e09-123">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span><br/>                 |
| [<span data-ttu-id="44e09-124">**EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="44e09-124">**EncodedParameters**</span></span>](publickey-encodedparameters.md)<br/> | <span data-ttu-id="44e09-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="44e09-125">Read-only</span></span><br/> | <span data-ttu-id="44e09-126">抓取可存取公開金鑰演算法之參數的 [**EncodedData**](encodeddata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="44e09-126">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span><br/>  |
| [<span data-ttu-id="44e09-127">**長度**</span><span class="sxs-lookup"><span data-stu-id="44e09-127">**Length**</span></span>](publickey-length.md)<br/>                       | <span data-ttu-id="44e09-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="44e09-128">Read-only</span></span><br/> | <span data-ttu-id="44e09-129">抓取公開金鑰的長度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="44e09-129">Retrieves the length of the public key in bits.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="44e09-130">備註</span><span class="sxs-lookup"><span data-stu-id="44e09-130">Remarks</span></span>

<span data-ttu-id="44e09-131">無法建立 **PublicKey** 物件。</span><span class="sxs-lookup"><span data-stu-id="44e09-131">The **PublicKey** object cannot be created.</span></span>

<span data-ttu-id="44e09-132">**PublicKey** 物件是由 [**PublicKey**](certificate-publickey.md)方法所使用。</span><span class="sxs-lookup"><span data-stu-id="44e09-132">The **PublicKey** object is used by the [**Certificate.PublicKey**](certificate-publickey.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="44e09-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="44e09-133">Requirements</span></span>



| <span data-ttu-id="44e09-134">需求</span><span class="sxs-lookup"><span data-stu-id="44e09-134">Requirement</span></span> | <span data-ttu-id="44e09-135">值</span><span class="sxs-lookup"><span data-stu-id="44e09-135">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44e09-136">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="44e09-136">Redistributable</span></span><br/> | <span data-ttu-id="44e09-137">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="44e09-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="44e09-138">DLL</span><span class="sxs-lookup"><span data-stu-id="44e09-138">DLL</span></span><br/>             | <dl> <span data-ttu-id="44e09-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44e09-139"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
