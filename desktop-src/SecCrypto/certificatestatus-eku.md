---
description: 傳回用來建立鏈物件的 EKU 物件。
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: CertificateStatus EKU 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988662"
---
# <a name="certificatestatuseku-method"></a><span data-ttu-id="ffdeb-103">CertificateStatus EKU 方法</span><span class="sxs-lookup"><span data-stu-id="ffdeb-103">CertificateStatus.EKU method</span></span>

<span data-ttu-id="ffdeb-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ffdeb-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="ffdeb-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ffdeb-106">**Eku** 方法會傳回用來建立 [**鏈**](chain.md)物件的 [**eku**](eku.md)物件。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-106">The **EKU** method returns the [**EKU**](eku.md) object used to build the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffdeb-107">語法</span><span class="sxs-lookup"><span data-stu-id="ffdeb-107">Syntax</span></span>


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a><span data-ttu-id="ffdeb-108">參數</span><span class="sxs-lookup"><span data-stu-id="ffdeb-108">Parameters</span></span>

<span data-ttu-id="ffdeb-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ffdeb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffdeb-110">Return value</span></span>

<span data-ttu-id="ffdeb-111">這個方法會傳回 [**EKU**](eku.md) 物件，指出 [*憑證*](../secgloss/c-gly.md)的擴充金鑰使用方式設定。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-111">This method returns an [**EKU**](eku.md) object that indicates the extended key usage setting of the [*certificate*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="ffdeb-112">EKU 設定會建立憑證的有效使用。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-112">The EKU setting establishes a certificate's valid use.</span></span> <span data-ttu-id="ffdeb-113">只能為每個憑證設定單一 **EKU** 物件。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-113">Only a single **EKU** object can be set for each certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffdeb-114">備註</span><span class="sxs-lookup"><span data-stu-id="ffdeb-114">Remarks</span></span>

<span data-ttu-id="ffdeb-115">[**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md)方法提供的功能與這個方法相同，但允許指定許多設定，而不是只有一個。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-115">The [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) method provides the same functionality as this method but allows many settings to be specified instead of only one.</span></span> <span data-ttu-id="ffdeb-116">如果 **ApplicationPolicies** 方法所傳回的 [**oid**](oids.md)集合包含一個或多個 [**OID**](oid.md)物件，則會忽略這個方法所傳回的 [**EKU**](eku.md)物件。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-116">If the [**OIDs**](oids.md) collection returned by the **ApplicationPolicies** method contains one or more [**OID**](oid.md) objects, the [**EKU**](eku.md) object returned by this method is ignored.</span></span> <span data-ttu-id="ffdeb-117">使用 **ApplicationPolicies** 方法，而不是此方法。</span><span class="sxs-lookup"><span data-stu-id="ffdeb-117">Use the **ApplicationPolicies** method instead of this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffdeb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffdeb-118">Requirements</span></span>



| <span data-ttu-id="ffdeb-119">需求</span><span class="sxs-lookup"><span data-stu-id="ffdeb-119">Requirement</span></span> | <span data-ttu-id="ffdeb-120">值</span><span class="sxs-lookup"><span data-stu-id="ffdeb-120">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffdeb-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ffdeb-121">End of client support</span></span><br/> | <span data-ttu-id="ffdeb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffdeb-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ffdeb-123">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ffdeb-123">End of server support</span></span><br/> | <span data-ttu-id="ffdeb-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffdeb-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ffdeb-125">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ffdeb-125">Redistributable</span></span><br/>       | <span data-ttu-id="ffdeb-126">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ffdeb-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ffdeb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ffdeb-127">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ffdeb-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffdeb-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffdeb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffdeb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffdeb-130">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="ffdeb-130">**CertificateStatus**</span></span>](certificatestatus.md)
</dt> <dt>

[<span data-ttu-id="ffdeb-131">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="ffdeb-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="ffdeb-132">**EKU**</span><span class="sxs-lookup"><span data-stu-id="ffdeb-132">**EKU**</span></span>](eku.md)
</dt> </dl>

 

 
