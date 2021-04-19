---
description: 抓取指向憑證實務聲明的 URI， (CPS) 由憑證授權單位單位 (CA) 發佈。
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: CPSPointer 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993219"
---
# <a name="qualifiercpspointer-property"></a><span data-ttu-id="e57f5-103">CPSPointer 屬性</span><span class="sxs-lookup"><span data-stu-id="e57f5-103">Qualifier.CPSPointer property</span></span>

<span data-ttu-id="e57f5-104">\[**CPSPointer** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e57f5-104">\[The **CPSPointer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e57f5-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="e57f5-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="e57f5-106">**CPSPointer** 屬性會抓取指向憑證實務聲明的 URI， (CPS) 由憑證授權單位單位 (CA) 發佈。</span><span class="sxs-lookup"><span data-stu-id="e57f5-106">The **CPSPointer** property retrieves the URI that points to a Certification Practice Statement (CPS) published by the certification authority (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="e57f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e57f5-107">Syntax</span></span>


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a><span data-ttu-id="e57f5-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="e57f5-108">Property value</span></span>

<span data-ttu-id="e57f5-109">指向 CA 所發佈之 CPS 的 URI。</span><span class="sxs-lookup"><span data-stu-id="e57f5-109">The URI that points to a CPS published by the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e57f5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e57f5-110">Requirements</span></span>



| <span data-ttu-id="e57f5-111">需求</span><span class="sxs-lookup"><span data-stu-id="e57f5-111">Requirement</span></span> | <span data-ttu-id="e57f5-112">值</span><span class="sxs-lookup"><span data-stu-id="e57f5-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e57f5-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e57f5-113">Redistributable</span></span><br/> | <span data-ttu-id="e57f5-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e57f5-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e57f5-115">DLL</span><span class="sxs-lookup"><span data-stu-id="e57f5-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="e57f5-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e57f5-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e57f5-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e57f5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e57f5-118">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="e57f5-118">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
