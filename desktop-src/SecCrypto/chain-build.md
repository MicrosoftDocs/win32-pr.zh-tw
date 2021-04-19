---
description: 從終端憑證建立憑證驗證鏈至受信任的根憑證，並傳回布林值，指出鏈的整體有效性。
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: IChain2：： Build 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979888"
---
# <a name="ichain2build-method"></a><span data-ttu-id="feab6-103">IChain2：： Build 方法</span><span class="sxs-lookup"><span data-stu-id="feab6-103">IChain2::Build method</span></span>

<span data-ttu-id="feab6-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="feab6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="feab6-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="feab6-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="feab6-106">**Build** 方法會從終端憑證建立憑證驗證鏈至受信任的 [*根憑證*](../secgloss/r-gly.md)，並傳回布林值，指出鏈的整體有效性。</span><span class="sxs-lookup"><span data-stu-id="feab6-106">The **Build** method builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md) and returns a Boolean value that indicates the overall validity of the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="feab6-107">語法</span><span class="sxs-lookup"><span data-stu-id="feab6-107">Syntax</span></span>


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="feab6-108">參數</span><span class="sxs-lookup"><span data-stu-id="feab6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feab6-109">*憑證* \[在\]</span><span class="sxs-lookup"><span data-stu-id="feab6-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feab6-110">[**憑證**](certificate.md)物件，代表要在其中建立驗證鏈的終端憑證。</span><span class="sxs-lookup"><span data-stu-id="feab6-110">A [**Certificate**](certificate.md) object that represents the end certificate upon which the verification chain is to be built.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feab6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="feab6-111">Return value</span></span>

<span data-ttu-id="feab6-112">指出鏈整體有效性的布林值。</span><span class="sxs-lookup"><span data-stu-id="feab6-112">A Boolean value that indicates the overall validity of the chain.</span></span> <span data-ttu-id="feab6-113">整體有效性是以適當的有效性檢查原則為基礎。</span><span class="sxs-lookup"><span data-stu-id="feab6-113">Overall validity is based on the validity checking policy in place.</span></span>

## <a name="remarks"></a><span data-ttu-id="feab6-114">備註</span><span class="sxs-lookup"><span data-stu-id="feab6-114">Remarks</span></span>

<span data-ttu-id="feab6-115">此鏈是使用 [**CertificateStatus CheckFlag**](certificatestatus-checkflag.md) 屬性，以及 [**CertificateStatus**](certificatestatus.md) 物件所指定的應用程式和憑證原則所建立。</span><span class="sxs-lookup"><span data-stu-id="feab6-115">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property as well as application and certificate policies specified by a [**CertificateStatus**](certificatestatus.md) object.</span></span> <span data-ttu-id="feab6-116">傳回的集合已排序;集合中的第一個憑證（certificate **. Item** (1) ）是鏈的最終憑證。</span><span class="sxs-lookup"><span data-stu-id="feab6-116">The returned collection is ordered; the first certificate in the collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="feab6-117">集合中的最後一個憑證（certificate **.** (Certificate **. Count**) ，是此鏈的 [*根憑證*](../secgloss/r-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="feab6-117">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span> <span data-ttu-id="feab6-118">**憑證。專案** (0) 代表整個鏈。</span><span class="sxs-lookup"><span data-stu-id="feab6-118">**Certificates.Item**(0) represents the entire chain.</span></span>

<span data-ttu-id="feab6-119">每次呼叫 **chain** 方法時，都會重設 [**連鎖店**](chain.md)物件的 [*狀態*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="feab6-119">Each time the **Chain.Build** method is called, the [*state*](../secgloss/s-gly.md) of the [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="feab6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="feab6-120">Requirements</span></span>



| <span data-ttu-id="feab6-121">需求</span><span class="sxs-lookup"><span data-stu-id="feab6-121">Requirement</span></span> | <span data-ttu-id="feab6-122">值</span><span class="sxs-lookup"><span data-stu-id="feab6-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="feab6-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="feab6-123">End of client support</span></span><br/> | <span data-ttu-id="feab6-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feab6-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="feab6-125">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="feab6-125">End of server support</span></span><br/> | <span data-ttu-id="feab6-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="feab6-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="feab6-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="feab6-127">Redistributable</span></span><br/>       | <span data-ttu-id="feab6-128">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="feab6-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="feab6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="feab6-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="feab6-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="feab6-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feab6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feab6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feab6-132">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="feab6-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="feab6-133">**鏈**</span><span class="sxs-lookup"><span data-stu-id="feab6-133">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
