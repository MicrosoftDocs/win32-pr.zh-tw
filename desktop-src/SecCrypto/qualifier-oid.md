---
description: 抓取辨識符號的物件識別碼。
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: 限定詞。 OID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984103"
---
# <a name="qualifieroid-property"></a><span data-ttu-id="a2d9b-103">限定詞。 OID 屬性</span><span class="sxs-lookup"><span data-stu-id="a2d9b-103">Qualifier.OID property</span></span>

<span data-ttu-id="a2d9b-104">\[**OID** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a2d9b-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a2d9b-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="a2d9b-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="a2d9b-106">**OID** 屬性會抓取辨識符號的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2d9b-106">The **OID** property retrieves the object ID of the qualifier.</span></span> <span data-ttu-id="a2d9b-107">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="a2d9b-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d9b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2d9b-108">Syntax</span></span>


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="a2d9b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="a2d9b-109">Property value</span></span>

<span data-ttu-id="a2d9b-110">識別辨識符號的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a2d9b-110">An [**OID**](oid.md) object that identifies the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d9b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2d9b-111">Requirements</span></span>



| <span data-ttu-id="a2d9b-112">需求</span><span class="sxs-lookup"><span data-stu-id="a2d9b-112">Requirement</span></span> | <span data-ttu-id="a2d9b-113">值</span><span class="sxs-lookup"><span data-stu-id="a2d9b-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d9b-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a2d9b-114">Redistributable</span></span><br/> | <span data-ttu-id="a2d9b-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a2d9b-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a2d9b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a2d9b-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="a2d9b-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2d9b-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2d9b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2d9b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d9b-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="a2d9b-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
