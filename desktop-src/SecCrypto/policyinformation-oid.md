---
description: 捕獲原則的 OID。 這是預設屬性。
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: PolicyInformation OID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981328"
---
# <a name="policyinformationoid-property"></a><span data-ttu-id="d1821-104">PolicyInformation OID 屬性</span><span class="sxs-lookup"><span data-stu-id="d1821-104">PolicyInformation.OID property</span></span>

<span data-ttu-id="d1821-105">\[**OID** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d1821-105">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d1821-106">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來處理憑證原則延伸中的原則資訊。\]</span><span class="sxs-lookup"><span data-stu-id="d1821-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="d1821-107">**Oid** 屬性會捕獲原則的 OID。</span><span class="sxs-lookup"><span data-stu-id="d1821-107">The **OID** property retrieves the policy's OID.</span></span> <span data-ttu-id="d1821-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="d1821-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1821-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1821-109">Syntax</span></span>


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="d1821-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="d1821-110">Property value</span></span>

<span data-ttu-id="d1821-111">作為 [**OID**](oid.md) 物件的原則物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1821-111">The policy's object identifier as an [**OID**](oid.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1821-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1821-112">Requirements</span></span>



| <span data-ttu-id="d1821-113">需求</span><span class="sxs-lookup"><span data-stu-id="d1821-113">Requirement</span></span> | <span data-ttu-id="d1821-114">值</span><span class="sxs-lookup"><span data-stu-id="d1821-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1821-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d1821-115">Redistributable</span></span><br/> | <span data-ttu-id="d1821-116">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d1821-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d1821-117">DLL</span><span class="sxs-lookup"><span data-stu-id="d1821-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="d1821-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1821-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1821-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1821-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1821-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="d1821-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
