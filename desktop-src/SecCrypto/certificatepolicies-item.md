---
description: 抓取代表索引原則的 PolicyInformation 物件。 這是預設屬性。
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: CertificatePolicies 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001627"
---
# <a name="certificatepoliciesitem-property"></a><span data-ttu-id="e2299-104">CertificatePolicies 專案屬性</span><span class="sxs-lookup"><span data-stu-id="e2299-104">CertificatePolicies.Item property</span></span>

<span data-ttu-id="e2299-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e2299-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e2299-106">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來取得憑證原則。\]</span><span class="sxs-lookup"><span data-stu-id="e2299-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="e2299-107">**Item** 屬性會抓取代表索引原則的 [**PolicyInformation**](policyinformation.md)物件。</span><span class="sxs-lookup"><span data-stu-id="e2299-107">The **Item** property retrieves the [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span> <span data-ttu-id="e2299-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="e2299-108">This is the default property.</span></span>

<span data-ttu-id="e2299-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e2299-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2299-110">語法</span><span class="sxs-lookup"><span data-stu-id="e2299-110">Syntax</span></span>


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="e2299-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="e2299-111">Property value</span></span>

<span data-ttu-id="e2299-112">代表索引原則的 [**PolicyInformation**](policyinformation.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e2299-112">A [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2299-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2299-113">Requirements</span></span>



| <span data-ttu-id="e2299-114">需求</span><span class="sxs-lookup"><span data-stu-id="e2299-114">Requirement</span></span> | <span data-ttu-id="e2299-115">值</span><span class="sxs-lookup"><span data-stu-id="e2299-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2299-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e2299-116">End of client support</span></span><br/> | <span data-ttu-id="e2299-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2299-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e2299-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e2299-118">End of server support</span></span><br/> | <span data-ttu-id="e2299-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2299-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e2299-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e2299-120">Redistributable</span></span><br/>       | <span data-ttu-id="e2299-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e2299-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e2299-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e2299-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e2299-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2299-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
