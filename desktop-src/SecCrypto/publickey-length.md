---
description: 抓取公開金鑰的長度（以位為單位）。
ms.assetid: 02cb631a-5a5d-4d16-bdad-55263a0a53b3
title: PublicKey. Length 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Length
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9429c2ab72845324ab024005cac2da2bfaf7eec1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990759"
---
# <a name="publickeylength-property"></a><span data-ttu-id="5ef32-103">PublicKey. Length 屬性</span><span class="sxs-lookup"><span data-stu-id="5ef32-103">PublicKey.Length property</span></span>

<span data-ttu-id="5ef32-104">\[[ **長度** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5ef32-104">\[The **Length** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5ef32-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="5ef32-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5ef32-106">**Length** 屬性會取出公開金鑰的長度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="5ef32-106">The **Length** property retrieves the length of the public key in bits.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef32-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ef32-107">Syntax</span></span>


```VB
PublicKey.Length As Long
```



## <a name="property-value"></a><span data-ttu-id="5ef32-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="5ef32-108">Property value</span></span>

<span data-ttu-id="5ef32-109">公開金鑰的長度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="5ef32-109">The length of the public key in bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef32-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ef32-110">Requirements</span></span>



| <span data-ttu-id="5ef32-111">需求</span><span class="sxs-lookup"><span data-stu-id="5ef32-111">Requirement</span></span> | <span data-ttu-id="5ef32-112">值</span><span class="sxs-lookup"><span data-stu-id="5ef32-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef32-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5ef32-113">Redistributable</span></span><br/> | <span data-ttu-id="5ef32-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5ef32-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5ef32-115">DLL</span><span class="sxs-lookup"><span data-stu-id="5ef32-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="5ef32-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ef32-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ef32-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ef32-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef32-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="5ef32-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
