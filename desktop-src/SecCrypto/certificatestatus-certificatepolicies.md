---
description: 傳回 Oid 集合，表示用來建立鏈物件的憑證原則。
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus. CertificatePolicies 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984049"
---
# <a name="certificatestatuscertificatepolicies-method"></a><span data-ttu-id="6c246-103">CertificateStatus. CertificatePolicies 方法</span><span class="sxs-lookup"><span data-stu-id="6c246-103">CertificateStatus.CertificatePolicies method</span></span>

<span data-ttu-id="6c246-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6c246-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6c246-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="6c246-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6c246-106">**CertificatePolicies** 方法會傳回 [**oid**](oids.md)集合，表示用來建立 [**Chain**](chain.md)物件的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="6c246-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c246-107">語法</span><span class="sxs-lookup"><span data-stu-id="6c246-107">Syntax</span></span>


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="6c246-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c246-108">Parameters</span></span>

<span data-ttu-id="6c246-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6c246-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c246-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c246-110">Return value</span></span>

<span data-ttu-id="6c246-111">[**Oid**](oids.md)集合。</span><span class="sxs-lookup"><span data-stu-id="6c246-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="6c246-112">集合中的每個 [**OID**](oid.md) 物件都代表一個憑證原則 OID。</span><span class="sxs-lookup"><span data-stu-id="6c246-112">Each [**OID**](oid.md) object in the collection represents a certificate policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c246-113">備註</span><span class="sxs-lookup"><span data-stu-id="6c246-113">Remarks</span></span>

<span data-ttu-id="6c246-114">將憑證原則 Oid 新增至集合，以指定應該用來建立憑證信任鏈的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="6c246-114">Add certificate policy OIDs to the collection to specify the certificate policies that should be used to build the certificate trust chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c246-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c246-115">Requirements</span></span>



| <span data-ttu-id="6c246-116">需求</span><span class="sxs-lookup"><span data-stu-id="6c246-116">Requirement</span></span> | <span data-ttu-id="6c246-117">值</span><span class="sxs-lookup"><span data-stu-id="6c246-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c246-118">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6c246-118">End of client support</span></span><br/> | <span data-ttu-id="6c246-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c246-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6c246-120">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6c246-120">End of server support</span></span><br/> | <span data-ttu-id="6c246-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c246-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6c246-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6c246-122">Redistributable</span></span><br/>       | <span data-ttu-id="6c246-123">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6c246-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6c246-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6c246-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6c246-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c246-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
