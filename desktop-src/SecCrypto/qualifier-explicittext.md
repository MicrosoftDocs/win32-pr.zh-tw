---
description: 抓取使用者通知的內容。
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: ExplicitText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d2ba5e6bbf6bb46e28c5dbb6fa9754c72b66dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989568"
---
# <a name="qualifierexplicittext-property"></a><span data-ttu-id="350d4-103">ExplicitText 屬性</span><span class="sxs-lookup"><span data-stu-id="350d4-103">Qualifier.ExplicitText property</span></span>

<span data-ttu-id="350d4-104">\[**ExplicitText** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="350d4-104">\[The **ExplicitText** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="350d4-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="350d4-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="350d4-106">**ExplicitText** 屬性會抓取使用者通知的內容。</span><span class="sxs-lookup"><span data-stu-id="350d4-106">The **ExplicitText** property retrieves the content of the user notice.</span></span> <span data-ttu-id="350d4-107">這個屬性可以是空的。</span><span class="sxs-lookup"><span data-stu-id="350d4-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="350d4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="350d4-108">Syntax</span></span>


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a><span data-ttu-id="350d4-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="350d4-109">Property value</span></span>

<span data-ttu-id="350d4-110">使用者通知的內容。</span><span class="sxs-lookup"><span data-stu-id="350d4-110">The content of the user notice.</span></span>

## <a name="requirements"></a><span data-ttu-id="350d4-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="350d4-111">Requirements</span></span>



| <span data-ttu-id="350d4-112">需求</span><span class="sxs-lookup"><span data-stu-id="350d4-112">Requirement</span></span> | <span data-ttu-id="350d4-113">值</span><span class="sxs-lookup"><span data-stu-id="350d4-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="350d4-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="350d4-114">Redistributable</span></span><br/> | <span data-ttu-id="350d4-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="350d4-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="350d4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="350d4-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="350d4-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="350d4-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="350d4-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="350d4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="350d4-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="350d4-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
