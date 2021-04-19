---
description: 捕獲公開金鑰的值。
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: PublicKey. EncodedKey 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979574"
---
# <a name="publickeyencodedkey-property"></a><span data-ttu-id="b4e8f-103">PublicKey. EncodedKey 屬性</span><span class="sxs-lookup"><span data-stu-id="b4e8f-103">PublicKey.EncodedKey property</span></span>

<span data-ttu-id="b4e8f-104">\[**EncodedKey** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b4e8f-104">\[The **EncodedKey** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4e8f-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="b4e8f-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b4e8f-106">**EncodedKey** 屬性會捕獲公開金鑰的值。</span><span class="sxs-lookup"><span data-stu-id="b4e8f-106">The **EncodedKey** property retrieves the value of the public key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e8f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4e8f-107">Syntax</span></span>


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="b4e8f-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="b4e8f-108">Property value</span></span>

<span data-ttu-id="b4e8f-109">提供存取公開金鑰值的 [**EncodedData**](encodeddata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b4e8f-109">An [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e8f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4e8f-110">Requirements</span></span>



| <span data-ttu-id="b4e8f-111">需求</span><span class="sxs-lookup"><span data-stu-id="b4e8f-111">Requirement</span></span> | <span data-ttu-id="b4e8f-112">值</span><span class="sxs-lookup"><span data-stu-id="b4e8f-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e8f-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b4e8f-113">Redistributable</span></span><br/> | <span data-ttu-id="b4e8f-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b4e8f-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b4e8f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="b4e8f-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="b4e8f-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4e8f-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4e8f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4e8f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e8f-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="b4e8f-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
