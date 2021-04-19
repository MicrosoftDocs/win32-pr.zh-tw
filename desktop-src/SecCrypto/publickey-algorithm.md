---
description: 演算法屬性會抓取識別公開金鑰所使用之演算法的 OID 物件。 這是預設屬性。
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey 演算法屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978758"
---
# <a name="publickeyalgorithm-property"></a><span data-ttu-id="8f24a-104">PublicKey 演算法屬性</span><span class="sxs-lookup"><span data-stu-id="8f24a-104">PublicKey.Algorithm property</span></span>

<span data-ttu-id="8f24a-105">\[[ **演算法]** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8f24a-105">\[The **Algorithm** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8f24a-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="8f24a-106">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8f24a-107">**演算法** 屬性會抓取識別公開金鑰所使用之演算法的 [**OID**](oid.md)物件。</span><span class="sxs-lookup"><span data-stu-id="8f24a-107">The **Algorithm** property retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="8f24a-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="8f24a-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f24a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f24a-109">Syntax</span></span>


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a><span data-ttu-id="8f24a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="8f24a-110">Property value</span></span>

<span data-ttu-id="8f24a-111">識別公開金鑰所使用之演算法的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8f24a-111">The [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f24a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f24a-112">Requirements</span></span>



| <span data-ttu-id="8f24a-113">需求</span><span class="sxs-lookup"><span data-stu-id="8f24a-113">Requirement</span></span> | <span data-ttu-id="8f24a-114">值</span><span class="sxs-lookup"><span data-stu-id="8f24a-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f24a-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8f24a-115">Redistributable</span></span><br/> | <span data-ttu-id="8f24a-116">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8f24a-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8f24a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8f24a-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="8f24a-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f24a-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f24a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f24a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f24a-120">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="8f24a-120">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
