---
description: 傳回 Oid 集合，表示用來建立鏈物件的應用程式原則。
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: CertificateStatus. ApplicationPolicies 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994001"
---
# <a name="certificatestatusapplicationpolicies-method"></a><span data-ttu-id="ef4b3-103">CertificateStatus. ApplicationPolicies 方法</span><span class="sxs-lookup"><span data-stu-id="ef4b3-103">CertificateStatus.ApplicationPolicies method</span></span>

<span data-ttu-id="ef4b3-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ef4b3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ef4b3-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="ef4b3-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ef4b3-106">**ApplicationPolicies** 方法會傳回 [**oid**](oids.md)集合，表示用來建立 [**Chain**](chain.md)物件的應用程式原則。</span><span class="sxs-lookup"><span data-stu-id="ef4b3-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4b3-107">語法</span><span class="sxs-lookup"><span data-stu-id="ef4b3-107">Syntax</span></span>


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="ef4b3-108">參數</span><span class="sxs-lookup"><span data-stu-id="ef4b3-108">Parameters</span></span>

<span data-ttu-id="ef4b3-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ef4b3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef4b3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef4b3-110">Return value</span></span>

<span data-ttu-id="ef4b3-111">[**Oid**](oids.md)集合。</span><span class="sxs-lookup"><span data-stu-id="ef4b3-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="ef4b3-112">集合中的每個 [**OID**](oid.md) 物件都代表一個應用程式原則 OID。</span><span class="sxs-lookup"><span data-stu-id="ef4b3-112">Each [**OID**](oid.md) object in the collection represents an application policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef4b3-113">備註</span><span class="sxs-lookup"><span data-stu-id="ef4b3-113">Remarks</span></span>

<span data-ttu-id="ef4b3-114">將應用程式原則 Oid 新增至集合，以指定應該用來建立憑證信任鏈的應用程式原則。</span><span class="sxs-lookup"><span data-stu-id="ef4b3-114">Add application policy OIDs to the collection to specify the application policies that should be used to build the certificate trust chain.</span></span> <span data-ttu-id="ef4b3-115">如果集合至少包含一個 [**OID**](oid.md)物件，則會忽略 [**CertificateStatus**](certificatestatus-eku.md)方法所傳回的 [**eku**](eku.md)物件。</span><span class="sxs-lookup"><span data-stu-id="ef4b3-115">If the collection contains at least one [**OID**](oid.md) object, the [**EKU**](eku.md) object returned by the [**CertificateStatus.EKU**](certificatestatus-eku.md) method is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef4b3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef4b3-116">Requirements</span></span>



| <span data-ttu-id="ef4b3-117">需求</span><span class="sxs-lookup"><span data-stu-id="ef4b3-117">Requirement</span></span> | <span data-ttu-id="ef4b3-118">值</span><span class="sxs-lookup"><span data-stu-id="ef4b3-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4b3-119">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ef4b3-119">End of client support</span></span><br/> | <span data-ttu-id="ef4b3-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef4b3-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ef4b3-121">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ef4b3-121">End of server support</span></span><br/> | <span data-ttu-id="ef4b3-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef4b3-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ef4b3-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ef4b3-123">Redistributable</span></span><br/>       | <span data-ttu-id="ef4b3-124">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ef4b3-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ef4b3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ef4b3-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ef4b3-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef4b3-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
