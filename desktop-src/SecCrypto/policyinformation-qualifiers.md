---
description: 捕獲原則限定詞的集合。
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: 'PolicyInformation 的限定詞屬性 (Iads. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977408"
---
# <a name="policyinformationqualifiers-property"></a><span data-ttu-id="7d7e5-103">PolicyInformation 的限定詞屬性</span><span class="sxs-lookup"><span data-stu-id="7d7e5-103">PolicyInformation.Qualifiers property</span></span>

<span data-ttu-id="7d7e5-104">\[[ **限定詞** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7d7e5-104">\[The **Qualifiers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d7e5-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來處理憑證原則延伸中的原則資訊。\]</span><span class="sxs-lookup"><span data-stu-id="7d7e5-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="7d7e5-106">**限定詞** 屬性會抓取原則的限定詞集合。</span><span class="sxs-lookup"><span data-stu-id="7d7e5-106">The **Qualifiers** property retrieves a collection of the policy's qualifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7e5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d7e5-107">Syntax</span></span>


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a><span data-ttu-id="7d7e5-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="7d7e5-108">Property value</span></span>

<span data-ttu-id="7d7e5-109">原則的認證實務聲明 (CPS) 指標或使用者聲明辨識符號，作為 [**限定詞**](qualifiers.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7d7e5-109">The policy's Certification Practice Statement (CPS) pointer or user notice qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d7e5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d7e5-110">Requirements</span></span>



| <span data-ttu-id="7d7e5-111">需求</span><span class="sxs-lookup"><span data-stu-id="7d7e5-111">Requirement</span></span> | <span data-ttu-id="7d7e5-112">值</span><span class="sxs-lookup"><span data-stu-id="7d7e5-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7e5-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7d7e5-113">Redistributable</span></span><br/> | <span data-ttu-id="7d7e5-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7d7e5-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7d7e5-115">標頭</span><span class="sxs-lookup"><span data-stu-id="7d7e5-115">Header</span></span><br/>          | <dl> <span data-ttu-id="7d7e5-116"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e5-116"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="7d7e5-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7d7e5-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="7d7e5-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e5-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d7e5-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d7e5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d7e5-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="7d7e5-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
