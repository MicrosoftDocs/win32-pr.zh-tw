---
description: 捕獲公開金鑰演算法的參數。
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: PublicKey. EncodedParameters 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984110"
---
# <a name="publickeyencodedparameters-property"></a><span data-ttu-id="0a365-103">PublicKey. EncodedParameters 屬性</span><span class="sxs-lookup"><span data-stu-id="0a365-103">PublicKey.EncodedParameters property</span></span>

<span data-ttu-id="0a365-104">\[**EncodedParameters** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="0a365-104">\[The **EncodedParameters** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0a365-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="0a365-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0a365-106">**EncodedParameters** 屬性會捕獲公開金鑰演算法的參數。</span><span class="sxs-lookup"><span data-stu-id="0a365-106">The **EncodedParameters** property retrieves the parameters of the public key algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a365-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a365-107">Syntax</span></span>


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="0a365-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="0a365-108">Property value</span></span>

<span data-ttu-id="0a365-109">[**EncodedData**](encodeddata.md)物件，可存取公開金鑰演算法的參數。</span><span class="sxs-lookup"><span data-stu-id="0a365-109">An [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a365-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a365-110">Requirements</span></span>



| <span data-ttu-id="0a365-111">需求</span><span class="sxs-lookup"><span data-stu-id="0a365-111">Requirement</span></span> | <span data-ttu-id="0a365-112">值</span><span class="sxs-lookup"><span data-stu-id="0a365-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a365-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0a365-113">Redistributable</span></span><br/> | <span data-ttu-id="0a365-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0a365-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0a365-115">DLL</span><span class="sxs-lookup"><span data-stu-id="0a365-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="0a365-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a365-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a365-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a365-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a365-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="0a365-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
