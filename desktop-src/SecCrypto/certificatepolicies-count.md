---
description: 抓取集合中的 PolicyInformation 物件數目。
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: CertificatePolicies Count 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994884"
---
# <a name="certificatepoliciescount-property"></a><span data-ttu-id="7c63c-103">CertificatePolicies Count 屬性</span><span class="sxs-lookup"><span data-stu-id="7c63c-103">CertificatePolicies.Count property</span></span>

<span data-ttu-id="7c63c-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7c63c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7c63c-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來取得憑證原則。\]</span><span class="sxs-lookup"><span data-stu-id="7c63c-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="7c63c-106">**Count** 屬性會抓取集合中的 [**PolicyInformation**](policyinformation.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="7c63c-106">The **Count** property retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span>

<span data-ttu-id="7c63c-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7c63c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c63c-108">語法</span><span class="sxs-lookup"><span data-stu-id="7c63c-108">Syntax</span></span>


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="7c63c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="7c63c-109">Property value</span></span>

<span data-ttu-id="7c63c-110">集合中的 [**PolicyInformation**](policyinformation.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="7c63c-110">The number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span> <span data-ttu-id="7c63c-111">每個 **PolicyInformation** 物件都代表集合中的單一憑證原則。</span><span class="sxs-lookup"><span data-stu-id="7c63c-111">Each **PolicyInformation** object represents a single certificate policy in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c63c-112">備註</span><span class="sxs-lookup"><span data-stu-id="7c63c-112">Remarks</span></span>

<span data-ttu-id="7c63c-113">當您使用 [**CertificatePolicies. Item**](certificatepolicies-item.md)屬性來抓取特定 **PolicyInformation** 物件時，可以使用 **Count** 屬性來指定集合中的最後一個 [**PolicyInformation**](policyinformation.md)物件。</span><span class="sxs-lookup"><span data-stu-id="7c63c-113">The **Count** property can be used to specify the last [**PolicyInformation**](policyinformation.md) object in the collection when retrieving a specific **PolicyInformation** object using the [**CertificatePolicies.Item**](certificatepolicies-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c63c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c63c-114">Requirements</span></span>



| <span data-ttu-id="7c63c-115">需求</span><span class="sxs-lookup"><span data-stu-id="7c63c-115">Requirement</span></span> | <span data-ttu-id="7c63c-116">值</span><span class="sxs-lookup"><span data-stu-id="7c63c-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c63c-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7c63c-117">End of client support</span></span><br/> | <span data-ttu-id="7c63c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c63c-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7c63c-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7c63c-119">End of server support</span></span><br/> | <span data-ttu-id="7c63c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c63c-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7c63c-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7c63c-121">Redistributable</span></span><br/>       | <span data-ttu-id="7c63c-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7c63c-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7c63c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7c63c-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7c63c-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c63c-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
